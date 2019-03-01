## Step 2 - Create the Azure Blob service and upload the data

The enrichment pipeline pulls from Azure data sources. Source data must originate from a supported data source type of an [Azure Search indexer](https://docs.microsoft.com/en-us/azure/search/search-indexer-overview). For this exercise, we use blob storage to showcase multiple content types.

1. [Download the sample data](https://1drv.ms/f/s!AsUn_SC4PosUkqZqDqS24ubRlk3eXw). The sample data consists of a small file set of different types. 

1. Sign up for Azure Blob storage, create a storage account, log in to Storage Explorer, and create a container named `basicdemo`. If you haven't done this before, you can refer to the [Azure Storage Explorer Quickstart](https://azure.microsoft.com/en-us/features/storage-explorer) for instructions on all the steps.

1. Using Azure Storage Explorer, in the `basicdemo` container you created, click **Upload** to upload the sample files. You can also upload the data from the [Azure Portal](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-portal). 

1. After sample files are loaded, get the container name and a connection string for your Blob storage. You could do that by navigating to your storage account in the Azure portal. On **Access keys**, and then copy the **Connection String**  field. We recommend storing the container name and connection string with your Azure Search URL and api-key from Step 1.

  The connection string should be a URL similar to the following hypothetical example:

  ```http
  DefaultEndpointsProtocol=https;AccountName=cogsrchdemostorage;AccountKey=<your key here>==;EndpointSuffix=core.windows.net
  ```

There are other ways to specify the connection string, such as providing a shared access signature. We won't be covering that in this workshop, but to learn more about data source credentials, see [Indexing Azure Blob Storage](https://docs.microsoft.com/en-us/azure/search/search-howto-indexing-azure-blob-storage).

