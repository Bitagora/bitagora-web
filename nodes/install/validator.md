---
layout: default
---
# Bitagora Node

![version](https://img.shields.io/badge/version-0.0.2-green.svg) 
![Hex.pm](https://img.shields.io/hexpm/l/plug.svg)


Bitagora Node is a distributed application to validate votes and maintain the Bitagora
blockchain voting system. Validator nodes play an indispensable role in sustaining reliable,
transparent and accountable voting processes without the need for any central
authority. This distributed application is free to install and runs on top of Hyperledger
Sawtooth.

## Contents

- [Components](#components)
- [Terms and conditions](#terms-and-conditions)
- [Installation](#installation)
- [Usage](#usage)
- [Support](#support)
- [Source code](#source-code)
- [Documentation](#documentation)
- [License](#license)

## Components

Running on top of the core components from Hyperledger Sawtooth, a Bitagora validator node
includes a number of elements to manage the Bitagora blockchain:

- polls-tp: a **transaction processor** which handles polls settings
- ballots-tp:  a **transaction processor** which handles ballots for polls
- settings-tp: a **transaction processor** which handles settings for the Bitagora blockchain
- poet-validator-registry-tp: a **transaction processor** which handles the registry of nodes on the PoET consensus network
- validator: a **Hyperledger/Sawtooth validator** node linked to other nodes in the Bitagora network
- rest-api: a **rest-api** that receives and provides poll and ballot data from clients
- shell: a **shell** container with the dependencies to run Bitagora commands to interact with the blockchain

## Terms and conditions

Before installing a Bitagora validator node in your system, you should read our [Terms of service](../../static/en/terms.md) and [Privacy policy](../../static/en/policy.md). By installing a node, you are expressly acknowledging and agreeing to the terms and conditions detailed in these documents.

## Installation

At the moment, Bitagora nodes can only be installed in Linux (Ubuntu) systems that are able to run Docker. 
You can find more information about installing and running Docker in the [Docker](https://www.docker.com/what-docker) webpage.

The following installation and usage instructions have only been tested for Ubuntu 16.04, but should work
for more recent distributions as well:

- [Ubuntu](./ubuntu.md)

## Usage

The different components will be installed in Docker containers. These containers communicate from the following ports, which should be left available:

- 8008 for REST-API communication with clients
- 4004 for Validator node internal components communication
- 8801 for Validator node network communication

### Shell commands

#### Access the shell

There are two ways to access the shell. 

The easiest way is to use the `bitagora-node.sh` script downloaded during installation. The UI in this script allows you to install, uninstall, stop, restart and check the status of your node. The script also includes a submenu option 'SHELL'. Enter this submenu to access all the functionalities of the shell without having to run any commands.

If you want more control, you can also access the shell container by openning a terminal window and running:

```
docker exec -it bitagora-shell bash
```

Once inside the shell, you can try running the following commands to obtain data from your validator node.

#### List all available polls

To get a list of all the polls stored in the Bitagora blockchain, including those currently active and inactive:

```
node shell.js list polls
```

#### Show poll information

To get detailed information on a particular poll, including a recount of the total ballots cast and the results obtained by every available options, use the following command. It requires an 8 digit alphanumerical Poll id as a single parameter.

```bash
node shell.js show poll [pollId]
```

#### Check a ballot

This script will look for a specific vote ballot in the blockchain. It requires two parameters.
The first one is an 8 digit alphanumerical Poll id. The second one can be any of the two: 
the id of the vote or the private key obtained by the voter at the moment of registration.

```
node shell.js show vote [pollId] [{voteId/privkey}]
```

#### View Bitagora blockchain blocks

From the shell you can list all the blocks in the blockchain with the following commmand:

```
node shell.js list blocks
```

If you want to view a particular block in more detail, use:

```
node shell.js show block [blockId] 
```

#### View Bitagora state

From the shell you can also list the current state of the blockchain:

```
node shell.js list state
```

If you want to view the data stored in a particular address of the state, use:

```
node shell.js show state [address]
```

#### View blockchain settings

You can also check the settings stored in the blockchain:

```
node shell.js list settings
```

#### View peer nodes

To check which other nodes your machine is peered with, use:

```
node shell.js list peers
```

#### Get node keys

From the shell, you can also access the keys used by your node. This command will output
the private key and the public key in that order.

```
cat /root/.sawtooth/keys/root.priv && cat /root/.sawtooth/keys/root.pub
```

#### Exit the shell

To exit the shell, you can simply run:

```
exit
```

## Support

Bitagora Node is open-source software. It is provided free of charge without
any guarantee of support. If you need help or assistance, please open an issue
in the [GitHub repo](https://github.com/Bitagora/bitagora-node/issues).

## Source code

The source code for the Bitagora Node software is available in the
[bitagora-node repo](https://github.com/bitagora/bitagora-node).

## Documentation

The latest documentation for Hyperledger/Sawtooth is available in the
[sawtooth-core repo](https://github.com/hyperledger/sawtooth-core).

## License

Bitagora Node is licensed under the [Apache License Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)
software license.

[back](../../.)
