# PART 1 (Variables, Arrays, Operators)
Here's a markdown file consisting of the concepts you need to know about PHP. The following codes shown below comes from Jon Duckett's book PHP and MySQL. If you want to study in advance, here's the [link](https://github.com/duaneywadey/PHP-Resources) to the repository containing all of the book's PHP codes.  

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

### Indexed Arrays in PHP

```php
<?php 
$best_sellers = ['Chocolate', 'Mints', 'Fudge',
    'Bubble gum', 'Toffee', 'Jelly beans',];
?>
<!DOCTYPE html>
<html>
  <head>
    <title>Indexed Arrays</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Best Sellers</h2>
    <ul>
      <li><?php echo $best_sellers[0]; ?></li>
      <li><?php echo $best_sellers[1]; ?></li>
      <li><?php echo $best_sellers[2]; ?></li>
    </ul>
  </body>
</html>
```

### Multidimensional Arrays

```php
<?php 
$offers = [
    ['name' => 'Toffee', 'price' => 5, 'stock' => 120,],
    ['name' => 'Mints',  'price' => 3, 'stock' => 66,],
    ['name' => 'Fudge',  'price' => 4, 'stock' => 97,],
];
?>
<!DOCTYPE html>
<html>
  <head>
    <title>Multidimensional Arrays</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Offers</h2>
    <p><?php echo $offers[0]['name']; ?> -
      $<?php echo $offers[0]['price']; ?> </p>
    <p><?php echo $offers[1]['name']; ?> -
      $<?php echo $offers[1]['price']; ?> </p>
    <p><?php echo $offers[2]['name']; ?> -
      $<?php echo $offers[2]['price']; ?> </p>
  </body>
</html>
```

### Associative Arrays
An associative array is a type of array in PHP that uses named keys instead of numeric keys to access and store values. It is also known as a map or dictionary in other programming languages. 

```php
<?php 
$nutrition = [
    'fat'   => 16,
    'sugar' => 51,
    'salt'  => 6.3,
];
?>
<!DOCTYPE html>
<html>
  <head>
    <title>Associative Arrays</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Nutrition (per 100g)</h2>
    <p>Fat:   <?php echo $nutrition['fat']; ?>%</p>
    <p>Sugar: <?php echo $nutrition['sugar']; ?>%</p>
    <p>Salt:  <?php echo $nutrition['salt']; ?>%</p>
  </body>
</html>
```

### Echo shorthand
```php
<?php 
$name      = 'Ivy';
$favorites = ['Chocolate', 'Toffee', 'Fudge',];
?>
<!DOCTYPE html>
<html>
  <head>
    <title>Echo Shorthand</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>

    <h1>The Candy Store</h1>

    // Shorter way to print variables in PHP
    <h2>Welcome <?= $name ?></h2>
    <p>Your favorite type of candy is:
       <?= $favorites[0] ?>.</p>

  </body>
</html>
```

### Application of the concepts
```php
<?php
$username = 'Ivy';                                   // Variable to hold username

$greeting = 'Hello, ' . $username . '.';             // Greeting is 'Hello' + username

$offer = [                                           // Create array to hold offer
    'item'     => 'Chocolate',                       // Item on offer
    'qty'      => 5,                                 // Quantity to buy
    'price'    => 5,                                 // Usual price per pack
    'discount' => 4,                                 // Offer price per pack
];

$usual_price = $offer['qty'] * $offer['price'];      // Usual total price
$offer_price = $offer['qty'] * $offer['discount'];   // Offer total price
$saving      = $usual_price - $offer_price;          // Total saving
?>
<!DOCTYPE html>
<html>
  <head>
    <title>The Candy Store</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>

    <h2>Multi-buy Offer</h2>

    <p><?= $greeting ?></p>

    <p class="sticker">Save $<?= $saving ?></p>

    <p>Buy <?= $offer['qty'] ?> packs of <?= $offer['item'] ?> 
      for $<?= $offer_price ?><br> (usual price $<?= $usual_price ?>)</p> 
  </body>
</html>
```

# Part 2 (Conditional Statements, Iteration)

