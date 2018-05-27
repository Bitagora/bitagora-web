---
layout: default
---

## Privacy policy

### 1. Personal information
1.	Bitagora is committed to safeguarding the confidentiality and privacy of any private information you provide to the system when registering to vote with the Bitagora platform and software.
2.	This policy applies where Bitagora is acting as the data controller agent with respect to the registration data of polls conducted with the Bitagora system, that is, wherever Bitagora determines the purposes and means of the processing of that registration data. This includes data processed by any Bitagora controlled server as well as by client-based web and mobile voting booths.
3. This policy does not apply to any instance where a third party acts as the data controller agent with respect to the registration data of polls conducted with the Bitagora voting system or where the platform or the software has been forked or modified to be used under the available license by any third party.
4. Bitagora NEVER collects or saves your personal information anywhere. 
5. During the registration process, the Bitagora server will process your ID number, date of birth, name, and other data that you might provide when using the Bitagora web or mobile voting booth, in order to produce a unique registration identification number. This number is calculated automatically without any human intervention using a one-way cryptographic hashing algorithm. This algorithm ensures that 
  (a) no other user will ever have the same identification number for a given poll, and
  (b) no-one, not even the administrators of Bitagora's servers, will ever be able to retrace your private data based on the identification number produced.
6. Once calculated, the identification number is automatically sent back to the web or mobile booth processing your registration, together with a random personal private key and a cryptographic signature that ensures that it's a genuine identification number that can cast a valid vote in the poll. Once the registration has been processed, none of your private information is stored or kept in the Bitagora server. 
7. After registering, you will be able to cast your vote by signing it with your personal private key using Bitagora's web or mobile booth applications. Only then will the unique identification number obtained at the time of registration be stored on the distributed public ledger where all the votes for a given poll are recorded. Although this identification number is accessible to anyone reading the public ledger, there is no feasible way for humans or machines with current cryptographic technology to recover your private information from this recorded data.
8.	Apart from the information required to obtain the unique identification number at registration, Bitagora does not process or require any other personal data from you for any purpose.
9. When you vote, your ballot is processed by the client-based web or mobile booth application and directly sent by to validator nodes in the network. If the ballot is valid, it will be permanently recorded in the distributed ledger. The data recorded in the public ledger is not linked in any way to the private information your provide during registration, to your IP, or to any other data that can identify you personally or allow any third party to trace you or your identity using the public ledger.
10.	Since Bitagora does not keep in any shape or form your personal data, it cannot disclose it to anyone.
11. Bitagora may update this policy from time to time by publishing a new version on its website.
12. By providing your personal data to Bitagora for registration purposes, you are acknowledging and consenting to this privacy policy.

### 2. Cookies
1. Neither Bitagora's website, mobile or web booth applications use any cookies.

### 3. Data stored locally
1.	Bitagora's web and mobile booths client-based applications run on your device and use local storage to store information about your registration and ballot.
2. Except for the purpose of registration (see point 1 above), the information stored in your device is not sent to Bitagora's server at any point.
3. You can delete the information stored in your device at your will. When you uninstall the web or mobile booth, this information is automatically deleted from your device.
4.	When using Bitagora's web or mobile booths, blocking local storage will disable the application's functionality.

### 4. Validator nodes
1.	Users who wish to install and run Bitagora's validator node software on their own machine are willingly participating in a peer-to-peer network under their sole responsibility, in accordance with Bitagora's [terms of service](./terms.md).
2. All the software required to install and run a validator node is open-source and can be reviewed in the [Bitagora repo](https://github.com/Bitagora/bitagora-node).
3. Once installed, validator nodes make their IP known to other nodes for the purpose of peering and consensus building using the PoET protocol adapted from the [Sawtooth-Hyperledger project](https://github.com/hyperledger/sawtooth-core). No other private information from the node is broadcasted to the network during peer-to-peer interaction. 
4. Nodes are accessible to other peers and clients through selected open ports. These ports should be made accessible by the user for the node to be fully functional.
5. The database containing the public ledger's transactions and state is stored locally at the node's machine.
6. When uninstalling the validator node, users will effectively remove all files and data related with the ledger and peer-to-peer network. Thereafter, their IP will no longer be discoverable by other nodes in the network.

### 5. Contact
1.	If you have any queries regarding this policy, you can contact Bitagora by email at [mail@bitagora.cc](mailto:mail@bitagora.cc).

[back](./)
