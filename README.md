# VOTECHAIN

codefundo++ 2019
---
## Team three-musketeers
College - **IIT Kanpur** <br />
Team members:-
* [Nirmal Suthar](https://github.com/nirmal-suthar)
* [Naman Biyani](https://github.com/namanbiyani)
* [Sparsh Agarwal](https://github.com/sparshag21)
---

# IDEA
## Abstract
Elections, referenda, and polls are very important processes & tools for the smooth operation of a modern democracy.
Some of the key considerations from the voters' perspective are:
-  Choice of candidate must remain secret
-  Vote counting should be public and accountable but at the same time should be inaccessible during the voting period.
-  Tamper proof by a third party

Problems with software based voting systems are :-
-  A single voting server would not be able to handle the load from many votes being placed at once. We would need to use sharding or allow voters to place votes to one of many servers.
-  As the number of voting servers increase, it becomes more difficult to ensure that no duplicate votes are placed across servers.
-    An attacker could spoof a voting machine's signature over the network and place unauthorised votes.

Elections are under constant threat from criminal groups, that alter vote count and hijack polling booths. These groups also spread misinformation about the main candidates. This has a heavy influence on our Country's economy & Decision making process.

About one third of India's population is on the move beacuse of education, work or any other reason. Therefore the manual authentication method of physically identifying yourself in your registered voting constituency is also something that we should avoid, potentially allowing people to place votes for a candidate in their home state even if they are travelling, which can drastically increase voter turnout.

To protect the virtue of democracy in our country, we would work on creating a web app that uses Microsoft AZURE's Blockchain technology and Django Framework (Python based). A basic overview of our idea is described below: 
## App features
We plan to make 2 apps, one for voters who are not in their respected  constituencies and other for those who can vote by going to their respective polling booths . First app will have major features as new voter registration and vote casting , first app will also be accessible to voters who are in their constituencies for new voter registration and to see details of candidates of his constituencies . Second app will be available at voting booths in Electronic Voting Machines wherein voters can cast their vote securely .


Major features of voter app will as follows :-

- **Registration** - Every eligible voter can register by entering three compulsory field - Name, DoB, Aadhar Card number. An OTP will be sent to the number linked with person's Aadhar Card. After successful verification of the details, Voter ID will be generated and the applicant will be registered as a voter and will be given sign-in access to the app. Incase, the applicant doesn't meet the eligible age, the Voter ID will be generated after once the applicant reach eligible age.
- **Verification and Sign-In** - After a successful registration or sign-in, the voter's application screen will be populated with a list of candidates of his/her constituency appearing in elections. Each candidate's profile would also be available and he/she can update his constituency by Aadhaar address verification .
-  **Directing the Voter to nearby Booth** - On the application voter will be given a notification of its near-by address of his/her voting centre at an interval of every one hour during the votinf period . The voting process could only be done on voting centre because voting will work on a specific Wi-Fi network. This is made possible through the Geo-fencing.
-  **Vote authentication** - For vote authentication, we will use Assymetric encryption as described in next section . 
- **Vote Accumulation** -  Shifting the voting machines to the Election commission is a problem. To solve this, we would store the votes in chunks locally until a stable connection is established. Chunking votes also makes it harder to place individual fraudulent votes from a rogue machine. 
- **Vote Casting** - When enough votes accumulate and a stable internet connection is established, a chunk of votes is pushed to the delegated voting servers as explained in the next section .
- **Vote Counting** - Count of votes starts just after the voting period has ended and a detailed explaination of vote counting is described in the next section .

## Use of blockchain in voting system
- We will build a decentralized system with each constituency as a node and there will be a central node which stores the database of all the users and has no role in voting procedure. As soon as a new user is registered , the central node database and node of his/her constituency gets updated , thus if anyone registers from multiple constituencies, this is detected in the central node. This way, neither there is inconvenience for new voters nor will a voter be able to cast vote from multiple constituencies.
- **Vote authentication** -
 ![alt text](https://res.cloudinary.com/practicaldev/image/fetch/s--sVKfEYOD--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/e8inq9uy4e8o07pppoa0.png)


 All of the data (data of voters and candidates) will be asymmetrically encrypted and decrypted via RSA algorithm & stored in multiple systems & this will make it impossible to tamper our data .When a voter identifies themselves with a voter ID, it is verified against the local voter list. If the ID is present, a key-pair is generated for the voter, with the 'opening' private key stored against their name and the public key used to encrypt or 'seal' their vote choice. This sealed choice is then stored on the local ledger, ready to be sent to the central voting nodes. (point 2 of blog , need to combine previous point with these if possible)
- **Vote Casting** - 
- **Vote Counting** - 
![alt text](https://res.cloudinary.com/practicaldev/image/fetch/s--ManETZX---/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/r1zxjvkjzg4xb41fsp4k.png)

- With blockchain, votes could be verified right after the voting is finished, so that officials can be certain that the votes are counted correctly. This can be achieved without the need for a central body overseeing the results, as we currently have in the system.
-    Each vote is conceptually equivalent to the asset in blockchain and transaction occurs between a voter and a contestant. Restrict asset to a process maximum of one transaction to potentially prevent multiple votes to the same candidate or voting for multiple contenders.
# Dataset used
We will be using the **Open Government Data Platform India' dataset**. (Digital India initiative)
# Technology used
- Microsoft Azure Blockchain
- Microsoft computer vision API
- Django-for back end development
- Bootstrap and JQuery for frontend development
