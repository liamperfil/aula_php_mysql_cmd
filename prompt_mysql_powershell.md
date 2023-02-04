## prompt, cmd, .bat

### Super admin
```bat
Net user administrador /active:yes
Net user administrador /active:no
```

### Retornando e avançando diretório
```cmd
cd .. [voltar diretorio]
cd nome_diretorio [avançar diretorio]

cp [copiar]
cp "c:/nova pasta" "d:/" [copiar e colar origem destino]
cp -R "c:/nova pasta" "d:/" [parametro r para todos os subdiretorios]
cp -fR [para sobrescrever conflitos]
cp -iR [interagir a cada conflito]
cp -uR [para atualizar]

mv "c:/nova pasta" "d:/" [colar origem destino]
mv texto2.txt olamundo.txt [age como estivesse renomeando]

mkdir "nova pasta" [criar nova pasta "make directory"]
touch texto.txt [criar um arquivo de texto vazio]
echo "Olá mundo!" > texto2.txt [criar novo arquivo com texto]
cat texto2.txt [verificar o conteúdo do arquivo]

clear [limpar terminal]

rmdir [remover diretorio vazio]
rm [remover diretorio]
rm -r [remover forçadamente]
```

## mysql, powershell, sql

### Conectando ao servidor
```cmd
mysql --host=localhost --user=root --password=
```

```cmd
XCOPY D:*.* E: /e /c /h /k /y
```

```cmd
Net user administrador /active:yes
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
