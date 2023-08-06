# student_registration
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>registration form</title>
</head>
<body>
    <form method="post">
        NAME:<input type="text" name="nm" required><br>
        EMAIL:<input type="email" name="em" required><br>
        <input type="submit" value="register" name="sm">
    </form>
    <?php
    $con=mysqli_connect('localhost','root','','record');
    if(isset($_POST['sm']))
    {
        $name=$_POST['nm'];
        $email=$_POST['em'];
        $query="INSERT INTO register(NAME,EMAIL)VALUES ('$name','$email')";
        $run=mysqli_query($con,$query);
    }
    ?>
</body>
</html>
