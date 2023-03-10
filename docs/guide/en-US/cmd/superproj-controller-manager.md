## superproj-controller-manager



### Synopsis

The cloud miner controller manager is a daemon that embeds
the core control loops. In applications of robotics and
automation, a control loop is a non-terminating loop that regulates the state of
the system. In CloudMiner, a controller is a control loop that watches the shared
state of the miner through the superproj-apiserver and makes changes attempting to move the
current state towards the desired state.

```
superproj-controller-manager [flags]
```

### Options

```
      --add_dir_header                            If true, adds the file directory to the header of the log messages (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --alsologtostderr                           log to standard error as well as files (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --concurrent-gc-syncs int32                 The number of garbage collector workers that are allowed to sync concurrently. (default 20)
  -c, --config FILE                               Read configuration from specified FILE, support JSON, TOML, YAML, HCL, or Java properties formats.
      --enable-garbage-collector                  Enables the generic garbage collector. MUST be synced with the corresponding flag of the kube-apiserver. (default true)
      --feature-gates mapStringBool               A set of key=value pairs that describe feature gates for alpha/experimental features. Options are:
                                                  APIListChunking=true|false (BETA - default=true)
                                                  APIPriorityAndFairness=true|false (BETA - default=true)
                                                  APIResponseCompression=true|false (BETA - default=true)
                                                  APIServerIdentity=true|false (ALPHA - default=false)
                                                  APIServerTracing=true|false (ALPHA - default=false)
                                                  AllAlpha=true|false (ALPHA - default=false)
                                                  AllBeta=true|false (BETA - default=false)
                                                  AnyVolumeDataSource=true|false (BETA - default=true)
                                                  AppArmor=true|false (BETA - default=true)
                                                  CPUManager=true|false (BETA - default=true)
                                                  CPUManagerPolicyAlphaOptions=true|false (ALPHA - default=false)
                                                  CPUManagerPolicyBetaOptions=true|false (BETA - default=true)
                                                  CPUManagerPolicyOptions=true|false (BETA - default=true)
                                                  CSIMigrationAzureFile=true|false (BETA - default=true)
                                                  CSIMigrationPortworx=true|false (BETA - default=false)
                                                  CSIMigrationRBD=true|false (ALPHA - default=false)
                                                  CSIMigrationvSphere=true|false (BETA - default=true)
                                                  CSINodeExpandSecret=true|false (ALPHA - default=false)
                                                  CSIVolumeHealth=true|false (ALPHA - default=false)
                                                  ContainerCheckpoint=true|false (ALPHA - default=false)
                                                  ContextualLogging=true|false (ALPHA - default=false)
                                                  CronJobTimeZone=true|false (BETA - default=true)
                                                  CustomCPUCFSQuotaPeriod=true|false (ALPHA - default=false)
                                                  CustomResourceValidationExpressions=true|false (BETA - default=true)
                                                  DelegateFSGroupToCSIDriver=true|false (BETA - default=true)
                                                  DevicePlugins=true|false (BETA - default=true)
                                                  DisableCloudProviders=true|false (ALPHA - default=false)
                                                  DisableKubeletCloudCredentialProviders=true|false (ALPHA - default=false)
                                                  DownwardAPIHugePages=true|false (BETA - default=true)
                                                  EndpointSliceTerminatingCondition=true|false (BETA - default=true)
                                                  ExpandedDNSConfig=true|false (ALPHA - default=false)
                                                  ExperimentalHostUserNamespaceDefaulting=true|false (BETA - default=false)
                                                  GRPCContainerProbe=true|false (BETA - default=true)
                                                  GracefulNodeShutdown=true|false (BETA - default=true)
                                                  GracefulNodeShutdownBasedOnPodPriority=true|false (BETA - default=true)
                                                  HPAContainerMetrics=true|false (ALPHA - default=false)
                                                  HPAScaleToZero=true|false (ALPHA - default=false)
                                                  HonorPVReclaimPolicy=true|false (ALPHA - default=false)
                                                  IPTablesOwnershipCleanup=true|false (ALPHA - default=false)
                                                  InTreePluginAWSUnregister=true|false (ALPHA - default=false)
                                                  InTreePluginAzureDiskUnregister=true|false (ALPHA - default=false)
                                                  InTreePluginAzureFileUnregister=true|false (ALPHA - default=false)
                                                  InTreePluginGCEUnregister=true|false (ALPHA - default=false)
                                                  InTreePluginOpenStackUnregister=true|false (ALPHA - default=false)
                                                  InTreePluginPortworxUnregister=true|false (ALPHA - default=false)
                                                  InTreePluginRBDUnregister=true|false (ALPHA - default=false)
                                                  InTreePluginvSphereUnregister=true|false (ALPHA - default=false)
                                                  JobMutableNodeSchedulingDirectives=true|false (BETA - default=true)
                                                  JobPodFailurePolicy=true|false (ALPHA - default=false)
                                                  JobReadyPods=true|false (BETA - default=true)
                                                  JobTrackingWithFinalizers=true|false (BETA - default=true)
                                                  KMSv2=true|false (ALPHA - default=false)
                                                  KubeletCredentialProviders=true|false (BETA - default=true)
                                                  KubeletInUserNamespace=true|false (ALPHA - default=false)
                                                  KubeletPodResources=true|false (BETA - default=true)
                                                  KubeletPodResourcesGetAllocatable=true|false (BETA - default=true)
                                                  KubeletTracing=true|false (ALPHA - default=false)
                                                  LegacyServiceAccountTokenNoAutoGeneration=true|false (BETA - default=true)
                                                  LocalStorageCapacityIsolationFSQuotaMonitoring=true|false (ALPHA - default=false)
                                                  LogarithmicScaleDown=true|false (BETA - default=true)
                                                  LoggingAlphaOptions=true|false (ALPHA - default=false)
                                                  LoggingBetaOptions=true|false (BETA - default=true)
                                                  MatchLabelKeysInPodTopologySpread=true|false (ALPHA - default=false)
                                                  MaxUnavailableStatefulSet=true|false (ALPHA - default=false)
                                                  MemoryManager=true|false (BETA - default=true)
                                                  MemoryQoS=true|false (ALPHA - default=false)
                                                  MinDomainsInPodTopologySpread=true|false (BETA - default=false)
                                                  MixedProtocolLBService=true|false (BETA - default=true)
                                                  MultiCIDRRangeAllocator=true|false (ALPHA - default=false)
                                                  NetworkPolicyStatus=true|false (ALPHA - default=false)
                                                  NodeInclusionPolicyInPodTopologySpread=true|false (ALPHA - default=false)
                                                  NodeOutOfServiceVolumeDetach=true|false (ALPHA - default=false)
                                                  NodeSwap=true|false (ALPHA - default=false)
                                                  OpenAPIEnums=true|false (BETA - default=true)
                                                  OpenAPIV3=true|false (BETA - default=true)
                                                  PodAndContainerStatsFromCRI=true|false (ALPHA - default=false)
                                                  PodDeletionCost=true|false (BETA - default=true)
                                                  PodDisruptionConditions=true|false (ALPHA - default=false)
                                                  PodHasNetworkCondition=true|false (ALPHA - default=false)
                                                  ProbeTerminationGracePeriod=true|false (BETA - default=true)
                                                  ProcMountType=true|false (ALPHA - default=false)
                                                  ProxyTerminatingEndpoints=true|false (ALPHA - default=false)
                                                  QOSReserved=true|false (ALPHA - default=false)
                                                  ReadWriteOncePod=true|false (ALPHA - default=false)
                                                  RecoverVolumeExpansionFailure=true|false (ALPHA - default=false)
                                                  RemainingItemCount=true|false (BETA - default=true)
                                                  RetroactiveDefaultStorageClass=true|false (ALPHA - default=false)
                                                  RotateKubeletServerCertificate=true|false (BETA - default=true)
                                                  SELinuxMountReadWriteOncePod=true|false (ALPHA - default=false)
                                                  SeccompDefault=true|false (BETA - default=true)
                                                  ServerSideFieldValidation=true|false (BETA - default=true)
                                                  ServiceIPStaticSubrange=true|false (BETA - default=true)
                                                  ServiceInternalTrafficPolicy=true|false (BETA - default=true)
                                                  SizeMemoryBackedVolumes=true|false (BETA - default=true)
                                                  StatefulSetAutoDeletePVC=true|false (ALPHA - default=false)
                                                  StorageVersionAPI=true|false (ALPHA - default=false)
                                                  StorageVersionHash=true|false (BETA - default=true)
                                                  TopologyAwareHints=true|false (BETA - default=true)
                                                  TopologyManager=true|false (BETA - default=true)
                                                  UserNamespacesStatelessPodsSupport=true|false (ALPHA - default=false)
                                                  VolumeCapacityPriority=true|false (ALPHA - default=false)
                                                  WinDSR=true|false (ALPHA - default=false)
                                                  WinOverlay=true|false (BETA - default=true)
                                                  WindowsHostProcessContainers=true|false (BETA - default=true)
  -h, --help                                      help for superproj-controller-manager
      --kubeconfig string                         Path to kubeconfig file with authorization and master location information.
      --leader-elect                              Start a leader election client and gain leadership before executing the main loop. Enable this when running replicated components for high availability. (default true)
      --leader-elect-lease-duration duration      The duration that non-leader candidates will wait after observing a leadership renewal until attempting to acquire leadership of a led but unrenewed leader slot. This is effectively the maximum duration that a leader can be stopped before it is replaced by another candidate. This is only applicable if leader election is enabled. (default 15s)
      --leader-elect-renew-deadline duration      The interval between attempts by the acting master to renew a leadership slot before it stops leading. This must be less than or equal to the lease duration. This is only applicable if leader election is enabled. (default 10s)
      --leader-elect-resource-lock string         The type of resource object that is used for locking during leader election. Supported options are 'leases', 'endpointsleases' and 'configmapsleases'. (default "leases")
      --leader-elect-resource-name string         The name of resource object that is used for locking during leader election. (default "superproj-controller-manager")
      --leader-elect-resource-namespace string    The namespace of resource object that is used for locking during leader election. (default "kube-system")
      --leader-elect-retry-period duration        The duration the clients should wait between attempting acquisition and renewal of a leadership. This is only applicable if leader election is enabled. (default 2s)
      --log-flush-frequency duration              Maximum number of seconds between log flushes (default 5s)
      --log-json-info-buffer-size quantity        [Alpha] In JSON format with split output streams, the info messages can be buffered for a while to increase performance. The default value of zero bytes disables buffering. The size can be specified as number of bytes (512), multiples of 1000 (1K), multiples of 1024 (2Ki), or powers of those (3M, 4G, 5Mi, 6Gi). Enable the LoggingAlphaOptions feature gate to use this.
      --log-json-split-stream                     [Alpha] In JSON format, write error messages to stderr and info messages to stdout. The default is to write a single stream to stdout. Enable the LoggingAlphaOptions feature gate to use this.
      --log_backtrace_at traceLocation            when logging hits line file:N, emit a stack trace (default :0) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --log_dir string                            If non-empty, write log files in this directory (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --log_file string                           If non-empty, use this log file (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --log_file_max_size uint                    Defines the maximum size a log file can grow to (no effect when -logtostderr=true). Unit is megabytes. If the value is 0, the maximum file size is unlimited. (default 1800) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --logging-format string                     Sets the log format. Permitted formats: "json" (gated by LoggingBetaOptions), "text".
                                                  Non-default formats don't honor these flags: --add-dir-header, --alsologtostderr, --log-backtrace-at, --log-dir, --log-file, --log-file-max-size, --logtostderr, --one-output, --skip-headers, --skip-log-headers, --stderrthreshold, --vmodule.
                                                  Non-default choices are currently alpha and subject to change without warning. (default "text")
      --logtostderr                               log to standard error instead of files (default true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --master string                             The address of the Kubernetes API server (overrides any value in kubeconfig).
      --metrics-bind-address string               The IP address with port for the metrics server to serve on (set to '0.0.0.0:10249' for all IPv4 interfaces and '[::]:10249' for all IPv6 interfaces). Set empty to disable. This parameter is ignored if a config file is specified by --config.
      --mysql-database string                     Database name for the server to use.
      --mysql-host string                         MySQL service host address. If left blank, the following related mysql options will be ignored. (default "127.0.0.1:3306")
      --mysql-max-connection-life-time duration   Maximum connection life time allowed to connect to mysql. (default 10s)
      --mysql-max-idle-connections int32          Maximum idle connections allowed to connect to mysql. (default 100)
      --mysql-max-open-connections int32          Maximum open connections allowed to connect to mysql. (default 100)
      --mysql-password string                     Password for access to mysql, should be used pair with password.
      --mysql-username string                     Username for access to mysql service.
      --node-image string                         The blockchain node image used by default. (default "ccr.ccs.tencentyun.com/marmotedu/tbb:v1.0.0")
      --one_output                                If true, only write logs to their native severity level (vs also writing to each lower severity level; no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --skip_headers                              If true, avoid header prefixes in the log messages (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --skip_log_headers                          If true, avoid headers when opening log files (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --stderrthreshold severity                  logs at or above this threshold go to stderr when writing to files and stderr (no effect when -logtostderr=true or -alsologtostderr=false) (default 2) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
  -v, --v Level                                   number for the log level verbosity
      --version version[=true]                    Print version information and quit
      --vmodule pattern=N,...                     comma-separated list of pattern=N settings for file-filtered logging (only works for text log format)
```

###### Auto generated by spf13/cobra on 29-Oct-2022
