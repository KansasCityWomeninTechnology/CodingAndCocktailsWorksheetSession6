1. Declare an array called `brainSkills` after the `clickHandler` function by typing `const brainSkills = [];`. (JAD TODO probably create a comment with where the array should be declared)
   {% hint style='info' %}
This creates an empty array called `brainSkills` that is accessible by anything in _script.js_.
   {% endhint %}  

1. Place your cursor between the opening and closing square brackets and press `Enter`. Type `"HTML"`. 
   {% hint style='info' %}
You added an element to the array. Your array now has a length of 1.
   {% endhint %}  

1. Inside the `document.addEventListener` method, add a `console.log` to log out the length of the array. Type
   ```javascript
console.log("brainSkills.length " + brainSkills.length);
   ```

1. Add more skills you learned at Coding & Cocktails to the array by comma separating values. Your `brainSkills` array might look something like this:
   ```javascript
const brainSkills = [
	"HTML",
	"CSS",
	"Command line operations",
	"Vim",
	"Git",
	"Front-End Architecture",
	"Yeoman"
];
   ```
   {% hint style='working' %}
What is your array length now?
   {% endhint %}  
