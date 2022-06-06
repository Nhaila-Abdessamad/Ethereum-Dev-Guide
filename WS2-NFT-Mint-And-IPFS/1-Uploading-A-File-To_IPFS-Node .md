
# Uploading a File to IPFS Node.
> By Finishing This Markdown:
- you have installed an IPFS node on your EC2 Instance/
- You have Uploaded a USD image to your IPFS Node


## Table of Contents
* [Installing IPFS](#installing-ipfs)
* [Downloading The USD Image](#downloading-the-usd-image)
* [Uploading The USD Image to IPFS](#uploading-the-usd-image-to-ipfs)
* [Taking your IPFS Node Online](#taking-your-ipfs-node-online)
* [Accessing the Image from The Browser](#accessing-the-image-from-the-browser)




## Installing IPFS

- First Download the Linux binary from dist.ipfs.io:

```
wget https://dist.ipfs.io/go-ipfs/v0.12.2/go-ipfs_v0.12.2_linux-amd64.tar.gz
```

- Unzip the file:

```
tar -xvzf go-ipfs_v0.12.2_linux-amd64.tar.gz
```

- Move into the go-ipfs folder 
```
cd go-ipfs
```


- run the install script:

```
sudo bash install.sh
```


- Test that IPFS has installed correctly:
```
ipfs --version
```



## Downloading The USD Image

- create a new directory called ipfsFILES:

```
mkdir ipfsFILES
```

- cd into it

```
cd ipfsFILES
```

- Download the image:

```
wget https://quotepark.com/media/authors/johannes-kepler.jpeg
```


## Upload The USD Image to IPFS

- add the file to ipfs:

```
ipfs add johannes-kepler.jpeg
```

- Save The CID into this this text file 
```
vi CID.txt
```

## Taking your IPFS Online

- open a new terminal and run this command to make your node accessible online:
```
ipfs daemon
```

## Accessing the Image from The Browser
- open your browser and use this link 
```
https://ipfs.filebase.io/ipfs/QmZAByyvDmULmjAFnY3repJtR86kfoGMKBy5Wr7bdaMcTp
```
- you should be able to retrieve your file, if you get an error just refresh.



## Resources
- [Instalation Guide](https://docs.ipfs.io/install/command-line/#official-distributions)

- [Files Browser Link](https://ipfs.filebase.io/ipfs/Qme9yNpup7qKTYiKUe75oSaxAR2E9nVLwpp6tpZ79Lv9U2)

- [IPFS: How to use IPFS CIDs and Fetch IPFS Links](https://docs.filebase.com/knowledge-base/fetching-data/how-to-use-ipfs-cids-and-fetch-ipfs-links)

- [Content addressing and CIDs](https://docs.ipfs.io/concepts/content-addressing/#identifier-formats)

- [A Technical Guide to IPFS – the Decentralized Storage](https://www.freecodecamp.org/news/technical-guide-to-ipfs-decentralized-storage-of-web3/#how-to-use-ipfs)

- [How IPFS works](https://docs.ipfs.io/concepts/how-ipfs-works/#content-addressing)


