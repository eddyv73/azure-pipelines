Azure pipeline for simple solution.

Azure DevOps : [![Build Status](https://dev.azure.com/wistercorp/azure-pipelines/_apis/build/status/BasePipelineMultiplePro?branchName=develop)](https://dev.azure.com/wistercorp/azure-pipelines/_build/latest?definitionId=46&branchName=develop)

This example works for a single solution with multiples projects.

## Cons
Considerations: This design is slow, because verify project by project.
## Pros
Considerations: This design is nice to identify errors in the build, because you can see Build and Restore every project.
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


