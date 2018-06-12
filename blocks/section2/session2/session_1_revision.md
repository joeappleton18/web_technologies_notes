# Session 1 Recap

In session 11 we introduced the basics of JavaScripts. Before we continue it's important that you understand the following concepts covered in session 11:

* [Comments](https://sirus21.gitbooks.io/cda401/content/sessions/session1/comments.html)
* [Variables](https://sirus21.gitbooks.io/cda401/content/sessions/session1/varibles.html)
* [The document object](https://sirus21.gitbooks.io/cda401/content/sessions/session1/document_object.html)

## Session 1 Revision Demo

The example below where we take a name and display `hello + name` within a empty `<p>` element, covers most of last weeks concepts.

```html
<html>
    <head>
    <script type="text/javascript">

        //define function display name 
        function displayName() {
            // get textBox value and assign value to var userName 
            var userName  = document.getElementById("userName").value;

            //set inner html of output to hello + userName
            document.getElementById("output").innerHTML = "Hello " + userName;   
        }


    </script>    
    </head>
    <body>
        <! -- an empty p element for us to output to -->


            <!-- An Input to get the users names -->
            <input  id="userName" type = "text" placeholder = "Enter Name">
            <!-- notice the onClick attribute which runs the display name function
                when the button is clicked -->
            <button onClick = displayName()> Click Me </button>    


        <p id = "output"><!-- result will be placed here --> </p>
    </body>

</html>
```



