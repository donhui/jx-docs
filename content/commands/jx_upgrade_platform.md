---
date: 2018-12-19T11:24:39Z
title: "jx upgrade platform"
slug: jx_upgrade_platform
url: /commands/jx_upgrade_platform/
---
## jx upgrade platform

Upgrades the Jenkins X platform if there is a new release available

### Synopsis

Upgrades the Jenkins X platform if there is a newer release

```
jx upgrade platform [flags]
```

### Examples

```
  # Upgrades the Jenkins X platform
  jx upgrade platform
```

### Options

```
      --always-upgrade                  If set to true, jx will upgrade platform Helm chart even if requested version is already installed.
  -b, --batch-mode                      In batch mode the command never prompts for user input
  -c, --chart string                    The Chart to upgrade (default "jenkins-x/jenkins-x-platform")
      --cleanup-temp-files              Cleans up any temporary values.yaml used by helm install [default true] (default true)
      --cloud-environment-repo string   Cloud Environments Git repo (default "https://github.com/jenkins-x/cloud-environments")
      --headless                        Enable headless operation if using browser automation
  -h, --help                            help for platform
      --install-dependencies            Should any required dependencies be installed automatically
      --local-cloud-environment         Ignores default cloud-environment-repo and uses current directory 
      --log-level string                Logging level. Possible values - panic, fatal, error, warning, info, debug. (default "info")
  -n, --name string                     The release name (default "jenkins-x")
      --namespace string                The Namespace to promote to
      --no-brew                         Disables the use of brew on macOS to install or upgrade command line dependencies
      --pull-secrets string             The pull secrets the service account created should have (useful when deploying to your own private registry): provide multiple pull secrets by providing them in a singular block of quotes e.g. --pull-secrets "foo, bar, baz"
  -s, --set string                      The helm parameters to pass in while upgrading
      --skip-auth-secrets-merge         Skips merging a local git auth yaml file with any pipeline secrets that are found
      --verbose                         Enable verbose logging
  -v, --version string                  The specific platform version to upgrade to
```

### SEE ALSO

* [jx upgrade](/commands/jx_upgrade/)	 - Upgrades a resource

###### Auto generated by spf13/cobra on 19-Dec-2018