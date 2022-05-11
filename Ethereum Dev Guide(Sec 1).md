# Ethereum & Solidity: The Complete Developer's Guide(Sec 1).
> Syntesis of the Ethereum Developer guide's First Section.


## Table of Contents
* [Glossary](#glossary)
* [Short History](#short-history)
* [What Is Ethereum?](#what-is-ethereum)
* [Interfacing With Ethereum Networks](#interfacing-with-ethereum-networks)
* [Transactions and Gas](#transactions-and-gas)
* [Smart Contracts](#smart-contracts)
* [Solidity](#solidity)
* [Deploying Contracts](#deploying-contracts)
* [Remix](#remix)
* [Project Status](#project-status)
* [Room for Improvement](#room-for-improvement)
* [Resources](#resources)



## Glossary

- Node : A machine that is running an Ethereum client machine.
- Networks : Networks are formed by one or more nodes.
- Transaction : Transactions are cryptographically signed instructions from accounts. An account will initiate a transaction to update the state of the Ethereum network. The simplest transaction is transferring ETH from one account to another.
- Block : Group of Transactions. 
- BlockChain : A database that stores a record of every transaction. And it's also where we store data in the form of a chain of Blocks(hence The Name).
- EVM : The EVM’s physical instantiation can’t be described in the same way that one might point to a cloud or an ocean wave, but it does exist as one single entity maintained by thousands of connected computers running an Ethereum client.
- Private Key : A private key is made up of 64 hex characters and can be encrypted with a password.
- Public Key : The public key is generated from the private key using the Elliptic Curve Digital Signature Algorithm.
- Account : An Ethereum account is an entity with an ether (ETH) balance that can send transactions on Ethereum. Accounts can be user-controlled or deployed as smart contracts.
- Metamask : Browser Extension to interact with the Ethereum network through Mnemonic generated accounts.
- Gas : Gas is essential to the Ethereum network. It is the fuel that allows it to operate, in the same way that a car needs gasoline to run.
- Smart Contract : A "smart contract" is simply a program that runs on the Ethereum blockchain. It's a collection of code (its functions) and data (its state) that resides at a specific address on the Ethereum blockchain.


## Short History
- BTC Paper - 2008 (BlockChain Technology for money Transfer Only) (Went Online in 2009)
- Ethereum white Paper - 2013 (Creation complex applications on top of BlockChain Technology) (Went Online in 2015)
- "ETH White Paper" discusses need for more programatic control over Transactions.
- Wanted to enable creation of Desentralised Autonumous Corporations (DAC).
- Introduces the Idea of 'smart contracts' as an entity that can send and receive currency beyond just humans. 


## What Is Ethereum?
- when we work with Ethereum, we are working with a network of computers.
- These networks are used to transfer money between different parties like you and me, and they're also
used to store data.
- there are many different Ethereum networks.
- there's one main Ethereum network that everyone uses for deployment of production applications.
- There are test networks.
- You can even create your own private Ethereum network on your own computer that is restricted to just you.
- Networks are formed by one or more nodes.
- anyone can run a node
- Each Node can contain a full copy of the BlockChain.


## Interfacing With Ethereum Networks
- Developers Interact with ETH network through Web.js 
- Normal Users(Cutomers) Interact with the network through Metamask.
![Example screenshot](./img/screenshot.png)




## Transactions And Gas
- An Ethereum transaction refers to an action initiated by an externally-owned account.
- Transactions, which change the state of the EVM, need to be broadcast to the whole network.
- Any node can broadcast a request for a transaction to be executed on the EVM; after this happens.
- A miner will execute the transaction and propagate the resulting state change to the rest of the network.
- Transactions require a fee and must be mined to become valid.
- A submitted transaction includes the following information:
  1. recipient – the receiving address (if an externally-owned account, the transaction will transfer value. If a contract account, the transaction will execute the contract code).
  2. signature – the identifier of the sender. This is generated when the sender's private key signs the transaction and confirms the sender has authorized this transaction.
  3. value – amount of ETH to transfer from sender to recipient (in WEI, a denomination of ETH).
  4. data – optional field to include arbitrary data.
  5. gasLimit – the maximum amount of gas units that can be consumed by the transaction. Units of gas represent computational steps.
  6. maxPriorityFeePerGas - the maximum amount of gas to be included as a tip to the miner.
  7. maxFeePerGas - the maximum amount of gas willing to be paid for the transaction (inclusive of baseFeePerGas and maxPriorityFeePerGas).


## Smart Contracts 
- A "smart contract" is simply a program that runs on the Ethereum blockchain.
- It's a collection of code (its functions) and data (its state) that resides at a specific address on the Ethereum blockchain.
- Smart contracts are a type of Ethereum account.
- This means they have a balance and they can send transactions over the network.
- However they're not controlled by a user, instead they are deployed to the network and run as programmed.
- User accounts can then interact with a smart contract by submitting transactions that execute a function defined on the smart contract.
- Smart contracts can define rules, like a regular contract, and automatically enforce them via the code.
- Smart contracts cannot be deleted by default, and interactions with them are irreversible.


## Solidity 
- Solidity is an object-oriented, high-level language for implementing smart contracts. 
- Smart contracts are programs which govern the behaviour of accounts within the Ethereum state.
- Solidity is a curly-bracket language designed to target the Ethereum Virtual Machine (EVM). 
- It is influenced by C++, Python and JavaScript.


## Deploying Contracts
- You need to deploy your smart contract for it to be available to users of an Ethereum network.
- To deploy a smart contract, you merely send an Ethereum transaction containing the compiled code of the smart contract without specifying any recipient.


## Remix
- Remix IDE is an open source web and desktop application. It fosters a fast development cycle and has a rich set of plugins with intuitive GUIs.
-  Remix is used for the entire journey of contract development as well as act as a playground for learning and teaching Ethereum.
-  Remix IDE is part of the Remix Project which is a platform for development tools that use a plugin architecture.
-  It encompasses sub-projects including Remix Plugin Engine, Remix Libs, and of course Remix-IDE.
-  Remix IDE is a powerful open source tool that helps you write Solidity contracts straight from the browser.
-  It is written in JavaScript and supports both usage in the browser, but run locally and in a desktop version.
-  Remix IDE has modules for testing, debugging and deploying of smart contracts and much more.



## Project Status
Project is: _in progress_ 


## Room for Improvement

- Recreate The Diagrams On Draw.io
- Imp 2


## Resources
- This project was based on [this tutorial](https://www.udemy.com/course/ethereum-and-solidity-the-complete-developers-guide/).
- [Ganache with remix article](https://medium.com/@kacharlabhargav21/using-ganache-with-remix-and-metamask-446fe5748ccf).

