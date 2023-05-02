# How to Install Proxmox Virtual Environment

Proxmox Virtual Environment is a powerful, open-source virtualization platform that allows users to run and manage multiple virtual machines and containers on a single physical server. Its user-friendly interface and robust feature set make it an ideal choice for both small and large organizations looking to maximize their virtualization capabilities. However, setting up Proxmox can be a complex process that requires careful planning and execution. In this guide, we will provide a step-by-step walkthrough of the Proxmox setup process, including installation, configuration, and optimization tips to ensure that your virtual infrastructure runs smoothly and efficiently.

## Prerequisites

You will need a local network with an internet connection, two computers, and a USB drive.

## Instructions

### Create Proxmox Installation Media

1.	Go to the ProxmoxVE downloads page: https://www.proxmox.com/en/downloads/category/iso-images-pve
2.	Download the most recent version of ProxmoxVE.
3.	Download balenaEtcher: https://www.balena.io/etcher#download-etcher
4.	Install balenaEtcher.
5.	Plug in the USB drive.
6.	Open balenaEtcher.
7.	Click “Flash from file”.
8.	Select the ProxmoxVE ISO file.
9.	Click “Select target”.
10.	Select the USB drive you plugged in.
11.	Click “Flash!”.
Warning: this will erase all data on the USB drive.
12.	Wait for the ISO file to finish flashing.
13.	Unplug the USB drive.

### Install Proxmox

*You will need a mouse, keyboard, and display for setup. You can unplug these later.*

1.	Plug the USB drive into the computer you wish to install ProxmoxVE on.
2.	Boot from the USB drive.
If the USB drive does not boot automatically, enter the BIOS boot menu on startup.
3.	Click “Install Proxmox VE”.
4.	Accept the EULA.
5.	Select a hard disk to install to.
Warning: this will erase all data on the hard disk.
6.	Keep the default filesystem.
7.	Select the country, time zone, and keyboard layout.
8.	Enter a password for the administrator account and email to receive notifications about your ProxmoxVE cluster.
9.	Fill out the management network configuration information if it is not auto filled.
Remember the IP address as you will need it to configure Proxmox later.
10.	Click “Install”

### Create a VM

1.	Open a web browser.
2.	Go to https://<IP_address>:8006/. Change this to the IP address you assigned to ProxmoxVE.
3.	Login.  
*The default administrator account username is root.*  
![Login Screen]()
4.	Click “OK” on the subscription dialog.
5.	To create a VM, you need an OS ISO. Go to your Proxmox management server partition and click “ISO Images”.
![ISO Images List Screen]()
6.	Either upload an ISO file or download one form a URL.  
*This is the URL for Ubuntu 22.04.2 Server: https://releases.ubuntu.com/22.04.2/ubuntu-22.04.2-live-server-amd64.iso?_ga=2.202918553.968848564.1677641201-1357489668.1674965353*
7.	Click “Create VM” in the top right.
8.	Configure your VM with your desired settings.
9.	Connect to the VM by clicking console.
![VM Console Screen]()

In conclusion, Proxmox Virtual Environment is an excellent choice for organizations looking to improve their virtualization capabilities. With its user-friendly interface, advanced features, and open-source license, Proxmox provides a flexible and cost-effective virtualization platform. By following the steps outlined in this guide, you can set up Proxmox, create virtual machines, and optimize your virtual infrastructure quickly and easily. Whether you're new to Proxmox or looking to improve your existing setup, this guide has everything you need to get started.

