The Bandit wargame is aimed at absolute beginners. It will teach the
basics needed to be able to play other wargames.

### Level 0

- This is straight forward

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f57d6da6-dbae-4063-877d-64dc245f90c9/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ce152b59-6f5a-4916-a0c2-65c2da59b712/Untitled.png)

We have successfully logged in as “bandit0”

By default ssh uses port TCP 22, so in this case we had to use -p flag to specify given port 2220

We can move into next challenge leve1

### Level 0

- First start off by locating the password file name “readme”

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fca18c20-bf6c-4af3-94b3-dd6c65d598d8/Untitled.png)

We have found two files and task says that it’s one home directory of bandit0, so let’s cat it out and use it to access the bandit1 user with password found

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a7d05286-e202-498b-9f72-65c1367f2c0f/Untitled.png)

We now can exit the bandit0 ssh connection and spin up new connection for bandit1 with same way as we did for Bandit0

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a9402072-54de-41c8-a4d1-9135636ac06b/Untitled.png)

Let’s move now to Level 2

### Level 1

This now get’s a bit spicy we need to find password file called (-) dash, but not that hard to do use the same find command in terminal and cat out the password

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8d086a4a-432f-4a5f-8562-4e241dd06763/Untitled.png)

CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

Let’s change the user to Bandit2 as we did before

### Level 2

Now we need to find password for next file called “spaces in this filename” 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/58da045a-5941-4c94-bfbe-cae9edc2ff03/Untitled.png)

This is a bit tricky as to see actual password from this file we need to set backslash (\) after each file space so it can be cat to terminal 

UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

### Level 3

This time we need to find the directory called “inhere”, we will adjust our find command a bit , pay attention what has changed

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/afaf5313-91f3-46b4-a0e8-cde1ffb4a5ea/Untitled.png)

We are now looking for directory called “inhere” and since it’s directory we can change directory with cd command to directory /home/bandit3/inhere 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1c517a0f-4b55-48d5-a1d0-5bf54ea5c158/Untitled.png)

There is our password for next bandit4 user - pIwrPrtPN36QITSp3EQaw936yaFoFgAB

### Level 4

We can use same command for find to find our directory , which I assume will probably on /home directory , but to be sure we can run it 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/65da108d-8792-4109-be53-f127c1e18a0b/Untitled.png)

Let’s change directory with bandit4 user , when we check the directory we have bunch of files from 0-9 and we need to look for password in one of these

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/81392d24-2ad6-4007-816a-f883d513651b/Untitled.png)

If we try to cat out one of these files we see that this is not human readable and also in order to cat it out, we need to use ./file as all files have (-) sign which plays wrong with terminal. 

Anyway I was starting to think that we can write one liner bash script that could print out all contents of files in this directory and bind it to the file 

After playing around we got all files content presented and we see the password for next challenge

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/059c44ca-7cc2-4978-b770-5eb2a609bfcd/Untitled.png)

password - koReBOKuIDDepwhWk7jZC0RTdopnAYKh

### Level 5

Seems like all tasks are under bandit home directory so we won’t spend time on find command anymore, so we can cd into inhere directory

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7a86aaf6-2ab4-403e-8e47-dcb71cdaab03/Untitled.png)

Our task for this one is to find file with password which has following properties:

- human-readable
- 1033 bytes in size
- not exe

This is bit tricky now as all files in this directory now are directories so we have to find one exact file , Following command find us the file with size of 1033bytes and we can cat it out to get the password 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ae6f89e6-7944-42b3-8bc0-8448401a4b4d/Untitled.png)

DXjZPULLxYr17uwoI01bNLQbtFemEgo7

### Level 6

Again we need to find a file where the password is stored in following file or directory “somewhere on the server” and have following properties: 

- owned by user bandit7
- owned by group6
- 33 bytes of size

This one was interesting, as I was not able to find the file at first , because I thought that the name of the file is “somewhere on the server” , but instead I had to just use given properties and then found the password

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f8ebb48d-34fd-479d-8c37-ea68c0a0e2d9/Untitled.png)

HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

### Level 7

The password for the next level is stored in the file **data.txt**
next to the word **millionth**

- First we need to find the data.txt
- Then we can use grep to look for word millionth and maybe pipe it to give as more characters with this word
1. data.txt exists on home directory of bandit7
2. If we check the content of the file we see that there are possible usernames and passwords

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d25ed90c-90a1-44e9-866a-b06a1cb1c42d/Untitled.png)

1. If we now cat out the data.txt and use grep to look for word “millionth” it should give us the password “cvX2JJa4CFALtqS87jk27qwqGhBM9plV” 
2. Let’s try to login to bandit8, which turns to be successful 

### Level 8

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

- File once again is on home directory, but now we need to cat out the content of data.txt and pipe it to one liner which will be the next user password, but this password happens to be written only once
- We can check that with sort function where we see that many strings are presented more than one time

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ee6f914f-f13c-4b24-8d99-2a2c1f707f0e/Untitled.png)

- First we sort data.txt which will show us lines that are more than one time by sorting them in order, then we can pipe it out to uniq -u to give us only one time line, which should be the password  (UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR)

### Level 9

The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

- File is on home directory and now we need to look for human readable string which comes before “=” sign.
- If we simply write following command

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0d647af7-a6b6-4822-9ada-c88c3b54835e/Untitled.png)

We got many options which are precede with “=” sign , so we can try to login into next bandit user and try one of the found passwords

the correct one was  - truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

### Level 10

The password for the next level is stored in the file data.txt, which contains base64 encoded data

- We can use simple command with flag -d which will decode the file

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4da78c79-65ac-4bba-bade-76f3499bff64/Untitled.png)

IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

### Level 11

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

- This challenge sounds like encryption method of ROT13
- We can create quick bash command that would help us to decrypt the data.txt and turn file into readable password for us

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0b4213d1-d3b8-4b18-8bd6-6e6ff545cae7/Untitled.png)

5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

### Level 12

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/719f52b1-cfbb-4256-8967-73cc57678c44/Untitled.png)

- Created new directory and copied data.txt to my created directory
- Now we have renamed file bandit and we can use xdd -r and output it to the file

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bba27dc5-295d-478a-ae6d-7b4b8814e714/Untitled.png)

- since file was compressed we revert file to previous version and got now gzip compressed data

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8fdce6fb-084d-4146-9e36-b11e7d6a55fd/Untitled.png)

- We renamed file with .gz extension this helped us to unzip the file and got new filetype bzip2

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/47e962b4-3ee6-42fd-9719-9f117bb82083/Untitled.png)

- Used bzip2 decompress function to get a new file, now we can check what type of file it is

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/037766e4-3782-4c7b-a788-ea3f578bfcc8/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7bfc70c9-ec6d-450b-a038-67b7d133fb65/Untitled.png)

- First we need to add gzip extension so we can use gunzip to unzip it and check new file once more which is POSIX tar archive

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5df2fff9-9567-4c51-93df-e8d40be2933b/Untitled.png)

- tar command with flag v - verbose x-extract f-create , gave as new file data5.bin and this looks same file type so we can use same tar command

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1b7476f7-dea4-4a07-9053-a55511046ea3/Untitled.png)

- data6.bin is what we got from data5.bin and it is bzip2 file so we can use previous command we used before

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1d5d57ed-b9e0-4cc8-bcc2-0bed0df17b22/Untitled.png)

- Another tar archive

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d46609f0-cf42-462e-a74d-04dc9536558a/Untitled.png)

- We need to move the data8.bin to .gz extension so we can unzip it again

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dde5397b-0206-449b-b29e-b2690289fc60/Untitled.png)

- After unzipping the data8.bin.gz we have data8.bin file which is ASCII text and we if cat it out we have finally found the password for next bandit

8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

### Level 13

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/af2bddd9-910b-4d2f-8f35-bbe2f06ce64f/Untitled.png)

