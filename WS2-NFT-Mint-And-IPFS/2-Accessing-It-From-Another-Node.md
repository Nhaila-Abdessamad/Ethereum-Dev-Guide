
# Accessing The File we Uploaded from another IPFS Node.
> By Finishing This Markdown:

- you have been able to access the image file you uploaded to your Ipfs node from your friend's Node.



## Table of Contents
* [Making sure both IPFS Nodes are Online](#making-sure-both-ipfs-nodes-are-online)
* [Download the Image using the CID](#download-the-image-using-the-CID)


## Making sure both IPFS Nodes are Online
- Make sure the ipfs daemon process is active on both nodes

## Download the Image using the CID  
- cd to ipfsFILES from the other instance you have access to

```
cd ipfsFILES
```

- Use this command to download the file on the second node 
- Don't forget to replace **<HASH>** with the image CID you got after uploading it to the first node.

```
ipfs get -o picture.png  <HASH>
```

## Resources
- [Files Manipulation examples in IPFS](https://gist.github.com/whyrusleeping/66a85789d2abb8971fff)


