#javaScript Scroll Function 

A nice feature that you can add to your HTML page using javaScript is a scroll to top button. This is particularly useful if you have a long page.  `window.scrollTo(x, y);` allows us to achieve this it takes a `x`and `y` coordinate and scrolls to that location.  `window.scrollTo(0, 0);` will scroll to the top left section of our screen.  


```html
 ...
 
<body onload="main()">
    <!-- a long div for the demo, also we're using inline styles, these 
        are fine demo purposes not for asessed work 
    -->
    <div style="height:1200px">  
        <button id="scrollToTop" style="position:absolute; top: 1200px">Scroll To Top</button>
    </div>
</body>
... 
```

>> HTML 
 


```javascript 
function main() {
    var button = document.getElementById("backToTop");
    document.addEventListener("click", scrollToTop);
} //end main 


function scrollToTop() {
    /* scroll to top */
    window.scrollTo(0, 0);   
    
} //end ScrollToTop 
```

>>  javaScript 