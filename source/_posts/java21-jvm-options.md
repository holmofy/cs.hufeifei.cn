---
title: java21-jvm
categories: jvm
keywords: java,jvm,参数调优,参考手册
description: jvm21调优参考手册
---

## get started

参考：

* https://docs.oracle.com/en/java/javase/21/gctuning/
* https://www.oracle.com/technetwork/tutorials/tutorials-1876574.html
* https://www.oracle.com/java/technologies/g1gc.html

### HotSpot JVM 启动结构

```bash
java [options] classname [args]
java [options] -jar filename [args]
```

### JVM 可用垃圾收集器（Java 21）

| Collector   | 特点                 | 启用参数                   |
| ----------- | ------------------ | ---------------------- |
| Serial GC   | 单线程，适合小堆/客户端       | `-XX:+UseSerialGC`     |
| Parallel GC | 多线程 stop‑the‑world | `-XX:+UseParallelGC`   |
| G1 GC (默认)  | 分代 GC，平衡延迟与吞吐      | `-XX:+UseG1GC`         |
| ZGC         | 极低停顿 (<1ms)，支持大堆   | `-XX:+UseZGC`          |
| Shenandoah  | 低停顿 (<10ms)，并发压缩   | `-XX:+UseShenandoahGC` |

> 说明：Java 21 默认 G1 为垃圾收集器；ZGC 有分代支持，提供更优新生代收集效果。

### GC 日志参数（统一 Xlog 体系）

Java 9+ 统一使用 `‑Xlog:gc*` 系列（更灵活替代 `PrintGC` 系列）。

| 参数                            | 说明                       |
| ----------------------------- | ------------------------ |
| `-Xlog:gc`                    | 输出基本 GC 信息               |
| `-Xlog:gc+heap`               | 显示堆内存变化                  |
| `-Xlog:gc+pause`              | 显示暂停时间                   |
| `-Xlog:gc+ergo`               | 显示 GC 人机调整（ergonomics）信息 |
| `-Xlog:gc*,safepoint`         | 包含安全点信息                  |
| `-Xlog:gc:file=<file>:<opts>` | 输出 GC 到文件（可加滚动等）         |

### 堆/内存大小设置

| 参数                                 | 说明                 |
| ---------------------------------- | ------------------ |
| `-Xms<size>`                       | 初始堆大小              |
| `-Xmx<size>`                       | 最大堆大小              |
| `-Xmn<size>`                       | 年轻代大小（某些 GC 有效）    |
| `-XX:MaxHeapFreeRatio=<percent>`   | GC 后最大堆空闲保留率       |
| `-XX:MinHeapFreeRatio=<percent>`   | GC 后最小堆空闲保留率       |
| `-XX:MaxDirectMemorySize=<size>`   | 最大 DirectBuffer 大小 |
| `-XX:InitialCodeCacheSize=<size>`  | Code Cache 初始大小    |
| `-XX:ReservedCodeCacheSize=<size>` | Code Cache 最大大小    |

### 常用 GC 通用参数（调优基础）

| 参数                                             | 说明               |
| ---------------------------------------------- | ---------------- |
| `-XX:MaxGCPauseMillis=<ms>`                    | GC 目标最大停顿        |
| `-XX:GCTimeRatio=<ratio>`                      | GC 与应用时间比例目标     |
| `-XX:InitiatingHeapOccupancyPercent=<percent>` | 并发标记触发阈值（G1 类）   |
| `-XX:+DisableExplicitGC`                       | 禁用 `System.gc()` |
| `-XX:+AlwaysPreTouch`                          | 启动时预热分配内存页       |
| `-XX:ParallelGCThreads=<n>`                    | 并行 GC 线程数        |
| `-XX:ConcGCThreads=<n>`                        | 并发 GC 线程数        |

### G1 GC（默认）参数

