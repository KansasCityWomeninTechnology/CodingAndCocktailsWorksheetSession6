### Part 4:  Content Slider

Next you'll add in a content slider to the page.  This is very useful to scroll through pictures, text, videos or any other html items on a website.  This project will utilize a library called bxSlider.

1. In the _index.html_ file, on line 26, find the HEADER section.  On line 32 you'll find a commented out unordered list HTML element `<ul>` with a class of "bxslider" and four list items `<li>`.  Uncomment the HTML markup (see GIF below). The bxSlider library is already included in the project for you as well as the necessary HTML markup.  You’re going to add the interactivity!

   ![](/images/uncomment.gif)

2. First, connect the bxSlider JavaScript file and CSS styling to the _index.html_ file so everything will work!  The JavaScript file (_jquery.bxslider.min.js_) and the CSS file (_jquery.bxslider.min.css_) are located in the _assets/lib/jquery.bxslider_ directory.  

   {% hint style='tip' %}
Don’t forget - JavaScript additions use a `<script>` tag while CSS additions use a `<link>` tag!

See step 1 of the “How to Install” section on [bxslider.com](http://bxslider.com) for further guidance.
   {% endhint %}

3. Look at the _index.html_ file and find the unordered list element `<ul>` with a `bxslider` class to identify the markup for the slider.

4. In Atom, in the _my-scripts.js_ file, call the **bxSlider** on your content.  Hint: See step 3 of  the “How to Install” section on [bxslider.com](http://bxslider.com/)

5. Try making some modifications to how your slider works:

   1. Change the mode of the slider to 'vertical'. Hint: [bit.ly/bxSExample](http://bit.ly/bxSExample):
   2. Add captions to your images. Hint: [bit.ly/bxSOpts](http://bit.ly/bxSOpts)

   3. Check your slider against the answer key here: [bit.ly/jQFinal](http://bit.ly/jQFinal)

**Congratulations!  You created an interactive website!**
