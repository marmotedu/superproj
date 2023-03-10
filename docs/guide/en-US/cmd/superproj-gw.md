## superproj-gw

Launch a superproj gateway server

### Synopsis

The gateway server is the back-end portal server of superproj. All 
requests from the front-end will arrive at the gateway, requests will be uniformly processed 
and distributed by the gateway.

```
superproj-gw [flags]
```

### Options

```
      --add_dir_header                                   If true, adds the file directory to the header of the log messages (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --alsologtostderr                                  log to standard error as well as files (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --client.debug                                     Enables the debug mode on Resty client.
      --client.retry-count int                           Enables retry on Resty client and allows you to set no. of retry count. Resty uses a Backoff mechanism. (default 3)
      --client.timeout duration                          Request timeout for client. (default 30s)
      --client.user-agent string                         Used to specify the Resty client User-Agent. (default "superproj")
  -c, --config FILE                                      Read configuration from specified FILE, support JSON, TOML, YAML, HCL, or Java properties formats.
      --consul.addr string                               Addr is the address of the consul server. (default "127.0.0.1:8500")
      --consul.scheme string                             Scheme is the URI scheme for the consul server. (default "http")
      --db.database string                               Database name for the server to use.
      --db.host string                                   MySQL service host address. If left blank, the following related mysql options will be ignored. (default "127.0.0.1:3306")
      --db.log-mode int                                  Specify gorm log level. (default 1)
      --db.max-connection-life-time duration             Maximum connection life time allowed to connect to mysql. (default 10s)
      --db.max-idle-connections int                      Maximum idle connections allowed to connect to mysql. (default 100)
      --db.max-open-connections int                      Maximum open connections allowed to connect to mysql. (default 100)
      --db.password string                               Password for access to mysql, should be used pair with password.
      --db.username string                               Username for access to mysql service.
      --enable-tls                                       Enable TLS for grpc server.
      --etcd.ca-cert string                              Path to cacert for connecting to etcd cluster.
      --etcd.cert string                                 Path to cert file for connecting to etcd cluster.
      --etcd.endpoints strings                           Endpoints of etcd cluster.
      --etcd.health-beat-iface-name string               health beat registry iface name, such as eth0.
      --etcd.health-beat-path-pre string                 health beat path prefix.
      --etcd.key string                                  Path to key file for connecting to etcd cluster.
      --etcd.lease-expire int                            Etcd expire timeout in seconds. (default 5)
      --etcd.namespace string                            Etcd storage namespace.
      --etcd.password string                             Password of etcd cluster.
      --etcd.request-timeout int                         Etcd request timeout in seconds. (default 2)
      --etcd.timeout int                                 Etcd dial timeout in seconds. (default 5)
      --etcd.use-tls                                     Use tls transport to connect etcd cluster.
      --etcd.username string                             Username of etcd cluster.
      --feature-gates mapStringBool                      A set of key=value pairs that describe feature gates for alpha/experimental features. Options are:
                                                         AllAlpha=true|false (ALPHA - default=false)
                                                         AllBeta=true|false (BETA - default=false)
                                                         ContextualLogging=true|false (ALPHA - default=false)
                                                         LoggingAlphaOptions=true|false (ALPHA - default=false)
                                                         LoggingBetaOptions=true|false (BETA - default=true)
                                                         MachinePool=true|false (ALPHA - default=false)
      --grpc.bind-address string                         The IP address on which to serve the --grpc.bind-port(set to 0.0.0.0 for all IPv4 interfaces and :: for all IPv6 interfaces). (default "0.0.0.0")
      --grpc.bind-port int                               The port on which to serve unsecured, unauthenticated grpc access. It is assumed that firewall rules are set up such that this port is not reachable from outside of the deployed machine and that port 443 on the iam public address is proxied to this port. This is performed by nginx in the default setup. Set to zero to disable. (default 8081)
      --grpc.max-msg-size int                            gRPC max message size. (default 4194304)
  -h, --help                                             help for superproj-gw
      --insecure.bind-address string                     The IP address on which to serve the --insecure.bind-port (set to 0.0.0.0 for all IPv4 interfaces and :: for all IPv6 interfaces). (default "127.0.0.1")
      --insecure.bind-port int                           The port on which to serve unsecured, unauthenticated access. It is assumed that firewall rules are set up such that this port is not reachable from outside of the deployed machine and that port 443 on the iam public address is proxied to this port. This is performed by nginx in the default setup. Set to zero to disable. (default 8080)
      --jaeger.server string                             Server is the url of the Jaeger server. (default "http://127.0.0.1:14268/api/traces")
      --jaeger.service-name string                       Specify the service name for jaeger resource.
      --jwt.expired duration                             JWT token expiration time. (default 2h0m0s)
      --jwt.key string                                   Private key used to sign jwt token. (default "superproj666")
      --jwt.max-refresh duration                         This field allows clients to refresh their token until MaxRefresh has passed. (default 2h0m0s)
      --jwt.signing-method string                        JWT token signature method. (default "HS512")
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
      --secure.bind-address string                       The IP address on which to listen for the --secure.bind-port port. The associated interface(s) must be reachable by the rest of the engine, and by CLI/web clients. If blank, all interfaces will be used (0.0.0.0 for all IPv4 interfaces and :: for all IPv6 interfaces). (default "0.0.0.0")
      --secure.bind-port int                             The port on which to serve HTTPS with authentication and authorization. It cannot be switched off with 0. (default 8443)
      --secure.tls.cert-dir string                       The directory where the TLS certs are located. If --secure.tls.cert-key.cert-file and --secure.tls.cert-key.private-key-file are provided, this flag will be ignored. (default "/var/run/iam")
      --secure.tls.cert-key.cert-file string             File containing the default x509 Certificate for HTTPS. (CA cert, if any, concatenated after server cert).
      --secure.tls.cert-key.private-key-file string      File containing the default x509 private key matching --secure.tls.cert-key.cert-file.
      --secure.tls.pair-name string                      The name which will be used with --secure.tls.cert-dir to make a cert and key filenames. It becomes <cert-dir>/<pair-name>.crt and <cert-dir>/<pair-name>.key (default "iam")
      --skip_headers                                     If true, avoid header prefixes in the log messages (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --skip_log_headers                                 If true, avoid headers when opening log files (no effect when -logtostderr=true) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
      --stderrthreshold severity                         logs at or above this threshold go to stderr when writing to files and stderr (no effect when -logtostderr=true or -alsologtostderr=false) (default 2) (DEPRECATED: will be removed in a future release, see https://github.com/kubernetes/enhancements/tree/master/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components)
  -v, --v Level                                          number for the log level verbosity
      --version version[=true]                           Print version information and quit
      --vmodule pattern=N,...                            comma-separated list of pattern=N settings for file-filtered logging (only works for text log format)
```

###### Auto generated by spf13/cobra on 29-Oct-2022
