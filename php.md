```php
$dbname = 'liam';
$dbuser = 'root';
$dbpass = '';
$dbhost = 'localhost';
```
	$dbname = 'liam';
	$dbuser = 'root';
	$dbpass = '';
	$dbhost = 'localhost';

	// criar conexão
	$conn = mysqli_connect($dbhost, $dbuser, $dbpass, $dbname) or die("Unable to Connect to '$dbhost'");
			
	$sql="SELECT * FROM pessoas WHERE id = '2'";
	$result = mysqli_query($conn,$sql);

	$campo = mysqli_fetch_array($result);
	echo "<br>Nome: " . $campo['nome'];
	echo "<br>CPF: " . $campo['id'];
	echo "<br>";
	
	
	$sql="SELECT * FROM pessoas";
	$result = mysqli_query($conn,$sql);
	foreach($result as $rowi) {
		echo '<br>'.$rowi['id']." ".$rowi['nome'];
	}
	
		
	$conn->close();

?>


</body>
</html>
