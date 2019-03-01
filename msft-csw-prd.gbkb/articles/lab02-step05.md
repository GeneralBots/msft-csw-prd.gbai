### Step 5 - Recreating the environment - Challenge!!
Now it is your time to guide the work. We are using a basic Azure Search service, so we can create skillsets with up to 5 skills. Since we currently are using 4, from the previous lab, we can add one more for image processing.

#### Step 5.1
Use the same skillset definition from Lab 1, but add in the [OCR image analysis skill](https://docs.microsoft.com/en-us/azure/search/cognitive-search-skill-ocr) you read about in Step 3. We suggest you add them at the end of the JSON of the body syntax definition. 

#### Step 5.2
Skipping the services and the data source creation, repeat the other steps of the Lab 1, in the same order. Use the previous lab as a reference.

1. ~~Create the services at the portal~~ **Not required, we did not delete it**.
2. ~~Create the Data Source~~ **Not required, we did not delete it**.
3. Recreate the Skillset
4. Recreate the Index
5. Recreate the Indexer
6. Check Indexer Status - Here you can repeat the same verification of Lab 2, Step 1. If you don't have a different result, something went wrong.  
7. Check the Index Fields - Check the image fields you just created.
8. Check the data - Here you can repeat the same verification of Lab 2, Step 2. If you don't have a different result, something went wrong.

**TIP 1:** What you need to do:
1. Create a new skillset exactly like the one we did in Lab 1, but with an extra skill, the OCR skillset. You can use the same json body field and add the new OCR skill in the end.
2. Create a new index exactly like the one we did in Lab 1 but with an extra field for the OCR text from the images. Name suggestion: myOCRtext. You can use the same json body field and add the new OCR field in the end.
3. Create a new indexer exactly like the one we did in Lab 1, but with and extra mapping for the new skill and the new field listed above. You can use the same json body field and add the new OCR mapping in the end.

**TIP 2:** Your new field in the Index must have the [Collection Data Type](https://docs.microsoft.com/en-us/rest/api/searchservice/Supported-data-types?redirectedfrom=MSDN).

**TIP 3:** You can query only the OCR field, to better visualize the results. Suppose that your new index field name is myOcrTex. You can query it using:
```http
GET https://[servicename].search.search.windows.net/indexes/rodindex2/docs?search=*&$select=myOcrText&api-version=2017-11-11-Preview
api-key: [api-key]
Content-Type: application/json
```
**TIP 4:** Your indexer sourceFieldName for the OCR text field has to be /document/normalized_images/*/myOcrText if your field is named myOcrText.  

