# Azure pipeline for multiples projects.

Azure DevOps : [![Build Status](https://dev.azure.com/wistercorp/azure-pipelines/_apis/build/status/BasePipelineMultiplePro?branchName=develop)](https://dev.azure.com/wistercorp/azure-pipelines/_build/latest?definitionId=46&branchName=develop)

This example works for a single solution with multiples projects.

## Cons
This design is slow, because verify project by project.
## Pros
This design is nice to identify errors in the build, because you can see the Build and Restore every project.
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
    - stage: Build and Restore Single per project # Conditional stage, only run if the stage 'Build and Restore' fails
        - job: restore single project # Conditional job restore project by project
        - job: build single project # Conditional job build project by project
    - stage: Test
        - job: test
    - stage: Publish
        - job: publish
        - job: upload
```

## Correct flow

<img width="502" alt="image" src="https://user-images.githubusercontent.com/19657324/178131885-4c89085b-bc13-49b0-a7da-65863d247585.png">

## Incorrect flow
If some project has errors in the build, the pipeline build every project.

<img width="502" alt="image" src="https://user-images.githubusercontent.com/19657324/178131885-4c89085b-bc13-49b0-a7da-65863d247585.png">