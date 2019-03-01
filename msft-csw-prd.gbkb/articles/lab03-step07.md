## Step 7 - Connect to your Pipeline, recreating the environment
Now let's use the [official documentation](https://docs.microsoft.com/en-us/azure/search/cognitive-search-custom-skill-interface) to learn the syntax we need to add the custom skill to our enrichment pipeline. 

As you can see, the custom skill works like all other predefined skills, but the type is **WebApiSkill** and you need to specify the URL you created above. The example below shows you how to call the skill. Because the skill doesn't handle batches, you have to add an instruction for maximum batch size to be just ```1``` to send documents one at a time. 
Like we did in Lab 2, we suggest you add this new skill at the end of the body definition of the skillset.

```json
      {
        "@odata.type": "#Microsoft.Skills.Custom.WebApiSkill",
        "description": "Our new translator custom skill",
        "uri": "https://[enter function name here].azurewebsites.net/api/Translate?code=[enter default host key here]",
        "batchSize":1,
        "context": "/document",
        "inputs": [
          {
            "name": "text",
            "source": "/document/content"
          },
          {
            "name": "language",
            "source": "/document/languageCode"
          }
        ],
        "outputs": [
          {
            "name": "text",
            "targetName": "translatedText"
          }
        ]
      }

```

### Step 7.1 - Challenge!!
As you can see, again we are not giving you the body request. One more time you need to use Lab 1 as a reference. We can't use lab 2 definition because we've hit the maximum number of skills allowed within a skillset of a basic account (five). So, let's use Lab 1 json requests again.
Skipping the services and the data source creation, repeat the other steps of the Lab 1, in the same order. 
1. ~~Create the services at the portal~~ **Not required, we did not delete it**.
2. ~~Create the Data Source~~ **Not required, we did not delete it**.
3. Recreate the Skillset
4. Recreate the Index
5. Recreate the Indexer
6. Check Indexer Status - Check the translation results.  
7. Check the Index Fields - Check the translated text new field.
8. Check the data - If you don't see the translated data, something went wrong.
