# Magebox 2.0
MageBox is a dead simple [Vagrant][1] LAMP Box for [Magento][2] 2 Development with tools like [Composer][3], [Nodejs][4] &amp; [Git][5]. This box is inspired from [Scotch Box](https://github.com/scotch-io/scotch-box/).

## Features
- Ubuntu 14.04 LTS Trusty Tahir
- Nginx v1.4.6
- MySQL v5.6.30
- PHP v7.0
- Composer v1.0
- Node v5.10.1
- NPM v3.8.3
- Git v1.9.1
- PhpMyAdmin


## Installation

#### Box Installation
* Download and Install [Vagrant][1]
* Download and Install [VirtualBox][6]
* Clone the MageBox [GitHub Repository](https://github.com/IamSwap/MageBox) ``` git clone https://github.com/IamSwap/MageBox project-name ```
* Change current directory to project ``` cd project-name ```
* Run ``` vagrant up ```
* You can place your project files into ``` public ``` directory or proceed for magento installation
* Access Your Project at  [http://192.168.33.10/][7]

#### Magento Installation
* Run ``` vagrant ssh ```
* Change current directory to ``` cd /home/vagrant/public ```
* Clone Magento Repository ``` git clone https://github.com/magento/magento2 --depth=1 . ```
* Run ``` composer install ``` & Follow installation [instructions](http://devdocs.magento.com/guides/v2.0/install-gde/prereq/dev_install.html).



## Basic Vagrant Commands
Here are some useful basic vagrant commands.

#### Start or resume your server
```bash
vagrant up
```

#### Pause your server
```bash
vagrant suspend
```

#### Delete your server
```bash
vagrant destroy
```

#### SSH into your server
```bash
vagrant ssh
```


## Setting a Hostname
To set hostname, just add a record like the following example to your computer's host file.

```bash
192.168.33.10 mage.dev
```

## Database Access

#### MySQL 
- Hostname: localhost or 127.0.0.1
- Username: root
- Password: root
- Database: magento

#### PhpMyAdmin
Access PhpMyAdmin at [http://192.168.33.10/phpmyadmin/](http://192.168.33.10/phpmyadmin/)
- Username: root
- Password: root


## SSH Access
User simple command for ssh into box ``` vagrant ssh ``` or use these credentials
- Hostname: 127.0.0.1:2222
- Username: vagrant
- Password: vagrant


 [1]: https://www.vagrantup.com/downloads.html
 [2]: http://magento.com
 [3]: https://getcomposer.org
 [4]: https://nodejs.org
 [5]: https://git-scm.com
 [6]: https://www.virtualbox.org/wiki/Downloads
 [7]: http://192.168.20.10/
