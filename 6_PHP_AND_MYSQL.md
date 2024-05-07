# Working with PHP and MySQL

For this section we're going to learn how to integrate PHP with MySQL for us to create CRUD (Create, Read, Update, Delete) Applications, but let's first focus on some concepts we need to learn before proceeding to the more advanced parts.


### Sessions in PHP
A session variable is a type of variable that allows data to be stored and accessed across multiple pages of a website during a user's visit. To learn how session variables work, create the given files below. 

We first create our ```index.php``` file. The main purpose of ```session_start()``` is to establish a connection to the existing session. ```session_unset()``` is for deleting all the session variables.

```php
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body>
	<?php session_start(); ?>

	<h1>Fill in the input fields below</h1>
	
	<h2>
		User logged in:
		<?php
		if(isset($_SESSION['firstName'])) {
			echo $_SESSION['firstName'];
		}
		?>		
	</h2>

	<h2>
		User password:
		<?php
		if(isset($_SESSION['password'])) {
			echo $_SESSION['password'];
		}
		?>		
	</h2>
	<a href="unset.php">Logout</a>

	<form action="handleForm.php" method="POST">
		<p><input type="text" placeholder="First name here" name="firstName"></p>
		<p><input type="password" placeholder="Password here" name="password"></p>
		<p><input type="submit" value="Submit" name="submitBtn"></p>
	</form>
</body>
</html>
```

Let's create ```handleForm.php``` file

```php
<?php 

session_start();

// Check if submitBtn exists
if(isset($_POST['submitBtn'])) {

	// Get the first name from index.php
	$firstName = $_POST['firstName'];

	// Get the password from the input field
	$password = md5($_POST['password']);

	// Set the session variables
	$_SESSION['firstName'] = $firstName;
	$_SESSION['password'] = $password;

	// Go back to index.php
	header('Location: index.php');
}

?>
```

And then ```unset.php```. Please keep in mind that ```session_unset()``` is for deleting all the session variables.

```php
<?php  
session_start(); // Establish connection to the current session
session_unset(); // Delete all session variables
header('Location: index.php'); // Go back to homepage
?>
```

### How to create a database in phpmyadmin?

Before we proceed with the PDO concepts, let's first <b>create a database in MySQL</b>. Make sure first that you <b>already started MySQL</b> in XAMPP.

<img src="Images/1_start and stop php mysql.png">

Next, create a database by clicking new.

<img src="Images/2_create_a_db_by_clicking_new.png">

Let's give a name to our database

<img src="Images/3_create_db_php_mysql.png">

And let's create a table in our database with a name ```php_my_sql_db```. We're gonna call it ```tasks``` table.

<img src="Images/4_create_tasks.png">

Create the columns and make sure to give the right data types as stated and fill in the other attributes given as well. 

<img src="Images/6_creating_the_tasks_table.png">

### Creating a template

Paste the following HTML template below in our ```index.php``` file. 

```index.php```

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body>
	<h1>Welcome to our to do list</h1>
	<form action="handleForms.php" method="POST">
		<p><input type="text" name="title" placeholder="title here"></p>
		<p><input type="text" name="description" placeholder="description here"></p>
		<p><input type="submit" value="Submit" name="submitBtn"></p>
	</form>
</body>
</html>
```

### PDO - PHP Data Objects

Now that we created a database and the tasks table, let's insert an entry on the ```tasks``` table, but first we have to create our ```dbConfig.php``` file to setup our connection to the MySQL database. PDO is used as a PHP interface to access MySql database. The ```conn``` variable is what we're gonna use to connect to the database. 

Create our ```dbConfig.php``` file and paste this to the given file.

```php
<?php 

$host = "localhost";
$user = "root";
$password = "";
$dbname = "php_mysql_db";
$dsn = "mysql:host={$host};dbname={$dbname}";

$conn = new PDO($dsn, $user, $password);
$conn->exec("SET time_zone = '+08:00';");

