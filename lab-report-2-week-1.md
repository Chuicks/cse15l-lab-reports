# **Week 1 Lab report**



## *Installing VScode*
![Installing VScode](/week1-screenshots/cse15l-week1-step1.png)
VScode is a code editor and I already had it before this course. You download it off of the VScode website.
<br />

---
## *Remotely Connecting*
![Remotely Connecting](/week1-screenshots/cse15l-week1-step2.png)
By using ssh command you can connect to remote computer.  
`ssh cs15lfa22ta10@ieng6.ucsd.edu`
<br />

---
## *Moving Files with `scp`*
![Moving Files with `scp`](/week1-screenshots/cse15l-week1-step3.png)
The `scp` command allows you to be able to copy a file from your local computer to another computer or server in this case.
Keep in mind that after using `scp` you still have to login to the remote computer to access the file you copied over.  
`scp WhereAmI.java cs15lfa22ta10@ieng6.ucsd.edu:~/`     
The `:~/` part of the command shows where to copy the file to on the remote computer. In this case `~` means that it is copied to the home directory of the remote computer.
<br />

---
## *Setting an SSH Key*
![Setting an SSH Key](/week1-screenshots/cse15l-week1-step4.png)
By using `ssh-keygen` (local) , `mkdir .ssh` (remote),                                      
 `scp /Users/hotw/.ssh/id_rsa.pub eyzhang@ieng6.ucsd.edu:~/.ssh/authorized_keys`(local)         
 it allows you to store your key on your computer and essentially bypass the password system.
 So you are able to access your remote computer without having to input your password everytime
<br />

---
## *Optimizing Remote Running*
![Optimizing Remote Running](/week1-screenshots/cse15l-week1-step5.png)
I was able to optimise remote running by using no password and also running commands on my remote computer via my `ssh` command.
So I was able to run everything with 3 keystrokes.
<br />




