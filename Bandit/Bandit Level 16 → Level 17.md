# Bandit Level 16 → Level 17 #

## Level Goal ## 
<p>The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.</p>

## Commands you may need to solve this level ##
<pre>
ssh, telnet, nc, openssl, s_client, nmap
</pre>

## Solve ## 
<p>My first idea was to scan localhost from ports 31000 to 32000 and inspect the results and see if that will stand out</p>
<p> Used following command:</p>
<pre>
nmap -vv -sV -sC -p 31000-32000 localhost
</pre>

<p>Nmap results there was two ports that really stood out and it was port 31518 and 31790, as the service on them was running SSL</p>

![image](https://user-images.githubusercontent.com/85706972/166139035-208d541d-76ce-4256-b03e-148e66e7f7ca.png)

<p> At first I tried to connect to both of them, but it did not worked and I tottaly forgot that they are working over SSL, so we should use openssl as we did before </p>

![image](https://user-images.githubusercontent.com/85706972/166139097-f90077c9-def3-4507-ba13-f1a667216f43.png)

<p>Now if we submit the current bandit password we got back private key which we can use to SSH into next level</p>

![image](https://user-images.githubusercontent.com/85706972/166139113-9a15eca2-9cd7-4f05-b28b-27b869b6798a.png)

<p>To login to next challenge we can save the key to our local pc and give it read permissions</p>

![image](https://user-images.githubusercontent.com/85706972/166139214-2534257e-6abc-4e73-811d-4bdf40f5434a.png)

![image](https://user-images.githubusercontent.com/85706972/166139221-2c6fcaf8-ee6a-4b0a-bff6-f9e9449f4406.png)
