# Week 1 Lab Report
## Dylan Atianzar A17609722
This is a tutorial on how to remotely access UCSD computers.
Let's start by looking up the course-specific `ieng6` account by going to this [link](https://sdacs.ucsd.edu/~icc/index.php).

Submit your credentials in these boxes:
![Link](https://user-images.githubusercontent.com/69043855/212187259-595af290-5ad1-4137-911e-56363e1d9968.png)

Then, there should be a button that says **cs15lwi23xxx** or similar. The *xxx* being letters specific to you.
This is your account name for remote access. If you've forgotten your password, learn how to reset it [here](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit).

---
# VSCODE Installation
In order to install VSCODE, visit this website to download the VSCODE installer: [https://code.visualstudio.com/](https://code.visualstudio.com/). 
Download the appropriate installer for your system, and the installer will have instructions once you run it.

After installation, VSCODE should look similar to this.
![Link](https://user-images.githubusercontent.com/69043855/212566904-b01d451d-5e5d-47a6-b194-7ae73415397c.png)

*PS:* The colors might be different because I run my VSCODE in **dark mode**. Otherwise, it should look generally the same.

---
# Remote Connect to a Remote Server
This is for course-specific accounts.

If you are on Windows, you **must** download git for Windows from [here](https://gitforwindows.org/). This provides some tools we need.
Then, go to [this](https://stackoverflow.com/a/50527994) to use git bash in the terminal of Visual Studio Code.

From here on, the commands will be run in the terminal now.
To begin a connection to the server, type "ssh (course-specific account)" in this case:
`ssh cs15lwi23xxx@ieng6.ucsd.edu`
 
If it is your first time connecting to the server from your device, this prompt will appear:
  
```
The authenticity of host 'ieng6.ucsd.edu (128.54.70.238)' can't be established.
RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])?
```
  
This is prompt is expected for the first time, therefore, type yes and press enter.
*Note:* It is concerning if this prompt appears when you are connecting to a server that you connect to **often**. As explained by [Ben Voigt](https://superuser.com/questions/421074/ssh-the-authenticity-of-host-host-cant-be-established/421084#421084).
  

Type your password when prompted to; however, be aware that your password does not show as you type it. Therefore, if your password is complicated, type it slowly.

Once connected, a bunch of text like this should pop up showing that you are connected to the server.
![Link](https://user-images.githubusercontent.com/69043855/212568317-c2821444-1fe9-4cc9-a7aa-f116590840fc.png)

You are now connected to the server, and it is ready to use!

---
# Trying commands in Remote Server
Simply run some commands in terminal in order to use the connected server.
In this case, I will run
`ls` to list the items in the current directory
`mkdir test` to make an empty folder
`pwd` to show the current directory
`cd test` to change current directory to the new folder

It is shown like this:
![Link](https://user-images.githubusercontent.com/69043855/212568782-04a2687a-8990-49b8-9e15-81e327b676c3.png)

You can use Ctrl-D or the `exit` command in order to log out from the remote server.
