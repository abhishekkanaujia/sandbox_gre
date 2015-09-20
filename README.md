<form action="" method="post">
Name:<input type="email" required name='n1'><br>
Password:<input type="password" required name='p1'>
<br>
<input type="submit">
<?php
if($_POST)
{
$name=$_POST['n1'];
$password=$_POST['p1'];
mysql_connect("localhost","root","");
		   mysql_select_db("homework1");
		   $a=mysql_query("select * from hw1 where name='$name' and password='$password'");
		   if(mysql_num_rows($a)!=0)
		   {
		   session_start();

$_SESSION['yo']=$name;
header("location:yo.php");
?>

