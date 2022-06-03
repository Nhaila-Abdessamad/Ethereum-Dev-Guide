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
- 

## Creating a bare Truffle project with no smart contracts included

- Use the following command to start a bare truffle project:

```
truffle init
```

## Accesing the directory with your Vs Code



## Writing The Smart Contract
- 

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
    
        // @TODO: Split `msg.value` into three                                          //0xb766F3e883Ea2d875488F948fbA715338Fa0d78E
                                                                                        //0x6396149f7eBaA0ddE9Fa91DCC537A676DABB0079
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



## Starting The Local BlockChain using Ganache-CLI



## Deploying The Smart Contract


## Resources
- [Bare Truffle Project](https://trufflesuite.com/docs/truffle/getting-started/creating-a-project/)