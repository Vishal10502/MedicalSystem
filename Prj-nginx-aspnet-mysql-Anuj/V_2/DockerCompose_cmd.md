
## For Version 2 (Task 2)
<pre>
Last login: Sun Aug 20 18:08:40 2023 from 150.242.86.118
ubuntu@ip-172-31-35-174:~$ ls
awesome-compose
ubuntu@ip-172-31-35-174:~$ cd awesome-compose/
ubuntu@ip-172-31-35-174:~/awesome-compose$ cd nginx-aspnet-mysql/
ubuntu@ip-172-31-35-174:~/awesome-compose/nginx-aspnet-mysql$ docker compose up
permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/json?all=1&filters=%7B%22label%22%3A%7B%22com.docker.compose.config-hash%22%3Atrue%2C%22com.docker.compose.project%3Dnginx-aspnet-mysql%22%3Atrue%7D%7D": dial unix /var/run/docker.sock: connect: permission denied
[+] Running 3/31-35-174:~/awesome-compose/nginx-aspnet-mysql$ sudo su
 ✔ Container nginx-aspnet-mysql-db-1       Healthy                             0.5s
 ✔ Container nginx-aspnet-mysql-backend-1  Running                             0.0s
 ✔ Container nginx-aspnet-mysql-proxy-1    Running                             0.0s
[+] Running 3/335-174:/home/ubuntu/awesome-compose/nginx-aspnet-mysql# docker compos
 ✔ Container nginx-aspnet-mysql-db-1       Healthy                             0.5s
 ✔ Container nginx-aspnet-mysql-backend-1  Running                             0.0s
 ✔ Container nginx-aspnet-mysql-proxy-1    Running                             0.0s
root@ip-172-31-35-174:/home/ubuntu/awesome-compose/nginx-aspnet-mysql# curl http://localhost
["Blog post #0","Blog post #1","Blog post #2","Blog post #3","Blog post #4"]root@ip-172-31-35-174:/home/ubuntu/awesome-compose/nginx-aspnet-mysql# client_loop: send disconnect: Connection reset

C:\Users\anuj.sharma5\.ssh>ssh -i sshkey.pem ubuntu@54.225.10.79
Welcome to Ubuntu 22.04.2 LTS (GNU/Linux 5.19.0-1025-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Sun Aug 20 18:36:48 UTC 2023

  System load:                      0.0
  Usage of /:                       47.7% of 7.57GB
  Memory usage:                     50%
  Swap usage:                       0%
  Processes:                        124
  Users logged in:                  1
  IPv4 address for br-8c8acb89b061: 172.18.0.1
  IPv4 address for docker0:         172.17.0.1
  IPv4 address for eth0:            172.31.35.174


Expanded Security Maintenance for Applications is not enabled.

113 updates can be applied immediately.
62 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable

Enable ESM Apps to receive additional future security updates.
See https://ubuntu.com/esm or run: sudo pro status


Last login: Sun Aug 20 18:29:12 2023 from 150.242.86.118
ubuntu@ip-172-31-35-174:~$ ls
awesome-compose
ubuntu@ip-172-31-35-174:~$ cd awesome-compose/
ubuntu@ip-172-31-35-174:~/awesome-compose$ cd nginx-aspnet-mysql/
ubuntu@ip-172-31-35-174:~/awesome-compose/nginx-aspnet-mysql$ docker compose up
permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/json?all=1&filters=%7B%22label%22%3A%7B%22com.docker.compose.config-hash%22%3Atrue%2C%22com.docker.compose.project%3Dnginx-aspnet-mysql%22%3Atrue%7D%7D": dial unix /var/run/docker.sock: connect: permission denied
ubuntu@ip-172-31-35-174:~/awesome-compose/nginx-aspnet-mysql$ sudo su
root@ip-172-31-35-174:/home/ubuntu/awesome-compose/nginx-aspnet-mysql# docker compose up
[+] Running 3/0
 ✔ Container nginx-aspnet-mysql-db-1       Running                             0.0s
 ✔ Container nginx-aspnet-mysql-backend-1  Running                             0.0s
 ✔ Container nginx-aspnet-mysql-proxy-1    Running                             0.0s
Attaching to nginx-aspnet-mysql-backend-1, nginx-aspnet-mysql-db-1, nginx-aspnet-mysql-proxy-1
q
^CGracefully stopping... (press Ctrl+C again to force)
Aborting on container exit...
[+] Stopping 3/3
 ✔ Container nginx-aspnet-mysql-proxy-1    Stopped                             0.2s
 ✔ Container nginx-aspnet-mysql-backend-1  Stopped                             0.2s
 ✔ Container nginx-aspnet-mysql-db-1       Stopped                             0.4s
canceled
root@ip-172-31-35-174:/home/ubuntu/awesome-compose/nginx-aspnet-mysql# $ docker compose down -d
$: command not found
root@ip-172-31-35-174:/home/ubuntu/awesome-compose/nginx-aspnet-mysql# docker compos
e down -d
unknown shorthand flag: 'd' in -d
root@ip-172-31-35-174:/home/ubuntu/awesome-compose/nginx-aspnet-mysql# docker compose down
[+] Running 4/4
 ✔ Container nginx-aspnet-mysql-proxy-1    Removed                             0.0s
 ✔ Container nginx-aspnet-mysql-backend-1  Removed                             0.0s
 ✔ Container nginx-aspnet-mysql-db-1       Removed                             0.0s
 ✔ Network nginx-aspnet-mysql_default      Removed                             0.1s
root@ip-172-31-35-174:/home/ubuntu/awesome-compose/nginx-aspnet-mysql#

<pre>

**Submitted By:**
**Anuj Sharma**
