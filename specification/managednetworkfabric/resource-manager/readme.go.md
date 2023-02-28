## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go) && !$(track2)
go:
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: managednetworkfabric
  clear-output-folder: true
```

```yaml $(go) && $(track2)
azure-arm: true
license-header: MICROSOFT_MIT_NO_VERSION
module-name: sdk/resourcemanager/managednetworkfabric/armmanagednetworkfabric
module: github.com/Azure/azure-sdk-for-go/$(module-name)
output-folder: $(go-sdk-folder)/$(module-name)
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2023-02-01-preview
```
### Tag: package-2022-01-15-privatepreview and go
These settings apply only when `--tag=package-2022-01-15-privatepreview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.
``` yaml $(tag) == 'package-2022-01-15-privatepreview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/$(namespace)/mgmt/2022-01-15-privatepreview/$(namespace)
```
### Tag: package-2023-02-01-preview and go
These settings apply only when `--tag=package-2023-02-01-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.
``` yaml $(tag) == 'package-2023-02-01-preview ' && $(go)
output-folder: $(go-sdk-folder)/services/preview/$(namespace)/mgmt/2023-02-01-preview/$(namespace)
```