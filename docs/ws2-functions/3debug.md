1. We want something nicer to display in the alert. Change the parameter you pass in to `alert` method to use the variable named `text`. You are using the same parameter passed into the `clickHandler` function. Your code should look like this:

   ```javascript
alert(text);
   ```
   {% hint style='working' %}
Notice there are no quotation marks. This now references the variable named `text`, not the string "text". Try adding quotation marks to see the difference.
   {% endhint %}   

1. We still want to see the button click counter for troubleshooting purposes. We can log the number of clicks to the console. Add `console.log(numberOfClicks);` right after incrementing the clicks in the `clickHandler` function.

1. To see console logging in action, open the Chrome DevTools and click on the button. You should see the number of clicks write to the console. Leave DevTools open.

   {% hint style='tip' %}
Open Chrome DevTools by using `cmd` + `shift` + `j` on Macs, `F12` on Windows, and `ctrl` + `shift` + `i` on Chromebooks. Refer to [Helpful Keyboard Shortcuts](/references).
   {% endhint %}   

1. We declared `numberOfClicks` using `var`. What happens if we used `const`? Change the declaration for `numberOfClicks` to use `const`.
   {% hint style='working' %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary>
Change <code>var numberOfClicks = 0;</code> to <code>const numberOfClicks = 0;</code>.
</details>
   {% endhint %}

1. Try clicking on the button. Oh no! Now we see an error in the console. Notice how DevTools helps you debug your script. It tells you which line of code the failure occurs `script.js:7`. The line number may be different for you.
   {% hint style='info' %}
It also provides information on caller of the failing line-- `HTMLButtonElement.onClick (index:25)`. As you create complex applications, there may be layers of functions called. The layers of functions called is a **call stack**. The output containing the error, along with all the functions called leading up to it, is a **stack trace**.
   {% endhint %}

1. The keyword `const` makes a variable read-only, so we can't increment the value. The error message helps us identify the problem by providing both the line of code and why. Change the declaration of `numberOfClicks` to use `let`. Leave DevTools open.

1. Click the button and notice we fixed the error.