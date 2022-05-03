# Bandit Level 24 → Level 25 #

## Level Goal ##
<p>A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.</p>

## Solve ##

<p>This challenge also requires to create a small bash script that will do the connection to listening port 30002 and if we give current bandit24 password and 4-digit pin code were we we need to create brute force</p>
Deamons in Linux are like services in Windows, so let's try to find the deamon which is running on port 30002

![image](https://user-images.githubusercontent.com/85706972/166311553-738ba46a-3ef8-4eeb-a0d0-1df58666c44a.png)

<p>We know it's working and waiting for password of bandit24 and the secret pincode which is going to be place for brute force</p>

![image](https://user-images.githubusercontent.com/85706972/166399604-eaf339a4-32a7-45a3-b5f9-54e32c136d05.png)

<p>Following script will loop through the number starting from 0000-9999 and submit every posssibility together with bandit24 password, this is called Range loops in bash. In the end we also got the password the next challenge</p>

![image](https://user-images.githubusercontent.com/85706972/166400064-bf5466f6-9922-403b-bab3-d758f3285d7c.png)


Password - uNG9O58gUE7snukf3bvZ0rxhtnjzSGzG
  
  

