# **Week 1 Lab report**



## *Installing VScode*
![Installing VScode](/week1-screenshots/cse15l-week1-step1.png)
<br />
VScode is a code editor and I already had it before this course. You download it off of the VScode website.
[Link to download](https://code.visualstudio.com/)
<br />

---
## *Remotely Connecting*
![Remotely Connecting](/week1-screenshots/cse15l-week1-step2.png)
<br />
By using ssh command you can connect to remote computer.  
`ssh cs15lfa22ta10@ieng6.ucsd.edu` .
It will prompt you to enter a password for your account and then it will log you into the user.
"Hello cs15lfa22od, you are currently logged into ieng6-201.ucsd.edu"
will be printed on the terminal when you log in successfully.
<br />

---
## *Trying some commands*
![Trying some commands](/week1-screenshots/cse15l-week1-step6.png)
<br />
I tested some of the commands given to us and the screenshot shows me trying
 - `cat /home/linux/ieng6/cs15lfa22/public/hello.txt`
 
`cat` prints out all of the contents of the file which in this case is hello.txt .
- `ls`

`ls` is used to display all public elements in the current directory. We are currently in the home directory of the remote computer. It contains some java files, some class files, a .txt file and perl5.
- `ls -a`

`ls -a`     displays all of the directories and files stored in the current directory, including the hidden ones.

 
<br />

---
## *Moving Files with `scp`*
![Moving Files with `scp`](/week1-screenshots/cse15l-week1-step3.png)
<br />
The `scp` command allows you to be able to copy a file from your local computer to another computer or server in this case.
Keep in mind that after using `scp` you still have to login to the remote computer to access the file you copied over.  
`scp WhereAmI.java cs15lfa22ta10@ieng6.ucsd.edu:~/`     
The `:~/` part of the command shows where to copy the file to on the remote computer. In this case `~` means that it is copied to the home directory of the remote computer.
<br />

---
## *Setting an SSH Key*
![Setting an SSH Key](/week1-screenshots/cse15l-week1-step4.png)
<br />
By using 
- `ssh-keygen` (local) 
- `mkdir .ssh` (remote),                                      
- `scp /Users/hotw/.ssh/id_rsa.pub eyzhang@ieng6.ucsd.edu:~/.ssh/authorized_keys`(local)         
 it allows you to store your key on your computer and essentially bypass the password system.
 So you are able to access your remote computer without having to input your password everytime.
<br />

---
## *Optimizing Remote Running*
![Optimizing Remote Running](/week1-screenshots/cse15l-week1-step5.png)
<br />
- the first `scp` command copies the WhereAmI.java file from my computer onto the remote computer
- the next command, `ssh` compiles the WhereAmI.java file on the remote computer using my computer
- the second `ssh` runs the complied WhereAmI.java file on the remote computer using my own computer

I was able to optimise remote running by using no password and also running commands remotely via my `ssh` command.

So I was able to run everything with 3 keystrokes.
<br />




