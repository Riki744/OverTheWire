# Bandit Level 7 → Level 8 #

## Level Goal ##

<p>The password for the next level is stored in the file data.txt next to the word millionth</p>

### Commands you may need to solve this level ###
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

## Solve ##
<p>First we need to find data.txt, which is of course located on home directory of Bandit7, afterwards we simply cat data.txt and use grep function which will look for word "millionth"
</p>

![image](https://user-images.githubusercontent.com/85706972/166111561-25624df7-033d-47c0-b11d-1c4bfca92097.png)

Password - cvX2JJa4CFALtqS87jk27qwqGhBM9plV
