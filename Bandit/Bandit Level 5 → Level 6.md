# Bandit Level 5 → Level 6 #

## Level Goal ##
<p>The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:</p>
    <li>human-readable</li>
    <li>1033 bytes in size</li>
    <li>not executable</li>
    
### Commands you may need to solve this level ###

<li>Seems like all tasks are under bandit home directory so we won’t spend time on find command anymore, so we can cd into inhere directory</li>

![image](https://user-images.githubusercontent.com/85706972/155693481-cd551e96-4c92-4180-bdc2-60e892793a14.png)

<li>We know our task, and we know that next password file contains parameters given, so we should craft one good find command, to do this</li>

![image](https://user-images.githubusercontent.com/85706972/155693679-013efaa3-ee23-4def-b40f-f1c7590e6f16.png)

<p>I used find command and I only specified the size of the file we are looking, so this got me some other files and also the correct one for the next challenge<p>
  
Password - "HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs"
