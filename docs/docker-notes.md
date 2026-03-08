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
 containerd:
  Version:          v2.2.1
  GitCommit:        dea7da592f5d1d2b7755e3a161be07f43fad8f75
 runc:
  Version:          1.3.4
  GitCommit:        v1.3.4-0-gd6d73eb8
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0


## Docker Info 
Client:
 Version:    29.1.3
 Context:    desktop-linux
 Debug Mode: false
 Plugins:
  ai: Docker AI Agent - Ask Gordon (Docker Inc.)
    Version:  v1.17.1
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-ai
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.30.1-desktop.1
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-buildx
  compose: Docker Compose (Docker Inc.)
    Version:  v5.0.1
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-compose
  debug: Get a shell into any image or container (Docker Inc.)
    Version:  0.0.47
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-debug
  desktop: Docker Desktop commands (Docker Inc.)
    Version:  v0.2.0
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-desktop
  extension: Manages Docker extensions (Docker Inc.)
    Version:  v0.2.31
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-extension
  init: Creates Docker-related starter files for your project (Docker Inc.)
    Version:  v1.4.0
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-init
  mcp: Docker MCP Plugin (Docker Inc.)
    Version:  v0.35.0
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-mcp
  model: Docker Model Runner (Docker Inc.)
    Version:  v1.0.6
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-model
  offload: Docker Offload (Docker Inc.)
    Version:  v0.5.40
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-offload
  pass: Docker Pass Secrets Manager Plugin (beta) (Docker Inc.)
    Version:  v0.0.22
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-pass
  sandbox: Docker Sandbox (Docker Inc.)
    Version:  v0.6.0
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-sandbox
  sbom: View the packaged-based Software Bill Of Materials (SBOM) for an image (Anchore Inc.)
    Version:  0.6.0
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-sbom
  scout: Docker Scout (Docker Inc.)
    Version:  v1.19.0
    Path:     /Users/dialaabedalqader/.docker/cli-plugins/docker-scout

Server:
 Containers: 7
  Running: 1
  Paused: 0
  Stopped: 6
 Images: 5
 Server Version: 29.1.3
 Storage Driver: overlayfs
  driver-type: io.containerd.snapshotter.v1
 Logging Driver: json-file
 Cgroup Driver: cgroupfs
 Cgroup Version: 2
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 CDI spec directories:
  /etc/cdi
  /var/run/cdi
 Discovered Devices:
  cdi: docker.com/gpu=webgpu
 Swarm: inactive
 Runtimes: runc io.containerd.runc.v2
 Default Runtime: runc
 Init Binary: docker-init
 containerd version: dea7da592f5d1d2b7755e3a161be07f43fad8f75
 runc version: v1.3.4-0-gd6d73eb8
 init version: de40ad0
 Security Options:
  seccomp
   Profile: builtin
  cgroupns
 Kernel Version: 6.12.54-linuxkit
 Operating System: Docker Desktop
 OSType: linux
 Architecture: aarch64
 CPUs: 12
 Total Memory: 7.653GiB
 Name: docker-desktop
 ID: 39b91c03-1bfa-4a0f-a0f0-4c73a1bb6f93
 Docker Root Dir: /var/lib/docker
 Debug Mode: false
 HTTP Proxy: http.docker.internal:3128
 HTTPS Proxy: http.docker.internal:3128
 No Proxy: hubproxy.docker.internal
 Labels:
  com.docker.desktop.address=unix:///Users/dialaabedalqader/Library/Containers/com.docker.docker/Data/docker-cli.sock
 Experimental: false
 Insecure Registries:
  hubproxy.docker.internal:5555
  ::1/128
  127.0.0.0/8
 Live Restore Enabled: false
 Firewall Backend: iptables

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

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/


## docker images
IMAGE                 ID             DISK USAGE   CONTENT SIZE   EXTRA
frappe/bench:latest   652962dbdf20        2.9GB          686MB    U   
hello-world:latest    ef54e839ef54       22.5kB         10.2kB    U   
mariadb:10.8          456709ab1465        490MB          114MB    U   
postgres:15-alpine    2bf082886c05        386MB          108MB    U   
redis:alpine          6cbef353e480        130MB         33.8MB    U   

