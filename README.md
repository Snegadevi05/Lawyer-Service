# lawyer-service

Index.php
<html>
<title>Lawyer</title>
<style>

p
{
	color:#ffffff;
	text-align: center;
	text-transform: uppercase;
	 font-size:15px;
}

ul {
	padding:50px;
	
  list-style-type: none;
  overflow: hidden;
  background:#fffff;
   background-repeat: no-repeat;
   background-size: 1420px  200px;
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
   border-radius:10px;
}

li {
  float: left;
}

li a {
  display: block;
  color: #000000;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #ccffff;
}

.active {
  background-color: #4CAF50;
}

#footer {
  border: 2px solid #fffff;
  padding: 45px;
  background: #000000;
  background-repeat: no-repeat;
  background-size: 1420px  100px;
  border-radius:10px;
  text-align:center;
  text-decoration:blink;
   font-family: Arial;
   font-size:15px;
}
#bg1 {

  padding:150px;
  background:url("images/1.jpg");
  background-repeat: no-repeat;
  background-size: 1420px  300px;
   border-radius:90px;
    text-align:left;
   font-size:35px;
   color:#000000;
}

</style>
</head>
<ul>
	 <li><a href="#">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</a></li>
  <li><a class="active" href="index.php"><strong>Home Page</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="admin.php"><strong>Admin login</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="lawyer.php"><strong>Advocate Login</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="user.php"><strong>User Login</a></li>
  <li><a href="#">&nbsp;</a></li>
   <li><a href="about.php"><strong>About Us</a></li>
   </ul>

<br />
<br />
<div id="bg1">Online Lawyer Web Application</div>



<div> &nbsp;</div>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<div id="footer"> <p>copyrights & designedby@lawyer Web Application</p>
</div>

Adminhome.php

<html>
<title>Lawyer</title>
<style>

p
{
	color:#ffffff;
	text-align: center;
	text-transform: uppercase;
	 font-size:15px;
}

ul {
	padding:50px;
	
  list-style-type: none;
  overflow: hidden;
  background:#fffff;
   background-repeat: no-repeat;
   background-size: 1420px  200px;
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
   border-radius:10px;
}

li {
  float: left;
}

li a {
  display: block;
  color: #000000;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #ccffff;
}

.active {
  background-color: #4CAF50;
}

#footer {
  border: 2px solid #fffff;
  padding: 45px;
  background: #000000;
  background-repeat: no-repeat;
  background-size: 1420px  100px;
  border-radius:10px;
  text-align:center;
  text-decoration:blink;
   font-family: Arial;
   font-size:15px;
}
#bg1 {

  padding:150px;
  background:url("images/1.jpg");
  background-repeat: no-repeat;
  background-size: 1420px  300px;
  border-radius:5px;
   border-radius:90px;
    text-align:left;
   font-size:35px;
   color:#000000;
}

</style>
</head>
<ul>
	 <li><a href="#">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</a></li>
 <li class="active"><a href="adminhome.php">Home</a></li>
  <li><a href="#">&nbsp;</a></li>
   <li><a href="lview.php"><strong>View Lawyers</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="uview.php"><strong>View Users</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="viewb.php"><strong>View Bookings</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="index.php"><strong>LogOut</a></li>
</ul>

<br />
<br />
<div id="bg1">Online Lawyer Web Application</div>



<div> &nbsp;</div>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<div id="footer"> <p>copyrights & designedby@Layer Web Application</p>
</div>

dbconnect.php
<?php
$connect=mysql_connect("localhost","root","");
mysql_select_db("online lawyer",$connect);
?>

admin.php
<?php
 	$connect=mysql_connect("localhost","root","");
	mysql_select_db("online lawyer",$connect);
	extract($_POST);
	session_start();

if(isset($_POST['btn']))
{
$qry=mysql_query("select * from admin where name='$uname' && psw='$password'");
$num=mysql_num_rows($qry);
if($num==1)
{
?>
<script>alert('welcome to admin home page');
</script>
<?php

header("location:adminhome.php");
}
else
{
echo "<script> alert('User Name Password Wrong.....')</script>";

}
}
?> 


