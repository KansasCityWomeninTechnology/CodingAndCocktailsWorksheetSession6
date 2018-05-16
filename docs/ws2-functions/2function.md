1. In your Atom, open _scripts.js_. You'll see MadLibs items like we had in the first section of the worksheet. 

1. Search for **\<noun\>** and **\<verb\>** and replace the variables. The lavender button now has text in it, but we want it do something when we click on it.

1. Let's display an alert message by adding `alert('click');` inside the `clickHandler` function. The `clickHandler` function should look like this:

   ```javascript
const clickHandler = function(text) {
    alert('click');
}
   ```

1. Now try clicking the button. An alert message appears!

1. Define a new variable called `numberOfClicks` above the `clickHandler` method so we can keep track of the number of button clicks. Set the value to 0. Your variable should look like this:

   ```javascript
var numberOfClicks = 0;
   ```
1. Track the clicks by incrementing `numberOfClicks` by 1 for each button click. We can do this inside the `clickHandler` function before the alert by using the following statement:

   ```javascript
numberOfClicks = numberOfClicks + 1;
   ```
   {% hint style='info' %}
We are adding 1 to `numberOfClicks` variables and setting the result back to `numberOfClicks`. 

There are other ways to assign variables. You could have also written:
`numberOfClicks += 1;`
`numberOfClicks++;`
  {% endhint %}   

1. Update the alert message to show the number of clicks by adding `numberOfClicks` to the display text.
   ```javascript
alert('click ' + numberOfClicks);
   ```

1. Click the button to see your click counter in action.


