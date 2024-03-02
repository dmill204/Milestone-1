<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>My Website</title>
    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
    <!-- Custom CSS -->
    <style>
      /* Add your custom CSS here */
    </style>
  </head>
  <body>
    <!-- Navigation Bar -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#">My Website</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item active">
            <a class="nav-link" href="index.html">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="about.html">About Us</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="contact.html">Contact Us</a>
          </li>
        </ul>
      </div>
    </nav>
    
    <!-- Home Page -->
    <div class="container">
      <h1>Welcome to My Website!</h1>
      <p>This is the home page of my website.</p>
    </div>
    
    <!-- About Us Page -->
    <div class="container">
      <h1>About Us</h1>
      <p>We are a small team of web developers.</p>
    </div>
    
    <!-- Contact Us Page -->
    <div class="container">
      <h1>Contact Us</h1>
      <form name="contactForm" onsubmit="return validateForm()" method="post">
        <div class="form-group">
          <label for="name">Name:</label>
          <input type="text" class="form-control" id="name" name="name" placeholder="Enter your name">
          <small id="nameError" class="text-danger"></small>
        </div>
        <div class="form-group">
          <label for="email">Email:</label>
          <input type="email" class="form-control" id="email" name="email" placeholder="Enter your email">
          <small id="emailError" class="text-danger"></small>
        </div>
        <div class="form-group">
          <label for="feedback">Feedback:</label>
          <textarea class="form-control" id="feedback" name="feedback" placeholder="Enter your feedback"></textarea>
          <small id="feedbackError" class="text-danger"></small>
        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
      </form>
    </div>
    
    <!-- JavaScript for form validation -->
<script>
// function to validate the form inputs
function validateForm() {
// get the form inputs
var name = document.forms["contactForm"]["name"].value;
var email = document.forms["contactForm"]["email"].value;
var feedback = document.forms["contactForm"]["feedback"].value;
// check if name is empty
if (name == "") {
document.getElementById("nameError").innerHTML = "Name must be filled out";
return false;
} else {
document.getElementById("nameError").innerHTML = "";
}
// check if email is empty or invalid
if (email == "") {
document.getElementById("emailError").innerHTML = "Email must be filled out";
return false;
} else if (!validateEmail(email)) {
document.getElementById("emailError").innerHTML = "Invalid email format";
return false;
} else {
document.getElementById("emailError").innerHTML = "";
}
// check if feedback is empty
if (feedback == "") {
document.getElementById("feedbackError").innerHTML = "Feedback must be filled out";
return false;
} else {
document.getElementById("feedbackError").innerHTML = "";
}
return true;
}
  // function to validate email format
  function validateEmail(email) {
    var re = /\S+@\S+\.\S+/;
    return re.test(email);
  }
</script>

<!-- Bootstrap JavaScript -->
<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js"></script>
  </body>
</html>
