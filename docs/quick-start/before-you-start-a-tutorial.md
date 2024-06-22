---
layout: page
---

# Before you  start a tutorial

These are the steps you must do before you can run
the tutorials for the Flight Management API service.

**Expect this preparation to take about 20 minutes to complete**.

## Preparing for the tutorials

The following instructions describe how to prepare for running the tutorials on Windows.

* A [GitHub account](https://github.com)
* A development system (PC, Mac, or Linux) running a current or
long-term support (LTS version of the operating system).
* The following software on your development system:
  * (Optional) [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) (for the command line).
  * [GitHub Desktop](https://desktop.github.com).
    * A fork of the [Flight-Management-service repo](https://github.com/radhikasundararaman24/flight-management-service).
    * A current copy of the Flight Management database file. You can get this by syncing your fork.
      * After forking the repo from GitHub, go to the forked clone on your local machine.
      * Go to **api**.
      * Check for the **flights-db-source.json** file.
    * **TIP**: If you're using a fork of the repo, create a working branch in which you test the API endpoints. Create a new branch for each test/tutorial to prevent a mistake in one from affecting your work in another.
* A current/LTS version of [node.js](https://nodejs.org/en/).
* A current version of [json-server](https://www.npmjs.com/package/json-server).
* A current version of [CURL](https://curl.se/download.html). By default, CURL is mounted in Windows operating system.
* The [Postman desktop app](https://www.postman.com/downloads/). Because you run the **Flight-Management service** on your development system with an `http://localhost` hostname, the web-version of Postman can't perform the exercises.

## Test your development system

To test your development system, follow these steps:

1. Check your json-server version.

    ```shell
    C:\> json-server --version
    ```
    This will display the installed json-server version.

    ```shell
    1.0.0-alpha.23
    ```

1. Check your Node.js version.
    ```shell
    C:\> node -v
    v20.13.0
    
    OR

    C:\> node --version
    v20.13.0
    ```
    This will display the installed Node.js version.
    
    ```shell
    v20.13.0
    ```

1. Create and checkout a test branch of your fork of the Flight Management service repo. Your `GitHub repo workspace` is the directory that contains your fork of the `flight-management-service` repo.

    ```shell
    cd <your GitHub repo workspace>
    cd flight-management-service
    cd api
    cd start-server.bat
    ```
1. To watch your server, type the following command: 
          
    ```shell
    C:\flight-management-service\api> json-server -w flights-db-source.json
     ```
   If your development system is installed correctly, you should see
   the service start and display the URL of the service: `http://localhost:3000`.
    
    ```shell
    --watch/-w can be omitted, JSON Server 1+ watches for file changes by default
    JSON Server started on PORT :3000
    Press CTRL-C to stop
    Watching flights-db-source.json...
    
    ( ˶ˆ ᗜ ˆ˵ )
    
    Index:
    http://localhost:3000/
    
    Static files:
    Serving ./public directory if it exists
    
    Endpoints:
    http://localhost:3000/flights
    http://localhost:3000/passengers
    http://localhost:3000/reservations
    ```
    
1. Make a test call to the service.

    ```shell
    curl http://localhost:3000/passengers
    ```

1. If the service is running correctly, you should see a list of users from the service, such as in this example.

    ```json
      {
        "email": "doejoe@abc.com",
        "id": "P001",
        "firstName": "John",
        "lastName": "Doe",
        "dob": "1985-10-10",
        "passportNumber": "A12345678",
        "nationality": "USA"
      },
      {
        "id": "P002",
        "firstName": "Jane",
        "lastName": "Smith",
        "dob": "1990-03-25",
        "passportNumber": "B87654321",
        "nationality": "Canada"
      }
    ```

If you don't see the list of passengers, or receive an error in any step
of the procedure, investigate and correct the error before continuing.
Some common situations that cause errors include:

- You mistyped a command.
- You aren't in the correct directory.
- A required software component didn't install correctly.
- A required software component isn't up to date.

If you see the list of passengers from the service, you're ready to do
the tutorials.

## Next steps

- [Create or import Postman collection.](create-postman-collection.md)
