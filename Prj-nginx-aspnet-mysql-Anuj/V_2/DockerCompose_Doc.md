







## Task 2 (v2):

 In this version I have cloned repository from the link “https://github.com/docker/awesome-compose/tree/master/nginx-aspnet-mysql” to the ubuntu machine and performed docker commands





Below is project structure
<pre>
├── backend
│   ├── Dockerfile
│   ├── aspnet.csproj
│   └── Program.cs
├── db
│   └── password.txt
├── compose.yaml
├── proxy
│   ├── conf
│   └── Dockerfile
└── README.md
</pre>
The compose.yml file defines an application with three services proxy, backend and db. When deploying the application, docker compose maps port 80 of the proxy service container to port 80 of the host as specified in the file.

For deploy with docker compose use the following command:

  ``docker compose up -d``

**Expected Result:**
<pre>
[+] Running 3/0
 ✔ Container nginx-aspnet-mysql-db-1       Running                             0.0s
 ✔ Container nginx-aspnet-mysql-backend-1  Running                             0.0s
 ✔ Container nginx-aspnet-mysql-proxy-1    Running                             0.0s
</pre>

After the application starts, navigate to `http://localhost:80` in your web browser or run:

**Command**

``curl localhost:80``

**Output**

`["Blog post #0","Blog post #1","Blog post #2","Blog post #3","Blog post #4"]`

**Finally to stop and remove container**

``docker compose down``

**Output:**
<pre>
[+] Running 4/4
 ✔ Container nginx-aspnet-mysql-proxy-1    Removed                             0.0s
 ✔ Container nginx-aspnet-mysql-backend-1  Removed                             0.0s
 ✔ Container nginx-aspnet-mysql-db-1       Removed                             0.0s
 ✔ Network nginx-aspnet-mysql_default      Removed                             0.1s
</pre>

                                                                                                       Submitted by:
                                                                                                         Anuj Sharma
