# Ansible Role: Pimp My Log

> **DEPRECATED**: This role has been deprecated. Please consider using other tools like GoAccess or forking this role and maintaining your own version if you still want to use Pimp my Log.

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>


Installs [Pimp my Log](http://pimpmylog.com/).

## Requirements

Requires PHP to be installed on the server, and a web server like Apache, Nginx, IIS. You can get Pimp my Log set up pretty quickly with this role in tandem with `nholuong.apache` and `nholuong.php` available on Ansible Galaxy.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    pimpmylog_install_dir: /var/www/pimpmylog

The location where Pimp my Log will be installed. You should configure a virtual host or server entry pointing to this directory so you can access the interface. Otherwise, you could choose a location that's within an existing docroot, e.g. the default docroot `/var/www/html/pimpmylog`, and access Pimp my Log at `http://localhost/pimpmylog/`.

    pimpmylog_repo: https://github.com/nholuongut/ansible-role-for-pimpmylog.git

The git repository URL from which Pimp my Log will be cloned.

    pimpmylog_version: master

The version of Pimp my Log to install. Can be any valid tag, branch, or `HEAD`.

    pimpmylog_grant_all_privs: false

The setup of Pimp my Log allows for auto-configuration if the installation directory has `777` privileges, but this is an insecure way to install Pimp my Log. If you're installing on a local development environment, this is relatively harmless to set to `true` to ease installation... but if you're running this on a production or publicly-available server, don't even _think_ about changing this value!

## Dependencies

None.

## Example Playbook

    - hosts: webservers
      roles:
        - { role: nholuong.apache }
        - { role: nholuong.php }
        - { role: nholuong.pimpmylog }

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
