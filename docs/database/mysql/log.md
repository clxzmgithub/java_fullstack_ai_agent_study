# MySQL日志系统学习文档

## 目录

1. 日志系统概述
2. 错误日志（Error Log）
3. 查询日志（General Query Log）
4. 慢查询日志（Slow Query Log）
5. 二进制日志（Binary Log）
6. 中继日志（Relay Log）
7. 事务日志（InnoDB Redo Log）
8. 回滚日志（Undo Log）
9. 日志配置与管理
10. 日志分析工具

## 1. 日志系统概述

MySQL的日志系统是数据库管理和故障排查的重要工具，主要包括以下几类日志：

- **错误日志**：记录MySQL启动、运行、关闭过程中的错误信息
- **查询日志**：记录所有数据库操作语句
- **慢查询日志**：记录执行时间超过指定阈值的查询语句
- **二进制日志**：记录所有更改数据的SQL语句，用于数据恢复和主从复制
- **中继日志**：用于主从复制，存储从主库接收到的二进制日志
- **事务日志**：InnoDB存储引擎的redo log，保证事务的持久性
- **回滚日志**：InnoDB存储引擎的undo log，保证事务的原子性和MVCC

## 2. 错误日志（Error Log）

### 2.1 功能概述

错误日志记录MySQL服务器启动、运行、关闭过程中的重要信息和错误，是排查问题的第一手资料。

### 2.2 主要内容

- MySQL启动和关闭信息
- 服务器运行时的错误信息
- 告警信息
- InnoDB存储引擎的初始化信息
- 主从复制相关的错误信息

### 2.3 配置方法

```sql
-- 查看错误日志配置
SHOW VARIABLES LIKE 'log_error';

-- 配置文件中设置（my.cnf）
[mysqld]
log_error = /var/log/mysql/error.log
```

### 2.4 查看日志

```bash
# Linux系统查看
tail -f /var/log/mysql/error.log
```

## 3. 查询日志（General Query Log）

### 3.1 功能概述

记录MySQL服务器接收到的所有客户端连接和执行的SQL语句。

### 3.2 主要内容

- 客户端连接和断开信息
- 所有执行的SQL语句
- 管理命令执行信息

### 3.3 配置方法

```sql
-- 动态开启查询日志
SET GLOBAL general_log = 'ON';

-- 设置日志文件位置
SET GLOBAL general_log_file = '/var/log/mysql/general.log';

-- 查看当前状态
SHOW VARIABLES LIKE 'general_log%';
```

### 3.4 配置文件配置

```ini
[mysqld]
general_log = 1
general_log_file = /var/log/mysql/general.log
```

### 3.5 注意事项

- 对性能影响较大，生产环境慎用

## 4. 慢查询日志（Slow Query Log）

### 4.1 功能概述

记录执行时间超过指定阈值的SQL语句，是性能优化的重要工具。

### 4.2 主要配置参数

```sql
-- 查看慢查询日志配置
SHOW VARIABLES LIKE 'slow_query_log%';
SHOW VARIABLES LIKE 'long_query_time';
SHOW VARIABLES LIKE 'log_queries_not_using_indexes';
```

### 4.3 配置方法

```sql
-- 开启慢查询日志
SET GLOBAL slow_query_log = 'ON';

-- 设置慢查询阈值（秒）
SET GLOBAL long_query_time = 2;

-- 设置日志文件位置
SET GLOBAL slow_query_log_file = '/var/log/mysql/slow.log';

-- 记录未使用索引的查询
SET GLOBAL log_queries_not_using_indexes = 'ON';
```

### 4.4 配置文件配置

```ini
[mysqld]
slow_query_log = 1
slow_query_log_file = /var/log/mysql/slow.log
long_query_time = 2
log_queries_not_using_indexes = 1
```

## 5. 二进制日志（Binary Log）

### 5.1 功能概述

记录所有更改数据库数据的SQL语句，主要用于数据恢复和主从复制。

### 5.2 日志格式

- **STATEMENT**：基于SQL语句的复制

### 5.3 配置方法

```sql
-- 查看二进制日志状态
SHOW MASTER STATUS;
SHOW BINARY LOGS;

-- 查看二进制日志内容
SHOW BINLOG EVENTS IN 'mysql-bin.000001';
```

### 5.4 配置文件配置

```ini
[mysqld]
# 开启二进制日志
log-bin = /var/log/mysql/mysql-bin.log

# 设置server-id（主从复制必需）
server-id = 1

# 设置日志格式
binlog-format = ROW

# 设置过期时间（天）
expire_logs_days = 7

# 设置最大日志文件大小
max_binlog_size = 100M
```

### 5.5 使用场景

- 数据库备份和恢复
- 主从复制
- 数据审计
- 数据变更追踪

## 6. 中继日志（Relay Log）

### 6.1 功能概述

