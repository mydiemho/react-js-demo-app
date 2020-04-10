# Overview

Sample react app to demonstrate setting up [cypress](https://www.cypress.io/) on [Azure DevOps](https://azure.microsoft.com/en-us/services/devops/).

The pipelines are written in yaml and leverage [templating](https://docs.microsoft.com/en-us/azure/devops/pipelines/yaml-schema?view=azure-devops&tabs=example%2Cparameter-schema#template-references)

## Pipelines

The 2 running pipelines are for linting markdown files and running tests.

### Markdown linting

The pipeline is defined [here](devops/pipelines/pr-validation-markdown-linting.yaml)

[![Build Status](https://dev.azure.com/mydiemho/demos/_apis/build/status/pr-validation-web-app?branchName=master)](https://dev.azure.com/mydiemho/demos/_build/latest?definitionId=3&branchName=master)

### Testing & JS Linting

The pipeline is defined [here](devops/pipelines/pr-validation-web-app.yaml)

[![Build Status](https://dev.azure.com/mydiemho/demos/_apis/build/status/pr-validation-web-app?branchName=master)](https://dev.azure.com/mydiemho/demos/_build/latest?definitionId=3&branchName=master)

### Deploy

The [deploy pipeline](devops/pipelines/deploy-web-app.yaml) is left for user to set up on their own as it requires Azure resources.
