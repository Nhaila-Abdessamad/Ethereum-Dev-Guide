# ENV-Setup.
>After finishing this markdown:
- You will be able to configure and connect your VS Code to your assigned EC2 Instance using the remote-SSH Extention.



## Table of Contents
* [Creating The Truffle Project Directory](#creating-the-truffle-project-directory)
* [Creating a bare Truffle project with no smart contracts included](#creating-a-bare-truffle-project-with-no-smart-contracts)
* [Accesing the directory with your Vs Code](Accessing-the-directory-with-your-vs-code)
* [Writing The Smart Contract](writing-the-smart-contract)
* [Compiling The Smart Contract](compiling-the-smart-contract)
* [Starting The Local BlockChain using Ganache-CLI](#starting-the-local-blockcahin-using-ganache-cli)
* [Deploying The Smart Contract](deploying-the-smart-contract)
* [Resources](#resources)


## Creating The Truffle Project Directory
- Open your terminal or CMD and SSH to your EC2 Instance.
- Use this Command to create a new repository:

```
mkdir DemoContract
```
- CD into this directory you created

```
cd DemoContract
```

## Creating a bare Truffle project with no smart contracts included

- Use the following command to start a bare truffle project:

```
truffle init
```

## Accesing the directory with your Vs Code
- Once you've SSH-ed to your remote EC2 Instance with VsCode
- you should see the directory you created above by hiting open folder and looking at the DropDown

## Writing The Smart Contract
- Once you've accessed the directory
- Open The Contracts Folder
- Create a new file with the name **AssociateProfitSplitter.sol**
- Copy The Following CodeBlock Into it:

```
// SPDX-License-Identifier: GPL-3.0

pragma solidity ^0.5.0;

// lvl 1: equal split
contract AssociateProfitSplitter {
    // @TODO: Create three payable addresses representing `employee_one`, `employee_two` and `employee_three`.
    address payable employee_one;
    address payable employee_two;
    address payable employee_three;
    
    constructor(address payable _one,address payable _two, address payable _three ) public {
        employee_one = _one;
        employee_two = _two;
        employee_three = _three;
    }

    function balance() public view returns(uint) {
        return address(this).balance;
    }

    function deposit() public payable {
    
        // @TODO: Split `msg.value` into three                                         
        uint amount = msg.value/3;  // Your code here!
 
        // @TODO: Transfer the amount to each employee
        // Your code here!
        employee_one.transfer(amount);
        employee_two.transfer(amount);
        employee_three.transfer(amount);
        // @TODO: take care of a potential remainder by sending back to HR (`msg.sender`)
        // Your code here!  
        msg.sender.transfer(msg.value - amount *3);
    }

    function() external payable {
        // @TODO: Enforce that the `deposit` function is called in the fallback function!
        // Your code here!
        deposit();
    }
}
```

## Compiling The Smart Contract

- Access the ***truffle-config.js*** and modify the Compiler Solc Version to ***0.5.0***

- Now go back to your terminal and run:

```
truffle compile
```


## Starting The Local BlockChain using Ganache-CLI

- In order to deploy the contarct, you need to create a local blockchain using ganache-cli

- open a new terminal and Run:

```
ganache-cli
```


## Preparing the migration file for our contract

- Than you need to access the migrations folder and create a new file with the name ***2_deploy_contracts.js***
- Now Add the following code to it:

```
const AssociateProfitSpliter = artifacts.require("AssociateProfitSpliter");

module.exports = function (deployer) {
  deployer.deploy(AssociateProfitSpliter);
};

```


## Deploying The Smart Contract

- Now you can run this command to deploy your contract

```
truffle migrate
```

## Resources
- [Bare Truffle Project](https://trufflesuite.com/docs/truffle/getting-started/creating-a-project/)
- [Running Migrations](https://trufflesuite.com/docs/truffle/getting-started/running-migrations/)