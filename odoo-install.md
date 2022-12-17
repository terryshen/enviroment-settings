Odoo 16.0 for Ubuntu 20.04.01
# apt update -y && apt upgrade -y

# apt install postgresql -y

# wget -O - https://nightly.odoo.com/odoo.key | apt-key add -

# echo "deb http://nightly.odoo.com/14.0/nightly/deb/ ./" >> /etc/apt/sources.list.d/odoo.list

# apt-get update && apt-get install odoo

防火墙策略：如果未开启防火墙可以不配置

安装完成后,在防火墙中添加 Odoo 端口。假设您使用的是 UFW。

# ufw allow 8069/tcp

# ufw reload

http://[server_IP]:8069 访问 Odoo。

https://devpress.csdn.net/linux/62eeb0e27e66823466182999.html

注意：

Ubuntu 18.04.1版本安装过程中遇到以下异常

The following packages have unmet dependencies:

odoo : PreDepends: init-system-helpers (>= 1.54~) but 1.51 is to be installed

Depends: python3-xlwt but it is not installable

Recommends: python3-ldap but it is not going to be installed

E: Unable to correct problems, you have held broken packages.

root@DESKTOP-CLGLE77:~# apt install init-system-helpers

Reading package lists... Done

Building dependency tree

Reading state information... Done

init-system-helpers is already the newest version (1.51).

init-system-helpers set to manually installed.

0 upgraded, 0 newly installed, 0 to remove and 2 not upgraded.

处理步骤

#先看看都有什么版本：

sudo apt-cache policy init-system-helpers

#装高版本的

sudo apt-get install init-system-helpers=1.56+nmu1~ubuntu18.04.1

安装 python3-ldap


sudo apt-get install python3-ldap

指定源：deb http://cz.archive.ubuntu.com/ubuntu kinetic main universe

安装剩下两个python3包

安装完成后将指定源注释掉重新执行安装脚本

# apt-get update && apt-get install odoo




