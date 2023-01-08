<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
    <p id="demo">JavaScript can change HTML content.</p>
	<button type="button" onclick='document.getElementById("demo").innerHTML = "Hello JavaScript!"'>Click Me!</button>
	<br>

<?php
	// definição dos dados de conexão
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
