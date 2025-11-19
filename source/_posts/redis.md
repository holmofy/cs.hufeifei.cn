---
title: Redis
categories: cli
keywords: redis
description: Redis命令速查
---

## get started

References: 

* https://redis.io/docs/latest/commands/

### KEY操作

| 命令                                          | 功能           |
| ------------------------------------------- | ------------ |
| `keys pattern`                              | 根据给定模式查找键    |
| `scan cursor [MATCH pattern] [COUNT count]` | 基于游标的迭代器     |
| `randomkey`                                 | 随机返回一个键      |
| `sort key [BY pattern] ...`                 | 对列表或集合排序     |

| 命令                                          | 功能           |
| ------------------------------------------- | ------------ |
| `dbsize`                                    | 返回当前数据库键数量   |
| `exists key [key ...]`                      | 检查一个或多个键是否存在 |
| `type key`                                  | 返回键的类型       |

| 命令                                          | 功能           |
| ------------------------------------------- | ------------ |
| `rename key newkey`                         | 重命名          |
| `renamenx key newkey`                       | 新名字不存在时重命名   |
| `move key db`                               | 将键移动到其他数据库   |
| `del key [key ...]`                         | 删除键          |
| `unlink key [key ...]`                      | 非阻塞删除键       |
| `flushdb`                                   | 清空当前数据库      |
| `flushall`                                  | 清空所有数据库      |

| 命令                                          | 功能           |
| ------------------------------------------- | ------------ |
| `expire key seconds [...]`                  | 设置键秒级过期时间    |
| `pexpire key milliseconds [...]`            | 设置键毫秒级过期时间   |

| 命令                                          | 功能           |
| ------------------------------------------- | ------------ |
| `ttl key`                                   | 剩余秒级过期时间     |
| `pttl key`                                  | 剩余毫秒过期时间     |
| `persist key`                               | 移除过期时间       |

### 字符串（string）

| 命令                          | 功能                   |
| --------------------------- | -------------------- |
| `set key value [...]`       | 设置键和值，带可选过期等参数       |
| `get key`                   | 获取值                  |
| `getset key value`          | 设置新值并返回旧值            |
| `setnx key value`           | 键不存在时设置成功            |
| `setex key seconds value`   | 设置值并指定秒级过期           |
| `psetex key ms value`       | 设置值并指定毫秒级过期          |

| 命令                          | 功能                   |
| ------------------------------- | ------------ |
| `mset key value [...]`      | 批量设置                 |
| `mget key [key ...]`        | 批量获取                 |
| `msetnx key value [...]`    | 批量设置（所有 key 都不存在才成功） |

| 命令                          | 功能                   |
| -------------------------------- | ------------ |
| `strlen key`                | 字符串长度                |
| `setrange key offset value` | 从 offset 开始修改字符串     |
| `getrange key start end`    | 获取区间字符串              |
| `append key value`          | 拼接字符串                |

| 命令                          | 功能                   |
| ---------------------------- | ------------ |
| `incr key`                  | 自增 1                 |
| `decr key`                  | 自减 1                 |
| `incrby key increment`      | 增加指定整数               |
| `decrby key decrement`      | 减少指定整数               |
| `incrbyfloat key increment` | 增加浮点数                |

### 列表(list)

| 命令                                       | 功能          |
| ---------------------------------------- | ----------- |
| `lpush key element [...]`                | 左侧入队        |
| `lpushx key element [...]`               | 左入队（仅列表存在时） |
| `rpush key element [...]`                | 右侧入队        |
| `rpushx key element [...]`               | 右入队（仅列表存在时） |

| 命令                                       | 功能          |
| ------------------------------------------- | ------------ |
| `lpop list`                              | 左出队         |
| `rpop list`                              | 右出队         |
| `blpop key [...] timeout`                | 阻塞左出队       |
| `brpop key [...] timeout`                | 阻塞右出队       |

