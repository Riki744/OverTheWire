# Bandit Level 17 → Level 18 #

## Level Goal ##
<p>There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new</p>

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

## Commands you may need to solve this level ##
<pre>
cat, grep, ls, diff
</pre>

## Solve ##
<p>If we check the command diff manpages, we see that it able to compare files line by line, so lets try and see what we get</p>

![image](https://user-images.githubusercontent.com/85706972/166139494-9e9ac3f6-3199-4e7d-9fbb-9d2158824c40.png)

<p>It looks like it found which line has been changed and from one to new characters so I assume that password for next level is at the top of the output </p>

Password -  kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

![image](https://user-images.githubusercontent.com/85706972/166139674-d56ec338-0ccd-4cee-ad4a-3cbf1fa37d52.png)

<p>As the note was saying that if we see ByeBye when we try to login then we have solved the challenge and it's related to next one</p>
