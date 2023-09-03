# VPC-Project-Tutorial
VPC – Virtual Private Cloud Assignment
On this assignment you will have to provision and define VPC with some servers.
Use the Canvas sandbox environment to do so.
You should take screenshots of every resource, and relevant definition steps. Order them in doc or slide 
deck, in a coherent manner, with needed explanations, in order to present your project.
Add code as an appendix
Create a github project that reflects all the resources, code snippets and scripts, you have created
1. Create VPC (without wizards – VPC only)
2. Add 4 subnets into it, in 2 different availability zones (2 in each AZ)
a. 2 private 
b. 2 public 
c. 2 routing tables, 1 public and 1 private, and assign to respective subnets.
d. Create an internet gateway and attach it to a public subnet. 
e. create NAT gateway attach it to private subnet.
3. On top of this infrastructure, you need to add two servers (pay attention to which subnet each 
one should be provisioned):
a. EC2 (Amazon Linux 2) with only SSH public access 
• SQL client should be installed in addition to other relevant services
b. EC2 (Amazon Linux 2) with MySQL server not accessible publicly (check what are the 
relevant requirements for running MySQL with minimal data) 
4. Create relevant Security groups
5. Verify that after connecting to ec2 using ssh, and operating the SQL client, we can “talk” with 
the MySQL server. (connect and see connection succeeded message )
Steps in problem decomposition
1. Review how to create the infrastructure 
a. VPC
b. Subnets
c. Route table
d. Internet Gateway
e. NAT
f. EC2 
g. Security groups
2. Review how to install MySQL on
3. Learn how to configure security issues in MySQL server (users, passwords, local access, remote 
access) 
4. Learn how to install SQL client (currently CLI one)
5. Learn how a client “talks” with the server locally (both on the same machine)
6. Learn how a client “talks” with the server remotely (pay attention to network, subnet, ports and 
other issues)
Bonus steps 1
1. Insert data to your database using the sample data script.
a. Download the data from here 
https://www.mysqltutorial.org/mysql-sample-database.aspx
b. Verify that you can query the data using the client.
Bonus steps 2
1. Automate the service installation on each ec2
2. Automate the data insertion to the database (hint - check the download link from the page 
given in the previous bonus)
3. Without any installations, verify that after connecting to ec2 using ssh, and operating the SQL 
client, we can query the data on MySQL server.
Bonus steps 3
1. Code an AWS CLI script that will provision the infrastructure.
2. Add to your script the installation automation for each EC2
3. Add the data insertion automation to the DB 
4. Add some commands that will monitor and show:
a. The infrastructure status
b. The ability to connect only to the public server from outside and query data in the 
private server
