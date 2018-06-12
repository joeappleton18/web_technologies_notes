#Advanced Form Validation 


##onBlur Event

The `onBlurEvent` is fired when the user leaves a form field. We can use this event to apply some real time form validation.

```html
    ....

    <body onload="main()"> 
     <form id="nameForm">
       <input type="text" name="userName" placeholder="User Name">
     </form>
   </body>
   
   ...  
```

```javascript
function main() {
	
	var nameForm = document.getElementById("nameForm");
	// listen for a onBlur event event on the userName field 
	nameForm.userName.addEventListener("blur", validateName)	
}


//onBlur call back function 
function validateName(event) {
     var nameForm = document.getElementById("nameForm");
     
     if(nameForm.name.value == "") {
        nameForm.name.style.backgroundColor = "red";
        return false; 
     } else {
        nameForm.userName.style.backgroundColor = "";
        return true; 
     }
}

```

In the above example the name input will appear red `nameForm.name.style.backgroundColor = "red";` if it's empty.  










