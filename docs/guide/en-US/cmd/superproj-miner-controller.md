## superproj-miner-controller



### Synopsis

The cloud miner controller is a daemon that embeds
the core control loops. In applications of robotics and
automation, a control loop is a non-terminating loop that regulates the state of
the system. In CloudMiner, a controller is a control loop that watches the shared
state of the miner through the superproj-apiserver and makes changes attempting to move the
current state towards the desired state.

```
superproj-miner-controller [flags]
```

### Options

```
      --add_dir_header                       If true, adds the file directory to the header of the log messages (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --alsologtostderr                      log to standard error as well as files (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --config string                        The path to the configuration file.
  -h, --help                                 help for superproj-miner-controller
      --kubeconfig string                    Path to kubeconfig file with authorization and master location information.
      --log-flush-frequency duration         Maximum number of seconds between log flushes (default 5s)
      --log-json-info-buffer-size quantity   [Alpha] In JSON format with split output streams, the info messages can be buffered for a while to increase performance. The default value of zero bytes disables buffering. The size can be specified as number of bytes (512), multiples of 1000 (1K), multiples of 1024 (2Ki), or powers of those (3M, 4G, 5Mi, 6Gi). Enable the LoggingAlphaOptions feature gate to use this.
      --log-json-split-stream                [Alpha] In JSON format, write error messages to stderr and info messages to stdout. The default is to write a single stream to stdout. Enable the LoggingAlphaOptions feature gate to use this.
      --log_backtrace_at traceLocation       when logging hits line file:N, emit a stack trace (default :0) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --log_dir string                       If non-empty, write log files in this directory (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --log_file string                      If non-empty, use this log file (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --log_file_max_size uint               Defines the maximum size a log file can grow to (no effect when -logtostderr=true). Unit is megabytes. If the value is 0, the maximum file size is unlimited. (default 1800) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --logging-format string                Sets the log format. Permitted formats: "json" (gated by LoggingBetaOptions), "text".
                                             Non-default formats don't honor these flags: --add-dir-header, --alsologtostderr, --log-backtrace-at, --log-dir, --log-file, --log-file-max-size, --logtostderr, --one-output, --skip-headers, --skip-log-headers, --stderrthreshold, --vmodule.
                                             Non-default choices are currently alpha and subject to change without warning. (default "text")
      --logtostderr                          log to standard error instead of files (default true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --master string                        The address of the Kubernetes API server (overrides any value in kubeconfig).
      --one_output                           If true, only write logs to their native severity level (vs also writing to each lower severity level; no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --provider-kubeconfig string           Path to miner provider kubeconfig file with authorization and master location information.
      --skip_headers                         If true, avoid header prefixes in the log messages (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --skip_log_headers                     If true, avoid headers when opening log files (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --stderrthreshold severity             logs at or above this threshold go to stderr when writing to files and stderr (no effect when -logtostderr=true or -alsologtostderr=false) (default 2) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
  -v, --v Level                              number for the log level verbosity
      --version version[=true]               Print version information and quit
      --vmodule pattern=N,...                comma-separated list of pattern=N settings for file-filtered logging (only works for text log format)
      --write-config-to string               If set, write the default configuration values to this file and exit.
```

###### Auto generated by spf13/cobra on 29-Oct-2022
