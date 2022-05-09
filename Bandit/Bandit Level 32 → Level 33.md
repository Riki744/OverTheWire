# Bandit Level 32 → Level 33 #

<p>After all this git stuff its time for another escape. Good luck!</p>

## Commands you may need to solve this level ##
<pre>
sh, man
</pre>

## Solve ##
<p>Alright, we no have to escape to get the password for the next challenge, from the login we can see that this is some UPPERCASE SHELL</p>

![image](https://user-images.githubusercontent.com/85706972/167013901-4b75a1c1-b8b3-4931-ad24-2ef9ce7ef07b.png)

<p>At first I was trying to look at the shell and see what commands are allowed to be run and it appeard that all of the commands were not found</p>

![image](https://user-images.githubusercontent.com/85706972/167480204-9b1824c7-bad7-4723-b5e4-08610bdfd6dd.png)

<p>Basically I was trying everything, and also went for re-search and to see how to escape restricted shells and the lucky finding for me was following characters</p>

<pre>
$0 returns the name of the running process. If used inside of a shell it will return the name of the shell.
</pre>

<p>This popped me a new shell and I was able to execute commands, so I went for vim to upgrade the shell</p>

<pre>
:set shell=/bin/bash
:shell
</pre>

![image](https://user-images.githubusercontent.com/85706972/167480526-5858c10a-490e-41cf-8a83-d468b5fffcca.png)

<p>Since we are able to execute commands now, I went to get the password for Bandit33</p>

![image](https://user-images.githubusercontent.com/85706972/167480812-cd672335-3e30-46f7-9f1e-9926217df2e0.png)


Password - c9c3199ddf4121b10cf581a98d51caee