<html>
<title>Lawyer</title>
<style>

p
{
	color:#ffffff;
	text-align: center;
	text-transform: uppercase;
	 font-size:15px;
}

ul {
	padding:50px;
	
  list-style-type: none;
  overflow: hidden;
  background:#fffff;
   background-repeat: no-repeat;
   background-size: 1420px  200px;
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
   border-radius:10px;
}

li {
  float: left;
}

li a {
  display: block;
  color: #000000;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #ccffff;
}

.active {
  background-color: #4CAF50;
}

#footer {
  border: 2px solid #fffff;
  padding: 45px;
  background: #000000;
  background-repeat: no-repeat;
  background-size: 1420px  100px;
  border-radius:10px;
  text-align:center;
  text-decoration:blink;
   font-family: Arial;
   font-size:15px;
}
#bg1 {

  padding:150px;
  background:url("images/1.jpg");
  background-repeat: no-repeat;
  background-size: 1420px  300px;
  border-radius:5px;
   border-radius:90px;
    text-align:left;
   font-size:35px;
   color:#000000;
}

</style>
</head>
<ul>
	 <li><a href="#">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</a></li>
  <li><a  href="index.php"><strong>Home Page</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a class="active" href="admin.php"><strong>Admin login</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="lawyer.php"><strong>Advocate Login</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="user.php"><strong>User Login</a></li>
  <li><a href="#">&nbsp;</a></li>
   <li><a href="about.php"><strong>About Us</a></li>
</ul>

<br />
<br />
<div id="bg1">Online Lawyer Web Application</div>


<form id="form1" name="form1" method="post" action="">
	   <table width="46%" border="0" align="center">
         <tr>
           <td colspan="2" rowspan="1"><div align="center" class="style1"><strong><font size="+1">Admin Login</font> </div></td>
		 </tr>
			<tr>
		<td width="48%">&nbsp;</td>
		    <td width="52%">&nbsp;</td>
	  		</tr>
         </tr>
         <tr>
           <td height="31"align="center"><span class="style2"><strong>User Name </strong></span></td>
           <td><label>
             <input name="uname" type="text" id="uname" />
           </label></td>
         </tr>
         <tr>
           <td height="44" align="center"><span class="style2"><strong>Password</strong></span></td>
           <td><label>
             <input name="password" type="password" id="password" />
           </label></td>
         </tr>
         <tr>
           <td>&nbsp;</td>
           <td rowspan="2"><label>
             <input name="btn" type="submit" id="btn" value="Login" />
             <input type="reset" name="Submit2" value="Cancel" />
           </label></td>
         </tr>
  </table>
</form>
<div> &nbsp;</div>
<br>
<br>
<div id="footer"> <p>copyrights & designedby@lawyer Web Application</p></div>

user.php
<?php
include("dbconnect.php");
session_start();
extract($_POST);
if(isset($_POST['btn']))
{
$qry1=mysql_query("select * from regist where uname='$uname' && psw='$password'");
$num=mysql_num_rows($qry1);
if($num==1)
{
$rw=mysql_fetch_array($qry1);
$_SESSION['uid']=$rw['id'];
echo $uid;
?>
<script language="javascript">
alert("Login Successfully..");
//alert("Your Account Not Approval..");
window.location.href="userhome.php";
</script>
<?php
}
}

?>



<html>
<title>Lawyer</title>
<style>

p
{
	color:#ffffff;
	text-align: center;
	text-transform: uppercase;
	 font-size:15px;
}

ul {
	padding:50px;
	
  list-style-type: none;
  overflow: hidden;
  background:#fffff;
   background-repeat: no-repeat;
   background-size: 1420px  200px;
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
   border-radius:10px;
}

li {
  float: left;
}

li a {
  display: block;
  color: #000000;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #ccffff;
}

.active {
  background-color: #4CAF50;
}

