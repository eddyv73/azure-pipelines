# Azure pipeline for simple solution with docker and docker compose.

Azure DevOps : [![Build Status](https://dev.azure.com/wistercorp/azure-pipelines/_apis/build/status/BaseDocker?branchName=develop)](https://dev.azure.com/wistercorp/azure-pipelines/_build/latest?definitionId=48&branchName=develop)

This example Contains a docker-compose file. The pipeline build the docker image and push it to the registry.
To make a push to the Docker Hub it's necessary create a `Service Connection`

<img width="200" alt="image" src="https://user-images.githubusercontent.com/19657324/178547294-6dd02dd5-4547-4fd5-8bcb-e07b4d8e0972.png">


Docker Hub [Repo](https://hub.docker.com/repository/docker/wister/azure-pipelines)

# Base
Steps

 - Restore
 - Build
 - Test
 - Publish
 - DockerBuild
 - DockerPush

Structure

```yml
stages:
    - stage: Build and Restore
        - job: restore
        - job: build
    - stage: Test
        - job: test
    - stage: Publish
        - job: publish
        - job: upload
    - stage: DockerBuild
        - job: dockerbuild
        - job: DockerPush
```
<img width="275" alt="image" src="https://user-images.githubusercontent.com/19657324/178546952-f7a0ed82-1e22-4717-9497-dc23e65d5620.png">