### If else statement 
```php
<?php 
$stock = 5;

if ($stock > 0) {
    $message = 'In stock';
} else {
    $message = 'Sold out';
}
?>
<!DOCTYPE html>
<html>
  <head>
    <title>if else Statement</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Chocolate</h2>
    <p><?= $message ?></p>
  </body>
</html>
```

### Else if statement in PHP
```php
<?php 
$stock   = 5;
$ordered = 3;

if ($stock > 0) {
    $message = 'In stock';
} elseif ($ordered > 0) {
    $message = 'Coming soon';
} else {
    $message = 'Sold out';
}
?>
<!DOCTYPE html>
<html>
  <head>
    <title>if else if Statement</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Chocolate</h2>
    <p><?= $message ?></p>
  </body>
</html>
```


### For loop in PHP
```php
<?php
$price = 1.99;
?>
<!DOCTYPE html>
<html>
  <head>
    <title>for Loop</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Prices for Multiple Packs</h2>
    <p>
      <?php
      for ($i = 1; $i <= 10; $i++) {
          echo $i;
          echo ' packs cost $';
          echo $price * $i;
          echo '<br>';
      }
      ?>
    </p>
  </body>
</html>
```

### Foreach loop  
Mostly for printing values inside associative arrays.
```php
<?php
$products = [
    'Toffee' => 2.99,
    'Mints'  => 1.99,
    'Fudge'  => 3.49,
];
?>
<!DOCTYPE html>
<html>
  <head>
    <title>foreach Loop</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Price List</h2>
    <table>
      <tr>
        <th>Item</th>
        <th>Price</th>
      </tr>
      <?php foreach ($products as $item => $price) { ?>
        <tr>
          <td><?= $item ?></td>
          <td>$<?= $price ?></td>
        </tr>
      <?php } ?>
    </table>
  </body>
</html>
```

It can also be used to access single values.

```php
<?php
$best_sellers = ['Toffee', 'Mints', 'Fudge',];
?>
<!DOCTYPE html>
<html>
  <head>
    <title>foreach Loop - Just Accessing Values</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Best Sellers</h2>
    <?php foreach ($best_sellers as $product) { ?>
      <p><?= $product ?></p>
    <?php } ?>
  </body>
</html>
```

### Switch statement in PHP

```php
<?php
$day = 'Monday';

switch ($day) {
    case 'Monday':
        $offer = '20% off chocolates';
        break;
    case 'Tuesday':
        $offer = '20% off mints';
        break;
    default:
        $offer = 'Buy three packs, get one free';
}
?>
<!DOCTYPE html>
<html>
  <head>
    <title>switch Statement</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Offers on <?= $day; ?></h2>
    <p><?= $offer ?></p>
  </body>
</html>
```

### While loop in PHP
```php
<?php
$counter = 1;
$packs   = 5;
$price   = 1.99;
?>
<!DOCTYPE html>
<html>
  <head>
    <title>while Loop</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Prices for Multiple Packs</h2>
    <p>
      <?php
      while ($counter <= $packs) {
          echo $counter;
          echo ' packs cost $';
          echo $price * $counter; 
          echo '<br>';
          $counter++;
      }
      ?>
    </p>
  </body>
</html>
```

### Ternary operator
The code below tells us that if $stock is greater than zero, we display 'In stock', or else, display 'Sold out'.

```php
<?php 
$stock   = 5;

$message = ($stock > 0) ? 'In stock' : 'Sold out';
?>
<!DOCTYPE html>
<html>
  <head>
    <title>Ternary Operator</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Chocolate</h2>
    <p><?= $message ?></p>
  </body>
</html>
```

# Part 3 (Functions)

### Basic Functions
In this code we created two functions. We called both functions in our HTML template.
```php
<?php
function write_logo()
{
    echo 'Writing a logo...';
}

function welcome_user()
{
  echo "Hello there! Welcome";
}
?>
<!DOCTYPE html>
<html>
  <head>
    <title>Basic Functions</title>
  </head>
  <body>
    <h1><?php write_logo()?> The Candy Store</h1>
    <h2><?php welcome_user()?></h2>
    <footer>
      <?php write_logo() ?>
    </footer>
  </body>
</html>
```

### Function with return statements

