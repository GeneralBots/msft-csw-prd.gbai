# Lab 3: Create a Cognitive Search Skillset with **Custom** Skills

In this lab, you will learn how to create a web API custom skill that accepts text in any language and translates it to English. It is required because there are documents in languages besides English in our dataset. The expected behavior of this code is to do nothing if the document language is English and translate to English if the document is in another language. **The provided dataset has documents in Spanish**.

We will use an [Azure Function](https://azure.microsoft.com/services/functions/) to wrap the [Translate Text API](https://azure.microsoft.com/services/cognitive-services/translator-text-api/) so that it implements the custom skill interface.

For documents in english we will replicate the original text in the output, so we can search only one field of our index. Another important detail, this function output is **Edm.String**, so we need to use the same type in the index definition.  
