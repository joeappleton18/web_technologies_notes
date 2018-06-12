#Adding Event Listeners 

Although we've not formally introduced the concept, we've already used javaScript event driven capabilities.  Remember this bit of code:

**The HTML**

```html 
 <p> <button onClick="showName()">Click Me</button> </p>  

```

**The javaScript**

```javascript
function showName(){
	// insert instructions    
} //end function
```





In the above example we're listening for a click event via the implementation of `onClick="showName()` attribute. The browser will then invoke the function `showName()`, when the click event occurs. Functions that react to events are known as **event handlers**.

##javaScript Events

So far, we've only looked at one event, **onClick**. There are however dozens of different events that we can react to. Here are some of the most common:

|Event | Description |
|------| ------------|
|  `onchange`   |    An HTML element has been changed . E.G. a form has been updated      |
| `onclick` |	The user clicks an HTML element |
| `onmouseover` |	The user moves the mouse over an HTML element |
| `onmouseout`	 | The user moves the mouse away from an HTML element|
| `onkeydown` |	The user pushes a keyboard key|
| `onload`	| The browser has finished loading the page|

## Adding Event Listeners 

There are two main ways to add event listeners: 

* Using an inline attribute to add a call back function (up to this point how we've added event listeners)
* Adding an the event listener using javaScript 

Just like with HTML we want to, where possible, avoid the use of inline elements. Therefore, in most cases it's advantageous to add event listeners using javaScript. 

We've seen the below example before, however we're now adding the callback using javaScript and also using an external .js file

>> demo.html

```html
<html>
	<head>
        <script type="text/javascript" src="scripts/event_demo.js">  </script>    	
	</head>
	<!-- we use onload here to initiate our program --> 
    <body onload="main()">
    		<input  id="userName" type = "text" placeholder = "Enter Name">
			<!-- An event listener will be added to the button using javaScript --> 
            <button id="button"> Click Me </button>	
            <p id = "output"><!-- result will be placed here --> </p>
	</body>

</html>

```

>> scripts/event_demo.js

```javascript
/**
    Main Function is invoked when the html 
    page has loaded

**/
function main() {
    //reference an html element 
    var myButton = document.getElementById("button");
     //myButton holds a reference to our button element 
    //we can now add a on click event 
    myButton.addEventListener("click", buttonClicked)
    
}

/**
  buttonClicked call back function 
**/

function buttonClicked() {
   //get the value entered into the user name     
   var myUserName = document.getElementById("userName").value 
   //ouput to our p tag 
   document.getElementById("output").innerHTML = "Hello " + myUserName;
}

```


In the above example notice how clean our HTML is. The only inline event listener we add is `<body onload="main()">` this effectively initiates our program when the document has loaded. Also **note** when we set up an event listener using javascript we can omit  the "on" for the event name. 

 ```html
 myButton.addEventListener("click", buttonClicked)  //onclick becomes click
 ```











x