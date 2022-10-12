## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: bing
  clear-output-folder: true
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2020-06-10
  - tag: package-2020-06-10-preview
```

### Tag: package-2020-06-10 and go

These settings apply only when `--tag=package-2020-06-10 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2020-06-10' && $(go)
output-folder: $(go-sdk-folder)/services/$(namespace)/mgmt/2020-06-10/$(namespace)
```

### Tag: package-2020-06-10-preview and go

These settings apply only when `--tag=package-2020-06-10-preview --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2020-06-10-preview' && $(go)
output-folder: $(go-sdk-folder)/services/preview/$(namespace)/mgmt/2020-06-10-preview/$(namespace)
```