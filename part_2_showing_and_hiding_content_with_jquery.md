#
## Part 2: Showing and Hiding Content with jQuery

#### Setup

If you don't want Version Control practice or don't know what Version Control is, just start with step 1 below.

If you were at the Version Control session in April and would like to practice your Git skills, expand the section below and follow the steps.

<!--sec data-title="Version Control Practice" data-id="section0" data-show=true data-collapse=true ces-->
1. Fork the repository from [https://github.com/KansasCityWomeninTechnology/DrinkOrderApp/tree/jquery-master](https://github.com/KansasCityWomeninTechnology/DrinkOrderApp/tree/jquery-master) to your own GitHub Account.

2. In iTerm2 or Git Bash, use your command line skills to `cd` your way to your _CodingAndCocktails_ directory.

3. In iTerm2 or Git Bash, `git clone` the repository inside your _CodingAndCocktails_ directory.

4. In iTerm2 or Git Bash type `git checkout jquery-master` to switch to the appropriate branch.

5. Jump in on step 4 below.

Grab a mentor if you need some support as you do this!
<!--endsec-->

1. In Google Chrome, navigate to https://github.com/KansasCityWomeninTechnology/DrinkOrderApp/archive/jquery-master.zip to download the project starting point.

2. Unzip the downloaded file and place the unzipped folder in your _CodingAndCocktails_ directory that was created during your tools setup.

3. Rename the folder from _DrinkOrderApp-jquery-master_ to just _DrinkOrderApp_.

4. In Atom, open the DrinkOrderApp folder by opening the **File** menu and choosing **Add Project Folder**. Navigate to the unzipped DrinkOrderApp folder and click OK.

5. In Google Chrome, open the _index.html_ file and try clicking the buttons. Not very exciting yet, is it?

    {% hint style='tip' %}
You can open the file in Google Chrome in three ways:

1. Open Google Chrome then choose **Open File...** from the **File** menu

2. Find the file in Finder (macs) or Windows Explorer (windows), right click on it and choose to open with Google Chrome.

3. Drag the file directly on to the Google Chrome browser window.
    {% endhint %}

#### Connecting HTML & JavaScript

1. Connect the HTML & the JavaScript files.

    {% hint style='tip' %}
If you missed the HTML session and aren't sure what an HTML tag is, grab a mentor to give you a quick overview and help catch you up!
    {% endhint %}

    1. In Atom, open the _index.html_ file by double clicking on it.

    2. Just above the closing `</head>` tag in the _index.html_ file, add a `<script>` tag for the jQuery library (jquery-3.2.1.min.js found in the _assets/lib_ directory of the project). The script tag should look like this: `<script src="assets/lib/jquery-3.2.1.min.js"></script>`

    ![](/images/addScript.gif)

    {% hint style='tip' %}
Ask a mentor to show you or remind you how to use Emmet to make your HTML writing faster!
    {% endhint %}

    3. On a separate line just below the jQuery script tag you just created and just above the `</head>` tag, add a `<script>` tag with a `src` attribute for the JavaScript file that you'll be changing (located at assets/scripts/my-scripts.js).

    {% hint style='tip' %}
Order of the script tags you add matters! Script tags are executed in the order that they appear in your HTML code so because our _my_scripts.js_ file will depend on jQuery, make sure the `<script>` tag for _my_scripts.js_ comes after the `<script>` tag for the jQuery library.

For a refresher on `<script>` tags check out [bit.ly/scriptElement](http://bit.ly/scriptElement).

For further reading on using jQuery in a project navigate to [bit.ly/StartjQuery](http://bit.ly/StartjQuery).
    {% endhint %}

#### Show the Menu
1. In Atom, open the _my-scripts.js_ file from the _assets/scripts_ directory. This is where jQuery code will be added.

2. First, the HTML document must be ready before it can attempt to run anything.

    1. In _my-scripts.js_, type `$(document).ready(function() {});`

    {% hint style='info' %}
For further reading on `$(document).ready();` navigate to [bit.ly/docReady](http://bit.ly/docReady) in Google Chrome.
    {% endhint %}

3. Add interaction to the “Show Menu” button. When the button is clicked, the `<div>` tag with the id of `#menu` should be displayed.

    1. Capture the click event inside the `$(document).ready(function () { });` code in _my-scripts.js_.

        1. In the _index.html_ file, find the id of the "Show Menu" button.

        2. In _my_scripts.js_, place your cursor between the curly braces of the function {} and press enter. This is the **body** of the function where the code that runs when the function is called lives. Add a click event handler to the button.

        {% hint style='tip' %}
`$("#my-id").click();`

Replace `#my-id` with the id you found in the _index.html_ file in the previous step.
    {% endhint %}

    2. In response to the click event, add an action to display the menu.

        1. Inside the parentheses of the click event handler, add a function to run the action: `$("#my-id").click(function () {});`.

        2. In the body of that function, select the element you want to act on, in this case the #menu div.

        3. Add a jQuery action to show that HTML div: `$("#another-id").show();`.

4. Save your _my-scripts.js_ file.

5. In Google Chrome, refresh the open _index.html_ file and try clicking the "Show Menu" button. It should now display the menu when you click on it!

#### Hide the Menu
Now that you can view the menu, make sure you can hide it when you don’t want to see it. Hide the `<div>` HTML element with the id of`#menu` when the "Hide Menu" button is clicked with code in _my-scripts.js_. This will be very similar to what we just did with the "Show Menu" button but a different action on the `<div>`.

1. Capture the click event.

    1. Select the "Hide Menu" button.

    2. Add the click event handler to the button.

        ![](/images/selectHideMenu.gif)

{% hint style='tip' %}
Hint: [bit.ly/CnCClick](http://bit.ly/CnCClick)

This will take you to documentation on the jQuery click event handler.
{% endhint %}

2. Add the action.

1. In between the parentheses of the click event handler, add the function like you saw in the gif above: `function() {}`.

2. In the body of that function (that means in between the curly braces), select the element you want to act on, in this case the `#menu` div.

{% hint style='tip' %}
Hint: [bit.ly/CnCSelect](http://bit.ly/CnCSelect)

This will take you to the jQuery documentation on id selectors.
{% endhint %}

3. Add a jQuery action to hide that HTML div.

{% hint style='tip' %}
Hint: [bit.ly/CnCHide](http://bit.ly/CnCHide)

This will take you to the jQuery documentation on the hide method.
{% endhint %}

4. Save your _my-scripts.js_ file.

5. In Google Chrome, refresh the open _index.html_ file and try clicking the "Show Menu" button and then the "Hide Menu" button. It should now show and hide the menu according to the button that you click!

**You’ve added your first interactivity to your website! Celebrate with a toast with your neighbor!**