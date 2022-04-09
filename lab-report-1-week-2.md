# Week 2 Lab Report
## Logging into a course specific account on ieng6 <br /> 
<br />
<br />

### Installing VScode
- To install Visual Studio Code go to their website and choose the option appropriate for your device

![installVSCode](installVSCode.PNG)

- After it is installed, opening VScode should look something similar to this:

![VScode SS](VSCodeSS.PNG) <br /> 
<br />
<br />

### Remotely connecting

- First, make sure you have OpenSSH installed by going to "Settings", "Apps", "Optional Features", then search for OpenSSH. If not installed already, install OpenSSH Client and OpenSSH Server now. 

![OpenSSH install](installOpenSSH.png)

- Then find your course specific account on [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php). You will use this account to connect remotely. 

![account](accountLookUp.png)

- To connect to the remote host, open the terminal in VScode and type "ssh" and the name of your account.

![connect remotely](connectingWithSSH.png)

- The first time connecting to the server will give you a message asking if you are sure you want to connect, so type "yes" and press enter.
- Then it will ask for your password, type your password in and press enter. *(Note: when you type your password it will not show up in the terminal, but it is typing)*

![connect success](resultFromConnecting.png)

- When you've successfully connected, you will see something similar to this.<br /> 
<br />
<br />

### Running some commands
- To run some basic commands type into the terminal.
- Some commands to try are "ls" which shows a list of nonhidden files and directories, "cat" plus a directory creates a new file, "echo" plus text >> text file adds text to the end of a text file.
- You can also combine some commands like "ls - lat" or "ls -a" and compare the difference.

![try commands](tryCommands.png)<br /> 
<br />
<br />

### Moving files with scp
- To move files using the scp command, write them in this format, using the appropriate file name and your own username.
![scp](usingSCP.PNG)
- To check if this worked, you can connect to the host and use the command "ls" like this:
![scp2](usingSCPp2.PNG)<br /> 
<br />
<br />

### Setting an SSH Key
- To set up your ssh key, first type the command "ssh-keygen".
- Then, enter the file to save the key in, using your own username: (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa
- Then it will ask for a passphrase, do not type in a passphrase, just press enter.
- If you are on Windows, follow the extra ssh-add steps here [extra steps for Windows](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation).

- Now to copy the public key to the .ssh directory for your user account on the server, connect to the host, use the command "mkdir .ssh" and log out. Then use the command "scp /Users/<user-name>/.ssh/id_rsa.pub
cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys" using your username and account to copy over the key. 

![ssh key](sshKey.PNG)

- Now you should be able to connect without typing in a password like in this picture. <br /> 
<br />
<br />

### Optimizing Remote Running 
- One shortcut you can use when connecting to the server and using commands is by connecting to the server usnig the normal command then adding a command you want to run on the server in quotes. This way it will run the command on the server after you connect in the same line. 
![optimize](optimize.PNG)

- Another helpful tip, you can recall the last command that you ran by using the up arrow on your keyboard. 


