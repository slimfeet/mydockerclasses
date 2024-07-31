slimfeet@DESKTOP-I9NO7VH:~$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED         SIZE
mysql         latest    31ebb0b19998   4 weeks ago     586MB
nginx         alpine    099a2d701db1   5 weeks ago     43.2MB
hello-world   latest    d2c94e258dcb   15 months ago   13.3kB
slimfeet@DESKTOP-I9NO7VH:~$ docker rmi nginx
Error response from daemon: No such image: nginx:latest
slimfeet@DESKTOP-I9NO7VH:~$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED         SIZE
mysql         latest    31ebb0b19998   4 weeks ago     586MB
nginx         alpine    099a2d701db1   5 weeks ago     43.2MB
hello-world   latest    d2c94e258dcb   15 months ago   13.3kB
slimfeet@DESKTOP-I9NO7VH:~$ docker rmi alpine
Error response from daemon: No such image: alpine:latest
slimfeet@DESKTOP-I9NO7VH:~$ docker rmi alpine:latest
Error response from daemon: No such image: alpine:latest
slimfeet@DESKTOP-I9NO7VH:~$ docker status
docker: 'status' is not a docker command.
See 'docker --help'
slimfeet@DESKTOP-I9NO7VH:~$ docker --status
unknown flag: --status
See 'docker --help'.

Usage:  docker [OPTIONS] COMMAND

A self-sufficient runtime for containers

Common Commands:
  run         Create and run a new container from an image
  exec        Execute a command in a running container
  ps          List containers
  build       Build an image from a Dockerfile
  pull        Download an image from a registry
  push        Upload an image to a registry
  images      List images
  login       Log in to a registry
  logout      Log out from a registry
  search      Search Docker Hub for images
  version     Show the Docker version information
  info        Display system-wide information

Management Commands:
  builder     Manage builds
  buildx*     Docker Buildx
  compose*    Docker Compose
  container   Manage containers
  context     Manage contexts
  image       Manage images
  manifest    Manage Docker image manifests and manifest lists
  network     Manage networks
  plugin      Manage plugins
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes

Swarm Commands:
  swarm       Manage Swarm

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  import      Import the contents from a tarball to create a filesystem image
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  wait        Block until one or more containers stop, then print their exit codes

Global Options:
      --config string      Location of client config files (default "/home/slimfeet/.docker")
  -c, --context string     Name of the context to use to connect to the daemon (overrides DOCKER_HOST env var and
                           default context set with "docker context use")
  -D, --debug              Enable debug mode
  -H, --host list          Daemon socket to connect to
  -l, --log-level string   Set the logging level ("debug", "info", "warn", "error", "fatal") (default "info")
      --tls                Use TLS; implied by --tlsverify
      --tlscacert string   Trust certs signed only by this CA (default "/home/slimfeet/.docker/ca.pem")
      --tlscert string     Path to TLS certificate file (default "/home/slimfeet/.docker/cert.pem")
      --tlskey string      Path to TLS key file (default "/home/slimfeet/.docker/key.pem")
      --tlsverify          Use TLS and verify the remote
  -v, --version            Print version information and quit

Run 'docker COMMAND --help' for more information on a command.

For more help on how to use Docker, head to https://docs.docker.com/go/guides/

