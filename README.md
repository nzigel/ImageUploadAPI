# ImageUploadAPI
Azure API App example for uploading photos from the Camera control in PowerApps to an Azure Blob storage account.

Updated to write metadata object to Document DB and create queue object to be triggered by azure function in https://github.com/nzigel/FunctionAppImageProcess project

Create a PrivateSettings.config file and store your keys as follows:

``` javascript
<appSettings>
<!-- Connection String for Azure Blob Storage -->
<add key="StorageConnectionString" value="DefaultEndpointsProtocol=[your storage endpoint]https;AccountName=[Your storage account name];AccountKey=[your storage key];EndpointSuffix=core.windows.net" />
<add key="documentDbName" value="db" />
<add key="documentDbCol" value="imageCollection" />
<add key="documentDbEndpoint" value="https://[your doc db name].documents.azure.com:443/" />
<add key="documentDbKey" value="" />
<add key="containerName" value="images" />
<add key="queueName" value="inputqueue" />      
</appSettings>
```
