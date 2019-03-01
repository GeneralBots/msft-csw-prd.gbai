## Step 1 - Create a data source

Now that your services and source files are prepared, start assembling the components of your indexing pipeline. We'll begin by creating a [data source object](https://docs.microsoft.com/rest/api/searchservice/create-data-source) that tells Azure Search how to retrieve external source data.

For this tutorial, we will use Postman to call Azure Search service APIs. In the request header, provide the service name you used while creating the Azure Search service, and the api-key generated for your search service. In the request body, specify the blob container name and connection string.

### Sample Request
```http
POST https://[service name].search.windows.net/datasources?api-version=2017-11-11-Preview  
api-key: [admin key]  
Content-Type: application/json
```
#### Request Body Syntax
```json
{   
    "name" : "demodata",  
    "description" : "Demo files to demonstrate cognitive search capabilities.",  
    "type" : "azureblob",
    "credentials" :
    { "connectionString" :
      "DefaultEndpointsProtocol=https;AccountName=<your account name>;AccountKey=<your account key>;"
    },  
    "container" : { "name" : "<your blob container name>" }
}  
```
Send the request. The web test tool should return a status code of 201 confirming success. 

Since this is your first request, check the Azure portal to confirm the data source was created in Azure Search. On the search service dashboard page, verify the Data Sources tile has a new item. You might need to wait a few minutes for the portal page to refresh. 

  ![Data sources tile in the portal](./media/data-source.PNG "Data sources tile in the portal")

If you got a 403 or 404 error, check the request construction: `api-version=2017-11-11-Preview` should be on the endpoint, `api-key` should be in the Header after `Content-Type`, and its value must be valid for a search service. You can reuse the header for the remaining steps in this lab.

> [!TIP]
> Now, before you do any more work and you're in the portal anyway, is a good time to verify that the search service is running in one of the supported locations providing the preview feature: South Central US or West Europe.

