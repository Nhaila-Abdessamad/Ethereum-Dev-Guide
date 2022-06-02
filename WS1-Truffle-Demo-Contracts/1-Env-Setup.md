
# ENV-Setup.
>After finishing this markdown:
- You will be able to SSH to the EC2 Instance allocated to you.
- Install The Required Packages to start Developing, Compiling, Testing & Deploying your smart Contracts.


## Table of Contents
* [SSH to your EC2 Instance](#ssh-to-your-ec2-instance)
* [Install NodeJs Through NVM](#install-nodejs-through-nvm)
* [install Truffle & Ganache-Cli](#install-truffle-&-ganache-cli)
* [Resources](#resources)


## SSH to your EC2 Instance
- Open Your CMD and make sure your working directory contains the SSH key "KPLR.pem".
- SSH To your EC2 Instance using the following command By changing the IP adress.
```
ssh -i "KPLR.pem" ec2-user@ec2-54-152-59-32.compute-1.amazonaws.com 
```

![alt text](https://github.com/Nhaila-Abdessamad/blockchain/blob/main/WS1-Truffle-Demo-Contracts/FIGs/EC2%20Log%20In.png "EC2 SSH")

## Install NodeJs Through NVM:

- First Install NVM Through These two Command.

1.Second Command:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```

![alt text](xxxx "EC2 SSH")


2.First Command:

```
. ~/.nvm/nvm.sh
```

![alt text](xxxx "EC2 SSH")


- Now you can Install NodeJs 14 through this command: 

```
nvm install 14
```

![alt text](xxxxx "EC2 SSH")

## install Truffle & Ganache-Cli

- Now you can Install Truffle & Ganache-Cli through this command:

```
npm install -g ganache-cli truffle --unsafe-perm
```

![alt text](xxxxx "EC2 SSH")


<!-- ## Resources
- This guide was based on:

- [NFT MarketPlace](https://gist.github.com/Warkanlock/d8bdd0f96aa7fa214fcb4bf800dea5b8).
- [NFT Mix](https://github.com/PatrickAlphaC/nft-mix).
- [Mintables](https://www.youtube.com/watch?v=CN1PJLsWujU).
- [basic NFT mint Contract](https://www.youtube.com/watch?v=8WPzUbJyoNg).
- [Code an NFT Marketplace like OpenSea ytb](https://www.youtube.com/watch?v=2bjVWclBD_s)-->