## Postgres Container
CONTAINER ID   IMAGE                COMMAND                  CREATED         STATUS         PORTS                                         NAMES
aa84a3cefa68   postgres:15-alpine   "docker-entrypoint.s…"   6 minutes ago   Up 4 minutes   0.0.0.0:5432->5432/tcp, [::]:5432->5432/tcp   


## Startup Logs

The files belonging to this database system will be owned by user "postgres".
This user must also own the server process.

The database cluster will be initialized with locale "en_US.utf8".
The default database encoding has accordingly been set to "UTF8".
The default text search configuration will be set to "english".

Data page checksums are disabled.

fixing permissions on existing directory /var/lib/postgresql/data ... ok
creating subdirectories ... ok
selecting dynamic shared memory implementation ... posix
selecting default max_connections ... 100
selecting default shared_buffers ... 128MB
selecting default time zone ... UTC
creating configuration files ... ok
running bootstrap script ... ok
sh: locale: not found
2026-02-28 07:59:10.120 UTC [35] WARNING:  no usable system locales were found
performing post-bootstrap initialization ... ok
initdb: warning: enabling "trust" authentication for local connections
initdb: hint: You can change this by editing pg_hba.conf or using the option -A, or --auth-local and --auth-host, the next time you run initdb.
syncing data to disk ... ok


Success. You can now start the database server using:

    pg_ctl -D /var/lib/postgresql/data -l logfile start

waiting for server to start....2026-02-28 07:59:10.312 UTC [41] LOG:  starting PostgreSQL 15.17 on aarch64-unknown-linux-musl, compiled by gcc (Alpine 15.2.0) 15.2.0, 64-bit
2026-02-28 07:59:10.312 UTC [41] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-02-28 07:59:10.314 UTC [44] LOG:  database system was shut down at 2026-02-28 07:59:10 UTC
2026-02-28 07:59:10.315 UTC [41] LOG:  database system is ready to accept connections
 done
server started

