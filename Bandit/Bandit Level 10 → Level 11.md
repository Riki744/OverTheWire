# Bandit Level 10 → Level 11 #

## Level Goal ##
<p>The password for the next level is stored in the file data.txt, which contains base64 encoded data</p>

## Commands you may need to solve this level ##
<p>grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd</p>

## Solve ##
<p>This challenge was very easy, first thing we need to check the data.txt, then as we know that it's base64 we can pipe the cat output and use decode function</p>

![image](https://user-images.githubusercontent.com/85706972/166112350-30e6031d-aaea-4047-a731-f9837ed1c099.png)


Password - IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
