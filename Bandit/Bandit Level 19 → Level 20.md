# Bandit Level 19 → Level 20 #

## Level Goal ##
<p>To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.</p>

### Helpful Reading Material ###
<p>https://en.wikipedia.org/wiki/Setuid</p>

## Solve ## 
<p>This time we don't have any mentioned command that will help us to solve the challenge, therefor we should do some re-search of setuid binary files</p>
<p>In short setuid stands for "Set user ID" which allows users to run an executable file with the file system permissions and often with elevated privileges in order to perform specific task</p>

![image](https://user-images.githubusercontent.com/85706972/166155296-45f08d80-6a9f-4384-bfd4-36c0a1a82d2a.png)

<p>After executing binary file we have also example how we should run it, so if we run it with id, we should see it's running as bandit20</p>

![image](https://user-images.githubusercontent.com/85706972/166155333-7aee3c79-eb41-4065-8c40-2cb9e1ae0ea6.png)

<p>Now we just need to find the password for Bandit20 under directory /etc/bandit_pass/bandit20

  ![image](https://user-images.githubusercontent.com/85706972/166155388-7275c27b-e72e-456a-9f3c-a7ffe1ba4865.png)

Password - GbKksEFF4yrVs6il55v6gwY5aVje5f0j
