###Cloud-IaaS-basics

- create a server (EC2 instance) on AWS and deploy an application on it
  
  - Setup and configured a server on AWS
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/953baf2a-49c6-429d-a03d-02133bbb79d8)
  - Configured Firewall rule to open port 22 for your IP address
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/d0ecb110-5687-44b4-837d-4e58c10af93c)

  - Login to server as a root user using an SSH client
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/8a9e857f-ce73-4c0f-9770-25ef45b48db2)

  - Created and configured a new Linux user on the Server (Security best practice)
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/117023d1-491c-497c-b982-26f21364473c)

  - Deploy and run a Java application on Server
    
  - Installation:
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/8a315bc1-0ae9-42cd-8299-ad5a748da02c)

  - Clone this repo and build the app locally: https://github.com/pmendelski/java-react-example.git
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/4042284e-3fbd-4ed1-b495-1f1b5c942a70)
    
  - copied the java app jar file to the server
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/8fcf70c0-d074-4664-aafe-033fc1ced93b)

    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/20c5697f-7810-4cef-8ce6-fc57f0770474)
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/03d8deba-20a0-40e7-b0d1-465e7ffb1e78)
    
    - Run the app on the server
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/55d8dae1-bed6-4787-9de4-f029b176319a)

    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/b6c1d489-2e8f-4c8b-9079-528ed7d1820b)
    application is ruuning on port 7071

    opening the same port in inbound rules of the security group attached to this instance
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/b7396c54-c266-4834-9c5e-630a5c6f82dd)

    accessing the app in new tab with public IPv4:7071 or PublicDNS:7071
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/995db3de-f20b-4472-8afe-28cf491ba90f)
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/aa9b57af-0efa-4e09-973f-6e0884702884)
    we can see the logs on server
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/31079142-e2bf-4b63-94a4-d37ebaa814b9)

    Running the app in detached mode
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/d3a2cef7-f138-4c2d-b171-5bca8a8bb9f8)

    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/c935334f-f30d-4ea2-886f-52c8a0b4990b)

    Checking the port on which the app is running in detached mode
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/c058a50b-34ca-4932-9e03-2c5aec7be82d)

    Security best practice is to not run the app/services as a root user, instead create a separate user for each service/app with minimum needed permissions to run the app
    switch user to demo and public key for the same as we have configured the public key just for the root user.
    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/49b9209b-b613-4368-b859-689de39f3515)

    adding the public key to this user in .ssh folder --> authorized_keys file

    ![image](https://github.com/hemu07/Cloud-IaaS-basics/assets/90203539/f4c4ce99-2091-4a00-9b21-2f402dd64b00)

