# Set up URL in Postman

## Step 1: Configure the Base URL variable

1. In the request pane, click on the **Params** tab.
1. Click on **Add Param** button.
1. Choose **URL** from the dropdown menu.
1. Enter a name for your variable, e.g., ```baseURL```.
1. Enter the base URL for your API, e.g., ```http://localhost:3000```.
1. Click **Save**.  

## Step 2: Use the Base URL variable in requests

Now, whenever you create a new request within this collection, you can use the ```baseURL``` variable as part of your URL. For example, if you want to make a request to ```http://localhost:3000/passengers```, you can simply use ```{{baseURL}}/passengers``` as your request URL.

## Step 3: (Optional) Configure environment variables 

If you want to use different ```base URLs``` for different environments (e.g., development, staging, production), you can create environment variables:

1. Click on the gear icon in the top-right corner of the Postman interface. 
1. To create a new environment, click **Add**.
1. Enter a name for your environment, e.g., "Development".
1. Add a variable called baseURL and set its value to the base URL for your development environment, e.g., https://dev.api.example.com.
1. Click **Add** and save the environment.


## Step 4: Switch environments

You can switch between environments using the dropdown menu in the top-right corner of the Postman interface. When you switch to a different environment, Postman will automatically use the corresponding base URL variable for your requests.

That's it! You've now set up base URL variables in Postman. This will make it easier to manage your API requests, especially when working with multiple environments.

## Next steps

- [Make your first API call.](make-your-first-api-call.md)
