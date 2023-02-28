## Go

These settings apply only when `--go` is specified on the command line.

```yaml $(go) && $(track2)
azure-arm: true
license-header: MICROSOFT_MIT_NO_VERSION
module-name: sdk/resourcemanager/metaverse/armmetaverse
module: github.com/Azure/azure-sdk-for-go/$(module-name)
output-folder: $(go-sdk-folder)/$(module-name)

directive:
- rename-model:
    from: 'MetaverseResource'
    to: 'ResourceInfo'
- rename-model:
    from: 'MetaverseResourceList'
    to: 'ResourceInfoList'
```