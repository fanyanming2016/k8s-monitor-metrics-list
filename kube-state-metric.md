### kube-state-metrics指标释义

Metric name | Type | Description | Unit (where applicable)|  ZH                     |
:-----------|:-----|:------------|:-----------------------|:------------------------|
| kube_configmap_info | Gauge | Information about configmap  | --- | configmap对象信息 
| kube_configmap_created | Gauge | Unix creation timestamp  | --- | configmap对象的创建时间戳
| kube_configmap_metadata_resource_version| Gauge | Resource version representing a specific version of the configmap | --- | configmap对象版本信息
| kube_cronjob_info | Gauge | Information about cronjob | --- | cronjob对象信息
| kube_cronjob_labels | Gauge | Information about cronjob | --- | 转换为Prometheus标签
| kube_cronjob_created | Gauge | creation timestamp about cronjob | --- | cronjob对象创建的时间戳
| kube_cronjob_next_schedule_time | Gauge | Next time the cronjob should be scheduled. The time after lastScheduleTime, or after the cron job's creation time if it's never been scheduled. Use this to determine if the job is delayed. | --- | cronjob对象下次执行时间
| kube_cronjob_status_active | Gauge | Active holds pointers to currently running job | --- | 当前正在运行job数量
| kube_cronjob_status_last_schedule_time | Gauge | LastScheduleTime keeps information of when was the last time the job was successfully scheduled. | --- | cronjob上次执行时间
| kube_cronjob_spec_suspend | Gauge | Suspend flag tells the controller to suspend subsequent executions | --- | job挂起标记
| kube_cronjob_spec_starting_deadline_seconds | Gauge | Deadline in seconds for starting the job if it misses scheduled time for any reason. | --- | 启动 Job 的期限（秒级别）
| kube_daemonset_created | Gauge | Unix creation timestamp  | --- | 创建时间 
| kube_daemonset_status_current_number_scheduled | Gauge | The number of nodes running at least one daemon pod and are supposed to.  | --- | 运行至少一个守护进程pod的节点的数量
| kube_daemonset_status_desired_number_scheduled| Gauge | The number of nodes that should be running the daemon pod. | --- | 期望运行daemonset POD 的节点数量
| kube_daemonset_status_number_available | Gauge | The number of nodes that should be running the daemon pod and have one or more of the daemon pod running and available | --- | 运行daemonset POD 并且可用的节点的数量
| kube_daemonset_status_number_misscheduled | Gauge | The number of nodes running a daemon pod but are not supposed to. | --- | 不应该运行daemonset POD节点的数量
| kube_daemonset_status_number_ready | Gauge | The number of nodes that should be running the daemon pod and have one or more of the daemon pod running and ready. | --- | 运行daemonset POD 并且ready的节点的数量
| kube_daemonset_status_number_unavailable | Gauge | The number of nodes that should be running the daemon pod and have none of the daemon pod running and available | --- | daemonset POD 不可用的节点的数量
| kube_daemonset_updated_number_scheduled | Gauge | The total number of nodes that are running updated daemon pod | --- | 当前正在运行daemonset POD 节点数量
| kube_daemonset_metadata_generation | Gauge | Sequence number representing a specific generation of the desired state. | --- | 表示期望状态的特定代的序列号。
| kube_daemonset_labels | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签
| kube_deployment_status_replicas | Gauge | The number of replicas per deployment.  | --- | 每个deployment副本数 
| kube_deployment_status_replicas_available | Gauge | The number of available replicas per deployment.  | --- | 每个deployment可用的POD副本数
| kube_deployment_status_replicas_unavailable| Gauge | The number of unavailable replicas per deployment. | --- | 每个deployment不可用的POD副本数
| kube_deployment_status_replicas_updated | Gauge | The number of updated replicas per deployment. | --- | 每个deployment更新的POD副本数
| kube_deployment_status_observed_generation | Gauge | The generation observed by the deployment controller. | --- | 被deployment可观察的应用的代（版本）
| kube_deployment_spec_replicas | Gauge | Number of desired pods for a deployment. | --- | 期望的副本数
| kube_deployment_spec_paused | Gauge | Whether the deployment is paused and will not be processed by the deployment controller. | --- | deployment是否处理暂停的POD
| kube_deployment_spec_strategy_rollingupdate_max_unavailable | Gauge | The total number of nodes that are running updated daemon pod | --- | 滚动更新部署期间的最大不可用副本数
| kube_deployment_spec_strategy_rollingupdate_max_surge | Gauge | Maximum number of replicas that can be scheduled above the desired number of replicas during a rolling update of a deployment. | --- | 在部署的滚动更新期间可以在所需数量的副本之上调度的最大副本数
| kube_deployment_labels | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签
| kube_deployment_created | Gauge | Unix creation timestamp. | --- | 创建时间
| kube_endpoint_address_not_ready | Gauge | Number of addresses not ready in endpoint. | --- | endpoint IP地址没有准备好的个数
| kube_endpoint_address_available | Gauge | Number of addresses available in endpoint. | --- | endpoint IP地址可用个数
| kube_endpoint_info | Gauge | Information about endpoint.. | --- | endpoint 对象信息
| kube_endpoint_labels | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签
| kube_endpoint_created | Gauge | Unix creation timestamp | --- | 创建时间
| kube_hpa_metadata_generation | Gauge | The generation observed by the HorizontalPodAutoscaler controller. | --- | 被HorizontalPodAutoscaler观察的代（版本）
| kube_hpa_spec_max_replicas | Gauge | Upper limit for the number of pods that can be set by the autoscaler; cannot be smaller than MinReplicas. | --- | 可水平扩容的POD副本最大限制
| kube_hpa_spec_min_replicas | Gauge | Lower limit for the number of pods that can be set by the autoscaler, default 1. | --- | 可水平扩容的POD副本最低限制 >= 1
| kube_hpa_status_current_replicas | Gauge | Current number of replicas of pods managed by this autoscaler. | --- | 当前被HorizontalPodAutoscaler管理的副本数
| kube_hpa_status_desired_replicas | Gauge | Desired number of replicas of pods managed by this autoscaler. | --- | 期望被HorizontalPodAutoscaler管理的副本数
| kube_job_info | Gauge | Information about job. | --- | job对象信息
| kube_job_labels | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签
| kube_job_spec_parallelism | Gauge | The maximum desired number of pods the job should run at any given time. | --- | job运行时期望的最大POD数量
| kube_job_spec_completions | Gauge | The desired number of successfully finished pods the job should be run with. | --- | job运行所需的成功完成的期望pod数量
| kube_job_spec_active_deadline_seconds | Gauge | The duration in seconds relative to the startTime that the job may be active before the system tries to terminate it. | --- | job终止时间(以秒为单位）
| kube_job_status_active | Gauge | The number of actively running pods. | --- | job中正在活动的pod
| kube_job_status_succeeded | Gauge | The number of pods which reached Phase Succeeded. | --- | job中完成任务的pod
| kube_job_status_failed | Gauge | The number of pods which reached Phase Failed | --- | job中任务失败的pod
| kube_job_status_start_time | Gauge | StartTime represents time when the job was acknowledged by the Job Manager. | --- | job对象信息
| kube_job_status_completion_time | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签
| kube_job_complete | Gauge | Information about job. | --- | job对象信息
| kube_job_failed | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签
| kube_job_created | Gauge | Unix creation timestamp. | --- | 创建时间
| kube_limitrange | Gauge | Information about limit range. | --- | 资源限制对象信息
| kube_limitrange_created | Gauge | Unix creation timestamp. | --- | 创建时间
| kube_namespace_status_phase | Gauge | kubernetes namespace status phase. | --- | namespace状态
| kube_namespace_labels | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签
| kube_namespace_annotations | Gauge | Kubernetes annotations converted to Prometheus labels. | --- | 转换为Prometheus标签
| kube_namespace_created | Gauge | Unix creation timestamp. | --- | 创建时间
| kube_node_info | Gauge | Information about a cluster node. | --- | 节点对象信息
| kube_node_labels | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签
| kube_node_spec_unschedulable | Gauge | Whether a node can schedule new pods. | --- | 节点是否可以部署应用
| kube_node_spec_taint | Gauge | The taint of a cluster node. | --- | 节点的污点
| kube_node_status_phase| Gauge | The phase the node is currently in. | --- | 节点当前阶段状态
| kube_node_status_capacity | Gauge | The capacity for different resources of a node.| --- | 节点资源容量
| kube_node_status_capacity_cpu_cores | Gauge | The total CPU resources of the node. | --- | 节点CPU容量
| kube_node_status_capacity_memory_bytes | Gauge | The total memory resources of the node. | --- | 节点内存资源容量
| kube_node_status_capacity_pods | Gauge | The total pod resources of the node. | --- | 节点POD容量
| kube_node_status_allocatable | Gauge | The allocatable for different resources of a node that are available for scheduling. | --- | 节点可分配资源的状态
| kube_node_status_allocatable_cpu_cores | Gauge | The CPU resources of a node that are available for scheduling. | --- | 节点可分配的cpu资源
| kube_node_status_allocatable_memory_bytes | Gauge | The memory resources of a node that are available for scheduling. | --- | 节点可分配的内存资源
| kube_node_status_allocatable_pods | Gauge | The pod resources of a node that are available for scheduling. | --- | 节点可分配pod资源
| kube_node_status_condition | Gauge | The condition of a cluster node. | --- | 节点的条件状态
| kube_node_created | Gauge | Unix creation timestamp. | --- | 创建时间
| kube_persistentvolume_status_phase | Gauge | The phase indicates if a volume is available, bound to a claim, or released by a claim. | --- | 当前阶段PV状态，是否可用，是否绑定pvc
| kube_persistentvolume_labels | Gauge | Kubernetes labels converted to Prometheus labels.  | --- | 转换为Prometheus标签
| kube_persistentvolume_info | Gauge | Information about persistentvolume. | --- | PV对象信息
| kube_persistentvolumeclaim_info | Gauge | Information about persistent volume claim. | --- | PVC对象信息
| kube_persistentvolumeclaim_labels | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签 
| kube_persistentvolumeclaim_status_phase | Gauge | The phase the persistent volume claim is currently in. | --- | PVC当前阶段状态
| kube_persistentvolumeclaim_resource_requests_storage_bytes | Gauge | The capacity of storage requested by the persistent volume claim. | --- | PVC声明存储容量大小
| kube_pod_info | Gauge | Information about pod.| --- | pod对象信息
| kube_pod_start_time | Gauge | Start time in unix timestamp for a pod. | ---| pod启动时间
| kube_pod_completion_time | Gauge | Completion time in unix timestamp for a pod. | --- | pod完成时间
| kube_pod_owner | Gauge | Information about the Pod's owner.  | --- | pod拥有者
| kube_pod_labels | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签 
| kube_pod_status_phase | Gauge | The pods current phase. | --- | pod当前阶段状态,Pending,Running,Succeeded,Failed,Unknown
| kube_pod_status_ready | Gauge |  Describes whether the pod is ready to serve requests. | --- | pod 是否可提供服务
| kube_pod_status_scheduled | Gauge |  Describes the status of the scheduling process for the pod. | --- | pod 部署阶段状态
| kube_pod_container_info | Gauge | Information about a container in a pod. | --- | pod 内部容器信息
| kube_pod_container_status_waiting | Gauge | Describes whether the container is currently in waiting state. | --- | pod内容器是否是等待状态
| kube_pod_container_status_waiting_reason | Gauge | Describes the reason the container is currently in waiting state. | --- | pod内部容器处于waiting状态的原因
| kube_pod_container_status_running | Gauge | Describes whether the container is currently in running state. | --- | pod内部容器是否运行状态
| kube_pod_container_status_terminated | Gauge | Describes whether the container is currently in terminated state. | --- | pod内部容器是否处于终止状态
| kube_pod_container_status_terminated_reason | Gauge | Describes the reason the container is currently in terminated state. | --- | pod内部容器处于终止状态的原因 
| kube_pod_container_status_last_terminated_reason | Gauge | Describes the last reason the container was in terminated state. | --- | pod内部容器处于终止状态的最终原因 
| kube_pod_container_status_ready | Gauge | Describes whether the containers readiness check succeeded. | --- | pod容器是否成功运行
| kube_pod_container_status_restarts_total | Counter | The number of container restarts per container. | --- | pod容器重启次数
| kube_pod_container_resource_requests_cpu_cores | Gauge | The number of requested cpu cores by a container. | --- | pod容器申请最低cpu资源大小
| kube_pod_container_resource_requests | Gauge | The number of requested request resource by a container. | --- | pod容器申请最低资源大小
| kube_pod_container_resource_requests_memory_bytes | Gauge | The number of requested memory bytes by a container. | --- | pod容器申请最低内存资源大小
| kube_pod_container_resource_limits_cpu_cores | Gauge | The limit on cpu cores to be used by a container. | --- | pod容器申请cpu资源限制
| kube_pod_container_resource_limits | Gauge | The number of requested limit resource by a container. | --- | pod容器申请资源限制
| kube_pod_container_resource_limits_memory_bytes | Gauge | The limit on memory to be used by a container in bytes. | --- | pod容器申请容器资源限制
| kube_pod_created | Gauge | Unix creation timestamp | --- | 创建时间
| kube_pod_spec_volumes_persistentvolumeclaims_info | Gauge | Information about persistentvolumeclaim volumes in a pod. | --- | pod PVC资源声明信息
| kube_pod_spec_volumes_persistentvolumeclaims_readonly | Gauge | `Describes whether a persistentvolumeclaim is mounted read only. | --- | pod 挂载的存储是否只读状态
| kube_pod_status_scheduled_time | Gauge | Unix timestamp when pod moved into scheduled status | --- | pod 转换成部署状态的时间
| kube_poddisruptionbudget_created | Gauge | Unix creation timestamp  | --- | 创建时间
| kube_poddisruptionbudget_status_current_healthy | Gauge | Current number of healthy pods  | --- | 当前处于健康状态的pod个数
| kube_poddisruptionbudget_status_desired_healthy | Gauge | Minimum desired number of healthy pods  | --- | 当前期望健康状态的pod个数
| kube_poddisruptionbudget_status_pod_disruptions_allowed | Gauge | Number of pod disruptions that are currently allowed  | --- | 当前允许的pod中断的个数
| kube_poddisruptionbudget_status_expected_pods | Gauge | Total number of pods counted by this disruption budget | --- | 当前被中断的所有pod总数
| kube_poddisruptionbudget_status_observed_generation | Gauge | Most recent generation observed when updating this PDB status | --- | 当更新此PDB的状态时可观察到的最新一代
| kube_replicaset_status_replicas | Gauge | The number of replicas per ReplicaSet. | --- | ReplicaSet中副本个数
| kube_replicaset_status_fully_labeled_replicas | Gauge | The number of fully labeled replicas per ReplicaSet. | --- | ReplicaSet中被完全打标签的个数
| kube_replicaset_status_ready_replicas | Gauge | The number of ready replicas per ReplicaSet. | --- | ReplicaSet中就绪状态副本的个数
| kube_replicaset_status_observed_generation | Gauge | The generation observed by the ReplicaSet controller. | --- | 被ReplicaSet观察到的代数(版本)
| kube_replicaset_spec_replicas | Gauge | Number of desired pods for a ReplicaSet. | --- | 每个副本中期望的pod个数
| kube_replicaset_metadata_generation | Gauge | Sequence number representing a specific generation of the desired state. | --- | 表示期望状态的特定代的序列号
| kube_replicaset_created | Gauge | Unix creation timestamp | --- | 创建时间
| kube_replicaset_owner | Gauge | Information about the ReplicaSet's owner. | --- | ReplicaSet拥有者信息
| kube_replicationcontroller_status_replicas | Gauge | The number of replicas per ReplicationController. | --- | ReplicationController 副本个数
| kube_replicationcontroller_status_fully_labeled_replicas | Gauge | The number of fully labeled replicas per ReplicationController. | --- | 每个ReplicationController的完全标记的副本数
| kube_replicationcontroller_status_ready_replicas | Gauge | The number of ready replicas per ReplicationController. | --- | 每个ReplicationController的就绪副本数
| kube_replicationcontroller_status_available_replicas | Gauge | The number of available replicas per ReplicationController. | --- | 每个ReplicationController的可用副本数。
| kube_replicationcontroller_status_observed_generation | Gauge | The generation observed by the ReplicationController controller. | --- | ReplicationController控制器观察到的代（版本）
| kube_replicationcontroller_spec_replicas | Gauge | Number of desired pods for a ReplicationController. | --- | ReplicationController所期望的pod数
| kube_replicationcontroller_metadata_generation | Gauge | Sequence number representing a specific generation of the desired state. | --- | 表示期望状态的特定代的序列号
| kube_replicationcontroller_created | Gauge | Unix creation timestamp | --- | 创建时间
| kube_resourcequota | Gauge | Information about resource quota. | --- | 资源配额对象信息
| kube_resourcequota_created | Gauge | Unix creation timestamp | --- | 创建时间
| kube_secret_info | Gauge | Information about secret. | --- | secret对象信息
| kube_secret_type | Gauge | Type about secret | --- | secret对象类型
| kube_secret_labels | Gauge | kube_secret_labels | --- | 转换为Prometheus标签
| kube_secret_created  | Gauge | Unix creation timestamp | --- | 创建时间
| kube_secret_metadata_resource_version  | Gauge | Resource version representing a specific version of secret. | --- | 表示特定版本的秘密的资源版本
| kube_service_info | Gauge |  Information about service. | --- | svc对象信息
| kube_service_labels | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签
| kube_service_created | Gauge | Unix creation timestamp | --- | 创建时间
| kube_service_spec_type | Gauge | Type about service. | --- | svc类型
| kube_service_spec_external_ip | Gauge | Service external ips. One series for each ip| --- | svc的Eip
| kube_service_status_load_balancer_ingress | Gauge | Service load balancer ingress status | --- | svc负载均衡状态
| kube_statefulset_status_replicas | Gauge | The number of replicas per StatefulSet.  | --- | StatefulSet副本个数
| kube_statefulset_status_replicas_current | Gauge | The number of current replicas per StatefulSet.  | --- |  StatefulSet当前副本个数
| kube_statefulset_status_replicas_ready | Gauge | The number of ready replicas per StatefulSet. | --- | StatefulSet副本就绪个数
| kube_statefulset_status_replicas_updated | Gauge | The number of updated replicas per StatefulSet.  | --- | StatefulSet的更新副本数
| kube_statefulset_status_observed_generation | Gauge | The generation observed by the StatefulSet controller. | --- | StatefulSet观察到的代（版本）
| kube_statefulset_replicas | Gauge | Number of desired pods for a StatefulSet. | --- | StatefulSet期望的副本数
| kube_statefulset_metadata_generation | Gauge | Sequence number representing a specific generation of the desired state for the StatefulSet. | --- | 表示StatefulSet的所期望状态的特定代的序列号。
| kube_statefulset_created | Gauge | Unix creation timestamp  | --- | 创建时间 
| kube_statefulset_labels | Gauge | Kubernetes labels converted to Prometheus labels. | --- | 转换为Prometheus标签
| kube_statefulset_status_current_revision | Gauge | Indicates the version of the StatefulSet used to generate Pods in the sequence [0,currentReplicas). | --- | 表示用于在序列[0，currentReplicas]中生成Pod的StatefulSet的版本。
| kube_statefulset_status_update_revision | Gauge | Indicates the version of the StatefulSet used to generate Pods in the sequence [replicas-updatedReplicas,replicas) | --- | 表示用于在序列[replicas-updatedReplicas，replicas]中生成Pod的StatefulSet的版本