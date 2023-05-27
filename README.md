# Wordpress

Deploy WordPress on EC2 by WordPress AMI
#aws #ec2 #wordpress #awscommunitybuilders
Wordpress
WordPress is a highly popular content management system (CMS). It is most commonly used for blogs but can also be used for running e-commerce sites, message boards, company websites, Portfolio Websites and many other popular use cases. In this guide, you will learn how to set up a WordPress site to run a blog.

AWS Services services that use in this project
An Amazon EC2 instance to install and host the WordPress application.

Implementation
Creating an EC2 INSTANCE and Choosing an Amazon Machine Image
a. Open the AWS Management Console. When the screen loads, enter EC2 in the search bar, then select EC2 to open the service console.
![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/7a31d36d-9fda-4b7e-a37a-173ede2dfd11)

b. Choose the Launch instance button to open the instance creation wizard.

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/b9dcc298-9086-411a-8661-11e2561193e4)

c. On the first page, enter wordpress app as your instance name.

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/da335dd3-0f30-4996-8a26-7a078dd17e97)

d. Next, choose an Amazon Machine Image (AMI). The AMI you choose will determine the base software that is installed on your new EC2 instance. This includes the operating system (Amazon Linux, Red Hat Enterprise Linux, Ubuntu, Microsoft Server, etc.), and the applications that are installed on the machine.

Many AMIs are general-purpose AMIs for running many different applications, but some are purpose-built for specific use cases, such as the Deep Learning AMI or various AWS Marketplace AMIs.

WordPress image is certified by Bitnami as secure, up-to-date, and packaged using industry best practices, and approved by Automattic, the experts behind WordPress, so choose WordPress Certified by Bitnami and Automattic after make search on AWS Marketplace AMIs in the AMI selection view.

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/e9dca552-5ace-4ca2-97bd-8e627e82433c)
e. You will find the first image, choose it and press on Select

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/512d50da-ff8f-4c6c-86ef-b1e651b2135b)

f. Read overview and all details about AMI then click Continue

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/9f793323-46ed-41a7-83b0-d9c6f0985d38)

g. You will return to the AMI Section and you will find that the image has been selected.

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/51f62975-2140-498a-b748-2c5b324c6b51)

Choosing an instance type
Scroll down to select an EC2 instance type. An instance type is a particular configuration of CPU, memory (RAM), storage, and network capacity.

AWS has a huge selection of instance types that cover many different workloads. Some are geared toward memory-intensive workloads, such as databases and caches, while others are aimed at compute-heavy workloads, such as image processing or video encoding.

Amazon EC2 allows you to run 750 hours per month of a t2.micro instance under the AWS Free Tier.

But in this image .. AMI vendor recommends using t3a.small instance

a. Select the t3a.small instance.
![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/87e81f6f-1ec9-4fa5-bea0-9debec6a3175)

Configuring an SSH key
You will see a details page on how to configure a key pair for your instance. You will use the key pair to SSH into your instance, which will give you the ability to run commands on your server.

a. Open the key pair (login) section and choose Create new key pair for your instance.
![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/7682c52d-3d6a-428d-b0dc-360ff3c455cd)

b. Give your key pair a name. Then choose .ppk in Private Key file format to can use with PuTTYThen. Then choose the Create key pair button, which will download the .ppk file to your machine. You will use this file later.
![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/9ad352b3-9b6c-4f38-b010-fc38a6960a78)

c. You will return to Key pair (login) Section and you will find that Key has been selected.

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/3a5e0118-bc09-4812-ab2d-844c1cf49568)

Configuring a security group and launching your instance
You need to configure a security group before launching your instance. Security groups are networking rules that describe the kind of network traffic that is allowed to your EC2 instance. You want to allow traffic to your instance:

SSH traffic from all IP addresses so you can use the SSH protocol to log in to your EC2 instance and configure WordPress.
HTTPS traffic from all IP addresses so that users can view your WordPress site Secured.
HTTP traffic from all IP addresses so that users can view your WordPress site.
a. To configure this, select Allow SSH traffic from Anywhere and select Allow HTTPS & HTTP traffic from the internet (These are the default choices when choosing an Wordpress AMI).

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/7bdc0cb7-a0db-4559-9c7a-778b70858e6e)

Configuring storage on instance
a. Here we can increase the storage space for the Root volume and also can be added more volume storage.

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/2a352f21-b195-4501-a6d5-0fd099f25d33)

Launch
It is now time to launch your EC2 instance.
a. Choose the Launch instance button to create your EC2 instance.
![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/16687ec8-a4a8-4038-9fd5-fd8587d9cef8)

b. Wait for instance to launch.

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/528c7f51-3c84-494e-acba-795da2fcd8f3)

c. You have successfully launched your EC2 instance. Click on Open address to view website.

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/38ccdfb6-5f10-4616-831a-3bdb1d1f5e9b)

Deploying Wordpress
![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/cd3d8cf9-4e60-4c49-b6b6-70043b7f60f7)

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/814d2dab-99d5-4b91-8bed-1b6d6a4659ff)

![image](https://github.com/vemula-chandi-priya/Wordpress/assets/113158270/47803b36-91bc-423b-98b1-cfecf6c0b445)
