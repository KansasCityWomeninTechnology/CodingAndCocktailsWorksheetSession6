
1. In `document.addEventListener` after the `forEach`, add `document.getElementById('coding-section').onclick = function() {};` to add an event listener.

   {% hint style='info' %}
We are adding a function that executes upon mouse click of the HTML element with id 'coding-section'. There's a few different ways to add a click handler. We will learn about event registration next session.
   {% endhint %} 

   {% hint style='working' %}
This doesn't look like the other functions we created!

We can define functions different ways. Here we defined the function and set it directly on the `onclick` property. The function we defined is only accessible by the `onclick` property. We can't reference the function from anywhere else. We could have also assigned the onclick handler to a variable so that we can use the function elsewhere to look like this:

```javascript
const myClickHandler = function() {
      // implementation here
}

document.getElementById('coding-section').onclick = myClickHandler;

``` 
   {% endhint %} 

1. Let's make sure we registered the listener correctly. Place your cursor between the opening and closing curly brace and press `Enter`. Add `console.log('click');`.

1. In Chrome, click on part of the web page that displays the array elements. Do you see anything in your console?

   {% hint style='tip' %}
Mentors are here to help! Feel free to grab a mentor if you don't see any output in the console.
   {% endhint %}  

      {% hint style="tip" %}
This is sneaky-- there's no button here! Unexpected interaction or surprises in an application are known as "Easter eggs".
   {% endhint %}

1. Remove the `console.log('click');` now that we've verified event registration.

1. Let's add or remove an existing CSS class called 'coding' to apply a style each time we click on the array elements by using the built in `toggle()` method. Add the following line inside the event listener function:
   ```javascript
document.getElementById('coding-section').classList.toggle('coding');
   ```
1. Click the array elements in Chrome. Does your style change on each click?

   ![](https://media.giphy.com/media/5PhpuOph9pwoyuqHjd/giphy.gif)

