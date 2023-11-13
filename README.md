# Assignment1-Part2
First Assignment Part2 Attempt

1.	Create Container
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker run assign1:1.0
INFO:     Started server process [1]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Uvicorn running on http://0.0.0.0:2010 (Press CTRL+C to quit)

2.	Docker PS
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker ps
CONTAINER ID   IMAGE         COMMAND            CREATED         STATUS         PORTS                    NAMES
1034011778d2   assign1:1.0   "python main.py"   6 seconds ago   Up 4 seconds                            hungry_wozniak
d2871e2e9ff4   assign1:1.0   "python main.py"   6 hours ago     Up 6 hours     0.0.0.0:2010->2010/tcp   1st_assign

3.	Docker Logs
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker logs 1st_assign
INFO:     Started server process [1]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Uvicorn running on http://0.0.0.0:2010 (Press CTRL+C to quit)
INFO:     172.17.0.1:52136 - "GET /count HTTP/1.1" 200 OK
INFO:     172.17.0.1:52136 - "GET /count HTTP/1.1" 200 OK
INFO:     172.17.0.1:52136 - "GET /docs HTTP/1.1" 200 OK
INFO:     172.17.0.1:52136 - "GET /openapi.json HTTP/1.1" 200 OK

4.	Docker Inspect 
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker inspect assign1:1.0
[
    {
        "Id": "sha256:b0e0301f15a1279f72fdf1125f9cb06c422229562a3144d0bd6bf5c9fdb01f91",
        "RepoTags": [
            "dockerassign/assign1:1.0",
            "assign1:1.0"
        ],
        "RepoDigests": [],
        "Parent": "",
        "Comment": "buildkit.dockerfile.v0",
        "Created": "2023-11-12T09:32:47.283664011Z",
        "Container": "",
        "ContainerConfig": {
            "Hostname": "",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": null,
            "Cmd": null,
            "Image": "",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": null
        },
        "DockerVersion": "",
        "Author": "",
        "Config": {
            "Hostname": "",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "LANG=C.UTF-8",
                "GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305",
                "PYTHON_VERSION=3.12.0",
                "PYTHON_PIP_VERSION=23.2.1",
                "PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c6add47b0abf67511cdfb4734771cbab403af062/public/get-pip.py",
                "PYTHON_GET_PIP_SHA256=22b849a10f86f5ddf7ce148ca2a31214504ee6c83ef626840fde6e5dcd809d11"
            ],
            "Cmd": null,
            "ArgsEscaped": true,
            "Image": "",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "python",
                "main.py"
            ],
            "OnBuild": null,
            "Labels": null
        },
        "Architecture": "amd64",
        "Os": "linux",
        "Size": 1045136771,
        "VirtualSize": 1045136771,
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/zaluh0p0alvn44drktwqxzoa8/diff:/var/lib/docker/overlay2/nj7s3syt5vtehe9bbyjx7f2ok/diff:/var/lib/docker/overlay2/e5122d877d108c3d11e2b4466cdd39ed8de5380bb655a0cd02b0342cccbde6d2/diff:/var/lib/docker/overlay2/671787fdb737e81905661d372382e8144c532bd37ff65d707744c7773648ef78/diff:/var/lib/docker/overlay2/d156eb351deb8f3db66f4bfd4ba3638137e71e7fc48203f34c45733161b2dce8/diff:/var/lib/docker/overlay2/30429d423cd409cf4e46fffa12a1ec28e1929e7253d5b499e309e6a1b9e4b46a/diff:/var/lib/docker/overlay2/70a0a6282cdceeb0cfcb4b481f5c5221f769f9f4b8ede924b946307393e4eca6/diff:/var/lib/docker/overlay2/739b4af0dad4043ca9c3397c45c518c3ed4caf0679232ab4e03c0239685ed59e/diff:/var/lib/docker/overlay2/57bc958111c0b5b4daff3ddea71d3318ac92ba076bc63acfedaa9a9ec769662e/diff:/var/lib/docker/overlay2/80d5a25f8f52f8423dcfabf08855476e308dbc817e0ab2f9a516cc6b82f17324/diff",
                "MergedDir": "/var/lib/docker/overlay2/isau7k38dzag71kgudog8qdyh/merged",
                "UpperDir": "/var/lib/docker/overlay2/isau7k38dzag71kgudog8qdyh/diff",
                "WorkDir": "/var/lib/docker/overlay2/isau7k38dzag71kgudog8qdyh/work"
            },
            "Name": "overlay2"
        },
        "RootFS": {
            "Type": "layers",
            "Layers": [
                "sha256:1777ac7d307bcbda4fe79323a921eda8d39d97513677ecda31b82244e7876520",
                "sha256:29e49b59edda8f520e3289a0df2f1aedc8c6774212c2b430359c9603310a3838",
                "sha256:266def75d28e675320db1c5d2870ff3ed8f2e7a78537a35fe495fbff6baa9dc7",
                "sha256:12b956927ba2b8fd3b59cd4db0f17068758e60eeb710ed307a0b006ddbf290b5",
                "sha256:86e50e0709eebc0f2f9de74341dd7330faa7cfe38a28d2cb2549d9b4629892f5",
                "sha256:ac630c4fd9602de2d6c99123caadba88885101582787ec1df5b2edee59834db2",
                "sha256:619584b251c8772c9d769a0fe95991e66785da834933e9ee9e49572422013cf3",
                "sha256:701d0b971f5f2c26b39eef7be204ffb84e491270a2181c115f952a1573f9e024",
                "sha256:8235090ff47b73432be41e348a0aec9d481962d2b45c639f33817e8dbf888c80",
                "sha256:034114ed35a435527d2c493df2dbb57576596c39feb57a6529d7f8ee2bc6b5a8",
                "sha256:ebe5b80a833eec80f2c4a0dd3671d4cdeaa0e78fce1e8f9beb221bc27822b5b0"
            ]
        },
        "Metadata": {
            "LastTagTime": "2023-11-12T10:49:16.990387996Z"
        }
    }
]

