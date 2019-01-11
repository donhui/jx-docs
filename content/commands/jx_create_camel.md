---
date: 2019-01-11T09:28:59Z
title: "jx create camel"
slug: jx_create_camel
url: /commands/jx_create_camel/
---
## jx create camel

Create a new Camel based application and import the generated code into Git and Jenkins for CI/CD

### Synopsis

Creates a new Apache Camel application using Spring Boot and then optionally sets up CI/CD pipelines and GitOps promotion. 

For more documentation about Camel see: https://camel.apache.org/

```
jx create camel [flags]
```

### Examples

```
  # Create a Camel application and be prompted for the folder name
  jx create camel
  
  # Create a Camel application called awesome
  jx create camel -a awesome
```

### Options

```
  -a, --artifact string                The artifact ID for the new application
  -b, --batch-mode                     In batch mode the command never prompts for user input
      --branches string                The branch pattern for branches to trigger CI/CD pipelines on
  -c, --camel-version string           The Version of the Archetype to use (default "RELEASE")
      --credentials string             The Jenkins credentials name used by the job
      --docker-registry-org string     The name of the docker registry organisation to use. If not specified then the Git provider organisation will be used
      --dry-run                        Performs local changes to the repo but skips the import into Jenkins X
      --external-jenkins-url string    The jenkins url that an external git provider needs to use
      --git-api-token string           The Git API token to use for creating new Git repositories
      --git-private                    Create new Git repositories as private
      --git-provider-kind string       Kind of Git server. If not specified, kind of server will be autodetected from Git provider URL. Possible values: bitbucketcloud, bitbucketserver, gitea, gitlab, github, fakegit
      --git-provider-url string        The Git server URL to create new Git repositories inside (default "https://github.com")
      --git-username string            The Git username to use for creating new Git repositories
  -g, --group string                   The group ID for the new application (default "com.example")
      --headless                       Enable headless operation if using browser automation
  -h, --help                           help for camel
      --import-commit-message string   Should we override the Jenkinsfile in the project?
      --install-dependencies           Should any required dependencies be installed automatically
  -i, --interactive                    Allow interactive input into the maven archetype:generate command
      --jenkinsfile string             The name of the Jenkinsfile to use. If not specified then 'Jenkinsfile' will be used
      --list-packs                     list available draft packs
      --log-level string               Logging level. Possible values - panic, fatal, error, warning, info, debug. (default "info")
      --name string                    Specify the Git repository name to import the project into (if it is not already in one)
      --no-brew                        Disables the use of brew on macOS to install or upgrade command line dependencies
      --no-draft                       Disable Draft from trying to default a Dockerfile and Helm Chart
      --no-import                      Disable import after the creation
      --no-jenkinsfile                 Disable defaulting a Jenkinsfile if its missing
      --org string                     Specify the Git provider organisation to import the project into (if it is not already in one)
  -o, --output-dir string              Directory to output the project to. Defaults to the current directory
      --pack string                    The name of the pack to use
      --pull-secrets string            The pull secrets the service account created should have (useful when deploying to your own private registry): provide multiple pull secrets by providing them in a singular block of quotes e.g. --pull-secrets "foo, bar, baz"
      --skip-auth-secrets-merge        Skips merging a local git auth yaml file with any pipeline secrets that are found
      --verbose                        Enable verbose logging
  -v, --version string                 The version for the new application (default "1.0-SNAPSHOT")
```

### SEE ALSO

* [jx create](/commands/jx_create/)	 - Create a new resource

###### Auto generated by spf13/cobra on 11-Jan-2019