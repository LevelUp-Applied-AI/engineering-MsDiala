# Docker Notes — Day 9

## Docker Version

Client:
 Version:           29.1.3
 API version:       1.52
 Go version:        go1.25.5
 Git commit:        f52814d
 Built:             Fri Dec 12 14:48:46 2025
 OS/Arch:           darwin/arm64
 Context:           desktop-linux

Server: Docker Desktop 4.57.0 (215387)
 Engine:
  Version:          29.1.3
  API version:      1.52 (minimum version 1.44)
  Go version:       go1.25.5
  Git commit:       fbf3ed2
  Built:            Fri Dec 12 14:50:40 2025
  OS/Arch:          linux/arm64
  Experimental:     false


## Hello World Test

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (arm64v8)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash


## Postgres Container

Command used:

docker run -d \
  --name pg-prework \
  -e POSTGRES_PASSWORD=prework \
  -p 5432:5432 \
  postgres:15-alpine


Startup Logs  
Output of docker logs pg-prework (include the full init sequence):

The files belonging to this database system will be owned by user "postgres".
This user must also own the server process.

The database cluster will be initialized with locale "en_US.utf8".
The default database encoding has accordingly been set to "UTF8".

creating configuration files ... ok
running bootstrap script ... ok

Success. You can now start the database server using:

pg_ctl -D /var/lib/postgresql/data -l logfile start

LOG: starting PostgreSQL 15.17
LOG: listening on IPv4 address "0.0.0.0", port 5432
LOG: listening on IPv6 address "::", port 5432
LOG: database system is ready to accept connections


Startup confirmation line found:  
LOG: database system is ready to accept connections


Stop and Restart

docker stop pg-prework  
pg-prework

docker restart pg-prework  
pg-prework

docker logs pg-prework (after restart)

PostgreSQL Database directory appears to contain a database; Skipping initialization

LOG: starting PostgreSQL 15.17
LOG: listening on IPv4 address "0.0.0.0", port 5432
LOG: listening on IPv6 address "::", port 5432
LOG: database system is ready to accept connections


Issues Encountered

When attempting to run the container creation command again, Docker returned a conflict error indicating that the container name "pg-prework" was already in use. This occurred because the container had already been created previously.

The issue was resolved by restarting the existing container using:

docker restart pg-prework

After restarting, PostgreSQL started successfully and the logs confirmed that the database system was ready to accept connections.