---
layout: default
---
# Bitagora-node validator

Bitagora-node is a distributed application to validate votes and maintain the Bitagora
blockchain voting system. Validator nodes play an indispensable role in sustaining reliable,
transparent and accountable voting processes without the need for any central
authority. This distributed application is free to install and runs on top of Hyperledger
Sawtooth.

## Contents

- [Components](#components)
- [Installation](#installation)
- [Usage](#usage)
- [Source code](#source-code)
- [Documentation](#documentation)
- [License](#license)

## Components

Running on top of the core components from Hyperledger Sawtooth, a Bitagora validator node
includes a number of elements to manage the Bitagora blockchain:

- Bitagora-polls-tp: a **transaction processor** which handles polls
- Bitagora-ballots-tp:  a **transaction processor** which handles incoming ballots
- Bitagora-settings-tp: a **transaction processor** which handles blockchain settings
- Bitagora-validator: a **Sawtooth validator** node linked to other nodes in the network
- Bitagora-rest-api: a **rest-api** that provides and received poll and ballot data from clients
- Bitagora-shell: a **shell** container with the dependencies to run Bitagora commands

## Installation

Since Bitagora nodes run on Docker containers, they can be installed on any Linux, Windows or Mac system 
that is able to run Docker. You can find more information about installing and running Docker in the [Docker](https://www.docker.com/what-docker) webpage.

Follow the installation and usage instructions for your system:

- [Ubuntu](./ubuntu.md)
- [Windows 10](./windows-10.md)
- [Mac](./mac.md)

## Usage

The different components will be installed in Docker containers. These containers 
communicate from the following ports, which should be left available:

- 8008 for REST-API communication with clients
- 4004 for Validator node internal components communication
- 8801 for Validator node network communication

### Shell commands

#### Access the shell

You can access the shell container by openning a terminal window and running:

Ubuntu:

```
docker exec -it bitagora-shell bash
```

Once inside the shell, you can try running the following commands to obtain data from your
validator node.

#### List all available polls

To get a list of all the polls stored in the Bitagora blockchain, including those
currently active and inactive:

```
bitagora list polls
```

#### Show poll information

To get detailed information on a particular poll, including a recount of
the total ballots cast and the results obtained by every available options, use
the following command. It requires an 8 digit alphanumerical Poll id as a single parameter.

```bash
bitagora show poll [pollId]
```

#### Check a ballot

This script will look for a specific vote ballot in the blockchain. It requires two parameters.
The first one is an 8 digit alphanumerical Poll id. The second one can be any of the two: 
the id of the vote or the private key obtained by the voter at the moment of registration.

```
bitagora show vote [pollId] [{voteId/privkey}]
```

#### View Bitagora blockchain blocks

From the shell you can list all the blocks in the blockchain with the following commmand:

```
bitagora list blocks
```

If you want to view a particular block in more detail, use:

```
bitagora show block [blockId] 
```

#### View Bitagora state

From the shell you can also list the current state of the blockchain:

```
bitagora list state
```

If you want to view the data stored in a particular address of the state, use:

```
bitagora show state [address]
```

#### View blockchain settings

You can also check the settings stored in the blockchain:

```
bitagora list settings
```

#### View peer nodes

To check which other nodes your machine is peered with, use:

```
bitagora list nodes
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

## Source code

The source code for the validator node software is available at
[Bitagora-node repo](https://github.com/Bitagora/bitagora-node).

## Documentation

The latest documentation for Hyperledger-Sawtooth is available in the
[sawtooth-core repo](https://github.com/hyperledger/sawtooth-core).

## License

Bitagora software is licensed under the [Apache License Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)
software license.