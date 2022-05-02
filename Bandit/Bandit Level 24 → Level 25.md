# Bandit Level 24 → Level 25 #

## Level Goal ##
<p>A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.</p>

## Solve ##

<p>This challenge also requires to create a small bash script that will do the connection to listening port 30002 and if we give current bandit24 password and 4-digit pin code were we we need to create brute force</p>
Deamons in Linux are like services in Windows, so let's try to find the deamon which is running on port 30002

![image](https://user-images.githubusercontent.com/85706972/166311553-738ba46a-3ef8-4eeb-a0d0-1df58666c44a.png)

<p>We know it's working and waiting for password of bandit24 and the secret pincode</p>