| 命令                                       | 功能          |
| ------------------------------------------- | ------------ |
| `rpoplpush source dest`                  | 右出源 → 左入目标  |
| `brpoplpush source dest`                 | 阻塞版本        |

| 命令                                       | 功能          |
| ------------------------------------------- | ------------ |
| `lindex list index`                      | 获取指定下标值     |
| `llen list`                              | 获取长度        |
| `lrange list start end`                  | 获取区间        |
| `linsert key BEFORE/AFTER pivot element` | 插入元素        |
| `lrem list count element`                | 删除指定元素      |
| `lset key index element`                 | 替换指定下标值     |
| `ltrim list start end`                   | 裁剪列表        |

### 字典(hash)

| 命令                                 | 功能         |
| ---------------------------------- | ---------- |
| `hset key field value [...]`       | 设置字段值      |
| `hsetnx key field value`           | 字段不存在时设置成功 |
| `hget key field`                   | 获取指定字段     |
| `hmset key field value [...]`      | 批量设置       |
| `hmget key field [...]`            | 批量获取       |

| 命令                                 | 功能         |
| ----------------------------------- | ------------ |
| `hincrby key field increment`      | 字段值自增整数    |
| `hincrbyfloat key field increment` | 字段值自增浮点数   |

| 命令                                 | 功能         |
| ------------------------------------- | ------------ |
| `hexists key field`                | 字段是否存在     |
| `hlen key`                         | 字段数量       |
| `hdel key field [...]`             | 删除字段       |

| 命令                                 | 功能         |
| ----------------------------- | ------------ |
| `hkeys key`                        | 返回所有字段名    |
| `hvals key`                        | 返回所有字段值    |
| `hgetall key`                      | 所有字段和值     |
| `hscan key cursor [...]`           | 哈希渐进式遍历    |

### 集合(set)

| 命令                           | 功能          |
| ---------------------------- | ----------- |
| `sadd key member [...]`      | 添加一个或多个成员 |
| `spop key [count]`           | 随机弹出成员      |
| `smove src dest member`      | 移动成员从source到destination集合 |
| `srem key member [...]`      | 删除成员        |

| 命令                           | 功能          |
| -------------------------------- | ------------ |
| `scard key`                  | 成员数量        |
| `sismember key member`       | 是否存在        |
| `srandmember key [count]`    | 随机返回成员（不删除） |
| `smembers key`               | 返回所有成员      |
| `sscan key cursor [...]`     | 渐进式遍历       |

| 命令                           | 功能          |
| ------------------------------- | ------------ |
| `sdiff key [...]`            | 差集          |
| `sdiffstore dest key [...]`  | 差集存储，存储至destination |
| `sunion key [...]`           | 并集          |
| `sunionstore dest key [...]` | 并集存储，存储至destination |

### 有序集合(sorted set)

| 命令                                   | 功能        |
| ------------------------------------ | --------- |
| `zadd key [...] score member [...]`  | 添加成员      |
| `zincrby key increment member`       | 增加分数      |
| `zscore key member`                  | 获取分数      |
| `zcard key`                          | 成员数量      |
| `zrank key member`                   | 从小到大排名    |
| `zrevrank key member`                | 从大到小排名    |

| 命令                                   | 功能        |
| --------------------------------- | ------------ |
| `zcount key min max`                 | 分值范围统计    |
| `zrange key start stop [...]`        | 区间成员（按分数） |
| `zrangebyscore key min max [...]`    | 分数区间查询    |
| `zscan key cursor [...]`             | 渐进式遍历     |
| `zrem key member [...]`              | 删除成员      |
| `zremrangebyrank key start stop`     | 删除指定排名区间  |
| `zremrangebyscore key min max`       | 删除指定分数区间  |

| 命令                                   | 功能        |
| -------------------------------------- | ------------ |
| `zinterstore dest numkeys key [...]` | 交集存储      |
| `zunionstore dest numkeys key [...]` | 并集存储      |

