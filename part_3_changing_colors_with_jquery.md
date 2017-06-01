### Part 3: Changing Colors with jQuery

Next we’ll practice another common interaction on web pages: changing HTML element styling triggered by an event. When the checkbox next to a drink is selected, make the background of the drink label change colors.

1. First, capture the event. Noticing a pattern? Capture the event, add an action.

  1. Look in the _index.html_ file to find the check box elements.

  We’ll need to utilize attribute selectors this time. These look like `Element[“attribute=value”]`

  Hint:[bit.ly/AttrSel](http://bit.ly/AttrSel)

  Don’t know what an attribute is? Check this out: [http://bit.ly/Attribs](http://bit.ly/Attribs)

  2.  Select the element.

  3. Add the click event handler.

  Hint: [bit.ly/CnCClick](http://bit.ly/CnCClick)

2.  Add the action:

    1.  Inside of the click event handler we need to add the function.

    2.  This time we’re going to need the input’s parent element: the label.  

    **Hint:** [bit.ly/CnCparent](http://bit.ly/CnCparent)

    3.  We only want the color to show when the box is checked. There are a few ways to do this. Since we want to both add and remove the styling change, we’re just going to toggle the CSS styling class using the jQuery method `toggleClass()`

    Hint: [bit.ly/ToggleC](http://bit.ly/ToggleC)  There is already a highlight class in the _assets/styles/main.css_ file.

    Info: Another other way to do this would be to use the `.css()` method.  Since we needed to toggle between having the styling and not, the toggleClass method fits better for our use case. [bit.ly/CnCCSS](http://bit.ly/CnCCSS).  This might be too much information.

You get a gold star!
