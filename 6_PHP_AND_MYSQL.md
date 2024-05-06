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

Before we proceed with the PDO concepts, let's first create a database in MySQL. Make sure first that you already started MySQL in XAMPP.

![image]([IMAGES]\1_start and stop php mysql.png)




