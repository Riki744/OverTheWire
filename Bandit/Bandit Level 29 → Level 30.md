# Bandit Level 29 → Level 30 #

## Level Goal ##
<p>There is a git repository at ssh://bandit29-git@localhost/home/bandit29-git/repo. The password for the user bandit29-git is the same as for the user bandit29.</p>

Clone the repository and find the password for the next level.


## Commands you may need to solve this level ##
<pre>
git
</pre>


## Solve ## 
<p>Let's start again by cloning the repository and see what we have to deal this time for the solve</p>

![image](https://user-images.githubusercontent.com/85706972/166987455-630504c5-630c-4f34-af67-11bc64aba806.png)

<p>Challenge looks the same as previous one, but it's says that there is no password in production, well we can see if there is any commits and if we are able to find any changes</p>

![image](https://user-images.githubusercontent.com/85706972/166987823-b4985743-c230-4c06-907f-6f3c49c1054e.png)

<p>The only change as we can see is only username, but that won't help us as there must be something else</p>

![image](https://user-images.githubusercontent.com/85706972/166995346-a535158a-2e03-45ea-935c-6272bcddccd4.png)

<p>As we can see that there is no password in production, we can possibly check if there is any other branch availabe to us</p>

![image](https://user-images.githubusercontent.com/85706972/167005688-f7a7517a-eaaf-46a1-aa35-ebc3814a740e.png)

<p>Next phase we change the branch to dev section and use git log to show us changes now</p>

![image](https://user-images.githubusercontent.com/85706972/167005793-9cd299dc-68df-4fe2-873e-18710ff39e0d.png)


We found the password - 5b90576bedb2cc04c86a9e924ce42faf


