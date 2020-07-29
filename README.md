# Container image: Fedora Ansible

This Dockerfile builds a Fedora-based container with Ansible and other Ansible testing tools pre-intalled.

# Branches/Tags

| Branch | Distribution version | Image tag |
| :----: | :------------------: | :-------: |
| master |          32          |  latest   |
|   31   |          31          |    31     |
|   30   |          30          |    30     |

# How to build locally

1. Install [Docker](https://docs.docker.com/engine/install/) or [Podman](https://podman.io/getting-started/installation.html).
2. Each branch represents a tag (version). Clone the branch you're interested in. E.g., `git clone --branch=31 https://github.com/chzerv/docker-fedora-ansible.git`.
3. `cd` into the directory and run `docker build -t fedora31-ansible`

# How to use

1. Install [Docker](https://docs.docker.com/engine/install/) or [Podman](https://podman.io/getting-started/installation.html).
2. Pull this image from _Docker hub_: `docker pull chzerv/docker-fedora-ansible:31`. Remember, the tag represents the distribution version, so change it according to your needs.
3. Run a container:

   ```shell
   docker run -d --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro docker-fedora-ansible:31
   ```

4. Run Ansible inside that container:

   ```shell
   docker exec -it $container_id ansible --version
   ```
