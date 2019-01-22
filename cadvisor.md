### cadvisor指标释义

Metric name | Type | Description | Unit (where applicable)|  ZH                     |
:-----------|:-----|:------------|:-----------------------|:------------------------|
`container_accelerator_duty_cycle` | Gauge | Percent of time over the past sample period during which the accelerator was actively processing | percentage | 容器加速周期占比
`container_accelerator_memory_total_bytes` | Gauge | Total accelerator memory | bytes | 容器加速总内存
`container_accelerator_memory_used_bytes` | Gauge | Total accelerator memory allocated | bytes | 容器加速所需内存
`container_cpu_cfs_periods_total` | Counter | Number of elapsed enforcement period intervals | --- |容器已执行的执行期间隔数
`container_cpu_cfs_throttled_periods_total` | Counter | Number of throttled period intervals | --- |容器限制周期间隔数
`container_cpu_cfs_throttled_seconds_total` | Counter | Total time duration the container has been throttled | seconds | 容器被限制的总持续时间
`container_cpu_load_average_10s` | Gauge | Value of container cpu load average over the last 10 seconds | --- | 过去10秒容器CPU的平均负载
`container_cpu_schedstat_run_periods_total` | Counter | Number of times processes of the cgroup have run on the cpu | --- |cgroup的进程在cpu上运行的次数
`container_cpu_schedstat_run_seconds_total` | Counter | Time duration the processes of the container have run on the CPU | seconds | 容器进程在CPU上运行的持续时间
`container_cpu_schedstat_runqueue_seconds_total` | Counter | Time duration processes of the container have been waiting on a runqueue | seconds | 容器进程等待执行队列的持续时间
`container_cpu_system_seconds_total` | Counter | Cumulative system cpu time consumed | seconds | 容器 System CPU累积消费占用时间
`container_cpu_usage_seconds_total` | Counter | Cumulative cpu time consumed | seconds | 统计cpu消耗的持续时间
`container_cpu_user_seconds_total` | Counter | Cumulative user cpu time consumed | seconds | 容器 User CPU累积消费占用时间
`container_file_descriptors` | Gauge | Number of open file descriptors for the container | --- | 容器打开文件描述使用统计
`container_fs_inodes_free` | Gauge | Number of available Inodes | --- | 可用Inode数量
`container_fs_inodes_total` | Gauge | Total number of Inodes | --- | 总的Inode数量
`container_fs_io_current` | Gauge | Number of I/Os currently in progress | ---| 当前进程的IO总数
`container_fs_io_time_seconds_total` | Counter | Cumulative count of seconds spent doing I/Os | seconds | IO时间消耗
`container_fs_io_time_weighted_seconds_total` | Counter | Cumulative weighted I/O time | seconds | IO时间消耗占比
`container_fs_limit_bytes` | Gauge | Number of bytes that can be consumed by the container on this filesystem | bytes | 容器可消费的文件系统容量
`container_fs_reads_bytes_total` | Counter | Cumulative count of bytes read | bytes | 容器读取的数据大小
`container_fs_reads_total` | Counter | Cumulative count of reads completed | --- | 已完成读取的累计计数
`container_fs_read_seconds_total` | Counter | Cumulative count of seconds spent reading | --- | 容器读消耗时间
`container_fs_reads_merged_total` | Counter | Cumulative count of reads merged | --- | 合并的累计读数计数
`container_fs_sector_reads_total` | Counter | Cumulative count of sector reads completed | --- | 扇区读取的累积计数
`container_fs_sector_writes_total` | Counter | Cumulative count of sector writes completed | --- | 扇区写累积计数
`container_fs_usage_bytes` | Gauge | Number of bytes that are consumed by the container on this filesystem | bytes | 容器在此文件系统上使用的字节数
`container_fs_write_seconds_total` | Counter | Cumulative count of seconds spent writing | seconds | 容器写操作累计时间
`container_fs_writes_bytes_total` | Counter | Cumulative count of bytes written | bytes | 容器写数据字节统计
`container_fs_writes_merged_total` | Counter | Cumulative count of writes merged | --- | 容器写合并数据统计
`container_fs_writes_total` | Counter | Cumulative count of writes completed | --- | 容器写数据统计
`container_last_seen` | Gauge | Last time a container was seen by the exporter | timestamp | 容器被exporter上一次查看的时间戳
`container_memory_cache` | Gauge | Total page cache memory | bytes | 缓存总page数
`container_memory_failcnt` | Counter | Number of memory usage hits limits | --- | 内存使用访问限制
`container_memory_failures_total` | Counter | Cumulative count of memory allocation failures | --- | 内存分配失败的累积计数   
`container_memory_max_usage_bytes` | Gauge | Maximum memory usage recorded | bytes | 记录的最大内存使用量
`container_memory_rss` | Gauge | Size of RSS | bytes | 容器RSS大小
`container_memory_swap` | Gauge | Container swap usage | bytes | 容器内存交换分区大小
`container_memory_mapped_file` | Gauge | Size of memory mapped files | bytes | 内存映射文件大小 
`container_memory_usage_bytes` | Gauge | Current memory usage, including all memory regardless of when it was accessed | bytes | 容器当前内存使用量
`container_memory_working_set_bytes` | Gauge | Current working set | bytes | 当前内存使用集合
`container_network_receive_bytes_total` | Counter | Cumulative count of bytes received | bytes | 网络接受流量统计
`container_network_receive_packets_dropped_total` | Counter | Cumulative count of packets dropped while receiving | --- |网络接受时丢包统计
`container_network_receive_packets_total` | Counter | Cumulative count of packets received | --- | 网络总的接收
`container_network_receive_errors_total` | Counter | Cumulative count of errors encountered while receiving | --- | 网络接收遇到错误统计
`container_network_transmit_bytes_total` | Counter | Cumulative count of bytes transmitted | bytes | 网络传输数据量统计
`container_network_transmit_packets_total` | Counter | Cumulative count of packets transmitted | --- | 网络已传输数据包统计
`container_network_transmit_packets_dropped_total` | Counter | Cumulative count of packets dropped while transmitting | --- | 网络传输时丢包统计
`container_network_transmit_errors_total` | Counter | Cumulative count of errors encountered while transmitting | --- | 网络传输时遇到错误统计
`container_network_tcp_usage_total` | Gauge | tcp connection usage statistic for container | --- | 容器tcp协议使用连接量
`container_network_tcp6_usage_total` | Gauge | tcp6 connection usage statistic for container | --- | 容器tcp6协议使用连接量
`container_network_udp_usage_total` | Gauge | udp connection usage statistic for container | --- | 容器udp协议使用连接量
`container_network_udp6_usage_total` | Gauge | udp6 connection usage statistic for container | --- |容器udp6协议使用连接量
`container_processes` | Gauge | Number of processes running inside the container | --- |容器内部进程数
`container_spec_cpu_period` | Gauge | CPU period of the container | --- | 容器cpu周期
`container_spec_cpu_quota` | Gauge | CPU quota of the container | --- |容器cpu限额 
`container_spec_cpu_shares` | Gauge | CPU share of the container | --- | 容器的CPU份额
`container_spec_memory_limit_bytes` | Gauge | Memory limit for the container | bytes | 容器内存限制
`container_spec_memory_swap_limit_bytes` | Gauge | Memory swap limit for the container | bytes | 容器交换分区限制
`container_spec_memory_reservation_limit_bytes` | Gauge | Memory reservation limit for the container | bytes | 容器的内存预留限制 
`container_start_time_seconds` | Gauge | Start time of the container since unix epoch | seconds | 容器启动时间
`container_tasks_state` | Gauge | Number of tasks in given state (`sleeping`, `running`, `stopped`, `uninterruptible`, or `ioawaiting`) | --- | 容器状态统计（睡眠，运行，停止，不间断，IO等待）


