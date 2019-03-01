## Step 6 - Cleaning the environment again
Let's do the same cleaning process of lab 2. Save all scripts (API calls) you did until here, including the definition json files you used in the "body" field. 

### Step 6.1
Let's start deleting the index and the indexer. You can use Azure Portal or API calls:
1. [Deleting the indexer](https://docs.microsoft.com/en-us/rest/api/searchservice/delete-indexer) - Just use your service, key and indexer name
2. [Deleting the index](https://docs.microsoft.com/en-us/rest/api/searchservice/delete-index) - Just use your service, key and indexer name

### Step 6.2
Skillsets can only be deleted through an HTTP command, let's use another API call request to delete it. Don't forget to add your skillset name in the URL.

```http
DELETE https://[servicename].search.windows.net/skillsets/demoskillset?api-version=2017-11-11-Preview
api-key: [api-key]
Content-Type: application/json
```
Status code 204 is returned on successful deletion.

