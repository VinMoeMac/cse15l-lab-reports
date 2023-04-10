# CS15l Login Tutorial
## Step 1: Installing VScode
- To install VScode the first thing you must do is go to the VScode website [here](https://code.visualstudio.com/).
- The page should look like this:

![Image](vscodescreen.png)

- Press the download button for whichever operating system you are using and you should be able to open and use it.

## Step 2: Remotely Connecting
- If you're on windows you must first use this [link](https://gitforwindows.org/) to download and install Git for Windows.
- You can refer to this [link](https://stackoverflow.com/a/50527994) to start using git for windows.
- Now that everything is set up you can use ssh in the bash terminal to __remotely connect__ to your cs account.
- In the bash terminal input `ssh cs15lsp23zz@ieng6.ucsd.edu` after the $ Character. (replace the zz in the username with your specific characters in your CS username.
- It should look like this:
![Image](login.png)
- Input the password in the terminal and you will remote connect.

## Step 3: Trying Some Commands.
- Now the final step is to try some commands in the console.
- Here is a few you could try:
```

- cd ~
- cd
- ls -lat
- ls -a
- pwd

```
- In the following screenshot I tried `ls -lat` and `pwd` (FYI I am not running it from the cs account because it says that the account is closed by remote host)

![Image](command.png)

You can try any number of commands at the terminal and see what they do!
