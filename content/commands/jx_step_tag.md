---
date: 2019-01-11T09:28:59Z
title: "jx step tag"
slug: jx_step_tag
url: /commands/jx_step_tag/
---
## jx step tag

Creates a git tag and pushes to remote repo

### Synopsis

This pipeline step command creates a git tag using a version number prefixed with 'v' and pushes it to a remote origin repo. 

This commands effectively runs: 

git commit -a -m "release $(VERSION)" --allow-empty git tag -fa v$(VERSION) -m "Release version $(VERSION)" git push origin v$(VERSION)

```
jx step tag [flags]
```

### Examples

```
  jx step tag --version 1.0.0
```

### Options

```
  -d, --charts-dir string                the directory of the chart to update the version
  -r, --charts-value-repository string   the fully qualified image name without the version tag. e.g. 'dockerregistry/myorg/myapp'
  -h, --help                             help for tag
  -v, --version string                   version number for the tag [required]
      --version-file string              The file name used to load the version number from if no '--version' option is specified (default "VERSION")
```

### SEE ALSO

* [jx step](/commands/jx_step/)	 - pipeline steps

###### Auto generated by spf13/cobra on 11-Jan-2019