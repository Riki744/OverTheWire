# Bandit Level 28 → Level 29 #

## Level Goal ##
<p>There is a git repository at ssh://bandit28-git@localhost/home/bandit28-git/repo. The password for the user bandit28-git is the same as for the user bandit28.</p>

## Commands you may need to solve this level ##
<pre>
git
</pre>

## Solve ##
<p>From the level goal description tasks seems to be the same as it was for bandit27, but there must be a trick, so lets do it and see what we got
  
  ![image](https://user-images.githubusercontent.com/85706972/166986086-76bcc0a1-a3f7-46bb-a4a7-6a5b18b323bd.png)

  So we cloned the repo and we got text of unknown password for next challenge, using git manpages we find interesting command that will show us history of the following file
  
  ![image](https://user-images.githubusercontent.com/85706972/166986582-71c3a3ef-08af-47fe-b2bf-d7b95040dead.png)

  We able to find out that this file have several commits and we should be able to see them to see the changes
  
  ![image](https://user-images.githubusercontent.com/85706972/166986804-3038054c-844b-47ce-b1a5-b432633e606c.png)

  By just using "show" command with git we are able to find the changes and the commit ID
  
  Password - bbc96594b4e001778eee9975372716b2
