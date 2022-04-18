# test-project

<html>
<head>
<style>
.error {color: #FF0000;}
</style>
</head>
<body>

<?php

$Name on cardErr = $ATM card and credit card detailsErr = $CVVErr = "";
$Name on card = $ATM card and credit card details = $CVV = "";

if ($_POST)
{
if (empty($_POST["name on card"]))
{
$name on cardErr ="Name on card is required";
}
else
{
$name on card= test_input($_POST["name on card"]))
}

if (empty($_POST["ATM card and credit card details"]))
{
$ATM card and credit card detailsErr= "ATM card and credit card details";
}
else
{
$ATM card and credit card details = test_input($_POST[" ATM card and credit card details"]);
}
if (empty($_POST["CVV"]))
{
$CVV= "CVV";
}
else
{
$CVV = test_input($_POST["CVV"]);
}
function test_input($data) {
$data = trim($data);
$data = stripslashes($data);
$data = htmlspecialchars($data);
return $data;
}
?>
<h2> Payment Gateway</h2>
<p><span class="error">* required field</span></p>
<form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>
Name on card: <input type="text" name="name on card">
<span class="error">* <?php echo $name on cardErr;?></span><br><br>
ATM card and credit card details: <input type="text" name="ATM card and credit card details">
<span class="error">* <?php echo $   ATM card and credit card detailsErr;?></span><br><br>
CVV: <input type="text" name="CVV">
<span class="error">* <?php echo $CVVErr;?></span><br><br>
<input type="submit" name="submit" value="Submit">
</form>
</body>
</html>
