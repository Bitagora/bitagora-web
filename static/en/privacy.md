---
layout: default
---
## Privacy policy

The following Privacy Policy ("Policy") is part of the [Terms of service](terms.md) ("Terms") agreed by every User of the Bitagora Platform when using any component of the Platform. All capitalized terms in this agreement will be given the same effect and meaning as in the Terms.

### 1. Personal information
1.	Bitagora is committed to safeguarding the confidentiality and privacy of any personal information provided to the system by Users when registering to vote with the Bitagora Platform.
2.	This policy applies where Bitagora is acting as the data controller agent with respect to the registration of data for polls conducted with the Bitagora Platform, that is, wherever Bitagora determines the purposes and means of the processing of that registration data. This includes data processed by any Bitagora controlled server (Bitagora registration API) as well as by client-based web and mobile voting booths (Bitagora Booth).
3. This policy does not apply to any instance where a third party acts as the data controller agent with respect to the registration of data for polls conducted with the Bitagora Platform or where the Bitagora Platform or the software has been forked or modified to be used under the available license by any third party.
4. Bitagora NEVER stores, keeps or saves the personal information of Users anywhere, under any circumstance. 
5. During the registration process, the Bitagora registration API will process the User's ID number, date of birth, name, and other data that the User might consent to provide when using the Bitagora Booth web or mobile applications. This information is used to produce a unique Private Voting Key. This key is calculated automatically without any human intervention using a one-way cryptographic hashing algorithm.
6. The algorithm used to produce the Private Voting Key ensures with sufficient confidence that 
  (a) no other User will ever have the same key for any given poll, and
  (b) no-one, not even the administrators of Bitagora's servers or validator nodes, will be able to retrace or figure out the User's personal data even if they could know the User's Private Voting Key.
6. After calculating this Private Voting Key, the Bitagora registration API server sends it to the web or mobile booth application processing the registration for the User, together with a signature that ensures that the Private Voting Key is genuine and is allowed to cast a vote in the poll. No User's personal information is stored, kept or recorded in Bitagora's or any other server in any way. 
7. The Private Voting Key sent by the Bitagora API allows the User to sign the ballot when ready to cast it using the Bitagora Booth mobile or web applications. The User is encouraged not to share this Private Voting Key with anyone. However, even if the Private Voting Key were to be made public by accident, no-one would be able to reconstruct the User's private data from it. Moreover, once the User has effectively cast his or her vote, the distributed blockchain protocol ensures that no-one will be able to vote again with the same Private Voting Key in the same poll. 
8.	Apart from the information required to obtain the unique Private Voting Key at registration, Bitagora does not process or require any other personal data from Users for any other purpose.
9. Once the User signs his or her ballot using with the Private Voting Key, the client-based Bitagora Booth application will broadcast the ballot directly to a decentralized network of validator nodes ("Bitagora Validators"). This ballot includes a public and unique Identification Number that is cryptographically linked to the Private Voting Key. Once the ballot has been validated, this Identification Number will be inscribed in the distributed public ledger where all the votes for a given poll are recorded. Although this number is accessible to anyone reading the public ledger, there is no feasible way for humans or machines with current cryptographic technology to recover from it the User's Private Voting Key, much less the personal information originally provided by Users.
10. If the ballot sent by the User is validated by the Bitagora Validators, it will be permanently recorded in the distributed ledger. The data recorded in the public ledger does not include the personal information provided by Users during registration, their IP, or any other data that can identify Users personally or allow any third party to trace their identity using the public ledger. 
11. Thanks to this system, ballots remain at all times completely confidential and can never be linked to individual Users by anyone, including Bitagora's administrators and validator nodes, while at the same time ensuring that Users are only allowed to vote once in a given poll.
12.	Since Bitagora does not keep in any shape or form the personal data of Users, it cannot disclose it to anyone. For the same reason, any third party that would be able to breach the security of the Bitagora registration API server would not be able to find there any personal information of the User, not even a record of the User's registration.
13. Moreover, communication between Bitagora Booth mobile and web applications is conducted using standard secure Internet protocols, minimizing the risk of a man-in-the-middle attack or any other security breach that could result in third parties acquiring the personal information provided by the User or the Private Voting Key obtained from the server. The likelihood of these attacks being successful for a given User is extremely low. However, Users should be aware of the consequences. 
14. If an attacker were to obtain the personal data sent by the User (ID card number, date of birth, name, etc.), it would be impossible for the attacker to know the content of the ballot which has yet to be cast. Also, the attacker would be unable to figure out the Private Voting Key of the user and, therefore, would not be able to trace in any way the ballot, once it has been cast. 
15. If an attacker were to learn the Private Voting Key of a user, the attacker would be able to cast a vote instead of the User (if the User has not done so already) or to find out the content of the vote cast (if the User has already voted). But the attacker, just by knowing the Private Voting Key, would not be able to determine the identity or any other personal information of the voter.
16. Only in the unlikely scenario where an attacker would be able to obtain at the same time the personal information sent by the User to the server and the Private Voting Key sent by the server to the User, the attacker would be able to cast the vote instead of the User and also would be able to link the ballot cast by the user with the User's identity.

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
4. Bitagora Validators are accessible to other peers and clients through selected open ports. These ports should be made accessible by the user for the node to be fully functional.
5. The database containing the public ledger's transactions and state is stored locally at the Bitagora Validator's machine.
6. When uninstalling the Bitagora Node software, users will effectively remove all files and data related with the ledger and peer-to-peer network. Thereafter, their IP will no longer be discoverable by other nodes in the network.

### 5. Acknowledgement, consent and revision
1. By using the Bitagora Platform, Users acknowledge and consent to this Privacy Policy.
2. Bitagora may revise this Privacy Policy at any time without notice, and such revisions will be effective upon being posted on Bitagora's website (https://bitagora.cc). Links to the updated version of the Policy will be provided in the software distributions of Bitagora Node and Bitagora Booth, as well as in any websites under administration of the Bitagora Team.

### 6. Contact
1.	If you have any queries regarding this policy, you can contact Bitagora by email at [mail@bitagora.cc](mailto:mail@bitagora.cc).

Last modified on: June 19, 2018

[back](../../../.)
