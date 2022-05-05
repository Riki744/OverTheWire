# Bandit Level 31 → Level 32 #

## Level Goal ##
<p>There is a git repository at ssh://bandit31-git@localhost/home/bandit31-git/repo. The password for the user bandit31-git is the same as for the user bandit31.
  
  Clone the repository and find the password for the next level.

 ## Commands you may need to solve this level ##
<pre>
  git
</pre>

## Solve ## 
<p>Start again by simply cloning the repo of the challenge</p>

![image](https://user-images.githubusercontent.com/85706972/167011125-3d48f8bd-f687-43a2-b280-3777980e47e4.png)

<p>This time I noticed that we have two files to work with</p>

![image](https://user-images.githubusercontent.com/85706972/167011295-800c53b9-eaa7-41dc-a8d3-d8bd27fab9ac.png)

<p>So this time it's says we have to push a file (key.txt) to the remote repository and this means that we need to create new file</p>

![image](https://user-images.githubusercontent.com/85706972/167012292-74a80c14-886b-489c-8d1e-e3727871c016.png)

<p>We created new file with the content and as we in beginning saw that new file is actually going to ignore *.txt which means if we push key.txt to remote repo it will not be pushed so this can be deleted.
Also we must create new commit so that key.txt can be pushed</p>

![image](https://user-images.githubusercontent.com/85706972/167013200-59a4cbf1-3c3b-4301-a6f2-746aaa6d9bad.png)

We added the key.txt to repo and pushed to remote repo and got back reply with next challenge password

Password - 56a9bf19c63d650ce78e6ec0354ee45e


