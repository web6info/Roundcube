Installare Roundcube su CentOS 6
=========
- [Roundcube site](http://roundcube.net/)
- [Roundcube git](https://github.com/roundcube/roundcubemail/blob/master/INSTALL)

Digitare i comandi:
```
# yum update
# yum install roundcubemail
```
Questo installerà Roundcube con cartella di configurazione in:
```
/etc/roundcubemail/
```
La cartella dei plugin sarà invece posizionata in:
```
/usr/share/roundcube/plugins/
```
Creare il database:
```
# mysql
> CREATE DATABASE roundcubemail /*!40101 CHARACTER SET utf8 COLLATE utf8_general_ci */;
> GRANT ALL PRIVILEGES ON roundcubemail.* TO roundcube@localhost
    IDENTIFIED BY 'password';
> quit

# mysql roundcubemail < SQL/mysql.initial.sql

```
