### ingress-controller指标释义

Metric name | Type | Description | Unit (where applicable)|  ZH                     |
:-----------|:-----|:------------|:-----------------------|:------------------------|
| nginx_ingress_controller_config_hash | Gauge | Running configuration hash actually running  | --- |  当前使用的配置文件hash
| nginx_ingress_controller_config_last_reload_successful | Gauge | Whether the last configuration reload attempt was successful | --- | 最新配置文件是否加载成功
| nginx_ingress_controller_config_last_reload_successful_timestamp_seconds | Gauge | Timestamp of the last successful configuration reload.  | --- | 配置文件最新加载的时间
| nginx_ingress_controller_success | Counter | Cumulative number of Ingress controller reload operations. | --- | ingress 控制器重载操作成功次数累计
| nginx_ingress_controller_errors | Gauge | Cumulative number of Ingress controller errors during reload operations | --- | ingress 控制器重载操作出错次数累计
| nginx_ingress_controller_ssl_expire_time_seconds | Gauge | Number of seconds since 1970 to the SSL Certificate expire | --- | SSL证书过期时间（1970年后累计）
| nginx_ingress_controller_nginx_process_connections_total | Counter | total number of connections with state {active, accepted, handled}  | --- | 总的连接数 
| nginx_ingress_controller_nginx_process_requests_total | Counter | total number of client requests | --- | 总的请求连接数
| nginx_ingress_controller_nginx_process_connections | Counter | current number of client connections with state {reading, writing, waiting} | --- | 当前处于给定状态(reading, writing, waiting)连接数
| nginx_ingress_controller_nginx_process_num_procs | Gauge | number of processes | --- | 进程数
| nginx_ingress_controller_nginx_process_cpu_seconds_total | Gauge | Cpu usage in seconds | --- | cpu使用情况
| nginx_ingress_controller_nginx_process_read_bytes_total | Gauge | number of bytes read | --- | 读数据总数
| nginx_ingress_controller_nginx_process_write_bytes_total | Gauge | number of bytes written | --- | 写数据总数
| nginx_ingress_controller_nginx_process_resident_memory_bytes | Counter | number of bytes of memory in use | --- | 内存使用
| nginx_ingress_controller_nginx_process_virtual_memory_bytes | Counter | number of bytes of memory in use | --- | 虚拟内存使用 
| nginx_ingress_controller_nginx_process_oldest_start_time_seconds | Counter | start time in seconds since 1970/01/01 | --- | 开始时间
| nginx_ingress_controller_response_duration_seconds | Histogram | The time spent on receiving the response from the upstream server | --- | 服务请求响应时间
| nginx_ingress_controller_response_size | Histogram | The response length (including request line, header, and request body) | --- | 响应数据大小
| nginx_ingress_controller_request_duration_seconds | Histogram | The request processing time in milliseconds | --- | 请求处理时长
| nginx_ingress_controller_request_size | Histogram | The request length (including request line, header, and request body) | --- | 请求数据大小
| nginx_ingress_controller_requests | Counter | The total number of client requests. | --- | 请求长度
| nginx_ingress_controller_bytes_sent | Counter | The number of bytes sent to a client | --- | 发送给客户端数据大小
| nginx_ingress_controller_ingress_upstream_latency_seconds | Summary | Upstream service latency per Ingress | --- | 上游服务延时