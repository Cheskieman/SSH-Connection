# Connecting two servers via SSH Connection

## A complete step by step guide on how to connect two servers via SSH Connection


### This project will demonstrate how to:

* Set up two EC2 instances
  
* Generate and copy an SSH key pair on the first EC2 instance
  
* Authorize the SSH key pair on the second EC2 instance
   
* Access the second EC2 instance via SSH from the first EC2 instance  





#### Step by Step Instruction guidance

* Search and select EC2 from AWS searchbar
<p align="center">  
  <img src="resources/Search and Select EC2 from aws searchbar.png" alt="Select EC2 from AWS Searchbar" />  
</p>  

* Select Instances from left-handed navigation panel
<p align="center">  
  <img src="resources/Select Instances from left handed navigation panel.png" alt="Select Instancews from left hand navigation panel" />  
</p>  

* Select from top right Lauch instances button
<p align="center">  
  <img src="resources/Select from top right Lauch instances button.png" alt="Select Launch Instance Button top right" />  
</p>  

* Give a name to the EC2 Instance
<p align="center">  
  <img src="resources/Give a name to your EC2.png" alt="Give EC2 Instance a name" />  
</p>  

* Select for AMI Ubuntu
<p align="center">  
  <img src="resources/Give a name to your EC2.png" alt="Select Ubuntu AMI" />  
</p>  

* Select Keypair
<p align="center">  
  <img src="resources/Select Keypair.png" alt="Select Keypair" />  
</p>  

* Select at the bottom Launch Instance
<p align="center">  
  <img src="resources/Select at bottom launch instance.png" alt="Select Launch Instance at bottom" />  
</p>  

* Select the recently created instance
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Scroll down and copy the Private IPv4 address
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

**Repeat the EC2 instance setup from the previous steps with the following modifications:**

* Assign the instance a different name than the first EC2 instance.
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Scroll down to Network Settings and select Edit.
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Add a security group rule with the following values:
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

**Type: SSH**

**Source Type: My IP**

* Select the Add security group rule button
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Add a security group rule with the following values:
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

**Type: SSH**

**Source type: Custom**

**Source: <your-private-IPv4-address>/32**

* Select at the bottom Launch Instance
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Select the first of two instances created
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Select the Connect Button from the top right 
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Select the SSH client tab
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Run the following command in PowerShell to enable SSH
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Run the key generation command
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Press enter for all prompts (default location , no passphrase)
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Copy the content of the newly created public key from output of following command
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Select the second EC2 Instance Created
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Scroll down and copy the Public IPV4 address
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Open a new PowerShell terminal and run the following command(s) before connecting via SSH
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Open authorized_keys file and insert the public key copied from the first-created instance
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Save and exit (Ctrl+O then Enter to save, Ctrl+X to exit)

* Set the correct permissions
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  

* Go back to Server A & connect to Server B using its Private IP
<p align="center">  
  <img src="resources/EC2INSTANCESETUPSELECTEC2FROMDASHBOARD.png" alt="Select EC2 from Dashboard" />  
</p>  





















##### ##### Contribution Policy

This project is not accepting external contributions, including pull requests or feature requests.

It serves as a personal archive of my learning journey in applying foundational concepts in software development and version control. Active development is not ongoing, and external changes will not be integrated.

Thank you for your understanding.
