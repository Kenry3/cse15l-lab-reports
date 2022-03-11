# Hi! Welcomed to the totorial for Remote Access and the Filesystem!

## Part 1: Install Visual Studio Code

>Visual Studio Code is a source-code editor with features including support for debugging, syntax highlighting, intelligent code completion, snippets, code refactoring, and embedded Git. And this is the tool I use to create this website!

*Go to the Visual Studio Code website https://code.visualstudio.com/, and follow the instructions to download and install it on your computer. If you need extra help, you can also watch this [Video Guideline.](https://www.youtube.com/watch?v=tCfbi5PF1y0)*

### If you install successfully and open it, you should see interface like this: 

![Image](/image/vsc.png)

----
## Part 2: Remotely Connecting

>SSH, also known as Secure Shell or Secure Socket Shell, is a network protocol that gives users, particularly system administrators, a secure way to access a computer over an unsecured network.

*To get basic understanding of ssh, you can watch this [video demonstration.](https://www.youtube.com/watch?v=z7jVOenqFYk)*

*To connect to the server, you should type*
<span style="background-color:cyan">```ssh + ip address of the romote server```</span> *like this:*

<span style="background-color:cyan">``````$ ssh cse15lwi22awk@ieng6.ucsd.edu``````</span>

*After you successfully log in. you should see something like this:*

![image](/image/sshlg.png)

*Now you are connecting to the romote server!*
_____

## Part 3: Trying Some Commands

>In computing, a command is a directive to a computer program to perform a specific task.

*There are some basic commands you should try out:*

* <span style="background-color:cyan">```cd``` </span>
* <span style="background-color:cyan">`cd ..`</span>
* <span style="background-color:cyan">`ls` </span>
* <span style="background-color:cyan">`pwd` </span>
* <span style="background-color:cyan">`rm` </span>
* <span style="background-color:cyan">`mkdir`</span>

*To learn more about commands and their applications, watch this [video.](https://www.youtube.com/watch?v=ogWoUU2DXBU)*

----

## Part 4: Moving Files with scp

>Secure copy protocol (SCP) is a means of securely transferring computer files between a local host and a remote host or between two remote hosts.

*To copy your local file to the romote server, you should type <span style="background-color:cyan">```scp + the file you want to copy + ip adress of the server```</span> like this:*

<span style="background-color:cyan">```scp WhereAmI.java cse15lwi22awk@ieng6.ucsd.edu:~/```</span>


----

## Part 5: Setting an SSH Key

>Ssh-keygen is a tool for creating new authentication key pairs for SSH. Such key pairs are used for automating logins, single sign-on, and for authenticating hosts.

*To generate the key, you should type* <span style="background-color:cyan">```ssh-keygen``` </span> *in the terminal, then you can see this shows up* 
![](/image/keygen.png)

*This created two new files on your system; the private key (in a file id_rsa) and the public key (in a file id_rsa.pub), stored in the .ssh directory on your computer.*

*Now we need to copy the public (not the private) key to the .ssh directory of your user account on the server. And here are the steps you should follow:*

1. use <span style="background-color:cyan">```ssh``` </span>```ssh``` login the server
2. type <span style="background-color:cyan">```mkdir .ssh``` </span> in the terminal
3. logout the server
4. type <span style="background-color:cyan">```scp /Users/kenry/.ssh/id_rsa.pub cs15lwi22awk@ieng6.ucsd.edu:~/.ssh/authorized_keys``` </span>, where you should use your username and the path you saw in the command above
5. then you can login in without entering password

----

## Part 6: Optimizing Remote Running

>Be more efficient!

*There are lots of ways to make command line more efficient! For example:*

* If you don't want to type the whole file name, you can use your <span style="background-color:cyan">```tab``` </span> on your key board 

* If you want to write a command that you ran before, you can use <span style="background-color:cyan">```up-arrow``` </span> on your key board you find that command, and type <span style="background-color:cyan">```history``` </span> may help you with that!

* You can write a command in quotes at the end of an <span style="background-color:cyan">```ssh``` </span> command to directly run it on the remote server, then exit. For example, this command will log in and list the home directory on the remote server:
<span style="background-color:cyan">```$ ssh cs15lwi22awk@ieng6.ucsd.edu "ls"``` </span>

* You can use semicolons to run multiple commands on the same line in most terminals. For example:
<span style="background-color:cyan">```$ cp WhereAmI.java Hello.java; javac OtherMain.java; java WhereAmI``` </span>

**Without these skills, I need to type every character to log in to the remote server and click enter every time I type any command. To finish the whole process of loging in to the romote server, listing files, printing directory, and loging out, it needs 43 keystrokes**

![](/image/ef.png)

**Combining these skills, I only need 9 key strokes to finish the whole process!**

![image](/image/keystroke.png)

*What you should do is to keep learning and asking questions! There are some [videos](https://www.youtube.com/watch?v=cXuXij68DtE) teaching you how to use command line more efficient!* 