slimfeet@DESKTOP-I9NO7VH:~$ docker --version
Docker version 27.0.3, build 7d4bcd8
slimfeet@DESKTOP-I9NO7VH:~$ sudo systemctl start docker
[sudo] password for slimfeet:
System has not been booted with systemd as init system (PID 1). Can't operate.
Failed to connect to bus: Host is down
slimfeet@DESKTOP-I9NO7VH:~$ sudo service docker start
Starting Docker: dockerslimfeet@DESKTOP-I9NO7VH:~$
slimfeet@DESKTOP-I9NO7VH:~$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED         SIZE
mysql         latest    31ebb0b19998   4 weeks ago     586MB
nginx         alpine    099a2d701db1   5 weeks ago     43.2MB
hello-world   latest    d2c94e258dcb   15 months ago   13.3kB
slimfeet@DESKTOP-I9NO7VH:~$ docker rmi nginx:alpine
Untagged: nginx:alpine
Untagged: nginx@sha256:a45ee5d042aaa9e81e013f97ae40c3dda26fbe98f22b6251acdf28e579560d55
Deleted: sha256:099a2d701db1f36dcc012419be04b7da299f48b4d2054fa8ab51e7764891e233
Deleted: sha256:db940ac5a279183401030c66787c5f36024bde0b89740fc15606e06dea0e7eec
Deleted: sha256:9bf69dac0ddcfe083a7145d426ebfaab10ed8080f8c2322e3a22bed2fdd1deaa
Deleted: sha256:5cde09e337a3cdadae5ad5afe11ad66db7beb4baa2c0e703099ebcd5c6ebbf85
Deleted: sha256:894db6797e5b3fda00ee6150cdd898b11cc560c4894cab95fc2461f35e636a62
Deleted: sha256:2f1b47358450451168cd3ec511726c9cca8f1327b6fb1bed822b9e09faa77438
Deleted: sha256:84dda86f2dcf4fa728ec391284d193aeca0260d752a53e7fd666316bcad4c3d3
Deleted: sha256:1db3b2c8f8e323b6817967ea81ad535c45e19087f7bf63b2004491d39d71cb8b
Deleted: sha256:af9a70194aa4d12f967dbd4bcb1ce9c98ba42adb4ec05536080fd4560155e809
slimfeet@DESKTOP-I9NO7VH:~$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED         SIZE
mysql         latest    31ebb0b19998   4 weeks ago     586MB
hello-world   latest    d2c94e258dcb   15 months ago   13.3kB
slimfeet@DESKTOP-I9NO7VH:~$ docker pull nginx:alpine
alpine: Pulling from library/nginx
46b060cc2620: Pull complete
21af147d2ad5: Pull complete
b3ee43e51ca6: Pull complete
b17a9d410da1: Pull complete
542e3e75411d: Pull complete
2b2faad386df: Pull complete
a5e22afba545: Pull complete
fb923a41dc10: Pull complete
Digest: sha256:208b70eefac13ee9be00e486f79c695b15cef861c680527171a27d253d834be9
Status: Downloaded newer image for nginx:alpine
docker.io/library/nginx:alpine
slimfeet@DESKTOP-I9NO7VH:~$ docker run -d nginx:alpine
42d78f14ef8d8be03931049db37a21ad1d3c2fdd6f35f23ed4ea654bb6ee9a0e
slimfeet@DESKTOP-I9NO7VH:~$ docker ps -l
CONTAINER ID   IMAGE          COMMAND                  CREATED         STATUS         PORTS     NAMES
42d78f14ef8d   nginx:alpine   "/docker-entrypoint.…"   8 seconds ago   Up 6 seconds   80/tcp    nice_goodall
slimfeet@DESKTOP-I9NO7VH:~$ docker rm nginx:alpine
Error response from daemon: No such container: nginx:alpine
slimfeet@DESKTOP-I9NO7VH:~$ docker rm 42d78f14ef8d
Error response from daemon: cannot remove container "/nice_goodall": container is running: stop the container before removing or force remove
slimfeet@DESKTOP-I9NO7VH:~$ docker rm -f 42d78f14ef8d
42d78f14ef8d
slimfeet@DESKTOP-I9NO7VH:~$ docker ps -a
CONTAINER ID   IMAGE         COMMAND    CREATED       STATUS                   PORTS     NAMES
ae9cfb7a2341   hello-world   "/hello"   4 days ago    Exited (0) 4 days ago              gifted_ptolemy
23ca8f6a68f4   hello-world   "/hello"   3 weeks ago   Exited (0) 3 weeks ago             intelligent_lehmann
slimfeet@DESKTOP-I9NO7VH:~$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED         SIZE
mysql         latest    31ebb0b19998   4 weeks ago     586MB
nginx         alpine    1ae23480369f   5 weeks ago     43.2MB
hello-world   latest    d2c94e258dcb   15 months ago   13.3kB
slimfeet@DESKTOP-I9NO7VH:~$ docker rmi nginx:alpine
Untagged: nginx:alpine
Untagged: nginx@sha256:208b70eefac13ee9be00e486f79c695b15cef861c680527171a27d253d834be9
Deleted: sha256:1ae23480369fa4139f6dec668d7a5a941b56ea174e9cf75e09771988fe621c95
Deleted: sha256:e0b206babc95f62cc88e4e8ace229b91819f790cda567e7926ca7e86326a5a70
Deleted: sha256:9b5b63f8f415e476a3428cb83219d57b614f25958d66943826ee4968c4bdc438
Deleted: sha256:1d7825e0074f589ee355fc1c2b9d6a951071ce13ff9d0622f44830afbfafa1f0
Deleted: sha256:02cd8aed4902e8f9cbe70f8ad383b7786b17df62bc596e4eaeed3fa5249848f7
Deleted: sha256:6ac01d1ffbf6d738d83a6cebf87871d2ef56d7a88aeded0b874e2635416db34c
Deleted: sha256:dd96251d38382802fb46416aac65b4a974a8caaf69e580ad7e5b9315a429ea25
Deleted: sha256:f58097011f75c975169b2ea1fa4ae8fd0883e199b91d763e64f732e7433c135b
Deleted: sha256:b895814e9e6408217eb0bf6d743ed1a1e2b7273a6b3ff66405b7a9c977a0c8e4
slimfeet@DESKTOP-I9NO7VH:~$ docker run -d nginx:alpine
Unable to find image 'nginx:alpine' locally
alpine: Pulling from library/nginx
46b060cc2620: Pull complete
21af147d2ad5: Pull complete
b3ee43e51ca6: Pull complete
b17a9d410da1: Pull complete
542e3e75411d: Pull complete
2b2faad386df: Pull complete
a5e22afba545: Pull complete
fb923a41dc10: Pull complete
Digest: sha256:208b70eefac13ee9be00e486f79c695b15cef861c680527171a27d253d834be9
Status: Downloaded newer image for nginx:alpine
c7067d9ffc6917a314ae59d33c0c43481cd49a8e1688316ac71974de98ddf297
slimfeet@DESKTOP-I9NO7VH:~$ docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED              STATUS              PORTS     NAMES
c7067d9ffc69   nginx:alpine   "/docker-entrypoint.…"   About a minute ago   Up About a minute   80/tcp    amazing_spence
slimfeet@DESKTOP-I9NO7VH:~$ docker rm -f docker-entrypoint
Error response from daemon: No such container: docker-entrypoint
slimfeet@DESKTOP-I9NO7VH:~$ docker rm -f c7067d9ffc69
c7067d9ffc69
slimfeet@DESKTOP-I9NO7VH:~$ docker run -d -p 9090:80 nginx:alpine
74ecc8cc4c41f7d650bac7c5abc5a7b24df04fd9437ee59caac2a59d7f4b628b
slimfeet@DESKTOP-I9NO7VH:~$ docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS         PORTS                                   NAMES
74ecc8cc4c41   nginx:alpine   "/docker-entrypoint.…"   10 seconds ago   Up 8 seconds   0.0.0.0:9090->80/tcp, :::9090->80/tcp   zen_khayyam
slimfeet@DESKTOP-I9NO7VH:~$