/usr/local/bin/docker-entrypoint.sh: ignoring /docker-entrypoint-initdb.d/*

waiting for server to shut down....2026-02-28 07:59:10.417 UTC [41] LOG:  received fast shutdown request
2026-02-28 07:59:10.418 UTC [41] LOG:  aborting any active transactions
2026-02-28 07:59:10.420 UTC [41] LOG:  background worker "logical replication launcher" (PID 47) exited with exit code 1
2026-02-28 07:59:10.420 UTC [42] LOG:  shutting down
2026-02-28 07:59:10.420 UTC [42] LOG:  checkpoint starting: shutdown immediate
2026-02-28 07:59:10.423 UTC [42] LOG:  checkpoint complete: wrote 3 buffers (0.0%); 0 WAL file(s) added, 0 removed, 0 recycled; write=0.002 s, sync=0.001 s, total=0.004 s; sync files=2, longest=0.001 s, average=0.001 s; distance=0 kB, estimate=0 kB
2026-02-28 07:59:10.425 UTC [41] LOG:  database system is shut down
 done
server stopped

PostgreSQL init process complete; ready for start up.

2026-02-28 07:59:10.536 UTC [1] LOG:  starting PostgreSQL 15.17 on aarch64-unknown-linux-musl, compiled by gcc (Alpine 15.2.0) 15.2.0, 64-bit
2026-02-28 07:59:10.536 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
2026-02-28 07:59:10.536 UTC [1] LOG:  listening on IPv6 address "::", port 5432
2026-02-28 07:59:10.537 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-02-28 07:59:10.539 UTC [55] LOG:  database system was shut down at 2026-02-28 07:59:10 UTC
2026-02-28 07:59:10.541 UTC [1] LOG:  database system is ready to accept connections



## Stop + Restart

pg-prework
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
CONTAINER ID   IMAGE                 COMMAND                  CREATED          STATUS                              PORTS     NAMES
c2a3cf3c4938   hello-world           "/hello"                 4 minutes ago    Exited (0) 4 minutes ago                      awesome_murdock
aa84a3cefa68   postgres:15-alpine    "docker-entrypoint.s…"   10 minutes ago   Exited (0) Less than a second ago             pg-prework
92909f830dfd   hello-world           "/hello"                 11 minutes ago   Exited (0) 11 minutes ago                     practical_bell
e2dd3702b296   hello-world           "/hello"                 5 days ago       Exited (0) 5 days ago                         serene_wescoff
dd9eccb680e9   redis:alpine          "docker-entrypoint.s…"   5 weeks ago      Exited (0) 5 weeks ago                        docker-redis-1
ee2f78b64368   frappe/bench:latest   "bash /workspace/ini…"   5 weeks ago      Exited (1) 5 weeks ago                        docker-frappe-1
f7df4cdf478a   mariadb:10.8          "docker-entrypoint.s…"   5 weeks ago      Exited (0) 5 weeks ago                        docker-mariadb-1
pg-prework
CONTAINER ID   IMAGE                COMMAND                  CREATED          STATUS                  PORTS                                         NAMES
aa84a3cefa68   postgres:15-alpine   "docker-entrypoint.s…"   10 minutes ago   Up Less than a second   0.0.0.0:5432->5432/tcp, [::]:5432->5432/tcp   pg-prework
The files belonging to this database system will be owned by user "postgres".
This user must also own the server process.

The database cluster will be initialized with locale "en_US.utf8".
The default database encoding has accordingly been set to "UTF8".
The default text search configuration will be set to "english".

Data page checksums are disabled.

fixing permissions on existing directory /var/lib/postgresql/data ... ok
creating subdirectories ... ok
selecting dynamic shared memory implementation ... posix
selecting default max_connections ... 100
selecting default shared_buffers ... 128MB
selecting default time zone ... UTC
creating configuration files ... ok
running bootstrap script ... ok
sh: locale: not found
2026-02-28 07:59:10.120 UTC [35] WARNING:  no usable system locales were found
performing post-bootstrap initialization ... ok
initdb: warning: enabling "trust" authentication for local connections
initdb: hint: You can change this by editing pg_hba.conf or using the option -A, or --auth-local and --auth-host, the next time you run initdb.
syncing data to disk ... ok


Success. You can now start the database server using:

    pg_ctl -D /var/lib/postgresql/data -l logfile start

waiting for server to start....2026-02-28 07:59:10.312 UTC [41] LOG:  starting PostgreSQL 15.17 on aarch64-unknown-linux-musl, compiled by gcc (Alpine 15.2.0) 15.2.0, 64-bit
2026-02-28 07:59:10.312 UTC [41] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-02-28 07:59:10.314 UTC [44] LOG:  database system was shut down at 2026-02-28 07:59:10 UTC
2026-02-28 07:59:10.315 UTC [41] LOG:  database system is ready to accept connections
 done
server started

/usr/local/bin/docker-entrypoint.sh: ignoring /docker-entrypoint-initdb.d/*

waiting for server to shut down....2026-02-28 07:59:10.417 UTC [41] LOG:  received fast shutdown request
2026-02-28 07:59:10.418 UTC [41] LOG:  aborting any active transactions
2026-02-28 07:59:10.420 UTC [41] LOG:  background worker "logical replication launcher" (PID 47) exited with exit code 1
2026-02-28 07:59:10.420 UTC [42] LOG:  shutting down
2026-02-28 07:59:10.420 UTC [42] LOG:  checkpoint starting: shutdown immediate
2026-02-28 07:59:10.423 UTC [42] LOG:  checkpoint complete: wrote 3 buffers (0.0%); 0 WAL file(s) added, 0 removed, 0 recycled; write=0.002 s, sync=0.001 s, total=0.004 s; sync files=2, longest=0.001 s, average=0.001 s; distance=0 kB, estimate=0 kB
2026-02-28 07:59:10.425 UTC [41] LOG:  database system is shut down
 done
server stopped

PostgreSQL init process complete; ready for start up.

2026-02-28 07:59:10.536 UTC [1] LOG:  starting PostgreSQL 15.17 on aarch64-unknown-linux-musl, compiled by gcc (Alpine 15.2.0) 15.2.0, 64-bit
2026-02-28 07:59:10.536 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
2026-02-28 07:59:10.536 UTC [1] LOG:  listening on IPv6 address "::", port 5432
2026-02-28 07:59:10.537 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-02-28 07:59:10.539 UTC [55] LOG:  database system was shut down at 2026-02-28 07:59:10 UTC
2026-02-28 07:59:10.541 UTC [1] LOG:  database system is ready to accept connections
2026-02-28 08:01:00.136 UTC [1] LOG:  received fast shutdown request
2026-02-28 08:01:00.137 UTC [1] LOG:  aborting any active transactions
2026-02-28 08:01:00.139 UTC [1] LOG:  background worker "logical replication launcher" (PID 58) exited with exit code 1
2026-02-28 08:01:00.139 UTC [53] LOG:  shutting down
2026-02-28 08:01:00.139 UTC [53] LOG:  checkpoint starting: shutdown immediate
2026-02-28 08:01:00.146 UTC [53] LOG:  checkpoint complete: wrote 43 buffers (0.3%); 0 WAL file(s) added, 0 removed, 0 recycled; write=0.002 s, sync=0.003 s, total=0.008 s; sync files=11, longest=0.002 s, average=0.001 s; distance=252 kB, estimate=252 kB
2026-02-28 08:01:00.148 UTC [1] LOG:  database system is shut down

PostgreSQL Database directory appears to contain a database; Skipping initialization

2026-02-28 08:01:18.362 UTC [1] LOG:  starting PostgreSQL 15.17 on aarch64-unknown-linux-musl, compiled by gcc (Alpine 15.2.0) 15.2.0, 64-bit
2026-02-28 08:01:18.362 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
2026-02-28 08:01:18.362 UTC [1] LOG:  listening on IPv6 address "::", port 5432
2026-02-28 08:01:18.363 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-02-28 08:01:18.365 UTC [29] LOG:  database system was shut down at 2026-02-28 08:01:00 UTC
2026-02-28 08:01:18.367 UTC [1] LOG:  database system is ready to accept connections
2026-02-28 08:06:18.467 UTC [27] LOG:  checkpoint starting: time
2026-02-28 08:06:18.475 UTC [27] LOG:  checkpoint complete: wrote 3 buffers (0.0%); 0 WAL file(s) added, 0 removed, 0 recycled; write=0.002 s, sync=0.001 s, total=0.009 s; sync files=2, longest=0.001 s, average=0.001 s; distance=0 kB, estimate=0 kB
2026-02-28 08:09:34.225 UTC [1] LOG:  received fast shutdown request
2026-02-28 08:09:34.225 UTC [1] LOG:  aborting any active transactions
2026-02-28 08:09:34.227 UTC [1] LOG:  background worker "logical replication launcher" (PID 32) exited with exit code 1
2026-02-28 08:09:34.227 UTC [27] LOG:  shutting down
2026-02-28 08:09:34.228 UTC [27] LOG:  checkpoint starting: shutdown immediate
2026-02-28 08:09:34.230 UTC [27] LOG:  checkpoint complete: wrote 0 buffers (0.0%); 0 WAL file(s) added, 0 removed, 0 recycled; write=0.001 s, sync=0.001 s, total=0.003 s; sync files=0, longest=0.000 s, average=0.000 s; distance=0 kB, estimate=0 kB
2026-02-28 08:09:34.232 UTC [1] LOG:  database system is shut down

PostgreSQL Database directory appears to contain a database; Skipping initialization

2026-02-28 08:09:34.527 UTC [1] LOG:  starting PostgreSQL 15.17 on aarch64-unknown-linux-musl, compiled by gcc (Alpine 15.2.0) 15.2.0, 64-bit
2026-02-28 08:09:34.527 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
2026-02-28 08:09:34.527 UTC [1] LOG:  listening on IPv6 address "::", port 5432
2026-02-28 08:09:34.529 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-02-28 08:09:34.531 UTC [29] LOG:  database system was shut down at 2026-02-28 08:09:34 UTC
2026-02-28 08:09:34.533 UTC [1] LOG:  database system is ready to accept connections