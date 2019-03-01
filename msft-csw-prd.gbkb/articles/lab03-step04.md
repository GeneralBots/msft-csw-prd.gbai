## Step 4 - Publish the function to Azure

When you are satisfied with the function behavior, you can publish it.

1. In **Solution Explorer**, right-click the project and select **Publish**. Choose **Create New** > **Publish**.

2. If you haven't already connected Visual Studio to your Azure account, select **Add an account....**

3. Follow the on-screen prompts. You are asked to specify the Azure account, the resource group, the hosting plan, and the storage account you want to use. You can create a new resource group, a new hosting plan, and a storage account if you don't already have these. When finished, select **Create**

4. After the deployment is complete, note the Site URL. It is the address of your function app in Azure. 

5. In the [Azure portal](https://portal.azure.com), navigate to the Resource Group, and look for the Translate Function you published. Under the **Manage** section, you should see Host Keys. Select the **Copy** icon for the *default* host key.  