#footer {
  border: 2px solid #fffff;
  padding: 45px;
  background: #000000;
  background-repeat: no-repeat;
  background-size: 1420px  100px;
  border-radius:10px;
  text-align:center;
  text-decoration:blink;
   font-family: Arial;
   font-size:15px;
}
#bg1 {

  padding:150px;
  background:url("images/1.jpg");
  background-repeat: no-repeat;
  background-size: 1420px  300px;
  border-radius:5px;
   border-radius:90px;
    text-align:left;
   font-size:35px;
   color:#000000;
}

</style>
</head>
<ul>
	 <li><a href="#">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</a></li>
  <li><a class="active" href="index.php"><strong>Home Page</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="admin.php"><strong>Admin login</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="lawyer.php"><strong>Advocate Login</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="user.php"><strong>User Login</a></li>
  <li><a href="#">&nbsp;</a></li>
   <li><a href="about.php"><strong>About Us</a></li>
</ul>

<br />
<br />
<div id="bg1">Online Lawyer Web Application</div>
<form id="form1" name="form1" method="post" action="">
	   <table width="46%" border="0" align="center">
         <tr>
           <td colspan="2" rowspan="1"><div align="center" class="style1"><strong><font size="+1">User Login</font> </div></td>
		 </tr>
			<tr>
		<td width="48%">&nbsp;</td>
		    <td width="52%">&nbsp;</td>
	  		</tr>
         </tr>
         <tr>
           <td height="31"align="center"><span class="style2"><strong>User Name </strong></span></td>
           <td><label>
             <input name="uname" type="text" id="uname" />
           </label></td>
         </tr>
         <tr>
           <td height="44" align="center"><span class="style2"><strong>Password</strong></span></td>
           <td><label>
             <input name="password" type="password" id="password" />
           </label></td>
         </tr>
         <tr>
           <td>&nbsp;</td>
           <td rowspan="2"><label>
             <input name="btn" type="submit" id="btn" value="Login" />
             <input type="reset" name="Submit2" value="Cancel" />
           </label></td>
         </tr>
  
  				
  			 
		  <tr>
           <td>&nbsp;</td>
           <td width="24%" rowspan="2"><label>
             <a href="regist.php">User Registration</a>
           </label></td>
         </tr>
  
  
  </table>
</form>
         <div> &nbsp;</div>
<br>
<br>
<div id="footer"> <p>copyrights & designedby@lawyer Web Application</p></div>


userhome.php
include("dbconnect.php");
session_start();
extract($_POST);
$id=$_SESSION['uid'];
?>


<html>
<title>Lawyer</title>
<style>

p
{
	color:#ffffff;
	text-align: center;
	text-transform: uppercase;
	 font-size:15px;
}

ul {
	padding:50px;
	
  list-style-type: none;
  overflow: hidden;
  background:#fffff;
   background-repeat: no-repeat;
   background-size: 1420px  200px;
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
   border-radius:10px;
}

li {
  float: left;
}

li a {
  display: block;
  color: #000000;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #ccffff;
}

.active {
  background-color: #4CAF50;
}

#footer {
  border: 2px solid #fffff;
  padding: 45px;
  background: #000000;
  background-repeat: no-repeat;
  background-size: 1420px  100px;
  border-radius:10px;
  text-align:center;
  text-decoration:blink;
   font-family: Arial;
   font-size:15px;
}
#bg1 {

  padding:150px;
  background:url("images/1.jpg");
  background-repeat: no-repeat;
  background-size: 1420px  300px;
  border-radius:5px;
   border-radius:90px;
    text-align:left;
   font-size:35px;
   color:#000000;
}

</style>
</head>
<ul>
	<ul>
		<li><a href="#">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</a></li>
              <li class="active"><a href="userhome.php">Home</a></li>
			   <li><a href="#">&nbsp;</a></li>
			   <li><a href="viewstatus.php">ViewStatus</a></li>
			   <li><a href="#">&nbsp;</a></li>
        <li><a href="payment.php">Make Payment</a></li>
		<li><a href="#">&nbsp;</a></li>
		<li><a href="index.php">LogOut</a></li>
		 </ul>
</ul>

