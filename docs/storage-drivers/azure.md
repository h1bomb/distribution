<!--GITHUB
page_title: Microsoft Azure storage driver
page_description: Explains how to use the Azure storage drivers
page_keywords: registry, service, driver, images, storage, azure
IGNORES-->

# Microsoft Azure storage driver

An implementation of the `storagedriver.StorageDriver` interface which uses [Microsoft Azure Blob Storage][azure-blob-storage] for object storage.

## Parameters

The following parameters must be used to authenticate and configure the storage driver (case-sensitive):

* `accountname`: Name of the Azure Storage Account.
* `accountkey`: Primary or Secondary Key for the Storage Account.
* `container`: Name of the root storage container in which all registry data will be stored. Must comply the storage container name [requirements][create-container-api].
* `realm`: (optional) Domain name suffix for the Storage Service API endpoint. Defaults to `core.windows.net`. For example realm for "Azure in China" would be `core.chinacloudapi.cn` and realm for "Azure Government" would be `core.usgovcloudapi.net`.

## Developing

To include this driver when building Docker Distribution, use the build tag
`include_azure`. Please see the [building documentation][building] for details.

[azure-blob-storage]: http://azure.microsoft.com/en-us/services/storage/
[create-container-api]: https://msdn.microsoft.com/en-us/library/azure/dd179468.aspx
[building]: https://github.com/docker/distribution/blob/master/docs/building.md#optional-build-tags
