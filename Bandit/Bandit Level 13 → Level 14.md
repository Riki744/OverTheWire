# Bandit Level 13 → Level 14 #

## Level Goal ##
<p>The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on</p>

## Commands you may need to solve this level ##
<pre>
ssh, telnet, nc, openssl, s_client, nmap
</pre>

## Solve ##
<p>This challenge is very interesting one as we don't need to find a password, but instead there will be SSH key that will allow us to login to next bandit</p>

<p>By checking our home directory we have private key there and by just simply using it with SSH we can easily login as Bandit14 and get next task flag</p>

![image](https://user-images.githubusercontent.com/85706972/166134627-42abca34-523a-4818-ac8e-270828ccb089.png)

<p>Password found</p>

![image](https://user-images.githubusercontent.com/85706972/166134641-4cb873be-feb6-4cb9-aa00-67b54997ec0f.png)

Password - 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
