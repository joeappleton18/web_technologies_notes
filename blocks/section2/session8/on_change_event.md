#The onChange Event

The `onChange` event is particularly useful when it's applied to a form. This event will fire whenever a form is updated. 


It's implemented as follows:


```html
	<form  id="carRental">
            <p>Extra Car Cleaning Services?</p>    
            <p><input type="checkbox" name="extras" value="wheelCleaning"> Wheel cleaning (£3) </p>
            <p><input type="checkbox" name="extras" value="rustProtection">  Rust protection (£2) </p>
            <p><input type="checkbox" name="extras" value="airFreshner">  Air freshener (£1) </p>
    </form>
```
>> HTML


```javascript

function main() {
    var carRentalForm = document.getElementById("carRental");
    carRentalForm.addEventLinstener("change", formChanged);
}

function formChanged(event) {
    console.log("the form has changed");
    // run some validation 
   // update some information for the user 
}

```
>> javaScript




