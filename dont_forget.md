#Slider with php tips
- https://slides.com/codepamoja/php-oop-crud#/2/2

# This wil show the errors
error_reporting(-1);
ini_set('display_errors', 'On');

# This will provide you with a redirect to the login if someone isn't logged in
- with this redirect you will be redirected to the login.php page is you aren't logged in

<?php 
  session_start(); 

  if ((!isset($_SESSION['gebruikersnaam'])) || isset($_GET['loguit'] )) {
    session_destroy();
    unset($_SESSION['gebruikersnaam']);
    header("location: login.php");
  }
?>


# How to setup a DB connection
$servername = "localhost";
$username = "root";
$password = "root";
$database = "crudDB";

$mysqli = mysqli_connect($servername, $username, $password, $database);

if ($mysqli->connect_error) {
    die("Connection failed: " . $mysqli->connect_error);
