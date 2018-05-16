1. In the `clickHandler` function, add an `if` statement to only show the alert for greater than 2 button clicks by adding an conditional statement:
   ```javascript
if (numberOfClicks > 2) {
   alert(text);
}
   ```

1. Use the `console.log` output to confirm we show the alert starting from the 3rd button click.

1. If we want to only show the alert the first 3 times you clicked the button, how would you change the conditional statement?
   {% hint style='working' %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary>
There are 2 different ways to apply this condition. 
Change <code>if (numberOfClicks > 2)</code> to <code>if (numberOfClicks <= 3)</code> or <code>if (numberOfClicks < 4)</code>.
</details>
   {% endhint %}

1. What if we want to show different alert message after 3 button clicks? Add a `else` clause to the conditional statement:
   ```javascript
if (numberOfClicks <= 3) {
    alert(text);
} else {
    alert("Drink in moderation-- no more cocktails for you!");
}
   ```

1. This is starting to become difficult to track just with `console.log`. Let's try **debugging** the `onClickHandler` function in DevTools. Add `debugger;` as the first line of the `clickHandler` function. Your function should look like this:
   ```javascript
const clickHandler = function(text) {
    debugger;
    numberOfClicks = numberOfClicks + 1;

    ...
}
   ```

1. Click on the button. Your web page paused execution and DevTools now shows _script.js_. We can now step through the code line by line and inspect the function along the way.

1. In the _script.js_ tab, hover over `numberOfClicks`. It shows you the current value of the variable, 0. Press `F10` or click ![](images/step_over.png) to execute the next line of code in _script.js_. The line where we increment `numberOfClicks` highlights. The current value of `numberOfClicks` is still 0.

1. Press `F10` again. Now we see `numberOfClicks` increment to 1. Press `F10` until the `if` statement highlights.

1. Press `F10` to execute the `if` statement. Since 1 is less than or equal to 3, we expect to execute `alert(text);` statement. Does it?

1. Press `F8` or click ![](images/resume.png). 

1. Repeat the stepping through the code and resuming until you click for the 4th time. Does the `else` condition execute?

1. Remove the `debugger;` statement so we aren't interrupted in the rest of the worksheet. Feel free to add it back if you get stuck!

1. Celebrate with a cocktail or mocktail! You deserve it, rockstar!

   ![](https://media.giphy.com/media/bEbRqmAnOeRi/giphy.gif)

