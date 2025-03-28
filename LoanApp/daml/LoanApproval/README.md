
OverView:-

This Project implement Loan Approval WorkFlow using DAML.
A Borrower request a loan, and bank can approve it. After approval the borrower's request is archieved and a Loan contract is Created.


Workflow design

1-> Borrower Submit a LoanRequest where borrower is the signatory
2-> Bank approves the request using ApproveRequest choice
3-> LoanRequest contract is Archied and a new Loan contract is created with signatories as Bank and Borrower


SmartContract Design

1-> LoanRequest Template : Created by borrower, observed by bank
2-> ApprovaRequest choice : invoked by bank, leading to loan contract creation
3-> Loan Template which represent the Loan approval status.

Script

1-> Allocate party (Bank, Borrower)
2-> Borrower creates LoanRequest
3-> Bank ApproveRequest, which creates a new loan with approval status 


How to Run this code

*Ensure DAML SDK is Installed*
*Run DAML sandbox*

Daml LoanApproavl 
cd LoanApproval
daml build 

*To view the process and the flow you can just download and run the script in the scripts file loadApproval->loanApproval.daml and Script.daml you get the transaction View of this workflow *

