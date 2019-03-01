### Step 1 - Checking part of the problem
Let's check the indexer status again, it has valuable information about our "images problem". You can use the same command we used in the previous lab (pasted below for convenience). If you used another indexer name, just change it in the URL.

```http
GET https://[servicename].search.windows.net/indexers/demoindexer/status?api-version=2017-11-11-Preview
api-key: [api-key]
Content-Type: application/json
```
If you check the response messages for any of the png or jpg files, there will be warnings and not data.  

