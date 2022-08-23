# Ansible - Web Server - Nginx or Apache

## Ansible Playbook : LEMP or LAMP Server on Debian

This Ansible script allows you to automate the configuration of a **LEMP web server** or a **LAMP web server** on **Debian 11** server.

These **Ansible roles** will automate the deployment for you:

* Install **Nginx** or **Apache**
* Install **MariaDB** (supported versions: 10.5, 10.6, 10.7)
* Install **PHP** (supported versions: 8.0, 8.1)
* Install **PhpMyAdmin**
* Create your Nginx / Apache Virtual Hosts (one per domain)
* Create your MariaDB databases (one per domain)
* Preparing the skeleton of your websites

[![Ansible](https://raw.githubusercontent.com/s-damian/medias/main/technos/ansible.webp)](https://github.com/s-damian)
[![Linux](https://raw.githubusercontent.com/s-damian/medias/main/technos/linux.webp)](https://github.com/s-damian)
[![PHP](https://raw.githubusercontent.com/s-damian/medias/main/technos/php.webp)](https://github.com/s-damian)
[![MariaDB](https://raw.githubusercontent.com/s-damian/medias/main/technos/mariadb.webp)](https://github.com/s-damian)
[![Nginx](https://raw.githubusercontent.com/s-damian/medias/main/technos/nginx.webp)](https://github.com/s-damian)
[![Apache](https://raw.githubusercontent.com/s-damian/medias/main/technos/apache.webp)](https://github.com/s-damian)

### Author

[![Freelance Web](https://raw.githubusercontent.com/s-damian/medias/main/s-damian-logo.webp)](https://github.com/s-damian)

This Ansible script was made by [Stephen Damian](https://github.com/s-damian)


## Getting Started

### Requirements:

* Debian 11
* SSH root access

### Introduction:

This example is configured for a Debian **local server**.

If you want to configure there for a Debian **remote server**, you need to configure the **ansible/hosts** file.

### Create your home user (if it doesn't exist yet):

```
adduser user_test
```

### Update and upgrade:

```
sudo apt-get update && sudo apt-get upgrade
```

### Install Ansible:

```
sudo apt-get install ansible
```

### Configure web-server.yml:

You need to configure your **ansible/web-server.yml** file.

You must configure at least all the **REQUIRED** lines.

### Ansible folder:

Send the **ansible** folder present in this package to the **/etc** folder of your Debian server.

### Run the Ansible script:

```
ansible-playbook -i /etc/ansible/hosts /etc/ansible/web-server.yml
```

### See the result:

* www.your-domain.com
* www.your-domain.com/phpmyadmin


## Go further

### Security

You must change the path of PhpMyAdmin, or remove PhpMyAdmin from public access.

Don't forget to secure your server with iptables, fail2ban, etc.

You can Configure SSL for your websites (with Certbot for example).

### Performance

To improve performance, you can add cache to your Nginx / Apache configuration.

### Send emails

To make your server able to send mails, you can use postfix.
