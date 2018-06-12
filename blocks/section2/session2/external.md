# Including External Javascript


> **In the head - executed when called**

```html
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

```html
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

## Including javaScript in an external file

Just like with CSS it's considered good practice to separate the javaScript code from our HTML. The `<script>` tag allows us to utilise the `src` attribute to include javaScript contained in an external file.   The following conventions must be adhered to:

* The external file should have a `.js` extension
* You do not need to use the `<script>` tag in the external `.js` file 

> **Below we include demo\_script\_src.js which lives int he **`scripts`** folder**

```html
<html>
<head>
    <script type="text/javascript" src="scripts/demo_script_src.js"></script>
</head>
<body>
  ....
</body>
```



