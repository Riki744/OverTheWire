# Bandit Level 23 → Level 24 #

## Level Goal ##
<p>A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.</p>

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

## Commands you may need to solve this level ##
<pre>
cron, crontab, crontab(5) (use “man 5 crontab” to access this)
</pre>

## Solve ##
<p>This challenge is very exciting as we are about to write or own shell script, so let's jump into the challenge</p>

![image](https://user-images.githubusercontent.com/85706972/166308821-c87d1329-17d9-4836-a618-42f310882b68.png)

The file looks like execute on @reboot in every minute,hour and etc

![image](https://user-images.githubusercontent.com/85706972/166305171-4fb118de-e6fb-4200-9d28-a27c5e6a8982.png)

<p>If we go trough the script it looks like we should be able to just simply set myname variable to bandit24 and move to this directory
  
 ![image](https://user-images.githubusercontent.com/85706972/166309218-29544ff0-1f2b-4ea9-997e-6cb3ffbb800b.png)

  It looks like the script will skip over the parent directory and sub-directory and if the file matches owner of bandit23 it will execute with timeout and then delete it
  so we should be able to create our own script in same directory that should show us password for next level
  
  ![image](https://user-images.githubusercontent.com/85706972/166309904-f443dd92-d839-4da2-82c9-b3fa19d496cb.png)

  ![image](https://user-images.githubusercontent.com/85706972/166310182-64563f22-e5ee-48da-85de-484f69eb1b55.png)
  
  <p>In short i created new directory with full access to everyone and the same did for the scrip which get's us the password and it worked just fine</p>
  
  Password - UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
