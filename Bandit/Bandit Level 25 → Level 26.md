# Bandit Level 25 → Level 26 #

## Level Goal ##
<p>Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.</p>

## Commands you may need to solve this level ##
<pre>
ssh, cat, more, vi, ls, id, pwd
</pre>

## Solve ##
<p>First we are going to check home directory for intersting files and there is sshkey for us to login as bandit26, but the shell is not /bin/bash</p>

![image](https://user-images.githubusercontent.com/85706972/166400391-3017c51b-717c-4b09-b3d8-a46a6cff760e.png)

<p>Lets try to login and see what happens when we do so</p>

![image](https://user-images.githubusercontent.com/85706972/166400444-10ba4718-363d-469e-8276-8c926d7b9347.png)

<p>Recived message that connection is closed, so we should do some re-search how to break out of it</p>

![image](https://user-images.githubusercontent.com/85706972/166401359-7d055127-5da7-4431-81df-e59dfb5940a7.png)

<p>I went to check the file that is set as the shell and its changing the terminal emulator to linux then it opens text.txt and exit is fairly obvious action.At first I also checked man pages for SSH and saw -t flag which sets pseudo shell, but that did not worked also
At this moment I'd no idea how we can possibly break from this as it executed when we login, so I went for other people writeups on this.
The solution is for this is very intersting way, I just think if there is any other way how to break out of this???</p>

<p>Anyway back to the solution, first thing we have to minimize the shell as small as possible and then try to connect using SSH</p>

![image](https://user-images.githubusercontent.com/85706972/166401925-3a3ff52a-09e2-4211-a781-f00ca3c032ae.png)

<p>This have opened up us a way to turn on vim editor and from there we can open /etc/bandit_pass/bandit26 password file</p>

![image](https://user-images.githubusercontent.com/85706972/166402146-ce65fed9-7d69-41c7-a9b1-8ae57b1983bf.png)


![image](https://user-images.githubusercontent.com/85706972/166402169-3829d4a9-052b-49fa-a4d7-3077bb32b002.png)

<p>This is something very new for me and very create who ever created this challenge</p>

Password - 5czgV9L3Xx8JPOyRbXh6lQbmIOWvPT6Z

