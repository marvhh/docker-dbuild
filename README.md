# docker-dbuild
A debian package build environment with docker this is meant to be a simple pbuilder replacement

# usage

```bash
# clone

# build docker image
docker build -t="debian-build" .

# source aliases and function into bash
source docker_aliases

# this will stop -> reset -> start the container named 'debian-build'
# and bind your current directory into the container under /development (read-only)
# and tries to binary build your package in /tmp/dev
docker_debian_build_all

# you can connect to your running instance with
docker_debian_exec bash
```
