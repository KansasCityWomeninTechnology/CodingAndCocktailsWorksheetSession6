1. In `document.addEventListener` after the `forEach`, add `document.getElementById('coding-section').addEventListener();` to register an event listener to the 'coding-section' DOM element. We will see an error in the console.

1. The `addEventListener()` method requires 2 parameters, the type of event and a function. Place your cursor between the opening and closing parenthesis and add the parameters `'click'` and `function() {}`. The event listener should look like this:
   ```javascript
document.getElementById('coding-section').addEventListener('click', function() {});
   ```

1. Let's make sure we registered the listener correctly. Place your cursor between the opening and closing curly brace and press `Enter`. Add `console.log('click');`.

1. In Chrome, click on part of the web page that has displays the array elements. This is sneaky-- there's no button here! Do you see anything in your console?
   {% hint style='tip' %}
Mentors are here to help! Feel free to grab a mentor if you don't see any output in the console.
   {% endhint %}  

1. Remove the `console.log('click');` now that we've verified event registration.

1. Let's add or remove an existing CSS class called 'coding' to apply a style each time we click on the array elements by using the built in `toggle()` method. Add the following line inside the event listener function:
   ```javascript
document.getElementById('coding-section').classList.toggle('coding');
   ```