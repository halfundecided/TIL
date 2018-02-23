### PHP & MySQL
1. PHP&MySQL 연동
````php
<?php
$conn = ("localhost", "root", "<password>", "<databasename>");
?>
````

2. Query
````php
mysqli_query($conn, "
	INSERT INTO topic
	  (<?php
$conn = mysqli_connect("localhost", "root", "Rhkgkrrh8818!", "opentutorials");
mysqli_query($conn, "
  INSERT INTO topic
    (title, description, created)
    VALUE (
      'MySQL',
      'MySQL is ..',
      NOW()
    )
  ");
 ?>
````
