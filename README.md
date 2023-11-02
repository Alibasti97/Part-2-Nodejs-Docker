# Part 2 Docker Container with Commands

## 1. Created a container using the command:
#### sudo docker run -d -p 8080:3000 --name dockercont-node 88493946db3f
## Output:
265795947bf7206e4fe73cfc5465888f137ed236462e725b7f8a0f278b196a30

## 2. Running the commands:

## 1. docker ps:
### Output:
CONTAINER ID   IMAGE          COMMAND                  CREATED              STATUS              PORTS                                       NAMES
265795947bf7   88493946db3f   "docker-entrypoint.s…"   About a minute ago   Up About a minute   0.0.0.0:8080->3000/tcp, :::8080->3000/tcp   dockercont-node

## 2. docker stats:
### Output:
CONTAINER ID   NAME              CPU %     MEM USAGE / LIMIT     MEM %     NET I/O           BLOCK I/O    PIDS
265795947bf7   dockercont-node   0.00%     6.184MiB / 949.7MiB   0.65%     8.01kB / 5.65kB   459kB / 0B   7

## 3. docker inspect 
### Output
[
    {
        "Id": "265795947bf7206e4fe73cfc5465888f137ed236462e725b7f8a0f278b196a30",
        "Created": "2023-11-02T07:22:03.5465098Z",
        "Path": "docker-entrypoint.sh",
        "Args": [
            "node",
            "app.js"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 4096,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2023-11-02T07:22:03.959805583Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:88493946db3fd4ffe84ae1018da9bb64333a1bfecaa8ab26b94f76b4cb52b085",
        "ResolvConfPath": "/var/lib/docker/containers/265795947bf7206e4fe73cfc5465888f137ed236462e725b7f8a0f278b196a30/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/265795947bf7206e4fe73cfc5465888f137ed236462e725b7f8a0f278b196a30/hostname",
        "HostsPath": "/var/lib/docker/containers/265795947bf7206e4fe73cfc5465888f137ed236462e725b7f8a0f278b196a30/hosts",
        "LogPath": "/var/lib/docker/containers/265795947bf7206e4fe73cfc5465888f137ed236462e725b7f8a0f278b196a30/265795947bf7206e4fe73cfc5465888f137ed236462e725b7f8a0f278b196a30-json.log",
        "Name": "/dockercont-node",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "default",
            "PortBindings": {
                "3000/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "8080"
                    }
                ]
            },
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "ConsoleSize": [
                43,
                211
            ],
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "private",
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": [],
            "BlkioDeviceWriteBps": [],
            "BlkioDeviceReadIOps": [],
            "BlkioDeviceWriteIOps": [],
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": null,
            "PidsLimit": null,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/79a59eb970297ab557ea1de43dcd92c3786ceb86bda35caffcc1d6d6fc3aa425-init/diff:/var/lib/docker/overlay2/20c275c40cb25f76bd67befe5ebeedd3a49e8114df91e7b14ebe3683b19fe74d/diff:/var/lib/docker/overlay2/5595d003b0c847b88ae5e510861d52916bf13e8f756c540abb81f18f3629a287/diff:/var/lib/docker/overlay2/5ec5159b926b0970fc7056b316dd9f75b0ba87b22644434dc56c11ca3e6414f1/diff:/var/lib/docker/overlay2/3e224967c312cadcd2cf3b9ef86439c8fd2aa8beb5f2cc4e93c38612abca6560/diff:/var/lib/docker/overlay2/61eeed791ae3e1e9e4f39a696d9b08d31d80a907e865be1f52ff0167bf18e12a/diff:/var/lib/docker/overlay2/2a8a33a7e0c625179c406b866ce4162b840f8cbd465772968f6f62befce2199c/diff:/var/lib/docker/overlay2/b5d48ffb683d1a35fe523bbe80f4d60b7c8f75e68703540d6a4bce0f242c0451/diff",
                "MergedDir": "/var/lib/docker/overlay2/79a59eb970297ab557ea1de43dcd92c3786ceb86bda35caffcc1d6d6fc3aa425/merged",
                "UpperDir": "/var/lib/docker/overlay2/79a59eb970297ab557ea1de43dcd92c3786ceb86bda35caffcc1d6d6fc3aa425/diff",
                "WorkDir": "/var/lib/docker/overlay2/79a59eb970297ab557ea1de43dcd92c3786ceb86bda35caffcc1d6d6fc3aa425/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "265795947bf7",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "3000/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "NODE_VERSION=14.21.3",
                "YARN_VERSION=1.22.19"
            ],
            "Cmd": [
                "node",
                "app.js"
            ],
            "Image": "88493946db3f",
            "Volumes": null,
            "WorkingDir": "/app",
            "Entrypoint": [
                "docker-entrypoint.sh"
            ],
            "OnBuild": null,
            "Labels": {}
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "2ead7cbddf6098ba3aadfc160c520f887f0c92f811c864b40cf292ef4bb5bb9a",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {
                "3000/tcp": [
                    {
                        "HostIp": "0.0.0.0",
                        "HostPort": "8080"
                    },
                    {
                        "HostIp": "::",
                        "HostPort": "8080"
                    }
                ]
            },
            "SandboxKey": "/var/run/docker/netns/2ead7cbddf60",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "6af647fdc8ee07aa6096d9c18a4d3ccda1275ca7687521847463d11f104e6e01",
            "Gateway": "172.17.0.1",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "172.17.0.2",
            "IPPrefixLen": 16,
            "IPv6Gateway": "",
            "MacAddress": "02:42:ac:11:00:02",
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "404307ab84cd9fc913cfa801c75eb407f111092da38afb5f6df2b913d98c7657",
                    "EndpointID": "6af647fdc8ee07aa6096d9c18a4d3ccda1275ca7687521847463d11f104e6e01",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.2",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "02:42:ac:11:00:02",
                    "DriverOpts": null
                }
            }
        }
    }
]

