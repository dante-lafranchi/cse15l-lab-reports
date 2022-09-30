# Lab Report 1 Week 1

## Step 1:
I already had Visual Studio Code installed but I remember it being a pretty easy process. VS Code is free and there are many tutorials on youtube to help you learn all about the different features in VS Code.
![Image](VSCode-home-page-SS.png)
![Image](New-VSCode-terminal-SS.png) 

## Step 2
I had a lot of trouble remotely connecting to the other computer. I had to reset my password four times, but it was a great feeling when the my password was finally accepted. Once logged in, the terminal displayed the clusters on the remote computer that I was logged into and how much of their power I was currently using (basically nothing at this point).
![Image](remotely-connecting.png)

## Step 3
I ran the "ls -a" command which displayed the names of all the files in the current directory and the names of the hiddne files. I ran the "pwd" command which displayed the current the path to get to the current directory. I used the "cat" command to display the contents of a file "hello.txt" on the remote computer.
![Image](running-some-commands.png)

## Step 4
I used the "scp" command to move a .java file I had on my local computer to the remote computer. I used the "javac" command to compile the file and then I used the "java" command to run the file. When the file ran, the terminal displayed some facts about the remote computer: the operating system, the username, the home directory, and the current directory. I exited ssh and ran the same file on my local computer, and you can see how the operating system, username, and directories were all different.
![Image](moving-file.png)
![Image](compiling-and-running-moved-file.png)
![Image](running-file-locally.png)

## Step 5
To use the "ssh" and "scp" commands without a password, I ran the ssh-keygen program on the local computer which created a private key (stored on local computer) and a public key (to be stored on remote computer). Then, I logged into the remote computer and created a new directory called authorized_keys using the "mkdir" command. I logged out and the used the "scp" command to move the file with the public key, id_rsa.pub, to the authorized_keys directory in the remote computer. After this, I was able to use the "ssh" and "scp" commands with no password.
![Image](running-ssh-keygen.png)
![Image](creating-authorized_keys-directory.png)
![Image](moving-public-key-file.png)
![Image](using-ssh-with-no-password.png)

## Step 6