```php
<?php
function create_logo()
{
    return 'Logo 1, now created';
}

function create_copyright_notice()
{
    $year    = date('Y');
    $message = '&copy; ' . $year;
    return $message;
}
?>
<!DOCTYPE html>
<html>
  <head>
    <title>Functions with Return Values</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <header>
      <h1><?= create_logo() ?>The Candy Store</h1>
    </header>
    <article>
      <h2>Welcome to The Candy Store</h2>
    </article>
    <footer>
      <?= create_logo() ?>
      <?= create_copyright_notice() ?>
    </footer>
  </body>
</html>
```

### Multiple return arguments
```php
<?php
$stock = 25;

function get_stock_message($stock)
{
    if ($stock >= 10) {
        return 'Good availability';
    }
    if ($stock > 0 && $stock < 10) {
        return 'Low stock';
    }
    return 'Out of stock';
}
?>
<!DOCTYPE html>
<html> 
  <head>
    <title>Multiple Return Statements</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Chocolates</h2>
    <p><?= get_stock_message($stock) ?></p>
  </body>
</html>
```


### Default values for function parameters
```php
<?php
function calculate_cost($cost, $quantity, $discount = 0)
{
    $cost = $cost * $quantity;
    return $cost - $discount;
}
?>
<!DOCTYPE html>
<html> 
  <head>
    <title>Default Values for Parameters</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Chocolates</h2>
    <p>Dark chocolate $<?= calculate_cost(5, 10, 5) ?></p>
    <p>Milk chocolate $<?= calculate_cost(3, 4) ?></p>
    <p>White chocolate $<?= calculate_cost(4, 15, 20) ?></p>
  </body>
</html>
```

### Global and local scope in PHP

```PHP
<?php
$tax = '20';

function calculate_total($price, $quantity)
{
    $cost  = $price * $quantity;
    $tax   = $cost  * (20 / 100);
    $total = $cost  + $tax;
    return $total;
}
?>
<!DOCTYPE html>
<html>
  <head>
    <title>Global and Local Scope</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <p>Mints:  $<?= calculate_total(2, 5) ?></p>
    <p>Toffee: $<?= calculate_total(3, 5) ?></p>
    <p>Fudge:  $<?= calculate_total(5, 4) ?></p>
    <p>Prices include tax at: <?= $tax ?>%</p>
  </body>
</html>
```

### Type declarations in PHP
```PHP
<?php
$price    = 4;
$quantity = 3;

function calculate_total(int $price, int $quantity): int
{
    return $price * $quantity;
}

$total = calculate_total($price, $quantity);
?>
<!DOCTYPE html>
<html> 
  <head>
    <title>Type Declarations</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Chocolates</h2>
    <p>Total $<?= $total ?></p>
  </body>
</html>
```

### Applying the concepts about functions

```php
<?php
declare(strict_types = 1);
$candy = [
    'Toffee' => ['price' => 3, 'stock' => 12],
    'Mints'  => ['price' => 2, 'stock' => 26],
    'Fudge'  => ['price' => 4, 'stock' => 8],
];

$tax = 20;

function get_reorder_message(int $stock): string
{
    return ($stock < 10) ? 'Yes' : 'No';
}

function get_total_value(float $price, int $quantity): float
{
    return $price * $quantity;
}

function get_tax_due(float $price, int $quantity, int $tax = 0): float
{
    return ($price * $quantity) * ($tax / 100);
}
?>
<!DOCTYPE html>
<html> 
  <head>
    <title>Functions Example</title>
    <link rel="stylesheet" href="css/styles.css">
  </head>
  <body>
    <h1>The Candy Store</h1>
    <h2>Stock Control</h2>
    <table>
      <tr>
        <th>Product</th><th>Stock</th><th>Re-order</th><th>Total value</th><th>Tax due</th>
      </tr>
      <?php foreach ($candy as $product_name => $data) { ?>
        <tr>
          <td><?=  $product_name ?></td>
          <td><?=  $data['stock'] ?></td>
          <td><?=  get_reorder_message($data['stock']) ?></td>
          <td>$<?= get_total_value($data['price'], $data['stock']) ?></td>
          <td>$<?= get_tax_due($data['price'], $data['stock'], $tax) ?></td>
       </tr>
      <?php } ?>
    </table>
  </body>
</html>
```