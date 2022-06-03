# ENV-Setup.
>After finishing this markdown:
- You will be able to configure and connect your VS Code to your assigned EC2 Instance using the remote-SSH Extention.



## Table of Contents
* [Install VsCode](#insall-vscode)
* [Install the remote SSH VsCode extension](#install-the-remote-vscode-extention)
* [Configuring the remote SSH extention](#configuring-the-remote-ssh-extention)
* [Testing the Setup](testing-the-setup)
* [Resources](#resources)


## Install VsCode
- If you don’t have Visual Studio Code installed on your machine, head over to their [download page](https://code.visualstudio.com/Download) and grab the correct package for your system.


## Install the remote SSH VsCode extension
- Once VS Code is installed, open the Extension tab in the editor.
- search for “remote ssh” in the extensions marketplace.
- Locate and install the Remote-SSH extension, ensuring that it’s the correct extension (authored by Microsoft with 11.6 million installs at the time of writing).


## Configuring the remote SSH extention
- Click the new button in the bottom left corner of the editor.
- This will open the command palette, where you should select **Remote-SSH: Open Configuration File**.
- An SSH config file will pop up (select the one for the current user if the extension recognizes multiple config files), into which you can enter the following configuration:

```
Host VS Code-ssh-tutorial
HostName <HOSTNAME>
User ubuntu
IdentityFile <PATH TO IDENTITY FILE> 
```
1. ```Host``` can be any name. This will appear in VS Code
2. ```HostName``` is your EC2 Instance’s IP address
3. ```User```is the default  username
4. ```IdentityFile```is the complete path to the private key (the pem file) that we provided you with


## Testing the Setup

- Click the remote-ssh button in the bottom-left corner and click Connect to Host from the dropdown which appears.
- Another dropdown will appear. Select the host configuration you created in the previous step (Your EC2 Instance).
- If all’s well, you should be presented with a new editor window asking you to select your working directory.


## Resources
- [VS CODE REMOTE SSH](https://www.sitepoint.com/vs-code-remote-development-amazon-ec2/)