# Practical 

This is the main practical for this session. This is going to be a good opportunity to practice the key points we've covered in this weeks session

* Create a new file called exercise3.html and save it in your session 11 folder

* Using a valid HTML structure place 3 input boxes on the page. You'll need to give each input boxes a unique id. Here's what input box one should look like:

```html
  <p> <input type="number" placeholder="enter number 1" id="number1">  </p>   
```

* Next, create a button that will invoke a javascript function. Notice the attribute `onClick="calculateNumber()`. calculateNumber\(\) is the javascript function that will be called when the button is pressed. We'll define this function in the next section. 

```html
<p> <button onClick="calculateNumber()">Click Me</button> </p>     
```

* In the head section of you document create the javaScript function calculateNumber

```html
    <head>  
     <!--
        This script in included in the head so we need to call it
     -->
     <script type="text/javascript">
         // This is a function
         function calculateNumber(){
             //your code will go here
         } //end function 
    </script>
```

* We now need to assign each number entered into the textbooks to a variable. The first number has been assigned for you. See if you can grab the other two.

```html
    <head>  
     <!--
        This script in included in the head so we need to call it
     -->
     <script type="text/javascript">
         // This is a function
         function calculateNumber(){
                var number1 =  parseInt(document.getElementById("number1").value);
          } //end function 
    </script>
```

* Now you've got the numbers stored in variables, go ahead and see if you can add them together and assign the sum to a variable called `result`

* Finally we need to actually display our result, you'll need to use a statement along the lines of:

```html
document.getElementById("result").innerHTML = result;
```

Where `result` corresponds to an element such as a `<p>` with and `id` of `result`

