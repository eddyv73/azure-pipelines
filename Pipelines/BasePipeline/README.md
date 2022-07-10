Azure pipeline for simple solution.

Azure DevOps : [![Build Status](https://dev.azure.com/wistercorp/azure-pipelines/_apis/build/status/BasePipeline?branchName=develop)](https://dev.azure.com/wistercorp/azure-pipelines/_build/latest?definitionId=45&branchName=develop)

This example works for a simple solution with one project.

# Base
Steps

 - Restore
 - Build
 - Test
 - Publish

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
```
<img width="275" alt="image" src="https://user-images.githubusercontent.com/19657324/178130746-d715d143-de59-48a1-a183-2f8c2c162c42.png">


