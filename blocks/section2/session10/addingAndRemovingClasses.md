#Adding and Removing A CSS Class Using javaScript

We can add or remove a CSS class using javaScript, you can use this technique to dynamically change the appearance of HTML elements. In the example below, we add a red border to an image with the id of `myImage` when the cursor is over the image:

```javascript

//global image var
var image;

function main() {

  image = document.getElementById("myImage");
  image.addEventListener("mouseover", outline);
  image.addEventListener("mouseout", removeOutline);    
    
}

function outline() {
  image.classList.add("redOutline");       
}

function removeOutline(){
  image.classList.remove("redOutline");       
}
```





