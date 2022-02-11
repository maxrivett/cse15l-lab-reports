# Lab Report 3, Week 6

*In this lab report I will be showcasing how I streamlined my ssh configuration on my computer. This speeds up the process of accessing a remote server/computer.*
<br><br>
To begin, I changed my directory to `.ssh`:
![cd .ssh](/images/labreport3/pic1.png)
<br>
As you can see, I already have the `config` file since I've done this before, but let's pretend it's not there.
<br>
In order to create the `config` file, I used the command `touch config`:
![touch config](/images/labreport3/pic2.png)
<br>
This creates a new file called config, which I then open using the command `open config`:
![open config](/images/labreport3/pic3.png)
<br>
Once it was open, I added text to make it look like this:
![tconfig file](/images/labreport3/pic4.png)
<br>
This means that my shortcut is `ieng6`, so that is all I need to type after `ssh` rather than `ssh cs15lwi22ahc@ieng6.ucsd.edu` which is a lot to type everytime I want to ssh into the remote computer.
<br><br>
So, it is now **this** easy to access the remote server:
![accessing](/images/labreport3/pic5.png)
<br>
Now we can also very easily securely copy (or `scp`) files into the remote server, as seen here:
![scp](/images/labreport3/pic6.png)
<br><br>
*Thank you for reading and I hope this helps!*