[https://help.ubuntu.com/community/SSH/OpenSSH/Keys](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)

- As the task informs us that password for next task is at specific location but that can be viewed by Bandit14, and we are given private key of next level that can be used to login. Private SSH key is used to login from device and public key is used to login to device, where the key is stored under location “.ssh/authorized_keys”
- With following command we specify [localhost](http://localhost) as machine we are working with and -i for the rsa key file

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5659e1b9-5e4a-4947-be2b-2a2b842657f2/Untitled.png)

We can now check the content of /etc/bandit_pass/bandit14

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/48698453-7166-4133-aa99-8c0a311d884c/Untitled.png)

4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

### Level 14

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d15f5010-e15b-42f0-896c-de1fda1ffcba/Untitled.png)

- First we need to identify the current machine IP address, that can be done by command hostname -I
- After that we can simply use host IP and port in the task then provide the password for the current user and we are presented with next bandit password

BfMYroe26WYalil77FoDi9qh59eK5xNr

### Level 15

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

To complete this challenge we need to use openssl command like this : 

```jsx
openssl s_client -connect localhost:30001 -ign_eof
```

This shows us all information and in the end if you give current user password we got new password string for next level 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eb606131-0fc5-4c46-a3fd-d246d6a76481/Untitled.png)

cluFn7wTiGryunymYOu4RcffSxQluehd

### Level 16

The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

1. First we run nmap scan on [localhost](http://localhost) between those ports

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9e4a9790-8520-4d2c-9301-3957d9a408f7/Untitled.png)

1. We identify that port 31790 should be the one who could gave us password if we connect to it with openssl as we did in previous task

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5d80a3a1-a586-4500-9b32-bfaedfa6980b/Untitled.png)

We got RSA private key which we can save and try to login as Bandit17

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4c01b688-ee98-42ea-8f38-23b0d5f93956/Untitled.png)

We saved the key in id_rsa , gave it proper rights and added -i flag to give private key for ssh 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2652ff8b-4829-4eac-ae92-3eac6168b352/Untitled.png)

We are now logged in as bandit17 and can move to next challenge 

### LEVEL 17

There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/33f7a120-19d2-4df6-b894-1fcc500817c8/Untitled.png)

Used command diff which check line by line from two given files and I assume that password is one of these, so we can try both and see if we get in. 

kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

w0Yfolrc5bwjS4qw5mq1nnQi6mF03bii

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dcfcfdba-b0e5-4880-8521-0b1c4ec8a368/Untitled.png)

As the notes says if we see ByeBye we have solved this level and this also is related to next level19

### Level 18

The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

What we can do is log back in to user bandit17 and try to change users with su command and see if we can get in that way and get password for next user , but that did not worked out 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3b967bfc-ebb1-41cf-854e-63caf367c437/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9e4686a4-4a24-44dc-9e5b-d8cd7adf97e8/Untitled.png)

I wasn’t sure how to complete this challenge until I found that we can print commands also, so we don’t need to be fully in to get any content, so this gave us new password for level19

IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

### **Level 19**

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

SETUID - set user ID , allow users to run an exe with the file system permission, these often are used to perform specific tasks or run application with elevated privileges. 

more on this link - [https://www.liquidweb.com/kb/how-do-i-set-up-setuid-setgid-and-sticky-bits-on-linux/](https://www.liquidweb.com/kb/how-do-i-set-up-setuid-setgid-and-sticky-bits-on-linux/)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/abe16811-3693-4784-97c5-c15fff02208b/Untitled.png)

This SETUID binary file allows us to execute command which we don’t have permission on, so if we check /etc/bandit_pass/bandit20 we don’t have permission in normal way

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bbeea9ef-3502-4acc-87f9-36246e3383f4/Untitled.png)

By executing binary file we should get the password now

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7724d3e3-f26d-4b2c-ac96-0ff1578828dc/Untitled.png)

There we go , we have the password

GbKksEFF4yrVs6il55v6gwY5aVje5f0j

### **Level 20**

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/045772b4-b307-4bdc-9533-533dac291d5b/Untitled.png)

