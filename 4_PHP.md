# PART 1 (Variables, Arrays, Operators)

### PHP Variables
PHP code always starts with ```<?php``` and then ends with ```?>```. We display outputs using the ```echo``` statement.
```php
<?php 

// Declaring variables in PHP
$name  = 'Ivy';
$price = 5;

?>
<!DOCTYPE html>
<html>
  <head>
    <title>Variables</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>

    // We display the value of the variables below.

    <h2>Welcome <?php echo $name; ?></h2>
    <p>The cost of your candy is 
      <?php echo $price; ?> per pack.</p>

  </body>
</html>
```

### Concatenating strings in PHP

We can concatenate variables in PHP using the dot symbol. 

```php
<?php
$prefix  = 'Thank you';
$name    = 'Ivy';
$message = $prefix . ', ' . $name;
?>
<!DOCTYPE html>
<html>
  <head>
    <title>String Operator</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2><?php echo $name; ?>'s Order</h2>
    <p><?php echo $message; ?></p>
  </body>
</html>
```

### Updating variables in PHP
```PHP
<?php 
$name  = 'Guest';
$name  = 'Ivy';
$price = 5;
?>
<!DOCTYPE html>
<html>
  <head>
    <title>Updating Variables</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Welcome <?php echo $name; ?></h2>
    <p>The cost of your candy is 
       $<?php echo $price; ?> per pack.</p>
  </body>
</html>
```


### Arithmetic operators 

```php
<?php 
$items    = 3;
$cost     = 5;
$subtotal = $cost * $items;
$tax      = ($subtotal / 100) * 20;
$total    = $subtotal + $tax;
?>
<!DOCTYPE html>
<html>
  <head>
    <title>Mathematical Operators</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Shopping Cart</h2>
    <p>Items: <?php echo $items ?></p>
    <p>Cost per pack: $<?php echo $cost ?></p>
    <p>Subtotal: $<?php echo $subtotal ?></p>
    <p>Tax: $<?php echo $tax ?></p>
    <p>Total: $<?php echo $total ?></p>
  </body>
</html>
```


### Logical operators in PHP
```php
<!DOCTYPE html>
<html>
<head>
    <title>Logical Operators Example</title>
</head>
<body>
    <?php
        // Logical OR (||) operator
        $age = 25;
        $country = "USA";

        if ($age >= 18 || $country == "USA") {
            echo "You are eligible to vote in the USA!";
        } else {
            echo "You are not eligible to vote in the USA.";
        }

        echo "<br>";

        // Logical AND (&&) operator
        $num1 = 10;
        $num2 = 5;

        if ($num1 > 0 && $num2 < 10) {
            echo "Both conditions are true!";
        } else {
            echo "At least one condition is false.";
        }

        echo "<br>";

        // Logical NOT (!) operator
        $isLoggedIn = false;

        if (!$isLoggedIn) {
            echo "Please log in to access this page.";
        } else {
            echo "Welcome to the protected page!";
        }
    ?>
</body>
</html>
```