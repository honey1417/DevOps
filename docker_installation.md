# docker install on CentOS 9

## Install Docker from the Official Docker Repository:

## Update the package list:
```bash
sudo dnf update -y
```
## Add Docker’s official repository:
```bash
sudo dnf config-manager --add-repo=https://download.docker.com/linux/centos/docker-ce.repo
```
## Install Docker:
```bash
sudo dnf install -y docker-ce docker-ce-cli containerd.io
```
## Start and Enable Docker:
```bash
sudo systemctl start docker
sudo systemctl enable docker
sudo systemctl status docker
```
## Verify Docker Installation:
```bash
docker --version
```
### Explanation:
docker-ce: Docker Community Edition, the upstream version of Docker.
containerd.io: A lightweight container runtime required by Docker.
