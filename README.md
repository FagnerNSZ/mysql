# mysql
Administrando Mysql 


Alterando senha de root
Como alterar senha ROOT MySQL/Percona quando você NÃO sabe a senha ou esqueceu a senha de ROOT
Pare o servidor MySQL

# /etc/init.d/mysql stop
ou
# /etc/init.d/mysqld stop
Inicie o servidor MySQL com o comando abaixo

# mysqld --skip-grant-tables &
ou
# mysqld_safe --skip-grant-tables &
Efetue o login ao MySQL com acesso ROOT mesmo sem senha

# mysql -u root mysql
Substitua a palavra “SENHA_SECNET” por uma nova senha ( Lembre-se de deixar as aspas simples ‘entre_a_senha’ )

use mysql; UPDATE user SET Password=PASSWORD('SENHA_SECNET') WHERE User='root'; FLUSH PRIVILEGES; exit;
Reinicie o servidor MySQL

# /etc/init.d/mysql start
ou
# /etc/init.d/mysqld start
Como alterar senha root MySQL /Percona quando você sabe a senha do ROOT
Efetue o login ao MySQL com acesso ROOT mesmo sem senha

# mysql -u root mysql -p SUASENHA
Substitua a palavra “SENHA_SECNET” por uma nova senha ( Lembre-se de deixar as aspas simples ‘entre_a_senha’ )

use mysql; UPDATE user SET Password=PASSWORD('SENHA_SECNET') WHERE User='root'; FLUSH PRIVILEGES; exit;
