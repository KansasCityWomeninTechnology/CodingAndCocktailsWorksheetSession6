1. Iterate through the array using a `for` loop. Inside the `document.addEventListener` method, iterate through `brainSkills` array and add a console log for `index`:
   ```javascript
for (let index = 0; index < brainSkills.length; index++) {
      console.log(index);
}
   ```
   {% hint style='info' %}
You are logging out the array index. The index is the value corresponding to the element's position in the array. 
   {% endhint %}  

1. We can access an array element by the index using the syntax `name-of-array[index]`. Inside the `for` loop, change the `console.log` to access each array element:
   ```javascript
console.log(index + " " + brainSkills[index]);
   ```

1. In Chrome, take a look in the DevTools console to see the output.
   {% hint style='tip' %}
Notice the first element is index 0 and the last index is array.length - 1. This affects conditional logic and is often the cause of errors. Developers call these errors "off by one error".
   {% endhint %}  

1. Let's call the provided `addDevSkill` function for each element of the array. Remove the `console.log` and replace with a call to `addDevSkill` and pass in the array element:
   ```javascript
addDevSkill(brainSkills[index]);
   ```

1. We now see the content of our array in the web page!
   {% hint style='working' %}
The `addDevSkill` function takes a string and adds it to the DOM as a list item. Feel free to inspect using `debugger` to see the parameter for each function call. We will cover DOM manipulation later tonight and more next month!
   {% endhint %}  

1. Let's refactor our `for` loop to use a shorthand syntax, `forEach`. Comment out the `for` loop by adding `//` before each line of code to look like this:
   ```javascript
// for (let index = 0; index < brainSkills.length; index++) {
//       addDevSkill(brainSkills[index]);
// }
   ```
   {% hint style='tip' %}
You can also highlight all 3 lines of the `for` loop and use keyboard shortcut `ctrl` + `/` on Windows and `cmd` + `/` on Macs to toggle between adding and removing comments.
   {% endhint %}  

   Below the existing `for` loop, add `brainSkills.forEach();`. We will get an error in the console.

1. The `forEach` method requires a parameter of type `function` that gets called on each array element. We need to pass in a function with an element parameter. Place your cursor between the open and close parenthesis of the `forEach` and add `function(element) {}` to look like this:
   ```javascript
brainSkills.forEach( function(element) {});
   ```
   {% hint style="info" %}
In JavaScript, you can declare **functions** and **function expressions**. Function declarations use the syntax `function myFunction(){}` while function expressions use the syntax `const myFunction = function(){};`. In a function expression, you are assigning the function to a variable. This makes it easier to pass functions as parameters. We have been using **function expressions**.

Additionally, JavaScript functions can be named or anonymous. The function declaration inside the `forEach` is an example of an anonymous function.

Check out the references in this section to read more about functions.
   {% endhint %}

1. Place your cursor between the opening and closing curly brace and press `Enter`. Type `console.log(element);` to log the element parameter to the console.

1. We're back in business! Remove the `console.log(element);` and replace it with the call to `addDevSkill`.
   {% hint style='working' %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary> 
Use <code>addDevSkill(element);</code> to call the function with the array element to display in the DOM.
</details>
   {% endhint %}

1. Delete the commented out `for` loop and the log for the array length above it.
