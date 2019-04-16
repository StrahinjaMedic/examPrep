## Database connection

# How to setup a DB connection
$servername = "localhost";
$username = "root";
$password = "root";
$database = " ";

$mysqli = mysqli_connect($servername, $username, $password, $database);

if ($mysqli->connect_error) {
    die("Connection failed: " . $mysqli->connect_error);

