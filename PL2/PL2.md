
# Exercise 1

1. Install FreeRadius on your virtual machine;
- First things first I installed WSL2 on my windows with ubuntu and updated it to the latest version.
![img.png](Images/PL2-Img1.png)


- Then I installed FreeRadius with the command: *sudo apt install freeradius freeradius-utils* 
![img_1.png](Images/PL2-Img2.png)


2. Create users on your machine: Bob, Alice, John, Madeleine, and Jake;

- I created the users with the command: *sudo adduser --disabled-password --gecos "" "<username>*
![img.png](Images/PL2-Img4.png)

- And later added passwords to them with the command: echo 'username:username123!' | sudo chpasswd
![img.png](Images/PL2-Img5.png)

3. Bob and Alice are standard users, Madeleine is an accountant, and Jake is the the ”IT Guy” (Administrator). Create the necessary groups;
- For this I used the command: *sudo groupadd <groupname>* and later added each user to the correct group with the command: *sudo usermod -aG <groupname> <username>*
![img.png](Images/PL2-Img6.png)

4. Configure FreeRadius such that it accepts authentications from Users and the Administrator only;

- First I search each user id
- ![img.png](Images/PL2-Img7.png)

- I added the code in white in this file: *sudo nano /etc/freeradius/3.0/clients.conf*
![img.png](Images/PL2-Img8.png)

- I added the code in white in this file: *sudo nano /etc/freeradius/3.0/mods-config/files/authorize*
- ![img_1.png](Images/PL2-Img9.png)
*