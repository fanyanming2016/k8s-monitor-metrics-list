### kubelet指标释义

Metric name | Type | Description | Unit (where applicable)|  ZH                     |
:-----------|:-----|:------------|:-----------------------|:------------------------|
| kubelet_containers_per_pod_count | Summary | The number of containers per pod. | --- | 每个pod容器个数
| kubelet_pod_worker_latency_microseconds | Summary | Latency in microseconds to sync a single pod. Broken down by operation type: create, update, or sync | --- | 操作pod对象(create, update, or sync)时延
| kubelet_pod_start_latency_microseconds | Summary | Latency in microseconds for a single pod to go from pending to running. | --- | pod 由pending转到running状态的时延
| kubelet_cgroup_manager_latency_microseconds | Summary | Latency in microseconds for cgroup manager operations. Broken down by method. | --- | cgroup 管理操作时延
| kubelet_pod_worker_start_latency_microseconds | Summary | Latency in microseconds from seeing a pod to starting a worker. | --- | pod开启一个工作进程的时延
| kubelet_pleg_relist_latency_microseconds | Summary | Latency in microseconds for relisting pods in PLEG. | --- | 在PLEG阶段中重新启动pod的延迟（以微秒为单位）（PLEG：PodLifecycleEventGenerator）
| kubelet_pleg_relist_interval_microseconds | Summary | Interval in microseconds between relisting in PLEG. | --- | 重新进入PLEG之间的间隔，以微秒为单位
| kubelet_eviction_stats_age_microseconds | Summary | Time between when stats are collected, and when pod is evicted based on those stats by eviction signal | --- | pod被驱逐的状态被收集的时长
| kubelet_runtime_operations | Counter | Cumulative number of runtime operations by operation type. | --- | 按操作类型累计运行时操作数
| kubelet_runtime_operations_latency_microseconds | Summary | Latency in microseconds of runtime operations. Broken down by operation type. | --- | 运行时操作延时,按操作类型细分
| kubelet_runtime_operations_errors | Counter | Cumulative number of runtime operation errors by operation type. | --- | 按操作类型累计运行时操作错误数
| kubelet_device_plugin_registration_count | Counter | Cumulative number of device plugin registrations. Broken down by resource name. | --- | 设备插件注册的累计数量,按资源名称细分
| kubelet_device_plugin_alloc_latency_microseconds | Summary | Latency in microseconds to serve a device plugin Allocation request. Broken down by resource name. | --- | 服务于设备插件分配请求的延迟（以微秒为单位）。按资源名称细分。
| kubelet_node_config_assigned | Gauge | The node's understanding of intended config. The count is always 1. | --- | 节点对预期配置的理解 1
| kubelet_node_config_active | Gauge | The config source the node is actively using. The count is always 1. | --- | 节点正在使用的配置源 1
| kubelet_node_config_last_known_good | Gauge | The config source the node will fall back to when it encounters certain errors. The count is always 1. | --- | 节点将在遇到某些错误时回退到配置源 1
| kubelet_node_config_error | Gauge | This metric is true (1) if the node is experiencing a configuration-related error, false (0) otherwise. | --- | 如果节点遇到与配置相关的错误 1 否则 0
| kubelet_network_plugin_operations_latency_microseconds | Summary | Latency in microseconds for network plugin operations. | --- | 网络插件操作时延

