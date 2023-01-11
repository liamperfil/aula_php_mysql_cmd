## prompt, cmd, .bat

### Super admin
```bat
Net user administrador /active:yes
Net user administrador /active:no
```

### Retornando e avançando diretório
```cmd
cd ..
cd nome_diretorio
```

## mysql, powershell, sql

### Conectando ao servidor
```cmd
mysql --host=localhost --user=root --password=
```

### Exibindo database
```sql
show databases;
```

### Selecionando database
```sql
use name_database;
```

### Redefinir senha do administrador
Atenção ao redefinir senha mysql no ambiente xampp é necessário alterar o arquivo config.inc.php em xampp/phpMyAdmin
```cmd
mysqladmin -u root password
```

### Exibir host que podem ser conectados com o usuário especifico
```sql
SELECT host FROM mysql.user WHERE user="root";
```

```sql
GRANT ALL ON database_name.* to 'database_username'@'10.24.96.%' IDENTIFIED BY 'database_password';
```
