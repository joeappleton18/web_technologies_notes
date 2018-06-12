#Accessing checkbox choices

Consider the following text box:


```javascript 
	<form  id="carRental">
            <p>Extra Car Cleaning Services?</p>    
            <p><input type="checkbox" name="extras" value="wheelCleaning"> Wheel cleaning (£3) </p>
            <p><input type="checkbox" name="extras" value="rustProtection">  Rust protection (£2) </p>
            <p><input type="checkbox" name="extras" value="airFreshner">  Air freshener (£1) </p>
    </form>
```

>> HTML

![checkbox](img/checkbox.png)

>> Rendered view 

Checkboxes present us with an interesting problem when it comes to form validation. The issues you're confronted with are:

-  A checkbox consists of multiple elements grouped together by the **name** attribute
-  A checkbox allows multiple selections, this means it can represent multiple values 

Consider the following bit of javaScript:


```javascript 
    var form  = document.getElementById("carRental");
    console.log(form.extras)
```
>> javaScript 

The value we see outputted to the console is:

	[input, input, input]
>> 	Console Output

As you've probably worked out the three input's correlate to the choices in our check. The square brackets `[..]` mean each input is in a list known as an array. An array is used to store multiple values in a single variable, it works like a table.  	We can access each individual form element like this:

```javascript 
 	
   var form  = document.getElementById("carRental");
   console.log(form.extras[0])
   console.log(form.extras[1])
   console.log(form.extras[2])
 
```
>> javaScript 

As you can see,  the above code passes back a reference to each input in our checkbox group. **Note** we start counting from **0**, this a standard computing convention. 


``` 
   <input type="radiobox" name="car"  value="2Door"> 
	<input type="checkbox" name="extras" value="rustProtection">  
	<input type="checkbox" name="extras" value="airFreshner">
```  
>> Console output
  	