# Bandit Level 20 → Level 21 #

## Level Goal ##
<p>There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).</p>

## Commands you may need to solve this level ##
<pre>
ssh, nc, cat, bash, screen, tmux, Unix ‘job control’ (bg, fg, jobs, &, CTRL-Z, …)
</pre>

## Solve ##
<p>It appears that we have to provide any port and command line of previous bandit password it should give us next level password</p>
My plan here was to open netcat listener on localhost bandit20 on my port in new terminal session

![image](https://user-images.githubusercontent.com/85706972/166155902-97ef07f4-7660-46d0-b56a-355a9858191d.png)

<p>Now on other session terminal we just connect using binary and my port i setup on netcat and of course provide password</p>

![image](https://user-images.githubusercontent.com/85706972/166155955-10cd59be-d1ab-4aad-b078-bc5caa80033f.png)

![image](https://user-images.githubusercontent.com/85706972/166155964-810fa5d4-3de1-47fb-a87b-88e71148d586.png)

<p>We provided the password in one terminal and in other we see that it matched and we got next level password </p>

Password - gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr



