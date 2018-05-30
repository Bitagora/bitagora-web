---
layout: default
---
## Privacy policy

### 1. Personal information
1.	Bitagora is committed to safeguarding the confidentiality and privacy of any private information you provide to the system when registering to vote with the Bitagora platform and software.
2.	This policy applies where Bitagora is acting as the data controller agent with respect to the registration data of polls conducted with the Bitagora system, that is, wherever Bitagora determines the purposes and means of the processing of that registration data. This includes data processed by any Bitagora controlled server (Bitagora API) as well as by client-based web and mobile voting booths (Bitagora Booth).
3. This policy does not apply to any instance where a third party acts as the data controller agent with respect to the registration data for polls conducted with the Bitagora voting system or where the platform or the software has been forked or modified to be used under the available license by any third party.
4. Bitagora NEVER collects or saves your personal information anywhere in any circumstance. 
5. During the registration process, the Bitagora API will process your ID number, date of birth, name, and other data that you might provide when using the Bitagora Booth (web or mobile), in order to produce a unique public registration number. This number is calculated automatically without any human intervention using a one-way cryptographic hashing algorithm. This algorithm ensures that 
  (a) no other user will ever have the same registration number for a given poll, and
  (b) no-one, not even the administrators of Bitagora's servers, will ever be able to retrace your private data based on the registration number produced.
6. Once calculated, the registration number is automatically sent back to the web or mobile booth application processing your registration, together with a personal private key and a signature. Once the registration has been processed, none of your private information is stored or kept in Bitagora's or any other server. 
7. The private key sent by the Bitagora API is linked cryptographically with your registration number and allows you to sign your ballot when you are ready to cast it. You should not share this private key with anyone. However, if you were to make it public by accident, no-one would be able to reconstruct your private data from it. And once you have effectively cast your vote, no-one will be able to vote again with the same key in the same poll. 
8. The cryptographic signature sent by the Bitagora API ensures that your key and registration number are genuine and are allowed to cast a vote in the poll.
7. After registering, you will be able to cast your vote by signing it with your personal private key using Bitagora's web or mobile booth applications (Bitagora Booth). Only then will the unique identification number obtained at the time of registration be stored on the distributed public ledger where all the votes for a given poll are recorded. Although this number is accessible to anyone reading the public ledger, there is no feasible way for humans or machines with current cryptographic technology to recover your private information from this recorded data.
8. The data for registration is sent back and forth between the Bitagora API and the Bitagora web or mobile booth applications over https, an encrypted, secure and standard communication protocol.
9.	Apart from the information required to obtain the unique identification number at registration, Bitagora does not process or require any other personal data from you for any purpose.
10. When you vote, your ballot is processed by the client-based web or mobile booth application (Bitagora Booth) and directly sent to decentralized nodes that participate in the network of validators. The ballot received by the validator nodes includes the unique identification number obtained at registration, but does not include any of the personal or private information you provided in order to obtain it. 
11. If your ballot is valid, it will be permanently recorded in the distributed ledger. The data recorded in the public ledger is not linked in any way to the private information your provide during registration, to your IP, or to any other data that can identify you personally or allow any third party to trace you or your identity using the public ledger. 
12. Thanks to this system, your vote remains at all times completely confidential and can never be linked to you personally by anyone, including Bitagora's administrators and validator nodes, while at the same time ensuring that you cannot vote twice in the same poll.
13.	Since Bitagora does not keep in any shape or form your personal data, it cannot disclose it to anyone.
14. Bitagora may update this policy from time to time by publishing a new version on its website.
15. By providing your personal data to Bitagora for registration purposes, you are acknowledging and consenting to this privacy policy.

### 2. Cookies
1. A cookie is a file containing an identifier (a string of letters and numbers) that is sent by a web server to a web browser and is stored by the browser. The identifier is then sent back to the server each time the browser requests a page from the server.
2.	Cookies may be either "persistent" cookies or "session" cookies: a persistent cookie will be stored by a web browser and will remain valid until its set expiry date, unless deleted by the user before the expiry date; a session cookie, on the other hand, will expire at the end of the user session, when the web browser is closed.
3	Cookies do not typically contain any information that personally identifies a user, but personal information that we store about you may be linked to the information stored in and obtained from cookies.
4. Bitagora's website (https://bitagora.cc) is hosted by github.com. When you load the page in your browser, the server will automatically send a cookie for the purpose of storing locally the session data. This cookie is not persistent and you can effectively disable or block it, as it is not necessary for the functioning of the website.   
5. Bitagora's mobile or web booth applications run entirely on your device and do not send any cookies between the server and the client. These applications, however, need to store data locally in your device in order to function properly. 

### 3. Data stored locally
1.	Bitagora's web and mobile booths client-based applications run on your device and use local storage to store information about your registration and ballot.
2. Except for the purpose of registration (see point 1 above), the information stored in your device is not sent to Bitagora's server at any point.
3. You can delete the information stored in your device at your will. When you uninstall the web or mobile booth applications, this information is automatically deleted from your device.
4.	When using Bitagora's web or mobile booths, blocking local storage will disable the application's functionality.

### 4. Validator nodes
1.	Users who wish to install and run Bitagora's validator node (Bitagora Validator) software on their own machine are willingly participating in a peer-to-peer network under their sole responsibility, in accordance with Bitagora's [terms of service](./terms.md).
2. All the software required to install and run a validator node is open-source and can be reviewed in the [Bitagora repo](https://github.com/Bitagora/bitagora-node).
3. Once installed, Bitagora Validator nodes make their IP known to other nodes for the purpose of peering and consensus building using the PoET protocol adapted from the [Sawtooth-Hyperledger project](https://github.com/hyperledger/sawtooth-core). No other private information from the node is broadcasted to the network during peer-to-peer interaction. 
4. Bitagora Validator nodes are accessible to other peers and clients through selected open ports. These ports should be made accessible by the user for the node to be fully functional.
5. The database containing the public ledger's transactions and state is stored locally at the Bitagora Validator node's machine.
6. When uninstalling the Bitagora Validator node, users will effectively remove all files and data related with the ledger and peer-to-peer network. Thereafter, their IP will no longer be discoverable by other nodes in the network.

### 5. Contact
1.	If you have any queries regarding this policy, you can contact Bitagora by email at [mail@bitagora.cc](mailto:mail@bitagora.cc).

