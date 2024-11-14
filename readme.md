# Introduction

Welcome to In-Class Activity number 10! In this activity we are going to learn about CSS Animations!

## Task List

### 1. Animate a logo in the header of the page.

Add a logo to the header of the page. Have the logo get bigger and slightly rotate when hovered over.

> [!TIP]
> Remember that the `transition` property can be given multiple values to transition multiple properties at once: like `transition: width 2s, height 2s, translate(3px, 5px) 2s;`

### 2. Highlight a dynamic quote in a box in the grid.

Insert a quote in any of the boxes, and create a `background-image` of a gradient that only has a `background-size` representative of an underline. The underline should grow along the bottom of the text on hover.

> [!TIP]
> Not sure what this means? Watch this 1-minute tutorial and it'll take you through the steps: [Watch Here](https://youtu.be/_1vEGYWaaQY?si=BkrLWJVMbVt1qlbD)

### 3. Change the position of any square in the grid continually.

Have the position of any square in the CSS grid change continuously by set parameters. There are many ways to go about this (think of order, align-self, or others), but I would definitely recommend changing the `grid-column` or `grid-row` properties through `@keyframes`.

### 4. Highlight a notification on the page.

Have a notification scroll in from anywhere offscreen on a set interval. In my example, I have a notification that scrolls in from the bottom right corner of the page every 10 seconds.

> [!TIP]
> It would be extremely beneficial to think through this task before you start coding. Start by asking yourself, "how can I make an element be positioned offscreen?" and "how can I make an element move from offscreen to onscreen?"

### 5. Have a square with a linear gradient background-image change on hover.

Now this is a fun one. Have a square in the grid with a `background-image` of a linear gradient. When hovered over, the gradient should change to a different gradient.

> [!TIP]
> The easiest way to do this is to have only one gradient set in the selector before the hover event. Then, during the hover, trigger an infinite, linear animation. Your `@keyframes` should have two states, where the property value pair of `filter: hue-rotate();` is set. Think of this like a color wheel, where your start will be `0deg` and the end will be `360deg`!

### 6. Make the circular text in one of the squares in the grid rotate continuously.

I provided an svg with a specific `textPath` that's been hard coded into the HTML. First, fill in whatever text content you would like in the `textPath`. You'll need to make the text rotate continuously around the circle, which you can do by just rotating the entire `svg`.

## Submission

Commit and push your changes to submit ICA10.

## Example Code

Here is an example website showcasing some of the tasks that you will be completing so you can get an idea of what the final product should be: [click to go to the example](https://ckearl.github.io/ica10-example/).

## Lecture Resources

If you need resources to help you complete the tasks, the content for the lecture slides from this week can be found in the `lecture-resources` folder in the repository. You can find information on CSS animations and transitions in the `animation-slides.md` file.

## A note on editing and your styling decisions

You may edit the CSS of the `template.css` file, but it would be nicer just to put your updates in `ica10.css`. I would take a moment to study the structure of the code in `template.css`. You'll notice that I've set up a CSS grid with a few different classes. You can use these classes to style the elements in the grid. You can also add new classes if you need to.

If you feel inclined, you can accomplish the six tasks in any way you'd like; I just provided a template that made an approachable canvas for us to learn about more GitHub functions and CSS Animations. You can add new elements, change the structure of the grid, or anything else you'd like to do.
