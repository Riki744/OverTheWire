# Bandit Level 22 → Level 23 #

## Level Goal ## 
<p>A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.</p>

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

## Commands you may need to solve this level ##
<pre>
cron, crontab, crontab(5) (use “man 5 crontab” to access this)
</pre>

## Solve ##

<p>We start off by going to the directory /etc/cron.d and inspect the cronjob_bandit23 file
  
  ![image](https://user-images.githubusercontent.com/85706972/166156531-94dcf7e2-2930-49c7-95b2-c1aef4f520f0.png)
  
  Bash script looks like will execute as bandit23 and the whole text will be turned into md5 hash + and afterwards '' will be removed, so in order to get the password we should create md5 hash of bandit23 + text and it that way we can get the password from /tmp location

  ![image](https://user-images.githubusercontent.com/85706972/166156735-e2e1a719-c876-4bb6-92e6-9ed20574263a.png)

  It looks like we found the password for next level
  
  Password - jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n
