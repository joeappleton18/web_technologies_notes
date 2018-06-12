#Advanced Form Validation  - Continued

##A complete form validation example

**Notice** how:

* We've created a generic `validateRequired` function which can be use to check if an input has a value, this stops us from repeating ourselves. 



```html
<!doctype html>
<html>
<head>
    <script src="main.js"></script>
    <meta charset="UTF-8">
    <title>Untitled Document</title>
    
</head>
<body onload="main()">

    <form id="logInForm">
        <input type="text" name="userName" placeholder="User Name">
        <input type="text" name="password" type="password" placeholder="Password">
        <input type="submit" value="login">
    </form>

</body>

```

>> HTML 

```javascript
function main() {
	
	  var logInForm = document.getElementById("logInForm");
	  logInForm.userName.addEventListener("blur", validateName);
     logInForm.password.addEventListener("blur", validatePassword);
    
    //validate form on submit
    logInForm.addEventListener('submit', validateForm);
    
}

// submit event validation 
function validateForm(event) {
    
    //if any of the form feilds are not valid prvent the form from submitting 
    if(validateName()  == false || validatePassword()  == false) {
        event.preventDefault();
    }
    
    event.preventDefault();
    
    
}

//generic required validation fucntion 
function  validateRequired(element) {
    
     if(element.value == "") {
        element.style.backgroundColor = "red";
        return false; 
     } else {
        element.style.backgroundColor = "";
        return true; 
     }
}


// validate name
function validateName(event) {
     var logInForm = document.getElementById("logInForm");
     return validateRequired(logInForm.userName);
}

//validate password
function validatePassword(event) {
     var logInForm = document.getElementById("logInForm");
     return validateRequired(logInForm.password);
}



``` 

>> javaScript 