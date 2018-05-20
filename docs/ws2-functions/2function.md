1. In your Atom, open _scripts.js_. You'll see MadLibs items like we had in the first section of the worksheet. 

1. Search for **< noun>** and **< verb>** and replace the variables. Save the file and look at the web page in Chrome. The lavender button now has text in it, but we want it do something when we click on it.
   {% hint style='tip' %}
Every time you make a change, save the file. The atom-live-server package will automatically refresh the Chrome tab to keep the app up to date with your **saved** work. Atom alerts you to unsaved work by displaying a blue circle in the tab:

![](images/atom-save.png)

Save the file by navigating to **File** <i class="fa fa-long-arrow-right"></i> **Save** or by using the keyboard shortcut `cmd` + `s` for Macs and `ctrl` + `s` for Windows. Refer to [Helpful Keyboard Shortcuts](/references).
   {% endhint %}

   {% hint style='tip' %}
View the worksheet and the IDE in split screen mode to make it easier to work through tonight's session. Check out the [helpful tips in the Setup guide](/setup#tips). 
   {% endhint %}

1. Let's display an alert message by adding `alert('click');` inside the `clickHandler` function. The `clickHandler` function should look like this:

   ```javascript
const clickHandler = function(text) {
    alert('click');
}
   ```

1. Now try clicking the button. An alert message appears!

1. Define a new variable called `numberOfClicks` above the `clickHandler` method so we can keep track of the number of button clicks and set the value to 0. Your variable should look like this:

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
```javascript
numberOfClicks += 1;
numberOfClicks++;
```
  {% endhint %}   

1. Update the alert message to show the number of clicks by adding `numberOfClicks` to the display text using string concatenation.
   ```javascript
alert('click ' + numberOfClicks);
   ```

1. Click the button a few times to see your click counter in action.


