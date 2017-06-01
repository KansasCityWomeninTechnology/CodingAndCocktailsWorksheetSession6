### Part 2: Showing and Hiding Content with jQuery

#### Setup

1.  In Git Bash or iTerm2, type `cd ~/CodingAndCocktails` to make sure you're in your CodingAndCocktails directory that was created during the setup of The Tools.

2. In Google Chrome, navigate to https://github.com/KansasCityWomeninTechnology/DrinkOrderApp/archive/jquery-master.zip to download the project starting point.

3. Unzip it.

# TODO - Unzip Directions

3. In Atom, open the DrinkOrderApp folder by going to the File menu and choosing **Add Project Folder**. Navigate to the unzipped DrinkOrderApp folder that you created and click OK.

4.  In Google Chrome, open the _index.html_ file and try clicking the buttons.  Not very exciting yet, is it?

#### Connecting HTML & JavaScript

1. Connect the HTML & the JavaScript files.

    {% hint style='tip' %}
If you missed the HTML session and aren't sure what an HTML tag is, grab a mentor to give you a quick overview and help catch you up!
    {% endhint %}

  1.  In Atom, open the _index.html_ file.  

  2. Just above the `</head>` tag in the _index.html_ file, add a `<script>` tag for the jQuery library (jquery-3.2.1.min.js found in the _assets/lib_ directory of the project). The script tag should look like this: `<script src="assets/lib/jquery-3.2.1.min.js"></script>`

   3. On a separate line just below the jQuery script tag you just created and just above the `</head>` tag, add a `<script>` tag with a `src` attribute for the JavaScript file that you'll be changing (located at assets/scripts/my-scripts.js).

   {% hint style='tip' %}
Order of the script tags you add matters! Script tags are executed in the order that they appear in your HTML code so because our _my_scripts.js_ file will depend on jQuery, make sure the `<script>` tag for _my_scripts.js_ comes after the `<script>` tag for the jQuery library.

For a refresher on `<script>` tags check out bit.ly/scriptElement.

For further reading on using jQuery in a project navigate to bit.ly/StartjQuery.
    {% endhint %}

#### Show the Menu
1.  In Atom, open the _my-scripts.js_ file from the _assets/scripts_ directory. This is where jQuery code will be added.

2.  First, the HTML document must be ready before it can attempt to run anything.  

    1. In _my-scripts.js_, type `$(document).ready(function() {});`

    {% hint style='info' %}
For further reading on `$(document).ready();` navigate to [bit.ly/docReady](http://bit.ly/docReady) in Google Chrome.
    {% endhint %}

3. Add interaction to the “Show Menu” button.  When the button is clicked, the `<div>` tag with the id of `#menu` should be displayed.

  1.  Capture the click event inside the `$(document).ready(function () { });` code in _my-scripts.js_.

      1.  In the _index.html_ file, find the id of the "Show Menu" button.

      2.  In _my_scripts.js_, place your cursor between the curly braces of the function {} and press enter.  This will is the of the function where the code to run when the function is called gets added.  Add a click event handler to the button.

    {% hint style='tip' %}
`$(“#my-id”).click();`
    {% endhint %}

  2.  In response to the click event, add an action to display the menu.

      1.  Inside the parentheses of the click event handler, add a function to run the action.

    {% hint style='tip' %}
`$(“#my-id”).click(function () { });`
    {% endhint %}

      2.  In the body of that function, select the element you want to act on, in this case the #menu div.

      3.  Add a jQuery action to show that HTML div.

    {% hint style='tip' %}
`$("#my-id").show();`
    {% endhint %}

4. In Google Chrome, refresh the open _index.html_ file and try clicking the "Show Menu" button.  It should now display the menu when you click on it!

#### Hide the Menu
Now that you can view the menu, make sure you can hide it when you don’t want to see it. Hide the `<div>` HTML element with the id of`#menu` when the "Hide Menu" button is clicked with code in _my-scripts.js_.  This will be very similar to what we just did with the "Show Menu" button but a different action on the `<div>`.

{% hint style='info' %}
Since this code is similar to the previous section, the instructions will be a little less detailed for you to try it with a little less guidance. This is hard stuff though so if you're unsure, re-read the section about showing the menu to see if you can figure out the changes to make hiding the menu work.  If you're still stumped, grab one of our awesome mentors to talk through it with you! You've got this!
{% endhint %}

1.  Capture the click event.

    1.  Select the "Hide Menu" button.

    2.  Add the click event handler to the button.
    {% hint style='tip' %}
    Hint: [bit.ly/CnCClick](http://bit.ly/CnCClick)

    This will take you to documentation on the jQuery click event handler.
    {% endhint %}

2.  Add the action.

    1.  In between the parentheses of the click event handler, add the function: `function()  {}`.

    2.  In the body of that function (that means in between the curly braces), select the element you want to act on, in this case the `#menu` div.

    {% hint style='tip' %}
    Hint: [bit.ly/CnCSelect](http://bit.ly/CnCSelect)

    This will take you to the jQuery documentation on id selectors.
    {% endhint %}

    3.  Add a jQuery action to show that HTML div.

    {% hint style='tip' %}
    Hint: [bit.ly/CnCHide](http://bit.ly/CnCHide)

    This will take you to the jQuery documentation on the hide method.
    {% endhint %}

**You’ve added your first interactivity to your website! Celebrate with a toast with your neighbor!**
