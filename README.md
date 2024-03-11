EtherWallet Smart Contract
Overview
EtherWallet is a simple Ethereum smart contract that allows users to deposit Ether into the contract and send Ether to other addresses. The contract is designed to be owned by a specific address, which has exclusive rights to send Ether stored in the contract.

Functionality
Constructor: Initializes the contract with an owner address.
Deposit: Allows users to deposit Ether into the contract.
Send: Allows the contract owner to send Ether to a specified address.
BalanceOf: Returns the current balance of Ether stored in the contract.
Usage
Deploy the Contract: Deploy the EtherWallet contract to the Ethereum blockchain, passing the owner address as a parameter to the constructor.
Deposit Ether: Users can deposit Ether into the contract using the deposit function.
Send Ether: Only the contract owner can send Ether to other addresses using the send function.
Check Balance: Use the balanceOf function to check the current balance of Ether stored in the contract.
Example
solidity
Copy code
// Deploy the contract with your address as the owner
EtherWallet etherWallet = new EtherWallet(msg.sender);

// Deposit Ether into the contract
etherWallet.deposit{value: msg.value}();

// Send Ether to another address
etherWallet.send(receiverAddress, amount);

// Check the balance of the contract
uint balance = etherWallet.balanceOf();
License
This project is licensed under the terms of the MIT license. See the LICENSE file for details.

