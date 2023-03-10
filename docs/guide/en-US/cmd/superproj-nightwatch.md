## superproj-nightwatch

Launch a superproj asynchronous task processing server

### Synopsis

The nightwatch server is responsible for executing some async tasks 
like linux cronjob. You can add Cron(github.com/robfig/cron) jobs on the given schedule
use the Cron spec format.

```
superproj-nightwatch [flags]
```

### Options

```
      --add_dir_header                                   If true, adds the file directory to the header of the log messages (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --alsologtostderr                                  log to standard error as well as files (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
  -c, --config FILE                                      Read configuration from specified FILE, support JSON, TOML, YAML, HCL, or Java properties formats.
      --db.database string                               Database name for the server to use.
      --db.host string                                   MySQL service host address. If left blank, the following related mysql options will be ignored. (default "127.0.0.1:3306")
      --db.log-mode int                                  Specify gorm log level. (default 1)
      --db.max-connection-life-time duration             Maximum connection life time allowed to connect to mysql. (default 10s)
      --db.max-idle-connections int                      Maximum idle connections allowed to connect to mysql. (default 100)
      --db.max-open-connections int                      Maximum open connections allowed to connect to mysql. (default 100)
      --db.password string                               Password for access to mysql, should be used pair with password.
      --db.username string                               Username for access to mysql service.
      --feature-gates mapStringBool                      A set of key=value pairs that describe feature gates for alpha/experimental features. Options are:
                                                         AllAlpha=true|false (ALPHA - default=false)
                                                         AllBeta=true|false (BETA - default=false)
                                                         ContextualLogging=true|false (ALPHA - default=false)
                                                         LoggingAlphaOptions=true|false (ALPHA - default=false)
                                                         LoggingBetaOptions=true|false (BETA - default=true)
                                                         MachinePool=true|false (ALPHA - default=false)
  -h, --help                                             help for superproj-nightwatch
      --kubeconfig string                                Path to kubeconfig file with authorization and master location information.
      --log-flush-frequency duration                     Maximum number of seconds between log flushes (default 5s)
      --log-json-info-buffer-size quantity               [Alpha] In JSON format with split output streams, the info messages can be buffered for a while to increase performance. The default value of zero bytes disables buffering. The size can be specified as number of bytes (512), multiples of 1000 (1K), multiples of 1024 (2Ki), or powers of those (3M, 4G, 5Mi, 6Gi). Enable the LoggingAlphaOptions feature gate to use this.
      --log-json-split-stream                            [Alpha] In JSON format, write error messages to stderr and info messages to stdout. The default is to write a single stream to stdout. Enable the LoggingAlphaOptions feature gate to use this.
      --log_backtrace_at traceLocation                   when logging hits line file:N, emit a stack trace (default :0) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --log_dir string                                   If non-empty, write log files in this directory (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --log_file string                                  If non-empty, use this log file (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --log_file_max_size uint                           Defines the maximum size a log file can grow to (no effect when -logtostderr=true). Unit is megabytes. If the value is 0, the maximum file size is unlimited. (default 1800) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --logging-format string                            Sets the log format. Permitted formats: "json" (gated by LoggingBetaOptions), "text".
                                                         Non-default formats don't honor these flags: --add-dir-header, --alsologtostderr, --log-backtrace-at, --log-dir, --log-file, --log-file-max-size, --logtostderr, --one-output, --skip-headers, --skip-log-headers, --stderrthreshold, --vmodule.
                                                         Non-default choices are currently alpha and subject to change without warning. (default "text")
      --logtostderr                                      log to standard error instead of files (default true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --metrics.allow-metric-labels stringToString       The map from metric-label to value allow-list of this label. The key's format is <MetricName>,<LabelName>. The value's format is <allowed_value>,<allowed_value>...e.g. metric1,label1='v1,v2,v3', metric1,label2='v1,v2,v3' metric2,label1='v1,v2,v3'. (default [])
      --metrics.disabled-metrics strings                 This flag provides an escape hatch for misbehaving metrics. You must provide the fully qualified metric name in order to disable it. Disclaimer: disabling metrics is higher in precedence than showing hidden metrics.
      --metrics.show-hidden-metrics-for-version string   The previous version for which you want to show hidden metrics. Only the previous minor version is meaningful, other values will not be allowed. The format is <major>.<minor>, e.g.: '1.16'. The purpose of this format is make sure you have the opportunity to notice if the next release hides additional metrics, rather than being surprised when they are permanently removed in the release after that.
      --one_output                                       If true, only write logs to their native severity level (vs also writing to each lower severity level; no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --redis.addr string                                Address of your Redis server(ip:port). (default "127.0.0.1:6379")
      --redis.database int                               Database to be selected after connecting to the server.
      --redis.max-retries int                            Maximum number of retries before giving up. (default 3)
      --redis.password string                            Optional auth password for Redis db.
      --redis.timeout duration                           Timeout when connecting to redis service. (default 5s)
      --redis.username string                            Username for access to redis service.
      --skip_headers                                     If true, avoid header prefixes in the log messages (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --skip_log_headers                                 If true, avoid headers when opening log files (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --stderrthreshold severity                         logs at or above this threshold go to stderr when writing to files and stderr (no effect when -logtostderr=true or -alsologtostderr=false) (default 2) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
  -v, --v Level                                          number for the log level verbosity
      --version version[=true]                           Print version information and quit
      --vmodule pattern=N,...                            comma-separated list of pattern=N settings for file-filtered logging (only works for text log format)
```

###### Auto generated by spf13/cobra on 29-Oct-2022
