# EnterpriseKnowledgeGraphService

> see https://aka.ms/autorest

This is the AutoRest configuration file for EnterpriseKnowledgeGraphService.



---

### Java multi-api

``` yaml $(java) && $(multiapi)
batch:
  - tag: package-2018-12-03
```

### Tag: package-2018-12-03 and java

These settings apply only when `--tag=package-2018-12-03 --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-2018-12-03' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.EnterpriseKnowledgeGraphService.v2018-12-03
  output-folder: $(azure-libraries-for-java-folder)/sdk/EnterpriseKnowledgeGraphService/mgmt-v2018-12-03
regenerate-manager: true
generate-interface: true
```


## Getting Started
To build the SDK for EnterpriseKnowledgeGraphService, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information
These are the global settings for the EnterpriseKnowledgeGraphService API.

``` yaml
openapi-type: arm
tag: package-2018-12-03
```

### Tag: package-2018-12-03

These settings apply only when `--tag=package-2018-12-03` is specified on the command line.

``` yaml $(tag) == 'package-2018-12-03'
input-file:
- Microsoft.EnterpriseKnowledgeGraph/preview/2018-12-03/EnterpriseKnowledgeGraphSwagger.json
directive:
  - None at the moment
```

---
# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-net
  - repo: azure-sdk-for-python
  - repo: azure-sdk-for-go
  - repo: azure-resource-manager-schemas
  - repo: azure-powershell
```

## C#

These settings apply only when `--csharp` is specified on the command line.
Please also specify `--csharp-sdks-folder=<path to "SDKs" directory of your azure-sdk-for-net clone>`.

``` yaml $(csharp)
csharp:
  azure-arm: true
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: Microsoft.Azure.Management.EnterpriseKnowledgeGraphService
  output-folder: $(csharp-sdks-folder)/enterpriseknowledgegraphservice/Microsoft.Azure.Management.EnterpriseKnowledgeGraphService/src/Generated
  clear-output-folder: true
```


