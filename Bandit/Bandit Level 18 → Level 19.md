# Bandit Level 18 → Level 19 #

## Level Goal ##
<p>The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.</p>

## Commands you may need to solve this level ##
<pre>
ssh, ls, cat
</pre>

## Solve ##
<p>As we know that from previous challenge when we try to login using SSH we got loged out instantly, from given commands we have only 3 options here, maybe it's possible to use SSH to login and at the same time execte another command</p>

![image](https://user-images.githubusercontent.com/85706972/166154997-972d85aa-86de-4186-9dbe-d7615d9c46a0.png)

<p>Simply by writing the cat for readme on homedirectory we are able to get the password for next challenge</p>

Password - IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
