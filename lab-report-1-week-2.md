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





