### Part 2: Showing and Hiding Content with jQuery

{% hint style='danger' %}

If you're using a Chromebook, skip down to the Cloud9 instructions at the bottom.

{% endhint %}

#### Setup

If you don't want Version Control practice or don't know what Version Control is, just start with step 1 below.

If you were at the Version Control session in April and would like to practice your Git skills, expand the section below and follow the steps.

<!--sec data-title="Version Control Practice" data-id="section0" data-show=true data-collapse=true ces-->
1. Fork the repository from [github.com/KansasCityWomeninTechnology/DrinkOrderApp](https://github.com/KansasCityWomeninTechnology/DrinkOrderApp) to your own GitHub Account.

2. In iTerm2 or Git Bash, use your command line skills to `cd` your way to your _CodingAndCocktails_ directory.

3. In iTerm2 or Git Bash, type `git clone https://github.com/<yourGitHubusernamehere>/DrinkOrderApp.git` to bring the repository to your local computer inside your _CodingAndCocktails_ directory.

4. In iTerm2 or Git Bash type `git checkout jquery-master` to switch to the appropriate branch.

5. Jump in on step 4 below.

Grab a mentor if you need some support as you do this!
<!--endsec-->

1. In Google Chrome, navigate to https://github.com/KansasCityWomeninTechnology/DrinkOrderApp/archive/jquery-master.zip to download the project starting point.

2. Unzip the downloaded file and place the unzipped folder in your _CodingAndCocktails_ directory that was created during your tools setup.

3. Rename the folder from _DrinkOrderApp-jquery-master_ to just _DrinkOrderApp_.

4. In Atom, open the _DrinkOrderApp_ folder by opening the **File** menu and choosing **Add Project Folder**. Navigate to the unzipped _DrinkOrderApp_ folder and click OK.

5. In Google Chrome, open the _index.html_ file and try clicking the buttons. Not very exciting yet, is it?

    {% hint style='tip' %}
You can open the file in Google Chrome in a number of ways:

1. Open Google Chrome then choose **Open File...** from the **File** menu

2. Find the file in Finder (macs) or Windows Explorer (windows), right click on it and choose to open with Google Chrome.

3. Drag the file directly on to the Google Chrome browser window.

4. In GitBash, make sure you've changed directories into the one containing the file you want to open and type `start index.html`.

5. In iTerm2, make sure you've changed directories into the one containing the file you want to open and type `open index.html`.
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
    
    3. Add a jQuery action to hide the `#menu` div.
    
    {% hint style='tip' %}
Hint: [bit.ly/CnCHide](http://bit.ly/CnCHide)

This will take you to the jQuery documentation on the hide method.
    {% endhint %}

3. Save your _my-scripts.js_ file.

4. In Google Chrome, refresh the open _index.html_ file and try clicking the "Show Menu" button and then the "Hide Menu" button. It should now show and hide the menu according to the button that you click!

**You’ve added your first interactivity to your website! Celebrate with a toast with your neighbor!**

<!--sec data-title="Chromebooks Only: Cloud9 Instructions" data-id="section1" data-show=true data-collapse=true ces-->

1. Sign up for an account at [c9.io](https://c9.io)

   Note: It will ask you for credit card information, but you will not get charged for anything since we do not use features of Cloud9 that cost money. Ask a mentor for the Coding & Cocktails card for Cloud9.

2. Confirm your account from your email and log in to Cloud9.

3. Select **Workspaces** from the left side panel if you are not already there.

4. Choose **Create a new workspace**.

5. Add a name for your workspace - it can be anything you like. You do not need a description, but feel free to add one if you like.

6. Leave your workspace as **Public**.

7. Clone the repo from Github so the files we need for Part I will be in our workspace for us.

  1. In the **Clone from Git or Mercurial URL** field enter `https://github.com/KansasCityWomeninTechnology/DrinkOrderApp.git`

8. In the template section leave the template as  **HTML5**.

9. Click on the **Create Workspace** button.

   Cloud9 will take a minute and create your workspace here.

  {% hint style='tip' %}

  To make the terminal section bigger, hover over the top line of the terminal section with your mouse - it will change to an up-down arrow icon and then you can drag up which will also make the file editing area smaller.

  ![](images/c9_terminal.png)

  {% endhint %}

10. All the files that were cloned from the Github repo are in your workspace. 

11. Close the open _README.md_ tab by clicking on the x on the tab.

12. Open the _index.html_ file in the editor by double clicking on the file name on the left.

13. On the top menu bar click on **Preview** and choose **Live Preview File** to open the preview in your workspace.  You may enlarge it to another Google Chrome tab by clicking on the expand icon.

    ![](/images/expand.png)

Now you're ready to start with the **Connecting HTML & JavaScript** section above!

<!--endsec-->
