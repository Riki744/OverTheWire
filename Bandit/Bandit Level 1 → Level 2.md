# Bandit Level 1 → Level 2 # 

## Level Goal ##

<p>The password for the next level is stored in a file called " - " located in the home directory</p>

## Commands you may need to solve this level ##
<p>ls, cd, cat, file, du, find</p>

<li>This now get’s a bit spicy we need to find password file called (-) dash, We can use command following find command</li>


<pre>find /home -type f -name "-" 2>/dev/null</pre>

![image](https://user-images.githubusercontent.com/85706972/152294513-7201d7fb-3268-4b84-b59a-07063852a0b2.png)

<li>This finds us the file we need and we can cat it out to get password for next challenge</li>

<p><strong>Bandit2 = CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9</strong></p>
