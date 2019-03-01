### Step 2 - Checking the other part of the problem
Now let's again repeat a previous lab request, but with another analysis. We will re-execute the step to verify content, but this time querying all fields.  

```http
GET https://[servicename].search.windows.net/indexes/demoindex/docs?search=*&$select=*&api-version=2017-11-11-Preview
api-key: [api-key]
Content-Type: application/json
```
You will probably see something similar to the image below - no information for the images we have.

![](./media/no-images-info.PNG)


## How can we fix it?

We will fix it, but there is a challenge for you increase your learning about Predefined Skills. The next steps will guide you through the challenge and don't worry if you get stuck (that's why it's a challenge!), we will share the solution, too. 

