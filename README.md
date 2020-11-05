# Container image: Fedora Ansible

[![Build Status](https://travis-ci.com/chzerv/docker-fedora-ansible.svg?branch=master)](https://travis-ci.com/chzerv/docker-fedora-ansible)
![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/chzerv/docker-fedora-ansible)

This Dockerfile builds a Fedora-based container with Ansible and other Ansible testing tools pre-intalled.

# Branches/Tags

| Branch | Distribution version | Image tag |
| :----: | :------------------: | :-------: |
| master |          33          |  latest   |
|   32   |          32          |    32     |
|   31   |          31          |    31     |
|   30   |          30          |    30     |

# How to build locally

1. Install [Docker](https://docs.docker.com/engine/install/) or [Podman](https://podman.io/getting-started/installation.html).
2. Each branch represents a tag (version), with the `master` branch being the latest version. Clone the branch you're interested in. E.g., for fedora32: `git clone --branch=32 https://github.com/chzerv/docker-fedora-ansible.git`.
3. `cd` into the directory and run `docker build -t fedora32-ansible`

# How to use

1. Install [Docker](https://docs.docker.com/engine/install/) or [Podman](https://podman.io/getting-started/installation.html).
2. Pull this image from _Docker hub_: `docker pull chzerv/docker-fedora-ansible:latest`. Remember, the tag represents the distribution version, so change it according to your needs.
3. Run a container:

   ```shell
   docker run -d --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro docker-fedora-ansible:latest
   ```

4. Run Ansible inside that container:

   ```shell
   docker exec -it $container_id ansible --version
   ```
