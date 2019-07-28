# VOTECHAIN
Elections, referenda, and polls are very important processes & tools for the smooth operation of a modern democracy.Elections are under constant threat from criminal groups, that alter vote count and hijack polling booths. These groups also spread misinformation about the main candidates. This has a heavy influence on our Country's economy & Decision making process. The major problems in present system of voting are :

- About one third of India's population is on the move beacuse of education, work or any other reason. Though they have a Voter ID card most of them don't vote becuase they will have to return to the hometown to vote and the process of changing the address on the Voter ID is tedious
-
To protect the virtue of democracy in our country, we would work on creating a web app that uses Microsoft AZURE's Blockchain technology and Django Framework (Python based). A basic overview of our idea is described below: 
# App features
- Every eligible voter can register by entering their Name, Date of Birth, Aadhaar card number and upload a Passport Photo . An OTP will be sent to the number linked with persons's Aadhaar card and passport size photographs would be verified using Image processing with Microsoft's computer vision APIs . After successful verification of the details, voterID will be generated and the applicant will be registered as a voter and can sign-in and access the app .
- After a successful registration or sign-in, the voter's application screen will be populated with a list of candidates of his/her constituency appearing in elections. Each candidate's profile would also be available and he/she can update his constituency by Aadhaar address verification .
-  On the application voter will be given a near-by address of his/her voting centre and a time slot. The voting process could only be done on voting centre because voting will work on a specific Wi-Fi network. This is made possible through the Geo-fencing.
- Our application will take advantage of the capabilities of the supported smartphones, which can detect if the operating system has been tampered with and disallows such voters from voting. We will be using end-to-end encryption for malware detection.

# Use of blockchain in voting system
-   All of the data (data of voters and candidates) will be asymmetrically encrypted via RSA algorithm & stored in multiple systems & this will make it impossible to tamper our data.
- We will build a decentralized system with each constituency as a node and a central node which stores the database of all the users and has no role in voting procedure . As soon as a new user is registered , the central node database and node of his/her constituency gets updated , thus if anyone registers from multiple constituencies, this is detected in the central node . This way, there is no inconvenience for new voters, neither is there the possibility of old voters' names getting deleted since it is present on a decentralized system.
- With blockchain, votes could be verified right after the voting is finished, so that officials can be certain that the votes are counted correctly. This can be achieved without the need for a central body overseeing the results, as we currently have in the system.
-   Anybody can participate and become a node in the system as long as they meet requirements which are confirmed during registration which will collectively ensure that the system is available throughout the duration of the election, and that the votes are counted correctly.
-    The whole voting process would be decentralized, which means that there is no central agency which must be trusted to conduct the elections fairly and securely.
- Eligible voters can receive a token which they can use to vote exactly once, getting rid of the double voting problem as well as ensuring full security.
-    Each vote is conceptually equivalent to the asset in blockchain and transaction occurs between a voter and a contestant.   Restrict asset to a process maximum of one transaction to potentially prevent multiple votes to the same candidate or voting for multiple contenders.
# Dataset used
We will be using the **Open Government Data Platform India' dataset**. (Digital India initiative)
# Technology used
- Microsoft Azure Blockchain
- Microsoft computer vision API
-  Django-for back end development
- Bootstrap
# issues
- online voting me without smartphone walon ka kya
- verification ka better idea ? fingerprint jyada accurate rahega?qr code?
# Impact
