#Our First JavaScript Program

Let's go ahead and create our first JavaScript program:

###Including JavaScript

There are 2 main way's to include a JavaScript code in our HTML pages:


> **In the head - executed when called** 

```javascript
<html>
<head>
  <script type="text/javascript">
     JavaScript code
      … …
  </script>
</head>
<body>
    … …
</body>
</html>
```


> **In the body - executed when the page loads** 

```javascript
<html>
<head>
  … …
</head>
<body>
  <script type="text/javascript">
   JavaScript code
   … …
  </script>
</body>
</html>
```

#Exercise1 

Create a new file called `myFirstJavaScript.html` and type in the below code:

```javascript
<html>
 <head>
  <title>JavaScript Page</title>
 </head>
 <body>
  <script type="text/javascript">
    //simple code to demonstrate output
    document.write("Hello World!");
    document.write("<h1>This is a heading</h1>");
    document.write("<p>This is a paragraph.</p>");
  </script>
 </body>
</html>
```

Save your file and open up the page in your browser and see what happens. 


