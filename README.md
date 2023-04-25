# Module20: Solidity Smart Contract



Automating the creation of joint savings accounts. Creating a solidity smart contract that accepts two user addresses that are then able to control a joint savings account.Our smart contract will use ether management functions to implement various requirements from the financial institution to provide the features of the joint savings account.

Steps:

1. Create and work within a local blockchain development environment using the JavaScript VM provided by the Remix IDE.

2. Script and deploy a JointSavings smart contract.

3. Interact with our deployed smart contract to transfer and withdraw funds.


Set up for test run
Using the setAccounts function to define the authorized Ethereum address that will be able to withdraw funds from our contract.

We used the following Ethereum addresses:

Dummy account1 address: 0x0c0669Cd5e60a6F4b8ce437E4a4A007093D368Cb

Dummy account2 address: 0x7A1f3dFAa0a4a19844B606CD6e91d693083B12c0

![Capture1](https://user-images.githubusercontent.com/118318397/234148779-be0bb36f-c85a-4e84-ad80-2740d3b190c0.JPG)


Transactions:

Successfully deposited 50 ether as initial funds into the contract, to test the contract’s withdrawal functionality we performed 3 transactions by withdrawing:

Transaction 1: 5 ether into accountOne
Transaction 2: 10 ether into accountTwo
Transaction 3: 1 ether into accountOne
After each transaction, use the contractBalance function to verify that the funds were withdrawn from our contract. Also, we use the lastToWithdraw and lastWithdrawAmount functions to verify that the address and amount were correct.


Transaction 1: 5 ether into accountOne: 0x0c0669Cd5e60a6F4b8ce437E4a4A007093D368Cb
![acc1](https://user-images.githubusercontent.com/118318397/234148943-2e980d0f-2316-4545-9512-fe430450fc6e.JPG)


Transaction 2: 10 ether into accountTwo: 0x7A1f3dFAa0a4a19844B606CD6e91d693083B12c0
![Transac 2](https://user-images.githubusercontent.com/118318397/234149010-e90fb74e-3d6e-4e9e-91b3-ea0caa901613.JPG)


Transaction 3: 1 ether into accountOne: 0x0c0669Cd5e60a6F4b8ce437E4a4A007093D368Cb
![acc3](https://user-images.githubusercontent.com/118318397/234149108-b1e24699-f3f6-4299-98f9-f5a36f22d74d.JPG)


Error Handling
Checking if the balance is sufficient to accomplish the withdraw operation. In case of insufficient funds, the text "Insufficient funds!" is returned.
![11](https://user-images.githubusercontent.com/118318397/234149498-83b0f577-debc-409a-a424-20dbd1cc09b0.JPG)


Checking if the recipient is equal to either accountOne or accountTwo. The require statement returns the text "You don't own this account!" if recipient is not accountOne or accountTwo.
![1112](https://user-images.githubusercontent.com/118318397/234149560-c61e4a9c-1baf-4e8a-98b0-0688cc5c38ed.JPG)
