# buildpack-repo
Buildpack repository example that can be deployed to Cloud Foundry as a staticfile app

## Getting Started

### Add your repo files
Place your repository files under `src/configured-item`. This project comes with [Tomcat configuration files](https://github.com/cloudfoundry/java-buildpack/blob/master/docs/container-tomcat.md#external-tomcat-configuration) as an example. 

### Build the repo
Use maven to build the repo, specifying the route to be used in [index.yml](https://github.com/cloudfoundry/java-buildpack/blob/master/docs/extending-repositories.md)

```
mvn clean install -Droute=myroute.cfapps.io
```

### Deploy the repo to Cloud Foundry

```
cf push
```