---
title: Systemd
categories: cli
keywords: systemd
description: Systemd速查表
---

## get started

References: 

* https://blog.hufeifei.cn/2025/04/Linux/systemd-history/

### 服务管理

| 命令示例                                  | 说明            |
| ------------------------------------- | ------------- |
| `systemctl start <服务名>`               | 立即启动服务        |
| `systemctl stop <服务名>`                | 停止服务          |
| `systemctl restart <服务名>`             | 重启服务          |
| `systemctl reload <服务名>`              | 重新加载配置（不重启进程） |
| `systemctl status <服务名>`              | 查看服务当前状态和日志   |
| `systemctl enable <服务名>`              | 服务随系统启动自动启动   |
| `systemctl disable <服务名>`             | 取消服务开机自动启动    |
| `systemctl is-enabled <服务名>`          | 查看是否设置为开机启动   |
| `systemctl list-units --type=service` | 列出所有正在运行的服务   |
| `systemctl --failed`                  | 查看启动失败的服务     |
| `systemctl daemon-reload`             | 重新加载所有单元配置    |

### 日志管理（journalctl）

| 命令示例                                    | 说明              |
| --------------------------------------- | --------------- |
| `journalctl -u <服务名>`                   | 查看指定服务的所有日志     |
| `journalctl -fu <服务名>`                  | 实时跟踪服务日志        |
| `journalctl -p err -b`                  | 查看当前启动的所有错误级别日志 |
| `journalctl -b`                         | 查看当前启动的所有日志     |
| `journalctl --since "2025-07-01 00:00"` | 查看某时间之后的日志      |
| `journalctl -p warning`                 | 只查看警告及以上级别的日志   |

### 系统状态

| 命令示例                                      | 说明                                 |
| ----------------------------------------- | ---------------------------------- |
| `systemctl is-system-running`             | 显示系统当前运行状态                         |
| `systemctl get-default`                   | 查看默认启动目标（类似运行级别）                   |
| `systemctl set-default multi-user.target` | 设置默认启动目标（multi-user.target = 纯命令行） |
| `systemctl isolate graphical.target`      | 切换当前运行目标（不重启）                      |
| `systemctl list-units --type=target`      | 查看所有当前激活的 target                   |

### 资源限制（CGroup）

| 命令示例                                            | 说明            |
| ----------------------------------------------- | ------------- |
| `systemctl set-property <服务名> CPUQuota=50%`     | 限制服务 CPU 使用比例 |
| `systemctl set-property <服务名> MemoryMax=500M`   | 限制服务最大内存使用    |
| `systemctl show <服务名> -p CPUQuota -p MemoryMax` | 查看服务当前资源限制    |

### 定时任务（Timers）

| 命令示例                     | 说明         |
| ------------------------ | ---------- |
| `systemctl list-timers`  | 列出所有激活的定时器 |
| `systemctl start <定时器名>` | 手动启动定时任务   |
| `systemctl stop <定时器名>`  | 停止定时任务     |
| `journalctl -u <定时器名>`   | 查看定时任务相关日志 |

### 系统电源管理

| 命令示例                  | 说明     |
| --------------------- | ------ |
| `systemctl reboot`    | 重启机器   |
| `systemctl poweroff`  | 关机     |
| `systemctl suspend`   | 进入睡眠模式 |
| `systemctl hibernate` | 进入休眠模式 |

### 其他常用命令

| 命令示例                                | 说明             |
| ----------------------------------- | -------------- |
| `systemctl list-units`              | 查看所有激活的单元      |
| `systemctl list-dependencies <单元名>` | 查看指定单元的依赖关系    |
| `systemctl kill <服务名>`              | 发送信号杀死服务相关所有进程 |
