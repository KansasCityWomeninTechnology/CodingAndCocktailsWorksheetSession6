### Part 2: Showing and Hiding Content with jQuery

#### Setup

1.  In Google Chrome, navigate to https://github.com/KansasCityWomeninTechnology/DrinkOrderApp/archive/jquery-master.zip to download the project starting point.

2. Unzip the downloaded file and place the unzipped folder in your _CodingAndCocktails_ directory that was created during your tools setup.

3. Rename the folder from _DrinkOrderApp-jquery-master_ to just _DrinkOrderApp_.

4. In Atom, open the DrinkOrderApp folder by opening the **File** menu and choosing **Add Project Folder**. Navigate to the unzipped DrinkOrderApp folder and click OK.

5.  In Google Chrome, open the _index.html_ file and try clicking the buttons.  Not very exciting yet, is it?

#### Connecting HTML & JavaScript

1. Connect the HTML & the JavaScript files.

  1.  In Atom, open the _index.html_ file by double clicking on it.  

  2. Just above the closing `</head>` tag in the _index.html_ file, add a `<script>` tag for the jQuery library (jquery-3.2.1.min.js found in the _assets/lib_ directory of the project). The script tag should look like this: `<script src="assets/lib/jquery-3.2.1.min.js"></script>`

      ![](/images/addScript.gif)

   3. On a separate line just below the jQuery script tag you just created and just above the `</head>` tag, add a `<script>` tag with a `src` attribute for the JavaScript file that you'll be changing (located at assets/scripts/my-scripts.js).

#### Show the Menu
1.  In Atom, open the _my-scripts.js_ file from the _assets/scripts_ directory. This is where jQuery code will be added.

2.  First, the HTML document must be ready before it can attempt to run anything.  

    1. In _my-scripts.js_, type `$(document).ready(function() {});`

3. Add interaction to the “Show Menu” button.  When the button is clicked, the `<div>` tag with the id of `#menu` should be displayed.

  1.  Capture the click event inside the `$(document).ready(function () { });` code in _my-scripts.js_.

      1.  In the _index.html_ file, find the id of the "Show Menu" button.

      2.  In _my_scripts.js_, place your cursor between the curly braces of the function {} and press enter.  This is the **body** of the function where the code that runs when the function is called lives.  Add a click event handler to the button.


  2.  In response to the click event, add an action to display the menu.

      1.  Inside the parentheses of the click event handler, add a function to run the action: `$("#my-id").click(function () {});`.

      2.  In the body of that function, select the element you want to act on, in this case the #menu div.

      3.  Add a jQuery action to show that HTML div: `$("#another-id").show();`.

4. Save your _my-scripts.js_ file.

5. In Google Chrome, refresh the open _index.html_ file and try clicking the "Show Menu" button.  It should now display the menu when you click on it!

#### Hide the Menu
Now that you can view the menu, make sure you can hide it when you don’t want to see it. Hide the `<div>` HTML element with the id of`#menu` when the "Hide Menu" button is clicked with code in _my-scripts.js_.  This will be very similar to what we just did with the "Show Menu" button but a different action on the `<div>`.

1.  Capture the click event.

    1.  Select the "Hide Menu" button.

    2.  Add the click event handler to the button.

        ![](/images/selectHideMenu.gif)

2.  Add the action.

    1.  In between the parentheses of the click event handler, add the function like you saw in the gif above: `function()  {}`.

    2.  In the body of that function (that means in between the curly braces), select the element you want to act on, in this case the `#menu` div.


    3.  Add a jQuery action to hide that HTML div.

TODO: hint here.

    4. Save your _my-scripts.js_ file.

    5. In Google Chrome, refresh the open _index.html_ file and try clicking the "Show Menu" button and then the "Hide Menu" button.  It should now show and hide the menu according to the button that you click!

**You’ve added your first interactivity to your website! Celebrate with a toast with your neighbor!**