?>
```

We now create our ```functions.php``` table. We first need to create a function that can insert a record to the database. 

```functions.php```

```php
function makeATask($conn, $title, $description) {
	// Prepare the SQL query to insert data into the 'posts' table
	$sql = "INSERT INTO tasks (title, description) VALUES(?,?)";
	
	// Prepare the statement using the connection object
	$stmt = $conn->prepare($sql);
	
	// Execute the statement with the provided title and description as parameters
	$stmt->execute([$title, $description]);
}

```

Now we need to create the ```handleForms.php``` which will handle our form. Info inputted here will be inserted to the tasks table. The require_once statement is used to include PHP code from another file. If the file is not found, a fatal error is thrown, and the program stops. 

```handleForms.php```

```php
<?php  
require_once('dbConfig.php'); // Include the 'dbConfig.php' file

require_once('functions.php'); // Include the 'functions.php' file

if(isset($_POST['submitBtn'])) { // Check if the 'submitBtn' is set in the POST request

	$title = $_POST['title']; // Assign the value of 'title' from the POST request to the $title variable

	$description = $_POST['title']; // Assign the value of 'title' from the POST request to the $description variable

	makeATask($conn, $title, $description); // Call the 'makeATask' function with the $conn, $title, and $description variables
}
?>

```

### Reading records from the database

For now, we should add a feature that can enable us to see the records from the database. Let's first add a function that selects all information from the database. 

```execute()```  method is used to execute a prepared SQL statement. It sends the SQL query to the database server and returns true on success or false on failure. 

```$stmt->execute()``` is used to execute the prepared statement $stmt and retrieve all the tasks from the database. 

```fetchAll()``` method is used to fetch all the rows returned by a SQL query as an array. It returns an array containing all the rows fetched from the database. Each row is represented as an associative array, where the keys are the column names and the values are the corresponding column values. In this code, $stmt->fetchAll() is used to fetch all the tasks returned by the SQL query and return them as an array.


```functions.php```

```php
function getAllTasks($conn) {

	// SQL query to select all tasks from the table
	$sql = "SELECT * FROM tasks";
	
	// Prepare the SQL statement
	$stmt = $conn->prepare($sql);
	
	// Execute the prepared statement
	$stmt->execute();
	
	// Return all the fetched rows as an array
	return $stmt->fetchAll();
}

```

Modify the ```index.php```. We need to call the ```getAllTasks()``` function and we can show now each task stored into the database. 

```index.php```

```php
<?php  
require_once('dbConfig.php');
require_once('functions.php');
?>

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
	<style>
		.tasks {
			height: auto;
			width: 500px;
			border-style: solid;
			margin-top: 10px;
		}
	</style>	
</head>
<body>
	<h1>Welcome to our to do list</h1>
	<form action="handleForms.php" method="POST">
		<p><input type="text" name="title" placeholder="title here"></p>
		<p><input type="text" name="description" placeholder="description here"></p>
		<p><input type="submit" value="Submit" name="submitBtn"></p>
	</form>

	<?php $allTasks = getAllTasks($conn); ?>

	<?php foreach ($allTasks as $row) { ?>
	
	<div class="tasks">
		<h1><?php echo $row['title']; ?></h1>
		<i><?php echo $row['date_created']; ?></i>
		<p><?php echo $row['description']; ?></p>
	</div>

	<?php } ?>
</body>
</html>
```

Add header function to our ```handleForms.php``` file. It is commonly used for redirection by setting the Location header.

```handleForms.php```

```php
<?php  
require_once('dbConfig.php'); // Include the 'dbConfig.php' file

require_once('functions.php'); // Include the 'functions.php' file

if(isset($_POST['submitBtn'])) { // Check if the 'submitBtn' is set in the POST request

	$title = $_POST['title']; // Assign the value of 'title' from the POST request to the $title variable

	$description = $_POST['title']; // Assign the value of 'title' from the POST request to the $description variable

	makeATask($conn, $title, $description); // Call the 'makeATask' function with the $conn, $title, and $description variables

	// Redirect to the index.php page
	header('Location: index.php');
}
?>
```

### How to create a login and registration page?

Let's first create ```users``` table. 

<img src="Images/7_create_users_table.png">

```dbConfig.php```

```php
<?php 

