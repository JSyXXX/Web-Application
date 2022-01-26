<!DOCTYPE html>
<html>
<head>
	<title>User Registration</title>
	<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
	<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>
	<script src="https://code.jquery.com/jquery-3.6.0.min.js" integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4=" crossorigin="anonymous"></script>
	<script defer type="text/javascript" src="src/script.js"></script>

</head>
<body>

		<!-- User Registratin Form--> 

	<div class="container mt-3 d-flex justify-content-center">
		<div class="card" style="width: 30rem;">
		  <div class="card-body">
			<form id="userForm" name="userForm">
			  <div class="mb-3">
			    <label for="idnumber" class="form-label">ID Number</label>
			    <input pattern="\d{3}-\d{5}" maxlength="9" minlength="9" required type="text" class="form-control" id="idnumber">
			  </div>
			  <div class="mb-3">
			    <label for="firstname" class="form-label">Firstname</label>
			    <input required type="text" class="form-control" id="firstname">
			  </div>
			  <div class="mb-3">
			    <label for="lastname" class="form-label">Lastname</label>
			    <input required type="text" class="form-control" id="lastname">
			  </div>
			  <div class="mb-3">
			    <label for="gender" class="form-label">Gender</label>
				<select required class="form-select" id="gender" aria-label="Default select example">
				  <option value="0">Female</option>
				  <option value="1">Male</option>
				</select>
				</div>
			  <div class="mb-3">
			    <label for="bday" class="form-label">Birthday</label>
			    <input required type="date" class="form-control" id="bday">
			  </div>
			  <div class="mb-3">
			    <label for="program" class="form-label">Program</label>
			    <input required type="text" class="form-control" id="program">
			  </div>
			  <div class="mb-3">
			    <label for="yearlevel" class="form-label">Year Level</label>
			    <input max="5" min="1" required type="number" class="form-control" id="yearlevel">
			  </div>
			  <button id="register" type="submit" class="btn btn-primary">Register</button>

			</form>	  	
		  </div>
		</div>
	</div>

	<!-- End of User Registration Form--> 


	<!-- Table to Display Users Data-->

	<div class="container">
		<table class="table" id="usertable">
		  <thead>
		    <tr>
		      <th scope="col">#</th>
		      <th scope="col">ID Number</th>
		      <th scope="col">Firstname</th>
		      <th scope="col">Lastname</th>
		      <th scope="col">Gender</th>
		      <th scope="col">Birthday</th>
		      <th scope="col">Program</th>
		      <th scope="col">Year Level</th>
		      <th scope="col" colspan="2">Action</th>
		    </tr>
		  </thead>
		  <tbody>
		  </tbody>
		</table>
	</div>
     
     <!-- End of Table that Display Users Data-->


	<!-- User Update  Modal Form-->

<div id= "myModal" class="modal">
	<div class="modal-content">
	<div class="container mt-3 d-flex justify-content-center">
		<div class="card" style="width: 30rem; height: 50rem; ">
         <h3><center>Update User</center></h3>
		  <div class="card-body">
			<form id="edituserForm" name="edituserForm">
				<input type="hidden" id="idofuser">
			  <div class="mb-3">
			  	  <label for="edit_idnumber" class="form-label">ID Number</label>
			    <input pattern="\d{3}-\d{5}" maxlength="9" minlength="9" type="text" class="form-control" id="edit_idnumber">
			  </div>
			    <div class="mb-3">
			    <label for="edit_firstname" class="form-label">Firstname</label>
			    <input required type="text" class="form-control" id="edit_firstname">
			  </div>
			  <div class="mb-3">
			    <label for="edit_lastname" class="form-label">Lastname</label>
			    <input required type="text" class="form-control" id="edit_lastname">
			  </div>
			  <div class="mb-3">
			    <label for="edit_gender" class="form-label">Gender</label>
				<select required class="form-select" id="edit_gender" aria-label="Default select example">
				  <option value="0">Female</option>
				  <option value="1">Male</option>
				</select>
				</div>
			  <div class="mb-3">
			    <label for="edit_bday" class="form-label">Birthday</label>
			    <input required type="date" class="form-control" id="edit_bday">
			  </div>
			  <div class="mb-3">
			    <label for="edit_program" class="form-label">Program</label>
			    <input required type="text" class="form-control" id="edit_program">
			  </div>
			  <div class="mb-3">
			    <label for="edit_yearlevel" class="form-label">Year Level</label>
			    <input max="5" min="1" required type="number" class="form-control" id="edit_yearlevel">
			  </div>
				<button id="editUser" class="btn btn-success" >Save Changes</button>
			    <button class="close" class="btn btn-success" >Cancel</button>
			</form>	  	
		  </div>
		</div>
	</div>
</div>
</div>

	<!-- End of User Update  Modal Form-->

</body>

<style type="text/css">
	input:invalid, select:invalid{
		border: 2px solid red;
	}
</style>

</html>
