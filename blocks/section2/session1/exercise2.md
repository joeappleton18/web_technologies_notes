#Exercise2 
We're going to expand on the first exercise and use variables. Pay close attention on how the  `+` is used to concatenate(join together) text with variables. 

e.g. `document.write("<p> Your name:" + name  + "</p>" );`

Create a new file called `ex2.html` and type in the below code:

```javascript
	<html>
	 <head>
	  <title>JavaScript Page</title>
	 </head>
	 <body>
		 <script type="text/javascript">
	    //set up our variables
	    var name;
	    var age;
	    var yourLocation;
	    
	    //assign values 
	    name = "Joe";
	    
	    //age is an integer so we don't use ""
	    age = 33
	    
	    yourLocation = "Brighton"
	 
	    //simple code to demonstrate output
	    document.write("<p> Your name:" + name  + "</p>" );
	    document.write("<p> Your age:" + age + "</p>" );
	    document.write("<p> Your location:" + yourLocation  + "</p>" );  
	   
	   </script>
   
 </body>
</html>

```


Save your file and open up the page in your browser and see what happens. 
