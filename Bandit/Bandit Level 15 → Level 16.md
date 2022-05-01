# Bandit Level 15 → Level 16 #

## Level Goal ##
<p>The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.</p>
Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

## Commands you may need to solve this level ##
<pre>
ssh, telnet, nc, openssl, s_client, nmap
</pre>

## Solve ##

<p>This one is similar to the previous, but this time we need to use openssl and on port 30001 using SSL encryption</p>

![image](https://user-images.githubusercontent.com/85706972/166138680-e2b9c42f-929f-4346-989c-653312a23e24.png)

<p>This give us a huge list of information and in the end if we paste current Bandit password it gives us next bandit password and we can login to next challenge</p>

![image](https://user-images.githubusercontent.com/85706972/166138709-45e7704b-953e-4c72-a3cf-57ed4e2284bc.png)


Password - cluFn7wTiGryunymYOu4RcffSxQluehd
