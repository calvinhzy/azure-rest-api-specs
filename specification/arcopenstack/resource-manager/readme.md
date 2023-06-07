# arcopenstack

> see https://aka.ms/autorest

This is the AutoRest configuration file for openstack.

## Getting Started

To build the SDKs for My API, simply install AutoRest via `npm` (`npm install -g autorest`) and then run:

> `autorest readme.md`

To see additional help and options, run:

> `autorest --help`

For other options on installation see [Installing AutoRest](https://aka.ms/autorest/install) on the AutoRest github page.

---

## Configuration

### Basic Information

These are the global settings for the openstack.

```yaml
openapi-type: arm
openapi-subtype: rpaas
tag: package-2022-08-31-privatepreview
```

### Tag: package-2021-05-31-privatepreview

These settings apply only when `--tag=package-2021-05-31-privatepreview` is specified on the command line.

```yaml $(tag) == 'package-2021-05-31-privatepreview'
input-file:
  - Microsoft.ConnectedOpenStack/preview/2021-05-31-privatepreview/arcopenstack.json
```
### Tag: package-2022-08-31-privatepreview

These settings apply only when `--tag=package-2022-08-31-privatepreview` is specified on the command line.

```yaml $(tag) == 'package-2022-08-31-privatepreview'
input-file:
  - Microsoft.ConnectedOpenStack/preview/2022-08-31-privatepreview/arcopenstack.json
```
---

# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

```yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-go-track2
  - repo: azure-sdk-for-java
  - repo: azure-sdk-for-js
  - repo: azure-sdk-for-ruby
    after_scripts:
      - bundle install && rake arm:regen_all_profiles['azure_mgmt_openstack']
```

## Go

See configuration in [readme.go.md](./readme.go.md)

## Python

See configuration in [readme.python.md](./readme.python.md)

## Ruby

See configuration in [readme.ruby.md](./readme.ruby.md)

## TypeScript

See configuration in [readme.typescript.md](./readme.typescript.md)

## CSharp

See configuration in [readme.csharp.md](./readme.csharp.md)