5.	Docker Exec
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1> docker exec -d hungry_wozniak touch /tmp/execWorks

6.	Docker Commit
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker commit d2871e2e9ff4  svendowideit/testimage:version3 sha256:39828326d10ad1145f8d159dd3dc408c1f72425a3c7e3668730b798930957efa

7.	Docker Stop
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker stop 1st_assign
1st_assign

8.	Docker Stats
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker stats
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.02%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.02%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.26%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.26%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.23%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.23%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.38%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.38%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.32%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.32%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.31%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.31%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.35%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.35%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.27%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.27%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.29%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.29%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.28%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.28%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1
CONTAINER ID   NAME                  CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O   PIDS
063ec4061f1c   exciting_williamson   0.29%     35.67MiB / 3.713GiB   0.94%     1.16kB / 0B   0B / 0B     1

9.	Docker Top
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker top exciting_williamson
UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                4367                4346                0                   16:48               ?                   00:00:02            python main.py

10.	Docker Start
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker start exciting_williamson

11.	Docker Pause
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker pause exciting_williamson
exciting_williamson

12.	Docker UnPause
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker unpause exciting_williamson
exciting_williamson

13.	Docker Rename
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker rename exciting_williamson my_assign1

14.	Docker Port
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker port my_assign1
2010/tcp -> 0.0.0.0:2010

15.	Docker Update
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker update --cpu-shares 512 my_assign1
my_assign1

16.	Docker Restart
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker restart my_assign1
my_assign1

17.	Docker Remove
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1>docker rm my_assign1
my_assign1

18.	Docker Copy
C:\Users\Hassan IPRI\Documents\DevOps Class lab\Assignment 1\Part1>docker cp ./copy.txt awesome_johnson:/bin/
Successfully copied 1.54kB to awesome_johnson:/bin/

