## Lab Tools for APIs
After the initial data upload to blob storage, we will use Postman for [REST API calls](https://docs.microsoft.com/en-us/azure/search/search-fiddler). You can use any other REST API tool that can formulate and send HTTP requests, but we suggest you to use Postman since the training was created with/for it. The image below shows a visual example of Postman being used for Cognitive Search.

![](./media/postman.PNG)

> Important details about Postman:
> + You can save your commands, which is useful for reuse, not only within this workshop, but also in your future projects.
> + You need to create a free account. A confirmation message is emailed to you.
> + You can export all your commands into json format. This file can then be saved into the storage account of the lab, into a cloud storage like OneDrive, or anywhere you like. This process helps you save, share, and reuse your work.
> + These return codes indicate success after an API call request: 200, 201 and 204. 
> + Error messages and warnings are very clear.
> + Besides the API URL and call type, we will use GET/PUT/POST (depending on what action we are taking), and you need to use the header for Content-Type and api-key. The json commands must be placed into the "body / raw" area. If you are struggling using Postman, here's a friendly reminder to [review the resource from the prerequisites](https://docs.microsoft.com/en-us/azure/search/search-fiddler).
