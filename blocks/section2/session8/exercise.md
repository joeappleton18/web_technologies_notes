#Solent Stores - Shopping cart exercise 

The purpose of this exercise is to implement the javaScript on a shopping cart. The HTML has already been created for you.  

##1 Setup 

[Download the project source file from here](https://www.dropbox.com/s/8ntpmdz1x2um9sp/shopping_cart_exercise.zip?dl=0).  Open up index.html in your browser, you should be presented with the following website:

![website](img/website.png)



##2  Add a data attribute to hold the price of each product

If you take a look at your source code for index.html you'll see that each product has a checkbox for the add to cart functionality.  Heres the one for our blender:   

```html
	
	<input type="checkbox" name="product" value="blender">  
	
```

[At the a data attribute to hold the ](https://sirus21.gitbooks.io/internet_technology_block_2/content/session17/enconding_information_into_elements.html) of each item. For example, our blender input would become:

```html

 	<input type="checkbox" name="product" data-price = "25" value="blender">  
	

```
             
             
##3 Our first bit of javaScript

Within index.html, notice how we've included an external javaScript file and also added a `onLoad` event that calls a `main()` function. 

1. Open up `script/main.js` 
2. Within `main.js` add an event listener that fires the `formChangedFunction`
3. Check that the message is output to the console when the form changes

##4 Working out the main totals and shipping costs 
1. Within `main.js` `formChangeFunction` create the following variables:

```javascript

	var form = document.getElementById("productForm"); 
    var subTotal = 0;
    var shipping = 0;
    var taxes = 0;
    var total = 0;
```

2. Next, within `formChangedFunction` Create a for loop that loops through the `product` check list, if a product has been checked you should cast the `price` to a number and add it to the subtotal. This is very similar to our the example in the notes.  

```javascript
	numberTotal =  parseInt(form.product[i].dataset.price);
    subTotal = subTotal +  numberTotal;
```
>> how to access the price from within the loop

Note, this is very similar to the in class example. 

3. After the loop, check to see if the `subTotal` is less than £100. If this is the case, set `shipping = £10`  
4. Set the variable `taxes =  20% of subTotal`
5. Set the variable `total = subTotal + taxes + shipping`
6. Set the inner HTML of each section in the summary table = to your new variable values:

```javascript
document.getElementById("sub-total").innerHTML =  "£" + subTotal;
document.getElementById("shipping").innerHTML =  "£" + shipping;
document.getElementById("taxes").innerHTML =  "£" + taxes;
document.getElementById("total").innerHTML = "£" + total;
```


#5 Product totals and multiple items 

Implement the functionality to allow the amount of each product to be increased. The total for each product should be displayed.   This is tricky, but let's take the blender as an example and consider its related elements:
	

```html
<input data-price="25" type="checkbox" name="product" value="blender">  
<input type="number"  value="1" name="blender-quantity"> 
<p>Total: <span  id="blender-total"> £0 </span> </p>
```

This naming convention is consistent for all the products, your solution will take advantage of this. 	







