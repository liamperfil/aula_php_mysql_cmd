# AULA SQL

[SQL Keywords Reference](https://www.w3schools.com/sql/sql_ref_keywords.asp "w3schools") <br>
[SQL Data Types](https://www.w3schools.com/sql/sql_datatypes.asp "w3schools") <br>

![Diagrama estrutura de banco de dados](/../../../../liamperfil/img/blob/main/estrutura_db.png)

```sql
CREATE DATABASE IF NOT EXISTS database1
DEFAULT CHARACTER SET utf8
DEFAULT COLLATE utf8_general_ci;
```

```sql
USE database1;
``` <br>

Criando uma tabela, comando create table seguido do nome da tabela, entre parênteses o nome da coluna seguido do tipo dado e demais constantes, cada coluna será separada por uma vírgula, exemplo:
```sql
CREATE TABLE pessoa(
CPF int NOT NULL PRIMARY KEY,
Sexo enum(‘M’, ‘F’),
Peso decimal(5,2),
Nacionalidade  varchar(20) DEFAULT ‘Brasil’
) DEFAULT CHARSET = utf8;
```

```sql
INSERT INTO tabela1 (coluna1, coluna2) VALUES ('valor1','valor2');
``` <br>

Diz selecionar os campos de tais colunas da tal tabela, use asterisco (*) para selecionar todos registros.
```sql
SELECT coluna1, coluna2 FROM tabela1;
```
<br>

- UPDATE - updates data in a database	
- DELETE - deletes data from a database
- ALTER DATABASE - modifies a database
- ALTER TABLE - modifies a table
- DROP TABLE - deletes a table
- CREATE INDEX - creates an index (search key)
- DROP INDEX - deletes an index
- SHOW DATABASES;
- SHOW TABLES;
- SHOW CREATE TABLE tabela1;
- AES_ENCRYPT('dado', 'chave') <br>

```sql
INSERT INTO tabela1 (coluna1, coluna2) VALUES (AES_ENCRYPT('valor1', 'chave'),'valor2');
```

```sql
CAST(AES_DECRYPT(senha,'chave') as char)
SELECT coluna1, CAST(AES_DECRYPT(coluna1,'chave') as char) from tabela1 WHERE colunax='valor1';
```
<br>
### Constantes
- NOT NULL
- ENUM(‘X’,’Y’)
- PRIMARY KEY
- DEFAULT
<br>
## Programas utilizados

### Wampserver
- WAMP é o acrônimo para Windows, Apache, MySQL e PHP. 
- É um pacote de softwares. 
- O WAMP age como um servidor virtual na sua máquina. Qual a diferença entre WAMP, XAMP, LAMP e MAMP? A diferença é para o sistema operacional.

### Workbench