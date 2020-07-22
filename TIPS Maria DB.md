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
