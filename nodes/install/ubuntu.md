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

### 2. Download the Bitagora Node script

You can download the installation script ``bitagora-node.sh`` from the [Bitagora Node repo](https://github.com/bitagora/bitagora-node) or running the following command from your terminal:

```
wget https://raw.githubusercontent.com/bitagora/bitagora-node/master/bitagora-node.sh
```

### 3. Run the Bitagora Node script

From the same directory, run the script:

```
bash bitagora-node.sh
```

This script needs to be run by the root user. You might need to type: `sudo bash bitagora-node.sh`. 

The script allows you to execute all operations necessary to install, uninstall, stop, restart and check the status
of a node. Select your chosen option using the interactive menu and follow the prompts.

#### Install

The script checks that your system has Docker installed and gets your external IP
to customize the configuration of the node. It will also check if you have a firewall. In order to
run a Bitagora node you need to open ports `8801` (used by validators to communicate between themselves) and `8008` 
(used by the REST-API to communicate with clients). Both of these ports should be accessible. 
If you have a firewall set up in your computer, please make sure the ports are accessible for remote tcp
connections before running the script. 

The installation script will then download the configuration files and run `docker-compose up`. This will 
automatically install and run all Bitagora-Sawtooth components in different docker containers. The installation 
script will ask you if you want to daemonize the node, so that the containers continue to run in the background 
even after you close the terminal. It is recommended that you answer 'yes' when prompted. Otherwise, the node will stop 
once you close your terminal.

All the files installed in the process are open-source and can be reviewed in the [Bitagora Node repo](https://github.com/bitagora/bitagora-node) or in the [Hyperledger/Sawtooth repo](https://github.com/hyperledger/sawtooth-core).

#### Status

The status option allows you to check the current status of the Bitagora Node containers installed in your system.

#### Stop

This option stops all containers running the node components. The containers are not removed and can be restarted
again with the same script.

#### Restart

To restart all the node components, use this option. Again, you will be prompted to confirm that you want to daemonize the node. It is recommended that you answer 'yes'.

#### Uninstall

Select this option to completely remove the validator node and uninstall Bitagora Node from your system. The script
will try to remove all the components automatically. If it encounters any errors, it will output the commands
you need to use to remove the components manually from the terminal. After all the components have been removed, you can
simply remove the script itself by running ``rm bitagora-node.sh`` from the same directory.

#### Shell

Select this option to enter a submenu that allows you to run the Bitagora-shell commands directly from the script. 
These commands can also be run from the shell. Follow the instructions in the [Usage](./validator.md#usage) section. 

[back](./validator.md)
