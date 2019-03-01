## Step 5 - Test the function in Azure

Now that you have the default host key, test your function as follows:

```http
POST https://translatecogsrch.azurewebsites.net/api/Translate?code=[enter default host key here]
```
#### Request Body
```json
{
   "values": [
        {
        	"recordId": "a1",
        	"data":
	        {
	           "text":  "Este es un contrato en Inglés",
	           "language": "es"
	        }
        }
   ]
}
```

This should produce a similar result to the one you saw previously when running the function in the local environment.

### Step 5.1 - Update SSL Settings
All Azure Functions created after June 30th, 2018 have disabled TLS 1.0, which is not currently compatible with custom skills. 
Today, August 2018, Azure Functions default TLS is 1.2, which is causing issues. This is a **required workaround**:

1.	In the Azure portal, navigate to the Resource Group, and look for the Translate Function you published. Under the Platform features section, you should see SSL.
2.	After selecting SSL, you should change the **Minimum TLS version** to 1.0. TLS 1.2 functions are not yet supported as custom skills.

For more information, click [here](https://docs.microsoft.com/en-us/azure/search/cognitive-search-create-custom-skill-example#update-ssl-settings ) .


