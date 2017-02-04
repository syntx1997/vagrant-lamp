# Vagrant LAMP (Linux Apache MySQL PHP)
Personal configuration for the setup of a LAMP server with Vagrant.

***Note:*** This configuration has been set to Windows 7 and Window 10. 

## Requirements
* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/)
* [Git](https://git-scm.com/)

## Vagrantfile and bootstrap.sh
* Install the [software](#software-installati)
* Set the web root directory in `/html`
* Move the MySQL database directory in `/mysql`

## Installed Software
* Ubuntu Server 14.04 LTS
* Apache 2.4.7
* PHP 5.5.9
* MySQL 5.5.54
* phpMyAdmin 4.0.10
* Git
* Composer
* Node.js
* npm

## Installation
Clone the repository
```
$ git clone https://github.com/davidecesarano/my-vagrant-lamp.git
```

## Usage
Run the command
```
$ cd my-vagrant-lamp
$ vagrant up
```
Now you can access the `DocumentRoot` here http://192.168.33.10

## Virtual Host
If you prefer to use a domain name than the IP address you can add a record to the host operating system files.
```
192.168.33.10    local.dev
```

## Database
* Username: root
* Password: vagrant
* Host: localhost
* Port: 3306

***Note:*** To access the MySQL database with phpMyAdmin http://192.168.33.10/phpmyadmin

## How to change the .vagrant directory ##
if you keep your Vagrantfile in a Dropbox (or Google Drive) folder in order to share the folder between your desktop and laptop (for example), Vagrant will overwrite the files in this directory with the details of the VM on the most recently-used host. To avoid this, you could set ***VAGRANT_DOTFILE_PATH*** to .vagrant-laptop and .vagrant-desktop on the respective machines.

In Windows you can set ***VAGRANT_DOTFILE_PATH***:

1. **System > Advanded system settings > Envirorment Variables**
2. Select **New**
3. Variable name = VAGRANT_DOTFILE_PATH, Variable value = .vagrant-home
