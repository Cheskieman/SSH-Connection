# Connecting two servers via SSH Connection

## A complete step by step guide on how to connect two servers via SSH Connection


### This project will demonstrate how to 


#### Step by Step Instruction guidance

* Search and select EC2 from AWS searchbar

* Select Instances from left-handed navigation panel

* Select from top right Lauch instances button

* Give a name to the EC2 Instance

* Select for AMI Ubuntu

* Select Keypair

* Select at the bottom Launch Instance

* Select the recently created instance

* Scroll down and copy the Private IPv4 address

Repeat the EC2 instance setup from the previous steps with the following modifications:

Assign the instance a different name than the first EC2 instance.

Scroll down to Network Settings and select Edit.

Add a security group rule with the following values:

Type: SSH

Source Type: My IP

Select the Add security group rule button

Add a security group rule with the following values:

Type: SSH

Source type: Custom

Source: <your-private-IPv4-address>/32

Select at the bottom Launch Instance

Select the first of two instances created

Select at the top right Connect Button

Select the SSH client tab

Copy and paste the following commands into an elevated (Administrator) PowerShell terminal to install the OpenSSH Client.

* Run the key generation command

* Press enter for all prompts (default location , no passphrase)

* Copy the content of the newly created public key from output of following command

* Select the second EC2 Instance Created

* Scroll down and copy the Public IPV4 address

* Open a new PowerShell terminal and run the following command(s) before connecting via SSH

* Open authorized_keys file and insert the public key copied from the first-created instance

* Save and exit (Ctrl+O then Enter to save, Ctrl+X to exit)

* Set the correct permissions

* Go back to Server A & connect to Server B using its Private IP
  




















##### ##### Contribution Policy

This project is not accepting external contributions, including pull requests or feature requests.

It serves as a personal archive of my learning journey in applying foundational concepts in software development and version control. Active development is not ongoing, and external changes will not be integrated.

Thank you for your understanding.