## 4. sudo docker logs 265795947bf7:
### Output:
Server running at http://0.0.0.0:8080/

## 5. sudo docker stop 265795947bf7
### Output
265795947bf7

## 6. sudo docker start 265795947bf7
### Output
265795947bf7

## 7. sudo docker pause 265795947bf7
### Output
265795947bf7

## 8. sudo docker unpause 265795947bf7
### Output
265795947bf7

## 9. sudo docker restart 265795947bf7
### Output
265795947bf7

## 10. sudo docker update --cpus 0.05 265795947bf7
### Output
265795947bf7

## 11. sudo docker port 265795947bf7
### Output
3000/tcp -> 0.0.0.0:8080
3000/tcp -> [::]:8080

## 12. sudo docker rename dockercont-node docker-nodejs
### Output
No output but the name was changed successfully when I checked using docker ps.

CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS         PORTS                                       NAMES
265795947bf7   88493946db3f   "docker-entrypoint.s…"   27 minutes ago   Up 6 minutes   0.0.0.0:8080->3000/tcp, :::8080->3000/tcp   docker-nodejs

## 13. sudo docker exec -i -t 265795947bf7 /bin/bash
### Output
I used this command to go inside the Docker Container directory.

ubuntu@ip-172-31-46-246:~$ sudo docker exec -i -t 265795947bf7 /bin/bash
root@265795947bf7:/app# ls
app.js

## 14. sudo docker attach 265795947bf7
### Output
I used this command to attach to the default shell of a running container.

## 15. sudo docker wait 265795947bf7
### Output
I used this command to wait for the given container to stop. Once the command stops it will print the exit code of the container.

## 16. sudo docker top 265795947bf7
### Output
UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                4549                4529                0                   07:42               ?                   00:00:00            node app.js

## 17. sudo docker commit 265795947bf7 docker_commit_image
### Output
sha256:204fc232d5b939800fcdafe38fc03f3bf2714fa7ab17de1fa771802506e1b38d
When I used docker ps, a new image was created with a name of docker_commit_image

REPOSITORY            TAG       IMAGE ID       CREATED              SIZE
docker_commit_image   latest    204fc232d5b9   About a minute ago   181MB
dockerimages          latest    88493946db3f   4 hours ago          181MB
hello-node            latest    88493946db3f   4 hours ago          181MB
node                  14-slim   7671819c5461   6 months ago         181MB

## 18. sudo docker cp 2.txt 265795947bf7:/app/file.txt
### Output
Successfully copied 1.54kB to 265795947bf7:/app/file.txt
I used this command to copy the 2.txt file inside the container in the app directory.

## 19. sudo docker rm -f 265795947bf7
### Output
265795947bf7