```
###Удаленный доступ

##RDP

##На виртуальном сервере, в зависимости от OS нужно произвести следующие действия.

###Debian:

$ apt-get install xrdp

$ systemctl enable xrdp

$ systemctl start xrdp


###CentOS:

$ yum install epel-release

$ yum install xrdp tigervnc-server tigervnc-server-module

$ chcon -t bin_t /usr/sbin/xrdp

$ chcon -t bin_t /usr/sbin/xrdp-sesman

$ firewall-cmd --zone=public --add-port=3389/tcp --permanent

$ firewall-cmd --zone=public --add-port=3389/udp --permanent

$ firewall-cmd --reload

$ systemctl enable xrdp

$ systemctl start xrdp
```
