### Part 3: Changing Colors with jQuery

Next we’ll practice another common interaction on web pages: changing HTML element styling triggered by an event. When the checkbox next to a drink is selected, make the background of the drink label change colors.

1. First, select your element and capture the event.

    {% hint style='tip' %}
Noticing a pattern? 
    
    1. Select the HTML element to react to
    2. Capture the event on that element (ie. click event handler)
    3. Add a function inside the event handler
    4. Inside the event handler function body, select the HTML element to change based on the event
    5. Add an action to that element
    {% endhint %}

  1. Look in the _index.html_ file to find the check box elements.
  
    ![](/images/checkbox.png)

  2.  Select the input element with a type attribute of checkbox.
  
    This time to select the element, we’ll need to utilize attribute selectors because we only want to select the input elements of type "checkbox". Attribute selectors look like `element[“attribute=value”]`.
  
    {% hint style='tip' %}
To read up on attribute selectors check out: [bit.ly/AttrSel](http://bit.ly/AttrSel)

Don’t know what an attribute is? Check this out: [http://bit.ly/Attribs](http://bit.ly/Attribs)
    {% endhint %}
    
    {% hint style='danger' %}
Watch your quotes here.  You may need to switch a set of double quotes (") to single quotes (') to make sure the string isn't interpreted incorrectly.
    {% endhint %}

  3. Now that the element has been selected, add the click event handler to it.

  For a documentation on using the click event handler navigate to: [bit.ly/CnCClick](http://bit.ly/CnCClick)

2.  Next, select the element that should change based on the previously captured event and add an action to it:

    1.  Inside of the click event handler parentheses, add the function.

    2.  This time, we need to select the input’s parent element: the label.  

    {% hint style='tip' %}
Because we only want the current element's styling to change instead of every checkbox element, first select `this` instead of `input[type="checkbox"]`.

For information on what `this` refers to, read [bit.ly/jQueryThis](http://bit.ly/jQueryThis).
        
How do we reference a parent element? Read up at [bit.ly/CnCparent](http://bit.ly/CnCparent).
    {% endhint %}

    3.  We only want the color to show when the box is checked. There are a few ways to do this. Since we want to both add and remove the styling change, we’re just going to toggle the CSS styling class using the jQuery method `toggleClass()`.
    
    {% hint style='tip' %}
For  more information on the `toggleClass()` method go to: [bit.ly/ToggleC](http://bit.ly/ToggleC).

There is already a CSS `highlight` class created for you to toggle.  You'll find the class styling in the _assets/styles/main.css_ file.
    {% endhint %}
    
3. Save your _my-scripts.js_ file.

4. In Google Chrome, refresh your page, show the menu and select a drink. The background of the selected drink should now turn green!

**Way to go rockstar!**
