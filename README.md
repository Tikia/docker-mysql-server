From mysql/mysql-server

New MySQL 8.0.11 is using caching_sha2_password as default authentication method.

PhpMyAdmin cannot understand this authentication method.

So I create user with one of the older authentication method : CREATE USER xyz@localhost IDENTIFIED WITH mysql_native_password BY 'passw0rd'.

Another idea: as long as the phpmyadmin and other php tools don't work with it, just add this line to your file /etc/mysql/my.cnf : default_authentication_plugin = mysql_native_password

SRC : https://stackoverflow.com/questions/49948350/phpmyadmin-on-mysql-8-0
--------------------------
MySQL 8 changed the default charset to utfmb4. But some clients don't know this charset. Hence when the server reports its default charset to the client, and the client doesn't know what the server means, it throws this error.

SRC : https://stackoverflow.com/questions/43437490/pdo-construct-server-sent-charset-255-unknown-to-the-client-please-rep
    
