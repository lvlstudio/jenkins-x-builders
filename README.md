# jenkins-x-builders

a monorepo containing builders for jenkins-x modified by lvlstudio.

Usage:
```
./lvl-docker-build.sh BUILDER_BASE_VERSION BUILDERS_VERSION
```

Select the BUILDER_BASE_VERSION from a recent tag of the JX builder base image
https://gcr.io/jenkinsxio/builder-base

Select the BUILDERS_VERSION from a recent tag of one of the released JX builder image (e.g. builder-go)
https://gcr.io/jenkinsxio/builder-go