$host = "localhost";
$user = "root";
$password = "";
$dbname = "test";
$dsn = "mysql:host={$host};dbname={$dbname}";

$conn = new PDO($dsn, $user, $password);
$conn->exec("SET time_zone = '+08:00';");

?>
```
```functions.php```

```php
<?php  
function addUser($conn, $username, $password) {
	$sql = "SELECT * FROM users WHERE username=?";
	$stmt = $conn->prepare($sql);
	$stmt->execute([$username]);

	if($stmt->rowCount()==0) {
		$sql = "INSERT INTO users (username,password) VALUES (?,?)";
		$stmt = $conn->prepare($sql);
		return $stmt->execute([$username, $password]);
	}
}

function login($conn, $username, $password) {
	$query = "SELECT * FROM users WHERE username=?";
	$stmt = $conn->prepare($query);
	$stmt->execute([$username]);

	if($stmt->rowCount() == 1) {
		// returns associative array
		$row = $stmt->fetch();

		// store user info as a session variable
		$_SESSION['userInfo'] = $row;

		// get values from the session variable
		$uid = $row['user_id'];
		$uname = $row['username'];
		$passHash = $row['password'];

		// validate password 
		if(password_verify($password, $passHash)) {
			$_SESSION['user_id'] = $uid;
			$_SESSION['username'] = $uname;
			$_SESSION['email'] = $email;
			$_SESSION['userLoginStatus'] = 1;
			return true;
		}
		else {
			return false;
		}
	}
}

?>
```


```handleForm.php```

```php
<?php  
session_start();
require_once('dbConfig.php');
require_once('functions.php');

if (isset($_POST['regBtn'])) {
	$username = $_POST['username'];
	$password = password_hash($_POST['password'], PASSWORD_DEFAULT);

	if(empty($username) || empty($password)) {
		echo '<script> 
		alert("The input field is empty!");
		window.location.href = "register.php";
		</script>';
	}
	
	else {

		if(addUser($conn, $username, $password)) {
			header('Location: index.php');
		}

		else {
			header('Location: register.php');
		}

	}
}

if (isset($_POST['loginBtn'])) {
	$username = $_POST['username'];
	$password = $_POST['password'];

	if(empty($username) && empty($password)) {
		echo "<script>
		alert('Input fields are empty!');
		window.location.href='index.php'
		</script>";
	} 
	else {

		if(login($conn, $username, $password)) {
			header('Location: index.php');
		}

		else {
			header('Location: login.php');
		}
	}
	
}
?>
```

```register.php```

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body>
	<p>Register here</p>
	<form action="handleForm.php" method="POST">
		<div class="fields">
			<p><input type="text" placeholder="username here" class="fields" name="username"></p>
			<p><input type="password" placeholder="password here" class="fields" name="password"></p>
			<p><input type="submit" value="Register" id="submitBtn" name="regBtn"></p>
		</div>
	</form>
</body>
</html>
```

```login.php```

```html
<?php 
session_start();

if(isset($_SESSION['welcomeMessage']) && !isset($_SESSION['username'])) {
	echo $_SESSION['welcomeMessage'];
}


?>
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body>
	<p>Login here</p>
	<form action="handleForm.php" method="POST">
		<div class="fields">
			<p><input type="text" placeholder="username here" class="fields" name="username"></p>
			<p><input type="password" placeholder="password here" class="fields" name="password"></p>
			<p><input type="submit" value="login" id="loginBtn" name="loginBtn"></p>
		</div>
	</form>
	<a href="register.php">Register</a>
</body>
</html>
```

```index.php```

```html
<?php 
session_start();

if(!isset($_SESSION['username'])) {
	header('Location: login.php');
} 
?>
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body>
	<h1>Welcome! <?php echo $_SESSION['username'];?></h1>
	<a href="logout.php">Logout</a>
</body>
</html>
```

```logout.php```

```php
<?php  
session_start();
session_unset();
header('Location: index.php');
?>
```













