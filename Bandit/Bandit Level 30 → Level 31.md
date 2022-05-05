# Bandit Level 30 → Level 31 #

## Level Goal ##
<p>There is a git repository at ssh://bandit30-git@localhost/home/bandit30-git/repo. The password for the user bandit30-git is the same as for the user bandit30.</p>

Clone the repository and find the password for the next level.


## Commands you may need to solve this level ##
<pre>
git
</pre>


## Solve ##
<p>Lets do the same as before and what challenge we have to beat this time</p>

![image](https://user-images.githubusercontent.com/85706972/167006515-540e4bc7-785c-4144-8a9d-766f7ef64379.png)

<p>Lol, we just got scammed with empty file, anyway lets try to find some logs in the repo, but there is not a single change, so we must start digg deeper...</p>
of course I tried to check branch and commit history there was no sign of password, then I found something interesting

![image](https://user-images.githubusercontent.com/85706972/167009807-d20f5f5b-dadd-41f2-a9a0-980e5dde4834.png)
 
<p>git uses tags for special places in repository so it was hidding the password for next challenge</p>

Password - 47e603bb428404d265f59c42920d81e5