在MySQL主从复制中，从服务器使用中继日志来存储从主服务器接收到的二进制日志事件。

### 6.2 主要特点

- 由从服务器的I/O线程创建
- 存储从主服务器接收到的binlog事件
- 由从服务器的SQL线程读取并执行

### 6.3 查看中继日志

```sql
-- 查看从服务器状态
SHOW SLAVE STATUS\G

-- 查看中继日志信息
SHOW RELAYLOG EVENTS;
```

## 7. 事务日志（InnoDB Redo Log）

### 7.1 功能概述

InnoDB存储引擎的redo log用于保证事务的持久性，记录物理页的修改。

### 7.2 核心参数

```sql
-- 查看redo log配置
SHOW VARIABLES LIKE 'innodb_log%';
```

### 7.3 配置文件配置

```ini
[mysqld]
# redo log文件大小
innodb_log_file_size = 256M

# redo log文件组数量
innodb_log_files_in_group = 2

# redo log缓冲区大小
innodb_log_buffer_size = 16M
```

### 7.4 工作原理

### 7.4 工作原理

Redo Log 的核心机制遵循 **WAL（Write-Ahead Logging，预写式日志）** 技术，确保数据不丢失：

11. **内存记录**：事务修改数据页时，先将修改记录写入内存中的 `redo log buffer`。
12. **日志刷盘**：事务提交时，按照配置策略（如 `innodb_flush_log_at_trx_commit=1`）将 `redo log buffer` 中的内容持久化到磁盘上的 redo log 文件。
13. **异步落盘**：后台线程在适当时机将内存中的脏页（Dirty Page）异步刷新到磁盘数据文件中。
14. **崩溃恢复**：若数据库发生宕机，重启时通过重放（Replay）redo log，将未写入数据文件的已提交事务重新应用，保证数据的持久性。

## 8. 回滚日志（Undo Log）

### 8.1 功能概述

InnoDB存储引擎的undo log用于保证事务的原子性和MVCC（多版本并发控制）。

### 8.2 主要功能

- 事务回滚：记录数据修改前的旧值
- MVCC：为其他事务提供一致性读视图
- 崩溃恢复：协助恢复未提交的事务

### 8.3 存储位置

- 存储在InnoDB的共享表空间或独立表空间中
- 与数据字典一起管理

## 9. 日志配置与管理

### 9.1 统一日志配置

```ini
[mysqld]
# 错误日志
log_error = /var/log/mysql/error.log

# 通用查询日志
general_log = 0
general_log_file = /var/log/mysql/general.log

# 慢查询日志
slow_query_log = 1
slow_query_log_file = /var/log/mysql/slow.log
long_query_time = 2

# 二进制日志
log-bin = /var/log/mysql/mysql-bin.log
server-id = 1
binlog-format = ROW
expire_logs_days = 7
```

### 9.2 日志轮转管理

```bash
# 使用logrotate管理日志轮转
/var/log/mysql/*.log {
    daily
    missingok
    rotate 7
    compress
    delaycompress
    notifempty
    create 640 mysql adm
    sharedscripts
    postrotate
        /usr/bin/mysqladmin --defaults-file=/etc/mysql/debian.cnf flush-logs
    endscript
}
```

### 9.3 性能监控

```sql
-- 监控二进制日志大小
SHOW MASTER STATUS;

-- 监控慢查询数量
SHOW GLOBAL STATUS LIKE 'Slow_queries';

-- 监控redo log使用情况
SHOW ENGINE INNODB STATUS\G
```

## 10. 日志分析工具

### 10.1 MySQL自带工具

```bash
# 分析二进制日志
mysqlbinlog mysql-bin.000001

# 分析慢查询日志
mysqldumpslow /var/log/mysql/slow.log
```

### 10.2 第三方工具

- **pt-query-digest**：Percona Toolkit中的慢查询分析工具
- **MySQL Enterprise Monitor**：官方商业监控工具
- **Prometheus + Grafana**：开源监控解决方案

### 10.3 pt-query-digest使用示例

```bash
# 安装Percona Toolkit
wget https://repo.percona.com/apt/percona-release_latest.$(lsb_release -sc)_all.deb
sudo dpkg -i percona-release_latest.$(lsb_release -sc)_all.deb
sudo apt-get update
sudo apt-get install percona-toolkit

# 分析慢查询日志
pt-query-digest /var/log/mysql/slow.log > slow_query_report.txt
```

## 总结

MySQL的日志系统是数据库运维的重要组成部分，合理配置和使用各类日志可以帮助我们：

15. **快速定位问题**：通过错误日志快速发现系统异常
16. **优化性能**：通过慢查询日志识别性能瓶颈
17. **保障数据安全**：通过二进制日志实现数据恢复
18. **提高并发性能**：通过事务日志保证ACID特性

在生产环境中，应根据实际需求合理配置日志级别，平衡日志功能和系统性能，同时建立完善的日志管理和分析机制。

