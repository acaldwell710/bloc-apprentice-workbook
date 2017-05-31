# Module 2 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

*Note: any topics from the first assessment should be reviewed in addition to the questions below!*

## CSS

### Questions

1. What is the box model?

--This represents the content's height and width surrounded by padding on all sides, which is surrounded by a border on all sides, and finally surrounded by a margin on all sides.
2. What is the difference between block and inline elements?

--A block level element literally takes up a visual block on the page and no other elements can sit on the same line by default. An Inline element can lie within a block level element, such as a link. Many of these elements can line up side by side on the same line.
3. What is responsive design?

--Responsive design refers to how a design reacts and interacts on different devices. Being concious of this is important due to the use of so many different device sizes.
4. Which selector is more specific, a tag selector or class selector?

--An element selector is the least selective, followed by the the class selector which is less inclusive as it only selects a certain class of elements, and the most selective selector is an id selector which is singular.
5. What does `box-sizing` do?

--Box sizing refers to the size of the contents + it's border + padding + margin, etc. When all is said and done, normally all of the extra space is not accounted for within the layout. However if you use box-sizing: border-box, or box-sizing: border-radius, etc. then you can easily account for how much space is actually being taken up by an element on your page.
6. What's the difference between `relative` and `absolute` positioning?

--The difference between relative and absolute position is that relative position is still within the flow of the layout. While desiging you can still make changes to the element's location "relative" to itself, such as top: 10px; which would move the element down 10px. However, with absolute positioning the element is removed from normal flow, and can really be placed anywhere on the page.

### Exercises

1. Write a CSS rule to turn the background color of the link with the `.btn` class blue on hover:

  ```html
  <a href="#" class="btn">Learn more</a>
  ```
  
  -- .btn on:hover {
          background-color: blue;
     }

2. Write a CSS rule to give the `.container` a maximum width of `980px` when the browser window is wider than `1200px`:

  ```html
  <div class="container">
    <h1>I'm a heading!</h1>
  </div>
  ```
  
  --.container(@media min-width: 1200px) {
                  max-width: 980px;
    }

3. Which text would be red in the following example?

  ```html
  <style>
    section p:last-child {
      color: red;
    }
  </style>

  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>
  </section>
  <section>
    <p>First paragraph</p>
    <p>Second paragraph</p>
    <p>Third paragraph</p>
  </section>
  ```
  
  --The third paragraph would be red.

4. Open this [JSBin](http://jsbin.com/qigiwuhepe/1/edit?html,css,output). Write a CSS rule using floats to make the HTML sample into a four column layout. Paste your udpated link below.

## JavaScript

### Questions

1. What is a callback?

--A callback is a way of enacting or enabling the / a function to run.

### Exercises

1. Write a function `filterLongWords()` that takes an array of words and an integer `num` and returns the array of words that are longer than `num`.

--
function filterLongWords (arr, num){
  var arr2 = []
  for (var i = 0; i < arr.length ; i++) {
    if (num.length <= arr[i].length) {
      arr[i] = arr2.push(arr[i]);
    }
  }
  return arr2;
}
filterLongWords(["hello", "hi", "how"], "one");
2. Write a function `charFreq()` that takes a string and builds a frequency listing of the characters contained in it. Represent the frequency listing as a Javascript object. Try it with something like `charFreq("abbabcbdbabdbdbabababcbcbab")`.

## DOM Scripting

### Questions

1. What does DOM stand for and what is it?

--DOM stands for Document Object Model and it is a representation of the "document" that is being written.

### Exercises

1. Write a JavaScript statement that finds the element with the ID, `next`, and saves it to a variable called `nextButton`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  ```
  
  --var nextButton = document.getElementById("next");

2. Write another line that updates the text of `nextButton` to `"Next image"`.

--
3. Write another line that adds a click event listener to `nextButton` so that when it's clicked the browser alerts `"Next image coming up."`.

--

## jQuery

### Questions

1. What is a JavaScript library and why do we use them?

--A javascript library basically houses lots of methods which can be used by external linking or internally linking the file. Sometimes you can even use just a small portion of the library. 
2. What is jQuery for?

--jQuery is a javascript library that adds similar functionality to a page as DOM scripting, but also contains even more complex methods and functionality.

### Exercises

1. Write a statement to select all elements with the `.btn` class using a jQuery selector and save them to a variable called `buttons`:

  ```html
  <a href="#" id="next" class="btn">Next</a>
  <a href="#" id="beginning" class="btn">Beginning</a>
  <a href="#" id="previous" class="btn">Previous</a>
  ```
  
 --var buttons = $('.btn');

2. Write another line that adds a click event to the buttons that logs `'click'` to the console when the button is clicked. Use the jQuery syntax.

--$(buttons).click();

## Angular

### Questions

1. How is a framework different than a library?

--A framework provides structure as well as functionality to a website or application.
2. What is a controller?

--A controller is what essentially runs the website or application, without the controller, the program would not make sense.
3. What is a view?

--The view is the platform through which the audience is seeing the program. 
4. What is a single page application?

--A single page application is a web application that presented solely on a singular HTML page.
5. What is a directive in Angular?

--A directive is basically an attribute or a marker that kind of gives direction to look out for this element or do this to this element, sometimes in the case of ng-model it even creates a variable.

## Git

### Exercises

1. Write a command to create a new branch called `bug-fix`.

--git branch bug-fix
--git checkout -b bug-fix
2. If you're on the `master` branch, write a command to merge a branch called `bug-fix` into the `master` branch.

--git merge bug-fix