<br />
<br />
<div id="bg1">Online Lawyer Web Application</div>
		  
			
			
			
			
			
			<form action="#" method="post">
			<table width="100" align="center">
			
			<tr>
			<td>&nbsp;</td>
			<td><label>
                               <select name="lt">
							   <option value=""> Select</option>
							   <option value="Criminal Lawyer"> Criminal Lawyer</option>
							   <option value="Business Lawyer"> Business Lawyer</option>
							   <option value="Corporate Lawyer"> Corporate Lawyer</option>
							   <option value="Civil Lawyer"> Civil Lawyer</option>
							   <option value="Real Estate Lawye"> Real Estate Lawyer</option>
							   <option value="Divorce Lawyer">Divorce Lawyer</option>
							   </select>
                             </label></td>
							 
							 <td><input type="submit" name="btn" />
							 
							 
							 </tr>
							 
							 </table>
							</form>
			
			
			 <table width="100%" border="0" align="center">
		
		<tr>
		<td colspan="11" align="center"><strong>Lawyers Details</strong></td>
		</tr>
		
		<tr>
		<td colspan="6">&nbsp;</td>
		</tr>
		<tr>
			<td>&nbsp;</td>
			 <td><div align="center" class="style6"><strong>Lawyer Name</strong> </div></td>
			  <td><div align="center" class="style6"><strong>Gender</strong> </div></td>
			  <td><div align="center" class="style6"><strong>Lawyer Type</strong> </div></td>
			  <td><div align="center" class="style6"><strong>Experiance</strong> </div></td>
			  <td><div align="center" class="style6"><strong>E-mail</strong></div></td>
			  <td><div align="center" class="style6"><strong>Location</strong></div></td>
			   <td><div align="center" class="style6"><strong>Book</strong></div></td>
			  </tr>
			<tr>
		<td colspan="6">&nbsp;</td>
		</tr>
	<?php
	
		$qry=mysql_query("select * from lregist where ltype='$lt'");
		$i=1;		
		while($row=mysql_fetch_array($qry))
		{
		?>
        <tr>
		<td>&nbsp;</td>
		 <td><div align="center"><?php echo $row['name'];?></div></td>
		  <td><div align="center"><?php echo $row['gender'];?></div></td>
		   <td><div align="center"><?php echo $row['ltype'];?></div></td>
		    <td><div align="center"><?php echo $row['exp'];?></div></td>
			 <td><div align="center"><?php echo $row['email'];?></div></td>
			  <td><div align="center"><?php echo $row['loc'];?></div></td>
			   <td><div align="center"><a href="book.php?id=<?php echo $row['id'];?>">Book </a></div></td>
		 
		 
		   </tr>
<?php
$i++;
}
?>
			
			
			</table>
			
			
        		  
<br>
<br>
<br>
<div id="footer"> <p>copyrights & designedby@Layer Web Application</p>
</div>

regist.php

<?php
 	include("dbconnect.php");
	extract($_POST);
	session_start();
if(isset($_POST['btn']))
{


	$max_qry = mysql_query("select max(id) from regist");
	$max_row = mysql_fetch_array($max_qry); 
	$id=$max_row['max(id)']+1;
	$qry=mysql_query("insert into regist  values('$id','$name','$gender','$age','$email','$ocup','$phone','$loc','$address','$uname','$psw')");
	if($qry)
	{
	
	echo "<script>alert('inserted sucessfully')</script>";
	
	}
	else
	{
	
	
		echo "failed";
	
}

}

?>
<html>
<title>Lawyer</title>
<style>

p
{
	color:#ffffff;
	text-align: center;
	text-transform: uppercase;
	 font-size:15px;
}

ul {
	padding:50px;
	
  list-style-type: none;
  overflow: hidden;
  background:#fffff;
   background-repeat: no-repeat;
   background-size: 1420px  200px;
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
   border-radius:10px;
}

li {
  float: left;
}

li a {
  display: block;
  color: #000000;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #ccffff;
}

.active {
  background-color: #4CAF50;
}

