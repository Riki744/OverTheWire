# Bandit Level 12 → Level 13 #

## Level Goal ##
<p>The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!) </p>

## Commands you may need to solve this level ##
<pre>
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file
</pre>

## Solve ##

<p>Ok, we need to create new directory and copy the file which we are going to work with to get the next password</p>

![image](https://user-images.githubusercontent.com/85706972/166133488-70156ab1-1bd9-4625-b67e-710274cea3ee.png)

<p>We have created new directory and moved data.txt over there, now we can statr working with it</p>

![image](https://user-images.githubusercontent.com/85706972/166133511-c08cdbc2-f671-496a-be19-f0fe45045f11.png)

<p>By opening the file we see hexdump with ASCII text, nothing really useful for now </p>
<p>Now that I looked and command that we are given to solve this challenge I thought to go over manpages for xxd and there is -r flag that does the reverse for hexdump file</p>

![image](https://user-images.githubusercontent.com/85706972/166133708-1eb3496c-789b-41dd-a32d-edb7e9203a37.png)

<p>We got new output and nothing more, but so far it's human-unreadible, we should maybe transfere this into new file</p>

![image](https://user-images.githubusercontent.com/85706972/166133732-d6525377-d3c5-47e5-9f1b-c956ffb16215.png)

<p>Something new to us, now we have new lead that we should try to unzip the compressed file, but to do that we need .gz extension of the file, so I moved Bandit > Bandit.gz and tried to unzip it</p>

![image](https://user-images.githubusercontent.com/85706972/166133849-c08a882a-008f-4a5c-bb75-5adb01e73b37.png)

<p>Which now gives us new file type bzip2</p>
<p> This is again some type of compressed file type, so we need to mv Bandit > Banidit.bz2 and try to unzip it </p>

![image](https://user-images.githubusercontent.com/85706972/166133931-00d7a497-4d9b-4283-bb52-9f7f8608e92d.png)

<p>Back to the file type gzip and this time compressed data was "data4.bin" so we are moving forward, lets check the file and if nothing helpful lets do the same unzip process </p>

![image](https://user-images.githubusercontent.com/85706972/166133962-e5ff1b88-7516-46e6-b267-8811d766aa4b.png)

<p> New file type discovered, I assume that Bandit > Bandit.tar and we can try to extract it</p>

![image](https://user-images.githubusercontent.com/85706972/166134351-ef83798e-c14f-4886-a58a-17a5e79ec760.png)

<p> To extract the tar file I used following flags v-verbose, x-extract and f-create, now that we have new file and again we see tar archive so lets move data5.bin to tar extension</p>

![image](https://user-images.githubusercontent.com/85706972/166134386-36d1a821-558e-41eb-8ad7-c7ffc209ddcb.png)

<p>New file and this time it's bzip2 format, as we already worked with bzip2 we know what to do here...</p>

![image](https://user-images.githubusercontent.com/85706972/166134427-643b2a41-828c-42e8-bdcf-dc6e1e51bb82.png)

<p>Now data6.bin is in tar extension, will do the same procedure to get the flag hopefully</p>

![image](https://user-images.githubusercontent.com/85706972/166134478-285531ff-9d18-4352-8004-8fb7066944d8.png)

<p>Again new file and data8.bin need to be in gzip format</p>

![image](https://user-images.githubusercontent.com/85706972/166134501-cc9b3c84-a445-447f-a0b5-2e132741f01c.png)

<p>Finally we have unzipped all the chain and got the password for next level bandit</p>

Password - 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL




