Logging on to TACC
==================

While projects and allocations are managed through the TACC user portal, most interactions with TACC resources will occur on the command line. This will require a basic understanding of Unix commands. If you are on a Mac, you can use the Terminal application (found under Utilities). On Windows, you can install [Git BASH](https://git-for-windows.github.io) for a shell emulator that includes most basic Unix commands (plus, git software is installed too, which is awesome if you're interested in version control).

To access Stampede, open Terminal or Git BASH. Type the following command, where `USERNAME` is your personal username for TACC:

```
ssh USERNAME@stampede.tacc.utexas.edu
```

The command `ssh` stands for "secure shell," which is a program that can securely connect you to a remote computer.

Hit "Enter" to run the command. The first time you log on to Stampede, you may see a message like this:
```
The authenticity of host 'stampede.tacc.utexas.edu' (...) 
can't be established. RSA key fingerprint is (...)  
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'stampede.tacc.utexas.edu,
129.114.50.163' (RSA) to the list of known hosts.
```
It is generally safe to answer "yes," as this is a report that tells you that you've not logged on before. You will not be prompted again.

Next, you will be prompted to enter your password. Type in your password. You won't see any characters entered on your screen, but don't worry, your password is still being registered! If you fail to enter the correct password three times, your login attempt will be cancelled. 

After successfully logging in, a standard login message will print to your screen (this will occur every time you log in). Starting from the top (you will probably have to scroll up), you will see the following pieces of information:
* date and time of last login (including IP address)
* welcome message
* reminder of guidelines and policies for use
* contact information for problems and questions
* links to documentation and user news
* system notes with basic infomation on job submission, software loading, and file systems (places where you can store files)
* project balances (SUs allocated to you for each registerd project)
* disk quotas (how much disk space is being used by your files, compared to your quota)
* helpful tips about using TACC

At the very bottom, you will see your command prompt, `$`, indicating that you are ready to start working on the command line.

You can also visit [this page](https://cvw.cac.cornell.edu/environment/LoggingOn?AspxAutoDetectCookieSupport=1) to learn how to connect to Stampede from a Windows machine using PuTTY.
