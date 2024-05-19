   # E-Commerce Platform Deployment with Git, Linux and AWS

   The objective of this projet is to utilize Git for version control, develop the platform in a Linux environment and deploy it to AWS EC2 instance. After the deployment on EC2 instance, it is also required to add new feature(s) and ensure that the new feature(s) is/are reflected on the EC2 instance. 
   This project made use of a ready-made website template which allows us to focus on deployment assignments rather than having to create the website from scratch.

   ## Initialization of Git Repository

   Firstly, a project directory named ***"MarketPeak_Ecommerce"*** was created, and Git was initialized in this repository to manage the version control. The name and the email were also configured while the first commit was made.<br>

![initialization](./img/01.%20git%20initialization.png)

This project required that I use a pre-existing e-commerce website since the actual web development is done by web/software developers. 
-	I downloaded a specific template as required by the project. 
-	I prepared the website template by extracting the downloaded template into my project directory “MarketPeak_Ecommerce”.
-	I did a little customization.
-	I created an empty repository on GitHub and linked the remote repository on my local repository. 
-	I uploaded the content of my local repository to GitHub.<br>

![picture2](./img/02.%20origin%20push.png)

### Set up an AWS EC2 Instance

-	I logged in to AWS management console.
-	I launched an EC2 instance using Amazon Linux AMI
-	I connected to the instance using SSH

![launch](./img/03.%20aws%20launch.png)

### Cloning to the launched instance 
-	I installed git on the Linux server(EC2 instance)
![git](./img/04.%20git%20install.png)
-	I cloned the URL into the Linux server 
![serverclone](./img/05.%20server%20clone.png)
-	I installed webserver (httpd)
![httpd](./img/07.%20install%20webserver.png)
-	I started and enabled the web server 
![](./img/06.%20httpd%20enable.png)
-	I configured the httpd for the website by replacing the default content of the “/var/www/html” 
![](./img/08.%20replace%20server%20dir.png)
-	I accessed the website using the IP address of the EC2 instance
![](./img/09.%20web.png)
![](./img/10.%20IP.png)

### Adding new feature

-	I created a new branch called development to add a new feature
![](./img/11.%20switch%20branch.png)
-	Changes were made on this branch, part of which include changes to some texts in the idex.html file.
-	The new changes were staged and a new commitment was made in line with the modification done.
-	The new branch with the modification was pushed to Github to enable collaboration and version tracking
![](./img/12.%20new%20feature.png)
-	Pull request was created on GitHub 
![](./img/13.%20created%20and%20merged%20PR.png)
-	The merged changes were pushed to GitHub to ensure the main branch now contains the latest changes 
-	The latest changes were then pulled into the EC2 instance to have the new feature in the main production line.
-	The new features were tested by navigating to the public IP address of the EC2 instance
![](./img/14.%20new%20feature.png) ![](./img/15.%20new%20feature.png)
![](./img/16.%20feature3.png)

