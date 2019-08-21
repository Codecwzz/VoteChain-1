# VOTECHAIN

codefundo++ 2019
---
## Team three-musketeers
College - **IIT Kanpur**
Team members
* [Nirmal Suthar](https://github.com/nirmal-suthar)
* [Naman Biyani](https://github.com/namanbiyani)
* [Sparsh Agarwal](https://github.com/sparshag21)
---

# IDEA
## Goal
To create a Decentralised Application which will make the entire process of voting more secure, transparent, and efficient. The major problems which we want to remove are the following :

- To allow people to vote securely. 
-  To expedite the process of vote counting. 
-  To ensure that every citizen over 18 can vote without applying for a voters id. 
-  To ensure that vote tampering is not possible and render all such claims invalid. 
-  To allow people to vote even from another constituency where they are registered as a voter.
# App details
## Roles
- **Election Commission** - the body which manages the election and declares the results .
-  **Voter** - Person who his eligible to vote for a candidate . 

## Stages
- **Setup**  - In this, the election commission may add the candidates and setup the election .
- **Voting** - This is the stage where voters can vote, and app will indicate whether a voter has voted or not
- **Results** - In this, Election Commission will count the votes and then declare the results .

## Working
A new Election smart contract may be created by the Election Commission (EC) and the name of the Election may be entered in the constructor. The initial state is the Setup State in which the EC has the permission to add candidates by invoking the function addCandidate. After the setup process is done, the EC may use the AllowVoting function to transition to the Voting Stage where the voter may vote for their favourite candidate. After voting, the voter will receive an email from the EC with the transaction id of the transaction which corresponds to their vote, which will allow them to be completely sure that their vote was properly registered. When the voting process is completed, the EC may calculate and declare the results by invoking the function ResCalc which expedites the process of vote counting. The winner of the election is shown in the table of the smart contract.

 To ensure that every person who is 18 and above can vote, we can use the python script (Check_Voters.ipynb) to filter out and create a csv with only people who are 18 years old. Now this csv is added directly to Azure Active Directory (AD) which assigns an ethereum id to them so that the new voters are able to vote on the blockchain without explicitly doing anything for it. The Aadhar database can be used for this purpose and this process will have to be repeated before the elections.

# AZURE services used:
- Azure Blockchain Workbench
Used to create the decentralised application on the blockchain and contains the main logic for the election process. A configuration file (Election.json) and solidity file (Election.sol) was used to set up the app.
- Logic Apps
This has been used to fully take advantage of the messaging API of Azure Blockchain Workbench to link it such that whenever the voting function is invoked in the workbench application, the transaction id of that transaction is sent to the voter who cast that vote. This transaction id can now be checked anytime to ensure that your vote is properly cast and thus render all claims of vote tampering invalid.
- Azure Active directory
This has been used to keep track of all the voters and assign an ethereum id as a key value pair with their email id. Also, those who turn 18 are added to the Azure Active Directory and in this way no prospective voters are left out. A python script has been used to automatically find all those who turned 18 before the election and create a csv file. This csv file is now added directly to the Azure AD.

# Youtube Video of Demo


