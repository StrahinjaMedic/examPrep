<?php

// laat de fouten zien
error_reporting(-1);
ini_set('display_errors', 'On');

$servername = "localhost";
$username = "root";
$password = "root";
$database = "-DBNAME-";

//maak de database verbinding
$mysqli = mysqli_connect($servername, $username, $password, $database);

// controleer de verbinding
if ($mysqli->connect_error) {
    die("Connection failed: " . $mysqli->connect_error);
}
