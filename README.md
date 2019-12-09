# What is this?

GitLab CI plugin to build Java projects.

### Usage

1. Include this plugin into your `.gitlab-ci.yml` file

```YAML
include:
  - project: iog/gitlab/gitlab-ci-plugins/java
    file: plugin.yml
    ref: master
```

or

```YAML
include: 'https://gitlab.ins.risk.regn.net/iog/gitlab/gitlab-ci-plugins/java/raw/master/plugin.yml'
```

2. Extend the `.plugin-java` job to define the environment variables for the Java build step.

```YAML
build_my_project:
  extends: .plugin-java
```


### Environment variables

The following environment variables are supported:

| Name | Description | Required | Default |
| ---- | ----------- | -------- | ------- |
| `ROOT_DIR` | The directory that contains the Maven or Gradle project file to build. | Optional | `$CI_PROJECT_DIR` |
