# JavaScript Conditional Form for bangladesh Division, District & Police Station and more

## HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>JavaScript Conditional Form for bangladesh Division, District & Police Station and more</title>
	<link rel="stylesheet" href="style.css">
</head>
<body>
	<div class="message">
		<h2 class="welcome">Welcome To Our Condational Form</h2>
		<h4>Please feel free <a href="https://www.facebook.com/hmbashar">contact us</a> for improvement</h4>
		<p>I will try to update it daily. It's <strong>open source</strong>, so anyone who can use it for its needs.</p>
		<p>Seurce file <a href="https://github.com/hmbashar/bangladesh-division-Districts-police-station-condational-form">Here</a></p>
	</div>
	<div class="javascript-condational-form">		
		<form action="">
			<!--Division Section-->
			<label for="divisions">Select Division</label>
			<select name="divisions" id="divisions" onchange="divisionsList();">
				<option disabled selected>Select Division</option>
				<option value="Barishal">Barishal</option>
				<option value="Chattogram">Chattogram</option>
				<option value="Dhaka">Dhaka</option>
				<option value="Khulna">Khulna</option>
				<option value="Mymensingh">Mymensingh</option>
				<option value="Rajshahi">Rajshahi</option>
				<option value="Rangpur">Rangpur</option>
				<option value="Sylhet">Sylhet</option>
			</select><!--/ Division Section-->
			<br>
			<br>
			<!--Districts Section-->
			<label for="distr">Select District</label>
			<select name="" id="distr" onchange="thanaList();"></select><!--/ Districts Section-->
			<br>
			<br>
			<!--Police Station Section-->
			<label for="polic_sta">Select Police Station</label>
			<select name="" id="polic_sta"></select><!--/ Police Station Section-->
		</form>
	</div>
	<script src="javascript.js"></script>
</body>
</html>

```
## JavaScript
```// Division Section select
function divisionsList() {
	// get value from division lists
	var diviList = document.getElementById('divisions').value;

	// set barishal division districts
	if(diviList == 'Barishal'){		
		var disctList = '<option disabled selected>Select District</option><option value="Barguna">Barguna</option><option value="Barishal">Barishal</option><option value="Bhola">Bhola</option><option value="Jhalokati">Jhalokati</option><option value="Patuakhali">Patuakhali</option><option value="Pirojpur">Pirojpur</option>';
	}
	// set Chattogram division districts
	else if(diviList == 'Chattogram') {
		var disctList = '<option disabled selected>Select Division</option><option value="Bandarban">Bandarban</option><option value="Chandpur">Chandpur</option><option value="Chattogram">Chattogram</option><option value="Cumilla">Cumilla</option><option value="Cox\'s Bazar">Cox\'s Bazar</option><option value="Feni">Feni</option><option value="Khagrachhari">Khagrachhari</option><option value="Noakhali">Noakhali</option><option value="Rangamati">Rangamati</option>';	
	}
	// set Dhaka division districts
	else if(diviList == 'Dhaka') {
		var disctList = '<option disabled selected>Select Division</option><option value="Dhaka">Dhaka</option><option value="Faridpur">Faridpur</option><option value="Gazipur">Gazipur</option><option value="Gopalganj">Gopalganj</option><option value="Kishoreganj">Kishoreganj</option><option value="Madaripur">Madaripur</option><option value="Manikganj">Manikganj</option><option value="Munshiganj">Munshiganj</option><option value="Narayanganj">Narayanganj</option><option value="Narsingdi">Narsingdi</option><option value="Rajbari">Rajbari</option><option value="Shariatpur">Shariatpur</option><option value="Tangail">Tangail</option>';
	}
	//  set/send districts name to District lists from division
	document.getElementById("distr").innerHTML= disctList;
}

// Thana Section select
function thanaList(){
	var DisList = document.getElementById('distr').value;
	if(DisList == 'Barguna') {
		var thanaList = '<option disabled selected>Select District</option><option value="Barguna">Barguna</option><option value="Barishal">Barishal</option><option value="Bhola">Bhola</option><option value="Jhalokati">Jhalokati</option><option value="Patuakhali">Patuakhali</option><option value="Pirojpur">Pirojpur</option>';
	}
	document.getElementById("polic_sta").innerHTML= thanaList;
}
```
