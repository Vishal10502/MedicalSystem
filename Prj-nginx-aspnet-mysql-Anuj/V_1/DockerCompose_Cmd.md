**Command Line Interface commands which i used during deployment of V1**

**For Version 1**
<pre>
Microsoft Windows [Version 10.0.19045.2006]
(c) Microsoft Corporation. All rights reserved.

C:\Users\anuj.sharma5>cd .ssh

C:\Users\anuj.sharma5\.ssh>ls
'ls' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\anuj.sharma5\.ssh>ssh -i sshkey.pem ubuntu@54.225.10.79
The authenticity of host '54.225.10.79 (54.225.10.79)' can't be established.
ECDSA key fingerprint is SHA256:powLJNofFXU0MTaI48J8wYSfUBGpCaloU1OsWr23iUA.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '54.225.10.79' (ECDSA) to the list of known hosts.
Welcome to Ubuntu 22.04.2 LTS (GNU/Linux 5.19.0-1025-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Sun Aug 20 18:08:38 UTC 2023

  System load:  0.98486328125     Processes:                116
  Usage of /:   30.4% of 7.57GB   Users logged in:          0
  Memory usage: 40%               IPv4 address for docker0: 172.17.0.1
  Swap usage:   0%                IPv4 address for eth0:    172.31.35.174

Expanded Security Maintenance for Applications is not enabled.

113 updates can be applied immediately.
62 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable

Enable ESM Apps to receive additional future security updates.
See https://ubuntu.com/esm or run: sudo pro status



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

ubuntu@ip-172-31-35-174:~$ sudo su
root@ip-172-31-35-174:/home/ubuntu# docker --version
Docker version 24.0.5, build ced0996
root@ip-172-31-35-174:/home/ubuntu# docker image ls
REPOSITORY   TAG       IMAGE ID   CREATED   SIZE
root@ip-172-31-35-174:/home/ubuntu# docker container ls
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
root@ip-172-31-35-174:/home/ubuntu# git clone https://github.com/docker/awesome-compose/tree/master/nginx-aspnet-mysql
Cloning into 'nginx-aspnet-mysql'...
fatal: repository 'https://github.com/docker/awesome-compose/tree/master/nginx-aspnet-mysql/' not found
root@ip-172-31-35-174:/home/ubuntu# git clone https://github.com/docker/awesome-compose/tree/master/nginx-aspnet-mysql
Cloning into 'nginx-aspnet-mysql'...
fatal: repository 'https://github.com/docker/awesome-compose/tree/master/nginx-aspnet-mysql/' not found
[+] Running 12/12-174:/home/ubuntu# git clone https://github.com/docker/awesome-comp
 ✔ db 11 layers [⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿]      0B/0B      Pulled                          10.7s
   ✔ d5fd17ec1767 Pull complete                                                3.7s
   ✔ 49b1cc1f34f7 Pull complete                                                3.8s
   ✔ 9924a2c30493 Pull complete                                                4.1s
   ✔ a2bb7d6219ce Pull complete                                                4.4s
   ✔ 1eb5d2e9991e Pull complete                                                4.4s
   ✔ 3cbaef7da880 Pull complete                                                4.9s
   ✔ 52f39675d129 Pull complete                                                5.0s
   ✔ a4c0075a397a Pull complete                                                5.0s
   ✔ 248a5800afac Pull complete                                               10.4s
   ✔ 27261e54ed45 Pull complete                                               10.4s
   ✔ 3b18f8f83243 Pull complete                                               10.4s
[+] Building 13.5s (9/16)
 => [backend internal] load metadata for mcr.microsoft.com/dotnet/sdk:6.0      0.3ss
 => [backend internal] load metadata for mcr.microsoft.com/dotnet/aspnet:6.0   0.3s
 => [backend base 1/4] FROM mcr.microsoft.com/dotnet/sdk:6.0@sha256:b1ac02d4  11.8s
[+] Building 13.6s (9/16)
 => [backend internal] load metadata for mcr.microsoft.com/dotnet/sdk:6.0      0.3s
 => [backend internal] load metadata for mcr.microsoft.com/dotnet/aspnet:6.0   0.3s
 => [backend base 1/4] FROM mcr.microsoft.com/dotnet/sdk:6.0@sha256:b1ac02d4  11.9s
 => => resolve mcr.microsoft.com/dotnet/sdk:6.0@sha256:b1ac02d48e170b007d2d23  0.0s
 => => sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778 28.31MB / 31.42MB  11.9s
 => => sha256:b1ac02d48e170b007d2d2392119fa037e531f1ad93cf843 1.82kB / 1.82kB  0.0s
 => => sha256:3ced45b0441dd414a9c6b95a627e557726bf95cf3042660 2.01kB / 2.01kB  0.0s
[+] Building 17.0s (9/16)
[+] Building 33.3s (24/24) FINISHED
 => [backend internal] load build definition from Dockerfile                   0.1s
 => => transferring dockerfile: 793B                                           0.0s
 => [backend internal] load .dockerignore                                      0.1s
 => => transferring context: 2B                                                0.0s
 => [backend] resolve image config for docker.io/docker/dockerfile:1.4         0.4s
 => [backend] docker-image://docker.io/docker/dockerfile:1.4@sha256:9ba7531bd  0.5s
 => => resolve docker.io/docker/dockerfile:1.4@sha256:9ba7531bd80fb0a85863272  0.0s
 => => sha256:9ba7531bd80fb0a858632727cf7a112fbfd19b17e94c4e8 2.00kB / 2.00kB  0.0s
 => => sha256:ad87fb03593d1b71f9a1cfc1406c4aafcb253b1dabebf569768 528B / 528B  0.0s
 => => sha256:1e8a16826fd1c80a63fa6817a9c7284c94e40cded14a9b0 2.37kB / 2.37kB  0.0s
 => => sha256:1328b32c40fca9bcf9d70d8eccb72eb873d1124d72dadce 9.94MB / 9.94MB  0.2s
 => => extracting sha256:1328b32c40fca9bcf9d70d8eccb72eb873d1124d72dadce04db8  0.3s
 => [backend internal] load metadata for mcr.microsoft.com/dotnet/sdk:6.0      0.3s
 => [backend internal] load metadata for mcr.microsoft.com/dotnet/aspnet:6.0   0.3s
 => [backend base 1/4] FROM mcr.microsoft.com/dotnet/sdk:6.0@sha256:b1ac02d4  17.9s
 => => resolve mcr.microsoft.com/dotnet/sdk:6.0@sha256:b1ac02d48e170b007d2d23  0.0s
 => => sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778 28.31MB / 31.42MB  31.7s
 => => sha256:b1ac02d48e170b007d2d2392119fa037e531f1ad93cf843 1.82kB / 1.82kB  0.0s
 => => sha256:3ced45b0441dd414a9c6b95a627e557726bf95cf3042660 2.01kB / 2.01kB  0.0s
 => => sha256:a65621c96b07cd4500f85cbab71a949ac3251ad056794 31.66MB / 31.66MB  1.0s
 => => sha256:c998ae9ecc920b5f674da908d8f10462f3b30209c06c12c 7.17kB / 7.17kB  0.0s
 => => sha256:6c3981608c2b6b3825fe63b9c920101d7bf4ca80ceda7 14.97MB / 14.97MB  0.5s
 => => sha256:5a9070a06ae012d7ce05a03c90b76c57ebca94c3f6d434e27ff1 0B / 156B  31.7s
 => => sha256:d757ae0f0e6a72da889c1c194992d6dcf786868b4ceff5 9.47MB / 9.47MB  31.7s
 => => sha256:5dec5cf8f8b08d89661916e820d41899d37227d934347 25.37MB / 25.37MB  1.6s
 => => extracting sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6  4.0s
 => => sha256:2c5489b3efcc87ebfd8bcba003c4a0f88377637eab2 148.73MB / 148.73MB  4.4s
 => => sha256:60a72515fb46798c93c10ac84c0e178ee5e18ffd8349c 13.71MB / 13.71MB  1.7s
 => => extracting sha256:6c3981608c2b6b3825fe63b9c920101d7bf4ca80ceda7ddc0dc0  0.6s
 => => extracting sha256:a65621c96b07cd4500f85cbab71a949ac3251ad056794e16566d  1.2s
 => => extracting sha256:5a9070a06ae012d7ce05a03c90b76c57ebca94c3f6d434e27ff1  0.0s
 => => extracting sha256:d757ae0f0e6a72da889c1c194992d6dcf786868b4ceff54d4022  0.4s
 => => extracting sha256:5dec5cf8f8b08d89661916e820d41899d37227d934347e734801  1.7s
 => => extracting sha256:2c5489b3efcc87ebfd8bcba003c4a0f88377637eab2763a06da2  7.4s
 => => extracting sha256:60a72515fb46798c93c10ac84c0e178ee5e18ffd8349cc6322e2  0.8s
 => [backend stage-4 1/3] FROM mcr.microsoft.com/dotnet/aspnet:6.0@sha256:e85  7.9s
 => => resolve mcr.microsoft.com/dotnet/aspnet:6.0@sha256:e855110445f4a1b48bb  0.0s
 => => sha256:6c3981608c2b6b3825fe63b9c920101d7bf4ca80ceda 14.97MB / 14.97MB  31.6s
 => => sha256:a65621c96b07cd4500f85cbab71a949ac3251ad05679 31.66MB / 31.66MB  31.6s
 => => sha256:e855110445f4a1b48bb0d5b6de9f14cd2dd311b1daaf047 1.82kB / 1.82kB  0.0s
 => => sha256:fa8fe66222e71452405b4487b4ebc50e6ddcd0297bd0e4d 1.37kB / 1.37kB  0.0s
 => => sha256:036528001cbbdf4a5e0ddfd164dd075e3c3372c5c51d8e6 3.26kB / 3.26kB  0.0s
 => => sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f 31.42MB / 31.42MB  0.7s
 => => sha256:5a9070a06ae012d7ce05a03c90b76c57ebca94c3f6d434e27ff 156B / 156B  0.6s
 => => sha256:d757ae0f0e6a72da889c1c194992d6dcf786868b4ceff54 9.47MB / 9.47MB  1.1s
 => => extracting sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc  30.7s
 => => extracting sha256:6c3981608c2b6b3825fe63b9c920101d7bf4ca80ceda7ddc0dc  26.6s
 => => extracting sha256:a65621c96b07cd4500f85cbab71a949ac3251ad056794e16566  25.9s
 => [backend internal] load build context                                      0.0s
 => => transferring context: 9.06kB                                            0.0s
 => [backend stage-4 2/3] WORKDIR /app                                         0.1s
 => [backend base 2/4] WORKDIR /src                                            0.1s
 => [backend base 3/4] COPY aspnetapp.csproj ./                                0.1s
 => [backend base 4/4] RUN ["dotnet", "restore"]                               4.1s
 => [backend builder 1/1] COPY . .                                             0.1s
 => [backend publisher 1/1] RUN ["dotnet", "publish", "-c", "Release", "-o",   6.6s
 => [backend stage-4 3/3] COPY --from=publisher /build .                       0.1s
 => [backend] exporting to image                                               0.1s
 => => exporting layers                                                        0.1s
 => => writing image sha256:e84c82c5d4f39eb4ac55589a94fda24c709bd25e0282eb92b  0.0s
 => => naming to docker.io/library/nginx-aspnet-mysql-backend                  0.0s
 => [proxy internal] load build definition from Dockerfile                     0.0s
 => => transferring dockerfile: 100B                                           0.0s
 => [proxy internal] load .dockerignore                                        0.0s
 => => transferring context: 2B                                                0.0s
 => [proxy internal] load metadata for docker.io/library/nginx:1.13-alpine     0.4s
 => [proxy internal] load build context                                        0.0s
 => => transferring context: 157B                                              0.0s
 => [proxy 1/2] FROM docker.io/library/nginx:1.13-alpine@sha256:9d46fd628d54e  1.0s
 => => resolve docker.io/library/nginx:1.13-alpine@sha256:9d46fd628d54ebe1633  0.0s
 => => extracting sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d9  0.2s
 => => sha256:9d46fd628d54ebe1633ee3cf0fe2acfcc419cfae541c630 2.04kB / 2.04kB  0.0s
 => => sha256:91d22184f3f9b1be658c2cc2c12d324de7ff12c8b9c9a59 1.15kB / 1.15kB  0.0s
 => => sha256:ebe2c7c61055cae340273904364fd6c6c0e8bab75ef9777 8.40kB / 8.40kB  0.0s
 => => sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504 2.07MB / 2.07MB  0.1s
 => => sha256:b430473be128c1302a75e8381dfbaa45182fec81db4f75b 5.82MB / 5.82MB  0.2s
 => => sha256:7d4e05a01906143afc15671a53151ea9755dac230db376a8b83 490B / 490B  0.1s
 => => sha256:8aeac9a3205fce5e21ab65ccce330fe389a9aaf47e4b682970b 628B / 628B  0.2s
 => => extracting sha256:b430473be128c1302a75e8381dfbaa45182fec81db4f75b749e4  0.4s
 => => extracting sha256:7d4e05a01906143afc15671a53151ea9755dac230db376a8b836  0.0s
 => => extracting sha256:8aeac9a3205fce5e21ab65ccce330fe389a9aaf47e4b682970b1  0.0s
 => [proxy 2/2] COPY conf /etc/nginx/conf.d/default.conf                       0.1s
 => [proxy] exporting to image                                                 0.1s
 => => exporting layers                                                        0.0s
 => => writing image sha256:005c7c246e8b562bfa40880518dcd53fb761b099031834d13  0.0s
 => => naming to docker.io/library/nginx-aspnet-mysql-proxy                    0.0s
[+] Running 5/3
 ✔ Network nginx-aspnet-mysql_default      Created                             0.1s
 ✔ Volume "nginx-aspnet-mysql_db-data"     Created                             0.0s
 ✔ Container nginx-aspnet-mysql-db-1       Created                             0.1s
 ✔ Container nginx-aspnet-mysql-backend-1  Created                             0.0s
 ✔ Container nginx-aspnet-mysql-proxy-1    Created                             0.0s
Attaching to nginx-aspnet-mysql-backend-1, nginx-aspnet-mysql-db-1, nginx-aspnet-mysql-proxy-1
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:32+00:00 [Note] [Entrypoint]: Entrypoint script for MariaDB Server 1:10.7.3+maria~focal started.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:33+00:00 [Note] [Entrypoint]: Switching to dedicated user 'mysql'
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:33+00:00 [Note] [Entrypoint]: Entrypoint script for MariaDB Server 1:10.7.3+maria~focal started.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:33+00:00 [Note] [Entrypoint]: Initializing database files
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:33 0 [Warning] 'default-authentication-plugin' is MySQL 5.6 / 5.7 compatible option. To be implemented in later versions.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:33 0 [Warning] You need to use --log-bin to make --expire-logs-days or --binlog-expire-logs-seconds work.
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | PLEASE REMEMBER TO SET A PASSWORD FOR THE MariaDB root USER !
nginx-aspnet-mysql-db-1       | To do so, start the server, then issue the following command:
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | '/usr/bin/mysql_secure_installation'
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | which will also give you the option of removing the test
nginx-aspnet-mysql-db-1       | databases and anonymous user created by default.  This is
nginx-aspnet-mysql-db-1       | strongly recommended for production servers.
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | See the MariaDB Knowledgebase at https://mariadb.com/kb
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | Please report any problems at https://mariadb.org/jira
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | The latest information about MariaDB is available at https://mariadb.org/.
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | Consider joining MariaDB's strong and vibrant community:
nginx-aspnet-mysql-db-1       | https://mariadb.org/get-involved/
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35+00:00 [Note] [Entrypoint]: Database files initialized
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35+00:00 [Note] [Entrypoint]: Starting temporary server
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35+00:00 [Note] [Entrypoint]: Waiting for server startup
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] mariadbd (server 10.7.3-MariaDB-1:10.7.3+maria~focal) starting as process 93 ...
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] InnoDB: Compressed tables use zlib 1.2.11
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] InnoDB: Number of transaction pools: 1
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] InnoDB: Using crc32 + pclmulqdq instructions
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] mariadbd: O_TMPFILE is not supported on /tmp (disabling future attempts)
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] InnoDB: Using Linux native AIO
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] InnoDB: Initializing buffer pool, total size = 134217728, chunk size = 134217728
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] InnoDB: Completed initialization of buffer pool
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] InnoDB: 128 rollback segments are active.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] InnoDB: Creating shared tablespace for temporary tables
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] InnoDB: Setting file './ibtmp1' size to 12 MB. Physically writing the file full; Please wait ...
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] InnoDB: File './ibtmp1' size is now 12 MB.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] InnoDB: 10.7.3 started; log sequence number 42173; transaction id 14
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] Plugin 'FEEDBACK' is disabled.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Warning] 'default-authentication-plugin' is MySQL 5.6 / 5.7 compatible option. To be implemented in later versions.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Warning] You need to use --log-bin to make --expire-logs-days or --binlog-expire-logs-seconds work.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Warning] 'user' entry 'root@5ed551929297' ignored in --skip-name-resolve mode.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Warning] 'proxies_priv' entry '@% root@5ed551929297' ignored in --skip-name-resolve mode.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:35 0 [Note] mariadbd: ready for connections.
nginx-aspnet-mysql-db-1       | Version: '10.7.3-MariaDB-1:10.7.3+maria~focal'  socket: '/run/mysqld/mysqld.sock'  port: 0  mariadb.org binary distribution
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:36+00:00 [Note] [Entrypoint]: Temporary server started.
nginx-aspnet-mysql-db-1       | Warning: Unable to load '/usr/share/zoneinfo/leap-seconds.list' as time zone. Skipping it.
nginx-aspnet-mysql-db-1       | Warning: Unable to load '/usr/share/zoneinfo/leapseconds' as time zone. Skipping it.
nginx-aspnet-mysql-db-1       | Warning: Unable to load '/usr/share/zoneinfo/tzdata.zi' as time zone. Skipping it.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:39+00:00 [Note] [Entrypoint]: Securing system users (equivalent to running mysql_secure_installation)
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:39+00:00 [Note] [Entrypoint]: Creating database example
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:39+00:00 [Note] [Entrypoint]: Stopping temporary server
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:39 0 [Note] mariadbd (initiated by: root[root] @ localhost []): Normal shutdown
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:39 0 [Note] InnoDB: FTS optimize thread exiting.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:39 0 [Note] InnoDB: Starting shutdown...
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:39 0 [Note] InnoDB: Dumping buffer pool(s) to /var/lib/mysql/ib_buffer_pool
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:39 0 [Note] InnoDB: Buffer pool(s) dump completed at 230820 18:15:39
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:39 0 [Note] InnoDB: Removed temporary tablespace data file: "./ibtmp1"
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:39 0 [Note] InnoDB: Shutdown completed; log sequence number 42185; transaction id 15
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:39 0 [Note] mariadbd: Shutdown complete
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40+00:00 [Note] [Entrypoint]: Temporary server stopped
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40+00:00 [Note] [Entrypoint]: MariaDB init process done. Ready for start up.
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       |
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] mariadbd (server 10.7.3-MariaDB-1:10.7.3+maria~focal) starting as process 1 ...
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: Compressed tables use zlib 1.2.11
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: Number of transaction pools: 1
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: Using crc32 + pclmulqdq instructions
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] mariadbd: O_TMPFILE is not supported on /tmp (disabling future attempts)
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: Using Linux native AIO
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: Initializing buffer pool, total size = 134217728, chunk size = 134217728
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: Completed initialization of buffer pool
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: 128 rollback segments are active.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: Creating shared tablespace for temporary tables
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: Setting file './ibtmp1' size to 12 MB. Physically writing the file full; Please wait ...
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: File './ibtmp1' size is now 12 MB.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: 10.7.3 started; log sequence number 42185; transaction id 14
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] Plugin 'FEEDBACK' is disabled.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Warning] 'default-authentication-plugin' is MySQL 5.6 / 5.7 compatible option. To be implemented in later versions.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Warning] You need to use --log-bin to make --expire-logs-days or --binlog-expire-logs-seconds work.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] InnoDB: Loading buffer pool(s) from /var/lib/mysql/ib_buffer_pool
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] Server socket created on IP: '0.0.0.0'.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:40 0 [Note] Server socket created on IP: '::'.
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:41 0 [Note] mariadbd: ready for connections.
nginx-aspnet-mysql-db-1       | Version: '10.7.3-MariaDB-1:10.7.3+maria~focal'  socket: '/run/mysqld/mysqld.sock'  port: 3306  mariadb.org binary distribution
nginx-aspnet-mysql-db-1       | 2023-08-20 18:15:41 0 [Note] InnoDB: Buffer pool(s) load completed at 230820 18:15:41
nginx-aspnet-mysql-backend-1  | info: Microsoft.Hosting.Lifetime[14]
nginx-aspnet-mysql-backend-1  |       Now listening on: http://[::]:8000
nginx-aspnet-mysql-backend-1  | info: Microsoft.Hosting.Lifetime[0]
nginx-aspnet-mysql-backend-1  |       Application started. Press Ctrl+C to shut down.
nginx-aspnet-mysql-backend-1  | info: Microsoft.Hosting.Lifetime[0]
nginx-aspnet-mysql-backend-1  |       Hosting environment: Production
nginx-aspnet-mysql-backend-1  | info: Microsoft.Hosting.Lifetime[0]
nginx-aspnet-mysql-backend-1  |       Content root path: /app/
client_loop: send disconnect: Connection reset

C:\Users\anuj.sharma5\.ssh>ssh -i sshkey.pem ubuntu@54.225.10.79
Welcome to Ubuntu 22.04.2 LTS (GNU/Linux 5.19.0-1025-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Sun Aug 20 18:29:11 UTC 2023

  System load:                      0.0
  Usage of /:                       47.7% of 7.57GB
  Memory usage:                     49%
  Swap usage:                       0%
  Processes:                        117
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

</pre>