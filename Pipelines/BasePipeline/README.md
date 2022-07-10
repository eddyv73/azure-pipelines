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
```


