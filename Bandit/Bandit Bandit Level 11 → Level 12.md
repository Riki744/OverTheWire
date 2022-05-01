# Bandit Level 11 → Level 12 #

## Level Goal ##
<p>The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions</p>

## Commands you may need to solve this level ##
<pre>
grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
</pre>

## Solve ##
<p>From past expierience on other platforms I do remember that ROT13 encryption method works in a way that every letter is rotated by 13 positions, so we just need to rotate them back bash or python </p>

![image](https://user-images.githubusercontent.com/85706972/166133284-20ca3758-038b-444c-b3f4-af2804a43787.png)

<p>Luckily for us helpful link from vikipedia is provided and there is a lot of information how ROT13 works and even example of TR command that encrypts, we can use the same to decrypt</p>

![image](https://user-images.githubusercontent.com/85706972/166133388-dd8d4a71-07a7-4835-b095-b4970cbba9b2.png)

Password - 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
