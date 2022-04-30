# Bandit Level 8 → Level 9 #

## Level Goal ##
<p>The password for the next level is stored in the file data.txt and is the only line of text that occurs only once</p>

## Commands you may need to solve this level ##

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

## Solve ##

<p>One of the commands that are recommended for this challenge is "sort" which will help us sort the text in data.txt so we can get the idea what kind of texts are in there</p>

![image](https://user-images.githubusercontent.com/85706972/166111811-03a4d530-d2b3-44ed-9383-1c0af7478df1.png)

<p>We got the output and it's hard to spot the one line that only repates once, so we should try to use another command "uniq" which will eventually show us one uniq line from all that data.txt</p>

![image](https://user-images.githubusercontent.com/85706972/166111900-d82e2bac-fb09-40a4-adae-a03f1612ca8e.png)

Password - UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
