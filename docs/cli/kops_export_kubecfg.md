
<!--- This file is automatically generated by make gen-cli-docs; changes should be made in the go CLI command code (under cmd/kops) -->

## kops export kubecfg

Export kubecfg.

### Synopsis

Export a kubecfg file for a cluster from the state store. By default the configuration will be saved into a users $HOME/.kube/config file. Kops will respect the KUBECONFIG environment variable if the --kubeconfig flag is not set.

```
kops export kubecfg CLUSTERNAME [flags]
```

### Examples

```
  # export a kubeconfig file with the cluster admin user (make sure you keep this user safe!)
  kops export kubecfg k8s-cluster.example.com --admin
  
  # export using a user already existing in the kubeconfig file
  kops export kubecfg k8s-cluster.example.com --user my-oidc-user
  
  # export using the internal DNS name, bypassing the cloud load balancer
  kops export kubecfg k8s-cluster.example.com --internal
```

### Options

```
      --admin duration[=18h0m0s]   export a cluster admin user credential with the given lifetime and add it to the cluster context
      --all                        export all clusters from the kOps state store
      --auth-plugin                use the kOps authentication plugin
  -h, --help                       help for kubecfg
      --internal                   use the cluster's internal DNS name
      --kubeconfig string          the location of the kubeconfig file to create.
      --user string                add an existing user to the cluster context
```

### Options inherited from parent commands

```
      --add_dir_header                   If true, adds the file directory to the header of the log messages
      --alsologtostderr                  log to standard error as well as files
      --config string                    yaml config file (default is $HOME/.kops.yaml)
      --log_backtrace_at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log_dir string                   If non-empty, write log files in this directory
      --log_file string                  If non-empty, use this log file
      --log_file_max_size uint           Defines the maximum size a log file can grow to. Unit is megabytes. If the value is 0, the maximum file size is unlimited. (default 1800)
      --logtostderr                      log to standard error instead of files (default true)
      --name string                      Name of cluster. Overrides KOPS_CLUSTER_NAME environment variable
      --one_output                       If true, only write logs to their native severity level (vs also writing to each lower severity level)
      --skip_headers                     If true, avoid header prefixes in the log messages
      --skip_log_headers                 If true, avoid headers when opening log files
      --state string                     Location of state storage (kops 'config' file). Overrides KOPS_STATE_STORE environment variable
      --stderrthreshold severity         logs at or above this threshold go to stderr (default 2)
  -v, --v Level                          number for the log level verbosity
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO

* [kops export](kops_export.md)	 - Export configuration.

