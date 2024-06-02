# Set up base URL and environment variables in Postman


## Step 1: Open Postman

Launch the Postman application on your computer.

## Step 2: Create a New Collection

If you don't have an existing collection, you can create a new one by clicking on the **New** button in the top-left corner of the Postman interface and selecting "Collection".

## Step 3: Create a New Request

Inside the collection you just created, click on the **Add Request** button to create a new request.

## Step 4: Add requests

Repeat step 3 for as many requests you want to create and save all the requests within the collection.

## Step 4: Set Up Base URL Variable

1. In the request pane, click on the **Params** tab.
1. Click on **Add Param** button.
1. Choose **URL** from the dropdown menu.
1. Enter a name for your variable, e.g., ```baseURL```.
1. Enter the base URL for your API, e.g., ```http://localhost:3000```.
1. Click **Save**.  

## Step 5: Use Base URL Variable in Requests

Now, whenever you create a new request within this collection, you can use the ```baseURL``` variable as part of your URL. For example, if you want to make a request to ```http://localhost:3000/passengers```, you can simply use ```{{baseURL}}/passengers``` as your request URL.

## Step 6: Environment Variables (Optional)

If you want to use different ```base URLs``` for different environments (e.g., development, staging, production), you can create environment variables:

1. Click on the gear icon in the top-right corner of the Postman interface. 
1. Click on **Add** to create a new environment.
1. Enter a name for your environment, e.g., "Development".
1. Add a variable called baseURL and set its value to the base URL for your development environment, e.g., https://dev.api.example.com.
1. Click **Add** to save the environment.


## Step 7: Switch Environments

You can switch between environments using the dropdown menu in the top-right corner of the Postman interface. When you switch to a different environment, Postman will automatically use the corresponding base URL variable for your requests.

That's it! You've now set up base URL variables in Postman. This will make it easier to manage your API requests, especially when working with multiple environments.
