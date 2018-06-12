#Global Variables (A Slight Aside)

Consider the following small javaScript program, which validates a single form field in real-time:

```html

... 

<body onload="main()">
    
    <form id="myForm">
        <input type="text" name="userName" placeholder="userName"> 
    </form>
    
</body>

...

```

>> HTML

```javaScript 
//global var
var form;

function main(){
   //notice we don't use the var keyword    
   form = document.getElementById("myForm");
   form.userName.addEventListener("blur", validateName);
} //end main

function validateName(event){
  //we can now use the form varible in a seperate function
  if( form.userName.value == "") {
      //make background color red
      form.userName.style.backgroundColor = "red"
  } else {
      //remove background color
      form.userName.style = ""       
  }
    
} //end validateName  

```

>> javaScript  

* The `form` variable is defined using the `var` keyword outside the function blocks
* In javaScript any variable defined outside a function becomes part of the global scope
* `form` can be accessed and changed anywhere in our program. As opposed to a variable declared in a function which can only be accessed in that function
* This saves us from having to re-reference the HTML form element multiple times  
* Notice how we can access form values in validate name, without using the instruction `form = document.getElementById("myForm");` a second time.  


**Caution** use global variables sparingly, due to the fact they can be accessed,  overridden or deleted anywhere in your program, they are risky to use. 





