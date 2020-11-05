# Container image: Fedora Ansible

[![Build Status](https://travis-ci.com/chzerv/docker-fedora-ansible.svg?branch=30)](https://travis-ci.com/chzerv/docker-fedora-ansible)

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
2. Each branch represents a tag (version). Clone the branch you're interested in. E.g., `git clone --branch=30 https://github.com/chzerv/docker-fedora-ansible.git`.
3. `cd` into the directory and run `docker build -t fedora30-ansible`

# How to use

1. Install [Docker](https://docs.docker.com/engine/install/) or [Podman](https://podman.io/getting-started/installation.html).
2. Pull this image from _Docker hub_: `docker pull chzerv/docker-fedora-ansible:30`. Remember, the tag represents the distribution version, so change it according to your needs.
3. Run a container:

   ```shell
   docker run -d --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro docker-fedora-ansible:30
   ```

4. Run Ansible inside that container:

   ```shell
   docker exec -it $container_id ansible --version
   ```
