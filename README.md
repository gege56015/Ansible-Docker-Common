## Ansible-Docker-Common

This repo contains an Ansible role which is able to configure Docker into a desired default state on a host. The role included in this repo will perform the following actions:

(NOTE: only Ubuntu 16.04 is supported at this time)

* Install pre-requisite packages for Docker
* Add Docker's stable repository to apt
* Install Docker CE
* Optionally enable Docker's user namespace feature for added security
* Install Docker Compose

**Required Variables**

The role requires only one variable:

* enable_docker_namespaces

This variable should be fairly self-explanatory.


## How To Use:

**Import With Ansible Galaxy CLI**

There a few ways to do this. But perhaps the simplest is to include something like the following in your requirements.yml:

```
- src: https://github.com/gege56015/Ansible-Docker-Common.git
  version: master
```

And then call 'ansible-galaxy install -r requirements.yml'. Of course, you might need to adjust various settings such as destination path, etc. 

