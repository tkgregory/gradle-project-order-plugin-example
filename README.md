A standalone example for the [Gradle Project Order Plugin](https://plugins.gradle.org/plugin/com.tomgregory.project-order).

The Gradle Project Order Plugin controls the execution order of the *deploy* task between these 3 projects:

1. 1-networking-resources
1. 2-security-resources
1. 3-compute-resources

This is done by prefixing the project name with a number. 

The result of `./gradlew deploy` is therefore:

```
> Task :1-networking-resources:deploy
Deploying from 1-networking-resources

> Task :2-security-resources:deploy
Deploying from 2-security-resources

> Task :3-compute-resources:deploy
Deploying from 3-compute-resources
```

See the [GitHub project](https://github.com/tkgregory/gradle-project-order-plugin) for documentation and more details.