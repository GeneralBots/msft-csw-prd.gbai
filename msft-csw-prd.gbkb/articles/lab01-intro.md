# Lab 1: Create a Cognitive Search Enrichment Process with **Text** Skills

Cognitive skills are natural language processing (NLP) and image analysis operations that extract text and text representations of an image, detect language, entities, key phrases, and more. The end result is rich additional content in an Azure Search index, created by a cognitive search indexing pipeline. 

**All the links in this lab are extra content for your learning, but you don't need them to perform the required activities.**

In this lab, we will learn how to create a Cognitive Search indexing pipeline that enriches source data in route to an index. The output is a full text searchable index on Azure Search. 


The list of activities we will do, using Azure Search REST APIs, is:

+ Create a data source for the uploaded data.
+ Create a Cognitive Search Skillset with entity recognition, language detection, text manipulation and key phrase extraction.
+ Create an index to store the enriched metadata.
+ Create an indexer process to execute the enrichment.
+ Check the indexer status
+ Check the enriched metadata
+ Query the metadata


>TIP for Later: You can enhance the index with other Azure Search standard capabilities, such as [synonyms](https://docs.microsoft.com/en-us/azure/search/search-synonyms), [scoring profiles](https://docs.microsoft.com/rest/api/searchservice/add-scoring-profiles-to-a-search-index), [analyzers](https://docs.microsoft.com/en-us/rest/api/searchservice/custom-analyzers-in-azure-search), and [filters](https://docs.microsoft.com/en-us/azure/search/search-filters).