![G1 GC](https://github.com/user-attachments/assets/2bde4de7-c612-40e9-b924-a879d663781a)
> 每个 Region 可以属于年轻代或老年代，动态划分。Mixed GC：并发标记老年代 + 年轻代
> ![YoungGC](https://www.oracle.com/technetwork/tutorials/tutorials-1876574.html)
> ![G1 GC过程](https://p0.meituan.net/travelcube/2f56a9a249bc8d74f4f455782abce6be147997.png)

| 参数                                             | 说明              |
| ---------------------------------------------- | --------------- |
| `-XX:+UseG1GC`                                 | 启用 G1 GC        |
| `-XX:G1HeapRegionSize=<size>`                  | G1 区块大小(1M–32M) |
| `-XX:MaxGCPauseMillis=<ms>`                    | 目标最大停顿          |
| `-XX:InitiatingHeapOccupancyPercent=<percent>` | 并发标记触发点         |
| `-XX:G1ReservePercent=<percent>`               | 堆预留空间百分比        |
| `-XX:G1HeapWastePercent=<percent>`             | 判断浪费内存阈值        |
| `-XX:G1MixedGCCountTarget=<count>`             | 混合 GC 次数目标      |
| `-XX:+UseStringDeduplication`                  | 对象字符串去重（可选）     |

> G1 大多数参数无默认启用即可运行，但可通过这些参数微调停顿/混合 GC 行为。G1 不固定老年代大小，使用 Region 动态管理堆空间，提高回收灵活性。
>
> `-XX:MaxGCPauseMillis=<ms>`是 目标值，不是硬限制，实际停顿可能超过；JVM 会自动调整 Region 大小和混合 GC 次数，尝试控制停顿。

### ZGC 参数（Java 21）

![ZGC内存布局](https://static.wixstatic.com/media/3cd8e5_b268f0d547fc4fe8a1f619f0da9852e0~mv2.jpg)
![ZGC回收周期](https://p0.meituan.net/travelcube/40838f01e4c29cfe5423171f08771ef8156393.png)

| 参数                           | 说明                 |
| ---------------------------- | ------------------ |
| `-XX:+UseZGC`                | 启用 ZGC             |
| `-XX:+ZGenerational`         | 启用分代 ZGC（Java 21+） |
| `-XX:SoftMaxHeapSize=<size>` | 可选，上限软堆大小          |
| `-XX:+ZUncommit`             | 释放未使用内存回 OS        |
| `-XX:MaxGCPauseMillis=<ms>`  | 低延迟目标              |
| `-XX:+DisableExplicitGC`     | 禁显式 GC 调用          |

> ZGC 设计上参数较少，因为它自动并发管理大多数行为。
> 理论上可设置目标停顿，但 ZGC 设计上停顿非常低（<10ms），几乎不依赖这个参数；低延迟堆管理自动完成，通常无需调优停顿

### Shenandoah GC 参数

| 参数                                    | 说明                         |
| ------------------------------------- | -------------------------- |
| `-XX:+UseShenandoahGC`                | 启用 Shenandoah              |
| `-XX:ShenandoahPauseTimeGoal=<ms>`    | 停顿时间目标                     |
| `-XX:ShenandoahGCThreads=<n>`         | 并发收集线程数                    |
| `-XX:ShenandoahHeapRegionSize=<size>` | 区域大小                       |
| `-XX:ShenandoahGCMode=<mode>`         | GC 模式（如 normal/iu/passive） |

> Shenandoah 中 `GCMode` 可控制标记策略等高级行为。

### 并发/分代调优参数

| 参数                               | 说明               |
| -------------------------------- | ---------------- |
| `-XX:MaxTenuringThreshold=<age>` | 新生代晋升年龄阈值        |
| `-XX:SurvivorRatio=<ratio>`      | Eden/Survivor 比率 |
| `-XX:NewRatio=<ratio>`           | 老代/新生代比率         |
| `-XX:+UseAdaptiveSizePolicy`     | 自适应分代大小调整        |

### 线程/栈配置

| 参数                           | 说明         |
| ---------------------------- | ---------- |
| `-Xss<size>`                 | 每线程栈大小     |
| `-XX:ThreadStackSize=<size>` | 线程栈配置      |
| `-XX:+UseTLAB`               | 启用线程局部分配缓冲 |
| `-XX:TLABSize=<size>`        | 分配缓冲初始大小   |

### HotSpot 行为调整参数（通用）

| 参数                               | 说明     |
| -------------------------------- | ------ |
| `-XX:ObjectAlignmentInBytes=<n>` | 对齐字节大小 |
| `-XX:-UseBiasedLocking`          | 禁用偏向锁  |
| `-XX:-UseCompressedOops`         | 关闭压缩指针 |

### 日志与调试

| 参数                                    | 说明           |
| ------------------------------------- | ------------ |
| `-XX:+PrintClassHistogramAfterFullGC` | Full GC 后类统计 |
| `-XX:+PrintHeapAtGC`                  | GC 时堆信息      |
