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
