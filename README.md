# Animal-Fun-Facts.github.io
Animal Fun Facts_CodeCademy

> In this project, we’ll build a program that allows users to click an animal on the screen in order to have a fun fact pop up.

<p align="center"><img src="https://content.codecademy.com/courses/React/react_jsx_project_preview.gif"></p>

> A preview that displays the final result of the Animal Fun Facts project. A user clicks on images of different animals, which displays a fun fact about them.

> Our program will display a selection of animals on the screen. We’ll be allowed to decide if we want to include a background or not. Clicking an animal will cause a fact to be randomly selected from a list of potential options. The selected fact will pop up on the screen. As we keep clicking, we’ll be able to see different facts.

> If you get stuck during this project or would like to see an experienced developer work through it, click “Get Unstuck“ to see a project walkthrough video.

> Let’s get started!

# TO-DO LIST:

Add a Title

## -[ ] 1.

> On line 1 in app.js, you should see an import statement. This is importing the `animals` object from animals.js. Feel free to take a look at it now, but we’ll be coming back to it in later tasks.

For now, let’s import the `React` from `react` and `createRoot` from `react-dom/client`.

## -[ ] 2.

> Click on index.html to find out the id of the HTML element to get a reference of. Use this id and the `document` object to get a reference of this element and store it in a constant called `container`.

## -[ ] 3.

> Create a React root so you can render content using the `createRoot()` method, passing `container` as an argument. Store this root in a constant called `root`.

## -[ ] 4.

> Add a `title` constant that will hold the value of the title. For now, set its value to an empty string.

> In addition, create an `animalFacts` constant to hold the JSX expression that we’ll want to be compiled. Set its value to a `<h1>` element that contains our title.

>We still shouldn’t see anything in the browser yet! We’ll have to wait until we write our React root’s `render()` method before anything shows up.

## -[ ] 5.

> We could fill in the empty string assigned to `title` if we wanted, but we could also leave it blank and let the JSX use a default value instead.

> Using the ternary operator, let the `<h1>` heading use ‘Click an animal for a fun fact’ as the default if `title` is an empty string.

## -[ ] 6.

> It’s time to call our `root`‘s `render()` method.

> Let’s pass in `animalFacts` as the JSX expression that we want to be compiled and rendered.

> When finished, click Save. If all goes well, we should see the text ‘Click an animal for a fun fact!’ appear on the screen!

> Add a Background

## -[ ] 7.

> Let’s add a background!

> Somewhere above where `animalFacts` is defined, create a constant named `background`. Set its value to a `<img />` element.

> Now let’s give it some attributes:

> Give it a class of `'background'`
> Let’s use `'ocean'` for alt.
> Finally, use `'/images/ocean.jpg'` as the value of src.

## -[ ] 8.
> Let’s reformat the JSX expression stored in `animalFacts` to include the `background` variable.

> Wrap the current `<h1>` element and our new `background` variable inside of `<div></div>` tags. Since the expression is going to be multiple lines, wrap it in parentheses.

> Click Save. If everything is working as it should, we should see our background image showing up underneath the title!

> Add an Array of Images

## -[ ] 9.

> Use a `for...in` loop to iterate over the `animals` object that we’re importing on line 1. Before the `animalFacts` definition, define an `images` array. For each animal, add a new `<img />` to that array.

> Assuming animal is the placeholder variable in your `for...in` loop, each image should have the following attributes:

```
key: {animal}
className: 'animal'
alt: {animal}
src: {animals[animal].image}
aria-label: {animal}
role: 'button'
```
## -[ ] 10.

> Now that we have our array of images, let’s inject it into the JSX expression.

> Within the `animalFacts` JSX, underneath `{background}`, create a `<div>`. Give it a `className` attribute and set it equal to `'animals'`. Nest the array of images inside of this element.

> Finally, click Save. We should see our animals!

> Adding Fun Facts

## -[ ] 11.

> Now that we have our animals displaying on the screen, we’re ready to add an event listener! But first, let’s write a function to handle this event.

> Create a function `displayFact()` that takes one parameter e, the event. We want this function to pick a random fun fact based on the selected animal.

> Inside of the function, use e.target.alt to get the name of the animal being clicked.

> Generate a random index and use it to access an element in the animal’s .facts array.

> Save the fun fact in a variable.

## -[ ] 12.

> We need a place to display our facts. Create an empty `<p>` element in `animalFacts` and give it an id attribute equal to `'fact'`.

## -[ ] 13.

> We’ll need to include the event listener with each `<img>` and edit the event listener so that it displays the fact in our new `<p>` element.

> In the `for...in` loop, inside each `<img>`, add an onClick event listener that calls displayFact.

> Inside `displayFact()` use `document.getElementById('fact')` to grab the `<p>` element where we’ll add our fact. Change the .innerHTML of the `<p>` element to our randomly selected fact.

> Now save the code and click on an animal. We should see a fact pop up on the screen!

> Extra Credit

## -[ ] 14.

> Let’s add one last feature to our awesome app!

> Create a `showBackground` constant. You can set its value to either `true` or `false`.

> If `showBackground` is `true`, `background` should show up. If it’s false, it should not. Use the `&&` operator in `animalFacts` to implement this feature.

> Toggle the value of` showBackground` between true and false and save the code to see if you got it working!

> Optional Task: In addition to the AND && operator, we can use the OR || operator. Given a list of variables or expressions, || will return the value of the first one whose boolean evaluates to true.

> Considering that the boolean of an empty string is false, can you think of a way to use || to replace the ternary operator in the heading