| 命令                                   | 功能        |
| -------------------------------------- | ------------ |
| `zlexcount key min max`              | 指定大小范围内的成员数量   |
| `zrangebylex key min max [...]`      | 按从小打到的顺序返回成员   |
| `zremrangebylex key min max`         | 从集合里移除指定大小范围的成员    |


### 位图（bitmap）

| 命令                                  | 功能     |
| ----------------------------------- | ------ |
| `setbit key offset value`           | 位图索引上设置0或者1 |
| `getbit key offset`                 | 获取索引上的二进制值 |

| 命令                                  | 功能     |
| ------------------------------------- | ------------ |
| `bitcount key [start end [BYTE | BIT]]` | 统计start-end 置1的数量 bit按位 byte按字节 |
| `bitop operation destkey key [...]` | 对多个位图进行逻辑运算（and、or、xor、not），并将结果存放至 destkey |

### HyperLogLog(基数)

| 命令                                | 功能     |
| --------------------------------- | ------ |
| `pfadd key element [...]`         | 一个或者多个添加至hyperloglog里   |
| `pfcount key [...]`               | 一个或者多个hyperloglog里基数的个数   |
| `pfmerge destkey sourcekey [...]` | 合并操作，将一个或者多个sourcekey合并至destkey  |


### 地理位置（Geospatial）

| 命令                                          | 功能         |
| ------------------------------------------- | ---------- |
| `geoadd key [...]`                          | 添加一个或者多个地理位置 |
| `geopos key member [...]`                   | 获取其经纬度 |
| `geodist key m1 m2 [UNIT]`                  | 两者之间的距离 |
| `georadiusbymember key member radius [...]` | 返回该位置方圆多少距离的其他位置 |
| `geohash key member [...]`                  | 计算 geo hash值 |

### Stream（消息队列）

