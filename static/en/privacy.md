---
layout: default
---
## Privacy policy

### 1. Personal information
1.	Bitagora is committed to safeguarding the confidentiality and privacy of any personal information provided to the system by users when registering to vote with the Bitagora Platform.
2.	This policy applies where Bitagora is acting as the data controller agent with respect to the registration of data for polls conducted with the Bitagora system, that is, wherever Bitagora determines the purposes and means of the processing of that registration data. This includes data processed by any Bitagora controlled server (Bitagora registration API) as well as by client-based web and mobile voting booths (Bitagora Booth).
3. This policy does not apply to any instance where a third party acts as the data controller agent with respect to the registration of data for polls conducted with the Bitagora voting system or where the platform or the software has been forked or modified to be used under the available license by any third party.
4. Bitagora NEVER stores, keeps or saves the personal information of users anywhere, under any circumstance. 
5. During the registration process, the Bitagora registration API will process the user's ID number, date of birth, name, and other data that the user might provide when using the Bitagora Booth web or mobile applications. This information is used to produce a unique private voting voting key. This key is calculated automatically without any human intervention using a one-way cryptographic hashing algorithm.
6. The algorithm used to produce the private voting key ensures with sufficient confidence that 
  (a) no other user will ever have the same registration number for any given poll, and
  (b) no-one, not even the administrators of Bitagora's servers or validator nodes, would be able to retrace or figure out the user's personal data even if they knew the private voting key.
6. After calculating this private voting key, the Bitagora registration API server sends it to the web or mobile booth application processing the registration for the user, together with a signature that ensures that the key is genuine and is allowed to cast a vote in the poll. None of the user's personal information is stored, kept or recorded in Bitagora's or any other server in any way. 
7. The private key sent by the Bitagora API allows the user to sign the ballot when ready to cast it using the Bitagora Booth mobile or web applications. The user is encouraged not to share this private key with anyone. However, even if the private voting key were to be made public by accident, no-one would be able to reconstruct the user's private data from it. Moreover, once the user has effectively cast his or her vote, the distributed blockchain protocol ensures that no-one will be able to vote again with the same key in the same poll. 
8.	Apart from the information required to obtain the unique private voting key at registration, Bitagora does not process or require any other personal data from users for any other purpose.
9. Once the user signs his or her ballot using with the private voting key, the client-based Bitagora Booth application will broadcast the ballot directly to a decentralized network of validator nodes. This ballot includes a public and unique identification number that is cryptographically linked to the private voting key. Once the ballot has been validated, this number will be inscribed in the distributed public ledger where all the votes for a given poll are recorded. Although this number is accessible to anyone reading the public ledger, there is no feasible way for humans or machines with current cryptographic technology to recover from it the user's private voting key, much less the personal information originally provided by users.
10. If the ballot sent by the user is valid, it will be permanently recorded in the distributed ledger. The data recorded in the public ledger does not include the personal information provided by users during registration, their IP, or any other data that can identify users personally or allow any third party to trace their identity using the public ledger. 
11. Thanks to this system, votes remain at all times completely confidential and can never be linked to individual users by anyone, including Bitagora's administrators and validator nodes, while at the same time ensuring that users are only allowed to vote once in a given poll.
12.	Since Bitagora does not keep in any shape or form the personal data of users, it cannot disclose it to anyone.
13. Bitagora may update this policy from time to time by publishing a new version on its website.
14. By providing their personal data to Bitagora for registration purposes, users are acknowledging and consenting to this privacy policy.

### 2. Cookies
1. A cookie is a file containing an identifier (a string of letters and numbers) that is sent by a web server to a web browser and is stored by the browser. The identifier is then sent back to the server each time the browser requests a page from the server.
2.	Cookies may be either "persistent" cookies or "session" cookies: a persistent cookie will be stored by a web browser and will remain valid until its set expiry date, unless deleted by the user before the expiry date; a session cookie, on the other hand, will expire at the end of the user session, when the web browser is closed.
3	Cookies do not typically contain any information that personally identifies a user, but personal information stored by the server may be linked to specific information stored in and obtained from cookies.
4. Bitagora's website (https://bitagora.cc) is hosted by github.com. When users load the page in their browser, the server will automatically send a cookie for the purpose of storing locally the session data. This cookie is not persistent and users can effectively disable or block it, as it is not necessary for the functioning of the website.   
5. Bitagora Booth mobile and web applications run entirely on the user's device and do not send any cookies between the server and the client. These applications, however, need to store data locally in the user's device in order to function properly. 

### 3. Data stored locally
1.	Bitagora Booth client-based web and mobile applications run on the user's device and use local storage to store information about the user's registration and ballot.
2. Except for the purpose of registration (see point 1 above), the information stored in the user's device is not sent to Bitagora's server at any point.
3. Users can delete the information stored in their device at their will. When uninstalling Bitagora Booth web or mobile applications, this data is automatically deleted from the device.
4.	When using Bitagora Booth web or mobile applications, blocking local storage is not recommended as it will disable the application's functionality.

### 4. Validator nodes
1.	Users who wish to install and run Bitagora Node software on their own machine are willingly participating in a peer-to-peer validator network under their sole responsibility, in accordance with Bitagora's [terms of service](./terms.md).
2. All the software required to install and run a validator node is open-source and can be reviewed in the [Bitagora repo](https://github.com/Bitagora/bitagora-node).
3. Once installed, Bitagora validator nodes make their IP known to other nodes for the purpose of peering and consensus building using the PoET protocol adapted from the [Sawtooth-Hyperledger project](https://github.com/hyperledger/sawtooth-core). 
4. Bitagora validator nodes are accessible to other peers and clients through selected open ports. These ports should be made accessible by the user for the node to be fully functional.
5. The database containing the public ledger's transactions and state is stored locally at the Bitagora validator node's machine.
6. When uninstalling the Bitagora Node software, users will effectively remove all files and data related with the ledger and peer-to-peer network. Thereafter, their IP will no longer be discoverable by other nodes in the network.

### 5. Contact
1.	If you have any queries regarding this policy, you can contact Bitagora by email at [mail@bitagora.cc](mailto:mail@bitagora.cc).

[back](../../../.)
