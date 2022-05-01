# Bandit Level 21 → Level 22 # 

## Level Goal ##
<p>A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.</p>

## Commands you may need to solve this level ##
<pre>
cron, crontab, crontab(5) (use “man 5 crontab” to access this)
</pre>

## Solve ##

<p>First let's look at the directory as mentioned /etc/cron.d/
 
 ![image](https://user-images.githubusercontent.com/85706972/166156147-8f043ce9-3075-446f-9a41-b2abe1c19fbc.png)

 I assume we are interested only in bandit22.sh file, let's check if we have enough permission to see what exactly happens in that file
  
  ![image](https://user-images.githubusercontent.com/85706972/166156274-f1d3f5ef-e9e9-4df6-8749-9dd2fde3cfcd.png)

We do have enough permission as the owner of the file have rw - read and write, r - group users have read and finally all other also have read permission
  
  ![image](https://user-images.githubusercontent.com/85706972/166156329-33e639a3-37bf-487f-b89d-b491a0063410.png)

 </p>
 
 Password - Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
  