what we can do here is that if we open netcat listener on port 8888 and use verbose flag 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7fdfbe76-b825-4acc-8a25-97232feb1744/Untitled.png)

it is going to listen on port 8888 and now we can use that file in our home directory and specify the netcat port 8888

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dca632d8-791a-4cff-96ec-a0dbb6fcdf4b/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2dd09bc9-c7a8-4a0d-8eaa-5d8f27abb865/Untitled.png)

We see that connection is made and by now if we provide current bandit password it should give us new password for next challenge

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4ef15a3e-3bdd-4428-95bf-e15f424ebdd7/Untitled.png)

Done, new password acquired  = gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr

### Level 21

A program is running automatically at regular intervals from
**cron**, the time-based job scheduler. Look in **/etc/cron.d/** for
the configuration and see what command is being executed.

By investigating the /etc/cron.d/ which is a directory we see following files 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8b9dd241-9686-425d-a0a5-86059d91da48/Untitled.png)

cronjobs are like scheduled task in windows OS, so let’s open Bandit22 cronjob and see what information it gives to us

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/61dc0397-7c94-434d-ab29-883d69f1dc43/Untitled.png)

By checking the bash script it gives us the password for the next 

Bandit22 = Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI

### Level 22

A program is running automatically at regular intervals from
**cron**, the time-based job scheduler. Look in **/etc/cron.d/** for
the configuration and see what command is being executed.

**NOTE:** Looking at shell scripts written by other people is a
very useful skill. The script for this level is intentionally made
easy to read. If you are having problems understanding what it does,
try executing it to see the debug information it prints

Let’s do the same as we did for last challenge, we can inspect the directory of  **/etc/cron.d/**

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/167fc3d6-7a86-41a6-9ef0-fe00746163f9/Untitled.png)

This far we have identified the location of the script which might give us the next level password, it looks like the script takes output of myname variable and created MD5 hash, which then is cut for spaced and -f to get rid of - sign, if we try to do it manually we can find already created file for next level bandit

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3aed928f-add7-4802-903a-c603de160d39/Untitled.png)

Bandit23 = jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n

### Level 23

A program is running automatically at regular intervals from
**cron**, the time-based job scheduler. Look in **/etc/cron.d/** for
the configuration and see what command is being executed.

This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8b60a8ff-01ef-4223-989d-9d0291386c87/Untitled.png)

If we go line by line, we know that it will move to directory of var/spool/bandit24, then it says that it will execute and delete all scripts in this directory , so what we can do is try to place new script in this directory which will be executed, since first line of do command is skipping the directories which starts with . and .. , also we need to give everyone read and write permission to /tmp/riki3 folder + we need to mark it as executable 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f367fe40-f713-4f14-a3f2-3662d5e3ab3a/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ab238cf1-54a0-4adb-91e4-7de8768793f4/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7e21e2d4-4ebd-4ba7-b4bd-59d9934e5f15/Untitled.png)

bandit24 = UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ

### Level 24

A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2ffc412c-9f5f-4e7b-9f81-7343528f6619/Untitled.png)

Deamons on Linux are processes or Services like on Windows, Here is our running process, which as said is listening on [localhost](http://localhost) port 30002 , it will ask for this bandit24 password + 4digit pincode which we need to bruteforce , This required additional script  

```python
#!/bin/bash
touch f.txt
for i in {0000..9999}
do
echo "UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i"
done | nc localhost 30002 > f.txt
```

```python
cat f.txt | grep -v Wrong
```

Simple bash loop script helped us to give the bandit24 and go through of combinations of 4-digits and get us next user password 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4a04e844-0afe-48c6-b3b8-dcec460b81b9/Untitled.png)

bandit25 is uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG

### Level 25

Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

First we can check /etc/passwd file and grep the bandit26 to see what kind of a shell it is, if it is not /bin/bash 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dd9ec031-6da7-4f77-87a1-34c5cb00dd9d/Untitled.png)

Its /usr/bin/showtext , but thats not really a shell , also in bandit25 we have sshkey for bandit26, so let’s try to check if we can log with ssh using this key

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f21ace82-d4b2-440a-9588-1fc2b5c34ecb/Untitled.png)

but after executing the command it kicks us back to bandit25 and connection closed to bandit26, lets now actually try to lookup for the showtext shell under /usr/bin 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/da219ff7-0b5f-4a60-b086-d7cbecd7f75e/Untitled.png)

Interesting is that the showtext shell is bash script which will set the terminal = linux , and the default is xterm, from googling I found following statement:

“TERM=linux means that you're supposedly going to be using Linux console, so the output will be minimalistic” so the linux terminal don’t work the same way as xterm for fully functional shell, what if we try to minimize the shell ? 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e5d8997c-4343-4621-b78c-af6cfc04229c/Untitled.png)

now if we click just a v button it will open vim editor and by simply writing following vim command it will open the password file : 

```python
e: /etc/bandit_pass/bandit26
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c2ff23ba-f26f-43d2-8df3-c82c33cf2a05/Untitled.png)

bandit26 - 5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z

We got the password but this won’t let us spawn the shell, with vim we can also set the shell back to /bin/bash and try to get working shell 

:set shell=/bin/bash and then :shell command gives us working shell 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f7559125-be4e-4bc9-923d-e506a7e395a8/Untitled.png)

This was great out-of-the box challenge which I had to google to find the way to complete, but new lesion learned 

### Level 26

Good job getting a shell! Now hurry and grab the password for bandit27!

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/06c6259f-38c8-4949-864d-ea6666b0f8cd/Untitled.png)

We have Bandit27-do file under home directory , if we check the file type it looks to be ELF binary file which have some function (ELF - Executable Linkable Format), it looks to be executable file and if we try to execute it gives us message 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/72aa742d-73b1-4073-a821-999d76496424/Untitled.png)

The file is also running with Bandit27 permissions and we have permission to execute it 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eac95558-7424-4b57-b329-4510c5707d45/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/203d7f83-cfff-4650-8f8f-84ab7e42dcfd/Untitled.png)

we are able to run command as bandit27 and get this user password 

bandit27 - 3ba3118a22e93127a4ed485be72ef5ea

### Level 27

There is a git repository at ssh://bandit27-git@localhost/home/bandit27-git/repo. The password for the user bandit27-git is the same as for the user bandit27.

Clone the repository and find the password for the next level

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2fedfb57-a946-4e43-aa6c-73a887f3a8c4/Untitled.png)

First I checked if we have git installed, now that we know the git is installed we need to find the proper command so that it is run as bandit27-git in order to clone it on home directory of bandit27

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7de649c3-94f9-4393-add9-f0eff55bb9ae/Untitled.png)

I went to tmp folder and created my own directory then moved to it and cloned the local repo to this folder so we are able to check it, I removed the ssh:// as it seemed to need to provide from where we are cloning and what we are cloning and by default it was doing it over ssh and asked password for bandit27-git which is the same as bandit27

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6f833de9-eb8c-48a1-9de8-b6a77bddea12/Untitled.png)

Bandit28 - 0ef186ac70e04ea33b4c1853d2526fa2

### Level 28

There is a git repository at ssh://bandit28-git@localhost/home/bandit28-git/repo. The password for the user bandit28-git is the same as for the user bandit28.

Clone the repository and find the password for the next level.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5bb270d7-14ab-4289-87b6-ee7dd112452e/Untitled.png)

We do the same as the last challenge, so now lets over the repo and try to find the password

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/61e27a99-7f7e-42bc-b3a1-ef8a37f890f7/Untitled.png)

we got notes for level29 but password seems to be bunch of x strings , but its not the password, so we have to keep looking for it, as the password should be under repo path, I’ve found that there is possibility to use log function of git which shows the actions done and possible differences with -p flag 

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/074ce6d7-8763-4daa-863f-a97e8f83ca73/Untitled.png)

as soon as we write new command we have the difference which is the password for next level 

bandit29 - bbc96594b4e001778eee9975372716b2




