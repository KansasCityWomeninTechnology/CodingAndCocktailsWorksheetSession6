### Part 3: Changing Colors with jQuery

Next we’ll practice another common interaction on web pages: changing HTML element styling triggered by an event. When the checkbox next to a drink is selected, make the background of the drink label change colors.

1. First, capture the event. Noticing a pattern? Capture the event, add an action.

  1. Look in the _index.html_ file to find the check box elements.
  
    ![](/images/checkbox.png)

  2.  Select the input element with a type attribute of checkbox.
  
    This time we’ll need to utilize attribute selectors because we only want to select the input elements of type "checkbox". Attribute selectors look like `element[“attribute=value”]`.
  
    {% hint style='tip' %}
To read up on attribute selectors check out:[bit.ly/AttrSel](http://bit.ly/AttrSel)

Don’t know what an attribute is? Check this out: [http://bit.ly/Attribs](http://bit.ly/Attribs)
    {% endhint %}
    
    {% hint style='danger' %}
Watch your quotes here.  You may need to switch a set of double quotes (") to single quotes (') to make sure the string isn't interpreted incorrectly.
    {% endhint %}

  3. Add the click event handler.

  For a documentation on using the click event handler navigate to: [bit.ly/CnCClick](http://bit.ly/CnCClick)

2.  Add the action:

    1.  Inside of the click event handler parentheses, add the function.

    2.  This time, we need to select the input’s parent element: the label.  

    {% hint style='tip' %}
Because we only want the current element's styling to change instead of every checkbox element, first select `this` instead of `input[type="checkbox"]`.
        
How do we reference a parent element? Read up at [bit.ly/CnCparent](http://bit.ly/CnCparent).
    {% endhint %}

    3.  We only want the color to show when the box is checked. There are a few ways to do this. Since we want to both add and remove the styling change, we’re just going to toggle the CSS styling class using the jQuery method `toggleClass()`

    {% hint style='tip' %}
For more information on the `toggleClass()` method go to: [bit.ly/ToggleC](http://bit.ly/ToggleC)  
    
There is already a CSS `highlight` class created for you to toggle.  You'll find the class styling in the _assets/styles/main.css_ file.
    {% endhint %}
    
3. Save your _my-scripts.js_ file.

4. In Google Chrome, refresh your page, show the menu and select a drink.



You get a gold star!
