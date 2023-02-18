# ansible__repo

This is my awesome Ansible Repo
---
## Virtualisation Software
In this project, I downloaded  an [Oracle virtual box](https://download.virtualbox.org/virtualbox/7.0.6/VirtualBox-7.0.6-155176-Win.exe, "Download Cirtual Box Here") for my virtualitaion environment.Since I am using a windows 10 as host, I downloaded the windows Virtual Box

## Guest Operating System
In this project, I made use of [Cent OS](https://sourceforge.net/projects/osboxes/files/v/vb/10-C-nt/9/Workstation/64bit.7z/download, "Download CentOS") as the guest Operating System downloaded from [oxboxes.org](https://www.osboxes.org/,"osboxes") which has several pre-installed and pre-configured linux distros

### Virtual Box Outlook
![Virtualbox](\asset\setup-of-all-vm.PNG)

## SSH Client
Using windows as a host OS, I download the MobaXterm which I used as my SSH Client.


## Virtual Machines

|vm name|ip address|
|-------|----------|
|Cent OS Template|    192.168.0.10|
|Ansible Controller|  192.168.0.58|
|Ansible Target|      192.168.0.34|
|Ansible Target1|      192.168.0.75|
|Ansible Target2|      192.168.0.**|

### Establishing an SSH Session to the Ansible Controller
The Image below shows an **SSH** session to the master ansible controller ![controller](\asset\SSH_TO_MASTER_CONTROLLER.PNG)

### Establishing an SSH Session to the Ansible Target VM
The Image below shows an **SSH** session to the ansible Target ![target](asset\ssh_to_ansible_target.PNG)

### Changing Hostname
I have to change the hostnames for the VM's for easy idnetification since for now they all have the same hostname as **osboxes**

In changing the hostname, I use the nano editor with the command below:
```
sudo nano /etc/hostname
sudo nano /etc/hosts
```
The hostname and host file is then changed from **osboxes** to **controller** for the VM serving as the controller and the second one changed to **target**. The third to **target1** and the forth to **target2**

## Installling Ansible on the Controller

```
sudo yum install ansible
```
![ansible_installation](asset\ansible_installation.PNG)



