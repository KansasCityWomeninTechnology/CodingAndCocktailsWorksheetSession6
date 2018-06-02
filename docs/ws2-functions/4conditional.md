1. Inside the `clickHandler` function, add an `if` statement to only show the alert for greater than 2 button clicks by adding a conditional statement:
   ```javascript
if (numberOfClicks > 2) {
      alert(text);
}
   ```
   {% hint style='tip' %}
Notice the indention on the `alert(text);`. Indent everything inside the `if` statement to make it easier to read your code. Doing so helps your brain group logical units of code together at a glance!
   {% endhint %}

1. Use the `console.log` output to confirm we show the alert starting from the 3rd button click. 
   {% hint style='tip' %}
You will use Atom to type code statements and Chrome to verify your work when your web page reloads. Don't forget to save _scripts.js_ every time you type a code statement.
   {% endhint %}

1. If we want to only show the alert the first 3 times you clicked the button, how would you change the conditional statement?
   {% hint style='working' %}
<details>
<summary>
Need a little help? Expand this section for guidance. 
</summary>
There are 2 different ways to apply this condition. 
Change <code>if (numberOfClicks > 2)</code> to either
<pre>
<code class="lang-javascript">
if (numberOfClicks &lt;= 3)

if (numberOfClicks < 4)
</code>
</pre>
</details>
   {% endhint %}

1. What if we want to show a different alert message after 3 button clicks? Add an `else` clause to the conditional statement:
   ```javascript
if (numberOfClicks <= 3) {
      alert(text);
} else {
      alert("Drink in moderation-- no more cocktails for you!");
}
   ```

1. This is starting to become difficult to track using `console.log`. Let's try **debugging** the `onClickHandler` function in DevTools. Add `debugger;` as the first line of the `clickHandler` function. Your function should look like this:
   ```javascript
const clickHandler = function(text) {
      debugger;
      numberOfClicks = numberOfClicks + 1;

      // rest of the function remains here
};
   ```

1. In Chrome, click on the button. Your web page paused execution and DevTools now shows _scripts.js_. We can now step through the code line by line and inspect the function along the way.
   {% hint style='tip' %}
`debugger;` works only when debugging capabilities, such as Chrome DevTools, is open. 
   {% endhint %}

1. In the _scripts.js_ tab in Chrome, hover over `numberOfClicks`. It shows you the current value of the variable, 0. Click **Step** button, ![](images/step.png) (located at the upper right of DevTools window), to execute the next line of code in _scripts.js_. The line where we increment `numberOfClicks` highlights. The current value of `numberOfClicks` is still 0.

   {% hint style='info' %}
The ![](images/step.png) steps through the source code. You can also Step into and step out of lines of code. Tonight we will use step. 
   {% endhint %}   

1. Click step again. Now we see `numberOfClicks` increment to 1. 

1. Click step until the `if` statement highlights.

1. Click step to execute the `if` statement. Since 1 is less than or equal to 3, we expect to execute `alert(text);` statement. Does it?

1. Click **Resume**, ![](images/resume.png), to resume execution on the rest of the code. 

   {% hint style='working' %}
We are using **Step** in this session, but debugging tools, such as Chrome DevTools, have other capabilities to make debugging easy. You can add **breakpoints** to force your web page to pause execution without adding `debugger;` statements so you can execute multiple lines of code pausing execution using the **Resume** button instead of **Step**. You can also add the `numberOfClicks` variable to a watch list so that you can see the value at a glance. 

Ask a mentor to help you set a breakpoint on the `if` statement and check out the homework to practice debugging using DevTools. 
   {% endhint %}

1. Repeat the stepping through the code and resuming until you click for the 4th time. Does the `else` condition execute?

1. In Atom, remove the `debugger;` statement so we aren't interrupted in the rest of the worksheet. Feel free to add it back if you get stuck!
   {% hint style='info' %}
`debugger;` is helpful for writing code, but don't use it for production code. Most linters will red flag `debugger` during the build process to help safe-guard your application. 
   {% endhint %}

1. Celebrate with a cocktail or mocktail! You deserve it, rockstar!

   ![](https://media.giphy.com/media/bEbRqmAnOeRi/giphy.gif)

