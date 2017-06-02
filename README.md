# resete-senha-Maria-DB
Reset de senha no MySQL/MariaDB
Bom, uma dica rápida para resetar a senha do MySQL/MariaDB. 

Digite no prompt: 

# mysqld_safe --skip-grant-tables & 

Agora que iniciou o MySQL, digite: 

# mysql 

Já logado no MySQL, digite: 

mysql> use mysql; 

Agora vamos resetar a senha: 

mysql> update user SET password=password('NOVA SENHA') WHERE user='root'; 

Agora saia do MySQL: 

mysql> quit 

Reinicie o serviço do MySQL e pronto. Já podes logar com a senha que tu definiu. 


Pasta msql sock

chown -R mysql /var/run/mysqld
chmod +x /var/run/mysqld/mysqld.sock
/etc/init.d/mysql restart
