## Step 3 - Test the function from Visual Studio

Press **F5** to run the program and test function behaviors. Use Postman or Fiddler to issue a call like the one shown below:

```http
POST https://localhost:7071/api/Translate
```
#### Request body
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
#### Response
You should see a response similar to the following example:

```json
{
    "values": [
        {
            "recordId": "a1",
            "data": {
                "text": "This is a contract in English"
            },
            "errors": null,
            "warnings": null
        }
    ]
}
```
