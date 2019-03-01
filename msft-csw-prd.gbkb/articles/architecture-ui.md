## Information Delivery - User Interface
Building an interface is not in the scope of this one day training, but we will address the topic by listing the possible options for a Cognitive Search solution.

The enriched metadata created by the Cognitive Search Pipeline is always loaded to an Azure Search Index. **How the final users would benefit from that?** 

+ Web and Mobile applications can search this index using the [Azure Search .net SDK](https://docs.microsoft.com/en-us/azure/search/search-query-dotnet) 
or the [Azure Search Rest API](https://docs.microsoft.com/en-us/azure/search/search-query-rest-api). This applications will translate user's search parameters into an Azure Search Query, what will retrieve the metadata from the Azure Search Index. 
One of the stored information is the file location, allowing users to visualize, download and open the documents.

+ Another option is a [Search Bot](https://docs.microsoft.com/en-us/azure/bot-service/dotnet/bot-builder-dotnet-search-azure?view=azure-bot-service-3.0), a CaaP (Conversation as a Platform) interface for interactive search using NLP (Natural Language Processing).
**In the image below you can see one example of architecture you can build using Cognitive Search, LUIS and a Bot as user interface**.

![](./media/just-a-bots-sample-architecture.png)


> The Microsoft Learn AI Team has a 2 day [Bootcamp Training](https://azure.github.io/LearnAI-Bootcamp/emergingaidev_bootcamp) that shows you how to create an intelligent bot with Azure Search and Cognitive Services.
