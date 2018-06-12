#The Document Object - Accessing HTML

Javascript becomes really interesting when we start to perform  actions on HTML elements. We can use `properties` and `attributes` attached to the `document` object to achieve this. 

Consider the demo below:

* We use `document.getElementById("name").value` to get the value of the input box with the id attribute `name` and assign it to a variable `nameValue`

* We can then use  `document.getElementById("demo").innerHTML =  "Hello " +  nameValue;` to display a message within a `<p>` element with an id of `demo`

* Notice how the code block to perform the above operations is wrapped in `  function showName()`. This function is invoked (run) when the button is clicked. The button element is given the attribute `onClick="showName()` in order to achieve this. 


```html
<html>
 <head>
  
     <title>JavaScript Page</title>
     
     <!--
        This script in included in the head so we need to call it
     -->
     <script type="text/javascript">
         //This is a function
         function showName(){
            // create a variable called name and assign it the value of the name input box 
            var nameValue =  document.getElementById("name").value;

            /* we can now print the name. The . allows us to append to a string */
            document.getElementById("demo").innerHTML =  "Hello " +  nameValue;
        } //end function 
    </script>
 </head>
 <body>
  
  
    <p> <input type="text" placeholder="enter name" id="name">  </p>   
    
     <!-- 
        Notice the onClick attribute. This will call the function showName()
     -->
     
    <p> <button onClick="showName()">Click Me</button> </p>     

    <!-- 
      
      We will display our output below 

     -->
     
    <p id="demo"></p>
    
 </body>
</html>
```