#footer {
  border: 2px solid #fffff;
  padding: 45px;
  background: #000000;
  background-repeat: no-repeat;
  background-size: 1420px  100px;
  border-radius:10px;
  text-align:center;
  text-decoration:blink;
   font-family: Arial;
   font-size:15px;
}
#bg1 {

  padding:150px;
  background:url("images/1.jpg");
  background-repeat: no-repeat;
  background-size: 1420px  300px;
  border-radius:5px;
   border-radius:90px;
    text-align:left;
   font-size:35px;
   color:#000000;
}

</style>
</head>
<ul>
	 <li><a href="#">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</a></li>
  <li><a x href="index.php"><strong>Home Page</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a  href="admin.php"><strong>Admin login</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="lawyer.php"><strong>Advocate Login</a></li>
  <li><a href="#">&nbsp;</a></li>
  <li><a href="user.php"><strong>User Login</a></li>
  <li><a href="#">&nbsp;</a></li>
   <li><a href="about.php"><strong>About Us</a></li>
</ul>

<br />
<br />
<div id="bg1">Online Lawyer Web Application</div>
	      <form id="form1" name="form1" method="post" action="">
			             <table width="100%" border="0">
                           <tr>
                             <td width="10%" height="43">&nbsp;</td>
                             <td width="17%">&nbsp;</td>
                             <td colspan="2"><div align="center" class="style2">New Users Registration </div></td>
                             <td width="22%">&nbsp;</td>
                             <td width="8%">&nbsp;</td>
                           </tr>
                           <tr>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                             <td width="16%">&nbsp;</td>
                             <td width="27%">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
                           <tr>
                             <td height="37">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td><span class="style8">Name </span></td>
                             <td><label>
                               <input name="name" type="text" id="name" />
                             </label></td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
						   
						   
						     <tr>
                             <td height="31">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td><span class="style8">Gender</span></td>
                             <td><label>
                               <input name="gender" type="radio" value="Male" />
                               Male
                               <input name="gender" type="radio" value="Female" />
                               Female</label></td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>  <tr>
                             <td height="31">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td><span class="style8">Age</span></td>
                             <td><label>
                               <input name="age" type="text">
                           </td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
						   
                          
                           <tr>
                             <td height="30">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td><span class="style8">Phone Number </span></td>
                             <td><label>
                               <input name="pnumber" type="text" id="pnumber" />
                             </label></td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
                           <tr>
                             <td height="34">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td><span class="style8">Email Id </span></td>
                             <td><label>
                               <input name="email" type="text" id="email" />
                             </label></td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
						   
						   
						   
						    <tr>
                             <td height="28">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td><span class="style8">Occupation</span></td>
                             <td><label>
                               <input name="ocup" type="text" id="ocup" />
                             </label></td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
						 
						   
						   
						    <tr>
                             <td height="34">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td><span class="style8">Location </span></td>
                             <td><label>
                               <input name="loc" type="text" id="loc" />
                             </label></td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
						   
						   
						   <tr>
                             <td height="31">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td><span class="style8">Address</span></td>
                             <td><label>
                               <textarea name="address" id="address"></textarea>
                             </label></td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
						 
						 
						  
						 
						 
                           <tr>
                             <td height="28">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td><span class="style8">User Name </span></td>
                             <td><label>
                               <input name="uname" type="text" id="uname" />
                             </label></td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
                           <tr>
                             <td height="51">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td><span class="style8">Password</span></td>
                             <td><label>
                               <input name="psw" type="password" id="psw" />
                             </label></td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
                           <tr>
                             <td height="28">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
                           <tr>
                             <td height="28">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                             <td><label>
                               <input name="btn" type="submit" id="btn" value="Register" />
                               </label>
                                 <label>
                                 <input type="reset" name="Submit2" value="Reset" />
                               </label></td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
                           <tr>
                             <td height="28">&nbsp;</td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                             <td>&nbsp;</td>
                           </tr>
                         </table>
			           </form>
                            		  
  <div> &nbsp;</div>
<br>
<br>
<div id="footer"> <p>copyrights & designedby@lawyer Web Application</p></div>

