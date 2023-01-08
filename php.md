## formas de conexão

```php
$dbname = 'liam';
$dbuser = 'root';
$dbpass = '';
$dbhost = 'localhost';

$conn = mysqli_connect($dbhost, $dbuser, $dbpass, $dbname) or die("A conexão com ".$dbhost." falhou");
```

```php
$conn = new mysqli($dbhost, $dbuser, $dbpass, $dbname);

if($conn->connect_errno){
    echo "Erro";
} else {
    echo "Conexão ok";
}
```

```php
$dbname = 'liam';
$dbuser = 'root';
$dbpass = '';
$dbhost = 'localhost';

$conn = mysqli_connect($dbhost, $dbuser, $dbpass, $dbname) or die(header('Location: error_xml.php'));
```

## exibindo dados

### fetch array
```php	
$sql="SELECT * FROM pessoas WHERE id = '1'";
$result = mysqli_query($conn,$sql);

$campo = mysqli_fetch_array($result);
echo "<br>Nome: " . $campo['nome'];
echo "<br>CPF: " . $campo['id'];
echo "<br>";
```

### foreach()
```php
$sql="SELECT * FROM pessoas";
$result = mysqli_query($conn,$sql);
foreach($result as $rowi) {
	echo '<br>'.$rowi['id']." ".$rowi['nome'];
}

$conn->close();
```	


