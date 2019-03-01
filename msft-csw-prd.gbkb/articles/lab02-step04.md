### Step 4 - Cleaning the environment
We need to prepare the environment to add the image analysis we will create. The most practical approach is to delete the objects from Azure Search and rebuild them. With the exception of the data source, we will delete everything else. Resource names are unique, so by deleting an object, you can recreate it using the same name. 

#### Step 4.1
 Save all scripts (API calls) you did until here, including the definition json files you used in the "body" field. Let's start deleting the index and the indexer. You can use Azure Portal or API calls:
1. [Deleting the indexer](https://docs.microsoft.com/en-us/rest/api/searchservice/delete-indexer) - Just use your service, key and indexer name
2. [Deleting the index](https://docs.microsoft.com/en-us/rest/api/searchservice/delete-index) - Just use your service, key and indexer name

#### Step 4.2
Skillsets can only be deleted through an HTTP command, let's use another API call request to delete it. If you used another skillset name, just change it in the URL.

```http
DELETE https://[servicename].search.windows.net/skillsets/demoskillset?api-version=2017-11-11-Preview
api-key: [api-key]
Content-Type: application/json
```
Status code 204 is returned on successful deletion.
