# Bandit Level 2 → Level 3 #

## Level Goal ##
<p>The password for the next level is stored in a file called <strong>spaces in this filename</strong> located in the home directory</p>

## Commands you may need to solve this level ##
ls, cd, cat, file, du, find


<li>We know that the file is on home directory, but anyway I wanted to use find command to look for the file</li>
<li>Of course when file is found we can cat it out, but this is bit tricky as we need to use backslash (\) in order to get the file</li>

<pre>find /home -type f -name "spaces in this file" 2>/dev/null</pre>

![image](https://user-images.githubusercontent.com/85706972/152295971-aa3d1cfc-fbb1-4e9f-b0af-2ff36db14d58.png)
