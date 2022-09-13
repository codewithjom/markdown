# :herb: Login Page

![img](../../img/login-page.jpg)

## Table of Contents

- [HTML](#html)
- [CSS](#css)
- [JAVASCRIPT](#javascript)

### HTML

``` html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1" />
		<link rel="stylesheet" href="./css/login.css" />
		<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css" />
		<link rel="icon" href="./img/favicon.ico" />
		<title>KanaBesh | Login Page</title>
	</head>
	<body>
		<div class="container">

			<div class="form-container log-in-container">
				<form action="#">
					<h1 style="color:#2B5B2E;">Login</h1>
					<div class="social-container">
						<a href="https://www.facebook.com/thefilipinocguy" target="_blank" class="facebook">
							<i class="fa fa-facebook fa-2x"></i>
						</a>
						<a href="https://www.instagram.com/cannabis.plants/" target="_blank" class="instagram">
							<i class="fab fa fa-instagram fa-2x"></i>
						</a>
					</div>

					<span>or use your account</span>
					<input type="text" placeholder="Username" id="username" />
					<input type="password" placeholder="Password" id="password" />
					<a href="https://giphy.com/gifs/joint-smoking-weed-a-kf9gb4VjDzatE1ncdN/fullscreen" target="_blank" class="forgot-password">
						Forgot your password? Smoke weed &#128168;
					</a>
          <input type="button" value="Login" onclick="validate();" id="submit" />
				</form>
			</div>

			<div class="overlay-container">
				<div class="overlay">
					<div class="overlay-panel overlay-right">
						<h1>KanaBesh</h1>
						<p>Herb is the healing of the nation, alcohol is the destruction.</p>
					</div>
				</div>
			</div>
		</div>
		
		<script src="./js/login.js"></script>
	</body>
</html>
```

### CSS

``` css
@import url('https://fonts.googleapis.com/css?family=Montserrat:400,800');

* {
	box-sizing: border-box;
}

body {
	background-image: url("../img/background.jpg");
	background-repeat: no-repeat;
	background-size: cover;
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column;
	font-family: 'Montserrat', sans-serif;
	height: 95vh;
	margin: -20px 0 50px;
}

h1 {
	font-weight: bold;
	margin: 0;
}

p {
	font-size: 14px;
	font-weight: 100;
	line-height: 20px;
	letter-spacing: 0.5px;
	margin: 20px 0 30px;
}

span {
	font-size: 12px;
}

a {
	color: #2B5B2E;
	font-size: 14px;
	text-decoration: none;
	margin: 15px 0;
}

#submit {
	border-radius: 20px;
	border: 1px solid #DDA15E;
	background-color: #DDA15E;
	color: #FEFAE0;
	font-size: 12px;
	font-weight: bold;
	padding: 12px 45px;
	letter-spacing: 1px;
	text-transform: uppercase;
}

#submit:hover {
	background-color: #B0814C;
	border: 1px solid #B0814C;
	cursor: pointer;
}

form {
	background-color: #FEFAE0;
	display: flex;
	align-items: center;
	justify-content: center;
	flex-direction: column;
	padding: 0 50px;
	height: 100%;
	text-align: center;
}

input {
	background-color: #D6D9CE;
	border: none;
	padding: 12px 15px;
	margin: 8px 0;
	width: 100%;
}

.container {
	border-radius: 10px;
  box-shadow: 0 14px 28px rgba(0,0,0,1), 0 10px 10px rgba(0,0,0,1);
	position: relative;
	overflow: hidden;
	width: 768px;
	max-width: 100%;
	min-height: 480px;
}

.form-container {
	position: absolute;
	top: 0;
	height: 100%;
}

.log-in-container {
	left: 0;
	width: 50%;
	z-index: 2;
}

.overlay-container {
	position: absolute;
	top: 0;
	left: 50%;
	width: 50%;
	height: 100%;
}

.overlay {
	background: #DDA15E;
	background: -webkit-linear-gradient(to right, #1E3F20, #4A7856);
	background: linear-gradient(to right, #1E3F20, #4A7856);
	background-repeat: no-repeat;
	background-size: cover;
	background-position: 0 0;
	color: #D6D9CE;
	position: relative;
	left: -100%;
	height: 100%;
	width: 200%;
}

.overlay-panel {
	position: absolute;
	display: flex;
	align-items: center;
	justify-content: center;
	flex-direction: column;
	padding: 0 40px;
	text-align: center;
	top: 0;
	height: 100%;
	width: 50%;
}

.overlay-right {
	right: 0;
}


.social-container {
	margin: 20px 0;
}

.social-container a {
	border: 1px solid #1E3F20;
	border-radius: 50%;
	display: inline-flex;
	justify-content: center;
	align-items: center;
	margin: 0 5px;
	height: 40px;
	width: 40px;
}

.facebook:hover, 
.instagram:hover {
	background-color: #2B5B2E;
	color: #FEFAE0;
}

.forgot-password:hover {
	color: #1E3F20;
}
```

### JAVASCRIPT

``` javascript
function validate() {
  var username = document.getElementById('username').value;
  var password = document.getElementById('password').value;

  if (username == 'admin' && password == 'admin' ) {
    // window.alert("Login Successfully");
    window.location.assign('dashboard.html');
    return false;
  } else {
    document.getElementById('username').disable = true;
    document.getElementById('password').disable = true;
    document.getElementById('submit').disable = true;
    window.alert("Login Failed!");
    return false;
  }
}
```
