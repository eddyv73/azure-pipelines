# Azure pipelines templates
Azure Pipelines for multiples escenarios

In this repository, you can found multiples escenarios for Azure Pipelines and some "Good" practices.

##### Considerations
All examples has the same code with minimum differences, this repository has the focus on the azure pipelines.

The solutions in the examples is named : Event Horizont, has two dotnet projects, and a two test projects. `Net 6`

The APIs in the examples are named : Voyager and Galileo.
(Like a spacecrafts)


All Azure DevOps Pipelines [Azure DevOps](https://dev.azure.com/wistercorp/azure-pipelines/_build)

# Base
Scenario :
- 1 Project Api
- 1 Project Test

Tech:
- Dotnet 6

Location: 
```
└ Pipelines /
    └ Basepipeline /
```
##### Azure DevOps Pipeline : [![Build Status](https://dev.azure.com/wistercorp/azure-pipelines/_apis/build/status/BasePipeline?branchName=develop)](https://dev.azure.com/wistercorp/azure-pipelines/_build/latest?definitionId=45&branchName=develop)
# Base multiples projects
Scenario :
- 2 Project Api
- 2 Project Test

Tech:
- Dotnet 6

Location: 
```
└ Pipelines /
    └ BaseMultiplesProjects /
``` 
##### Azure DevOps Pipeline  V1 :  [![Build Status](https://dev.azure.com/wistercorp/azure-pipelines/_apis/build/status/BasePipelineMultiplePro?branchName=develop)](https://dev.azure.com/wistercorp/azure-pipelines/_build/latest?definitionId=46&branchName=develop)
Pipeline Basic Configuration

Location: 
```
└ Pipelines /
    └ BaseMultplesprojectsv2 /
```

##### Azure DevOps Pipeline  V2 : [![Build Status](https://dev.azure.com/wistercorp/azure-pipelines/_apis/build/status/BasePipelineMultipleProV2?branchName=develop)](https://dev.azure.com/wistercorp/azure-pipelines/_build/latest?definitionId=47&branchName=develop)
Pipeline Avanced Configuration

# Base docker using docker-compose
Scenario :
- 2 Project Api
- 2 Project Test
  
Tech:
- Dotnet 6
- Docker
- Docker-compose

##### Azure DevOps Pipeline : [![Build Status](https://dev.azure.com/wistercorp/azure-pipelines/_apis/build/status/BaseDocker?branchName=develop)](https://dev.azure.com/wistercorp/azure-pipelines/_build/latest?definitionId=48&branchName=develop)
Location: 
```
└ Pipelines /
    └ BaseDocker /
```
# Avanced build with docker using docker-compose
`Coming soon`
# Avanced build and deployment in Azure Kubernetes Service (AKS)
`Coming soon`