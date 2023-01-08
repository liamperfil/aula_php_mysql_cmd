## prompt, cmd, .bat

Net user administrador /active:yes
Net user administrador /active:no

cd ..
cd nome_diretorio

## mysql, powershell, sql

### Conectando ao servidor
mysql --host=localhost --user=root --password=

### Exibindo database
show databases;

### Selecionando database
use name_database;

### Redefinir senha do administrador
Atenção ao redefinir senha mysql no ambiente xampp é necessário alterar o arquivo config.inc.php em xampp/phpMyAdmin
mysqladmin -u root password

### Exibir host que podem ser conectados com o usuário especifico
SELECT host FROM mysql.user WHERE user="root";

GRANT ALL ON database_name.* to 'database_username'@'10.24.96.%' IDENTIFIED BY 'database_password';