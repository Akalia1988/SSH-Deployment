# SSH-Deployment
SSH Deployment Task in Azure DevOps Pipelines

1. Create and Upload the Public Key to Azure VM

To set up our SSH Task we need a SSH Service Connection but to configure the connection we need to generate the Public and Private keys.

Command to create Public and private key 

ssh-keygen -t rsa -b 2048

Now we can manually SSH into our VM and add our public key to the VMs authorized_keys.

ssh root@IP

Once you are logged in to the VM, you can add the newly generated public key to the authorized_keys.

cd .ssh/
touch authorized_keys

You can add the content by running the preceding command.

echo "<RSA Public Key>" > authorized_keys
  

Set Up the SSH Service Connection

![image](https://user-images.githubusercontent.com/58148717/107423597-215f9f00-6ae2-11eb-8ac5-df4491fdaa23.png)


![image](https://user-images.githubusercontent.com/58148717/107423724-4fdd7a00-6ae2-11eb-8b8f-630cb4cfaa31.png)


Create the Release Pipeline

Add Task

![image](https://user-images.githubusercontent.com/58148717/107423801-6d124880-6ae2-11eb-8989-8cd2a29f10d8.png)

We can run script file, Commands and inline scripts on our Linux VM 

![image](https://user-images.githubusercontent.com/58148717/107423909-9a5ef680-6ae2-11eb-971a-c51bd318daec.png)













  









