# Bandit Level 9 → Level 10 #

## Level Goal  ##
<p>The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.</p>

## Commands you may need to solve this level ##
<p>grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd</p>

## Solve ## 
<p>At first if you try to cat data.txt it's clearly human unreadable format and in this way we won't find a password for next bandit</p>

![image](https://user-images.githubusercontent.com/85706972/166112110-f1e38154-f48c-4508-813e-cc1b7d47f03e.png)

<p>Now i though that maybe string command will let me read possible information in this file </p>

![image](https://user-images.githubusercontent.com/85706972/166112175-1c4646ce-9055-4f3e-9bbe-59e950eb178e.png)

<p>By scrolling through the file I already found the password which was very obvious, but for learning purposes we can us folloing cmdline and get it also</p>

![image](https://user-images.githubusercontent.com/85706972/166112231-7c995568-5b6c-444b-aebe-92a0f1329b9d.png)

Password - truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
