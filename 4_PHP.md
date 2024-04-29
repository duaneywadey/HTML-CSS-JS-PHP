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