![Stream数据结构](https://redis.com.cn/images/stream1.png)

| 消息队列命令                                          | 功能说明                  |
| ------------------------------------------------------ | --------------------- |
| `XADD key ID field value [field value ...]`          | 添加消息到流末尾              |
| `XTRIM key MAXLEN ~ count`                           | 修剪流，按长度限制（近似或精确）      |
| `XDEL key id [id ...]`                               | 删除指定消息                |
| `XLEN key`                                           | 获取流中消息数量              |
| `XRANGE key start end [COUNT n]`                     | 按 ID 从小到大获取消息（过滤已删除的） |
| `XREVRANGE key end start [COUNT n]`                  | 按 ID 从大到小获取消息         |
| `XREAD [BLOCK ms] STREAMS key [key ...] id [id ...]` | 阻塞或非阻塞读取消息            |

| 消费者组命令                                         | 功能说明                                 |
| ------------------------------------------------------- | ------------------------------------ |
| `XGROUP CREATE key groupname id [MKSTREAM]`           | 创建消费者组（不存在流可用 MKSTREAM 创建）           |
| `XREADGROUP GROUP group consumer STREAMS key id`      | 从消费者组读取消息                            |
| `XACK key group id [id ...]`                          | 标记消息为已处理（ACK）                        |
| `XGROUP SETID key group id`                           | 设置消费者组的 last-delivered-id            |
| `XGROUP DELCONSUMER key group consumer`               | 删除消费者                                |
| `XGROUP DESTROY key group`                            | 删除整个消费者组                             |
| `XPENDING key group [start end count] [consumer]`     | 查看 pending 状态（待处理消息）                 |
| `XCLAIM key group consumer min-idle-time id [id ...]` | 转移消息归属权（消息重新分配给某消费者）                 |
| `XINFO GROUPS key`                                    | 查看消费者组列表及其状态                         |
| `XINFO STREAM key`                                    | 查看 Stream 信息（长度、last entry、groups 等） |

### 事务（transaction）

| 命令                | 功能   |
| ----------------- | ---- |
| `multi`           | 开启事务 |
| `exec`            | 执行事务 |
| `discard`         | 取消事务 |

| 命令                | 功能   |
| ------------------- | ------------ |
| `watch key [...]` | 监视一个或者多个键，（上乐观锁）|
| `unwatch`         | 取消所有键的监视 |

### 脚本（script）

| 命令                           | 功能        |
| ---------------------------- | --------- |
| `eval script numkeys [...]`  | 执行 Lua 脚本 |
| `evalsha sha1 numkeys [...]` | 执行校验并载入相应的脚本 |
| `script load script`         | 载入给定的lua脚本 |
| `script exists sha1 [...]`   | 判断lua脚本是否载入 |
| `script kill`                | 杀死正在执行的lua脚本 |
| `script flush`               | 移除所有lua脚本 |

### 发布和订阅(publish/subscribe)

| 命令                           | 功能         |
| ---------------------------- | ---------- |
| `publish channel message`    | 给某频道发布消息 |
| `subscribe channel [...]`    | 订阅 |
| `psubscribe pattern [...]`   | 根据模式订阅 |

| 命令                           | 功能         |
| ----------------------------- | ------------ |
| `unsubscribe [channel ...]`  | 取消订阅       |
| `punsubscribe pattern [...]` | 根据模式取消订阅，如果没有提供模式，则取消所有模式订阅 |

| 命令                           | 功能         |
| ------------------------------------------- | ------------ |
| `pubsub channels`            | 查看订阅频道     |
| `pubsub channel`             | 查看频道订阅者数量  |
| `pubsub numpat`              | 查看被订阅的模式数量 |

### Redis配置&其他

| 命令                        | 功能           |
| ------------------------- | ------------ |
| `auth password`           | 使用密码连接redis |
| `echo message`            | 打印           |
| `ping`                    | 向服务器发送ping请求 |
| `quit`                    | 退出连接 |
| `select number`           | 切换数据库        |

| 命令                        | 功能           |
| ----------------------- | ------------ |
| `client setname name`     | 设置客户端名称      |
| `client getname`          | 获取客户端名称      |
| `client list`             | 查看客户端信息      |
| `client kill ip:port`     | 杀死客户端        |

| 持久化相关命令             | 功能           |
| -------------------------- | ------------ |
| `save`                    | 同步保存 RDB（阻塞） |
| `bgsave`                  | 异步保存 RDB     |
| `bgrewriteaof`            | 重写 AOF       |
| `lastsave`                | 上次持久化时间      |

| 配置相关命令                | 功能           |
| ---------------------- | ------------ |
| `config set option value` | 设置配置         |
| `config get option`       | 获取配置         |
| `config rewrite`          | 持久化配置        |
| `config resetstat`        | 重置统计         |

| 命令                     | 功能           |
| ------------------------ | ------------ |
| `info [section]`          | 查看服务器信息      |
| `time`                    | 获取服务器时间      |
| `shutdown [save | nosave]`| 关闭服务器         |

| 命令                     | 功能           |
| ------------------------ | ------------ |
| `slowlog get [n]`         | 获取慢日志        |
| `slowlog len`             | 慢日志条数        |
| `slowlog reset`           | 清空慢日志        |
| `monitor`                 | 打印所有操作       |
| `debug segfault`          | 让 Redis 崩溃   |
| `debug object key`        | 查看调试信息       |
| `object refcount key`     | 引用计数         |
| `object encoding key`     | 内部编码         |
| `object idletime key`     | 空闲时间         |

### 命令行

| 命令                | 功能            |
| ----------------- | ------------- |
| `redis-server`    | Redis 服务器     |
| `redis-cli`       | Redis 客户端     |
| `redis-benchmark` | 性能测试工具        |
| `redis-check-rdb` | 检查 RDB 文件     |
| `redis-check-aof` | 检查 AOF 文件     |
| `redis-sentinel`  | Sentinel 守护进程 |
