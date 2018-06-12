#Image Gallery 

You've already seen[ how we can update the `src` attribute of an HTML element](image_roll_overs.md) and how to add [onClick() event listeners](https://sirus21.gitbooks.io/internet_technology_block_2/content/session13/event_listener.html) - . We can use these techniques to make a very simple image gallery:

![gallery](img/gallery.jpg)

```html

...

<body onload="main()">
         
           <section>
              <img id="mainImage" src="img/ocean.jpeg">
              <ul>  
                  <li id="image1Link"> Image 1   </li>  
                  <li id="image2Link"> Image 2   </li>
                  <li id="image3Link"> Image 3   </li>
              </ul>  
               
          </section>       
</body>

...

```
>>HTML 

We've partially completed the solution to the image gallery below:


```javascript 
//global slider var 
var mainImage;
//main function runs on page load 
function main(){
     //set up the element references
    var image2Link = document.getElementById("image2Link");
    //set up the listener
    image2Link.addEventListener("click", image2Clicked);
       
}    

function image2Clicked() {

    mainImage.src = "img/trees.jpeg";
    
}

function image3Clicked() {
   mainImage.src = "img/plant.jpeg";
    
}

```

>> javaScript
