---
layout: default
---
## Ubuntu installation

***When trying these instructions, remember to use 'sudo' before commands if your user doesn't 
have administrator access to the shell.**

### 1. Install Docker and Docker-Compose

If you haven't done so already, the first step is to install Docker (more information on 
[Docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/)):

```
apt-get remove docker docker-engine docker.io
apt-get update
apt-get install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
apt-key fingerprint 0EBFCD88
add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
apt-get update
apt-get install docker-ce
```

Next, install Docker-compose (more information on [Docker-compose](https://github.com/docker/compose/releases)):


```
curl -L https://github.com/docker/compose/releases/download/1.20.0-rc1/docker-compose-`uname -s`-`uname -m` \
  -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```

Now you are ready to install the Bitagora node containers.

### 2. Download and run the Bitagora Node installation script

You can download the installation script bitagora-node-ubuntu.sh from the [Bitagora-node repo](https://github.com/Bitagora/bitagora-node) and run the following command:

```
bash bitagora-node-ubuntu.sh install
```

Alternatively, use the following instruction to download and run the installation script directly:

```
curl -o- https://raw.githubusercontent.com/Bitagora/bitagora-node/master/download/bitagora-node-ubuntu.sh | bash install
```

The installation script will check that your system has Docker installed and will get its external IP
to customize the configuration of the node. It will also check if you have a firewall. In order to
run a Bitagora node you need to open ports 8801 (used by validators to communicate between them) and 8008 
(used by the REST-API to communicate with clients). Both of these ports should be available. 
If you have any firewall set up in your computer, please make sure the ports are accessible for remote tcp
connections. 

The installation script will then download the configuration files and run:

```
docker-compose up
```

This will automatically install and run all Bitagora-Sawtooth components in different docker containers. 
The installation will daemonize the node, so that the containers will continue to run in the background 
even if you close the terminal. 

All the files installed in the process are open-source and can be reviewed in this repo or in hyperledger/sawtooth 
repo.

## Troubleshooting 

### Check status of Bitagora node containers

From the commmand line, run:

```
bash bitagora-node-ubuntu.sh status
```

### Stop all Bitagora node containers

To stop all containers running the node components, use the following instruction from the
commmand line:

```
bash bitagora-node-ubuntu.sh stop
```

### Restart all Bitagora node containers

To restart all containers running the node components, use the following instruction from the
commmand line:

```
bash bitagora-node-ubuntu.sh restart
```

### Uninstall Bitagora node 

To uninstall the Bitagora node, run:

```
bash bitagora-node-ubuntu.sh uninstall
``` 

[back](./validator.md)

