VERIFICANDO AS PERMISSÕES PARA UM USUÁRIO ESPECÍFICO NO LOCALHOST.
MariaDB [(none)]> SHOW GRANTS FOR root@localhost;
+---------------------------------------------------------------------+
| Grants for root@localhost                                           |
+---------------------------------------------------------------------+
| GRANT ALL PRIVILEGES ON *.* TO `root`@`localhost` WITH GRANT OPTION |
| GRANT PROXY ON ''@'%' TO 'root'@'localhost' WITH GRANT OPTION       |
+---------------------------------------------------------------------+
2 rows in set (0.000 sec)
==================================================================================================================================================

VERIFICANDO AS PERMISSÇOES DO USUÁRIO CORRENTE.
MariaDB [(none)]> SHOW GRANTS FOR CURRENT_USER;
+---------------------------------------------------------------------+
| Grants for root@localhost                                           |
+---------------------------------------------------------------------+
| GRANT ALL PRIVILEGES ON *.* TO `root`@`localhost` WITH GRANT OPTION |
| GRANT PROXY ON ''@'%' TO 'root'@'localhost' WITH GRANT OPTION       |
+---------------------------------------------------------------------+
2 rows in set (0.000 sec)
==================================================================================================================================================

VERIFICANDO AS PERMISSÕES ATRIBUÍDAS AO USUÁRIO "root".
MariaDB [(none)]> select * from mysql.user where user = 'root' \G;
==================================================================================================================================================
MARIADB VIA TERMINAL (LOCAL)
luciolemos@dell:~$ sudo /opt/lampp/bin/mysql -u root -p
Enter password: # Não tem senha.
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 15
Server version: 10.4.13-MariaDB Source distribution
Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.
Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| test               |
+--------------------+
5 rows in set (0.001 sec)
MariaDB [(none)]> 

ACESSANO BANCO DE DADOS REMOTO
meustestes@luciolemos.lemavorum.com [~]# mysql -u root -p
Enter password: lemos35@
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 2681
Server version: 10.3.23-MariaDB MariaDB Server
Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.
Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> show databases;
+----------------------+
| Database             |
+----------------------+
| egovlemavorum_site   |
| helixlemavorum_site  |
| information_schema   |
| joomlalemavorum_site |
| lemavo13_fiscadm     |
| lemavoru_site        |
| meustestes_blog      |
| meustestes_laravel   |
| meustestes_site      |
| mysql                |
| mytipslemavorum_site |
| performance_schema   |
| sys                  |
+----------------------+
13 rows in set (0.001 sec)

MariaDB [(none)]> 
