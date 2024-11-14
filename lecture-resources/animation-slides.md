# Slide 1

CSS Animations

# Slide 2

## Agenda

-   Prayer
-   AIS Announcements
-   Project 2 Introduction
-   Lecture
-   Class Demo

# Slide 3

## Project 2 Introduction

# Slide 4

## Let's talk about CSS Animations

# Slide 5

## The Transition Property

CSS transitions allows you to change property values smoothly (over a given duration).
HTML elements that are affected by a CSS transition must be triggered by some event or action.

<!-- For example, on hover or on focus -->

For example, when you change the background color of an element on hover, you can use the transition property to make the change abrupt to smooth.
code example

```css
div {
    width: 100px;
    height: 100px;
    background-color: red;
    transition: background-color 2s;
}
div:hover {
    background-color: green;
}
```

# Slide 6

## The Transition Property

The transition property can also be used to changed all properties of the action element.

```css
div {
    width: 100px;
    height: 100px;
    background-color: red;
    transition: all 2s;
}
div:hover {
    width: 300px;
    height: 300px;
    background-color: green;
}
```

# Slide 7

## The Transition Property

The transition property actually is a shorthand property for the four specific transition properties:

-   `transition-property` - Specifies the name of the CSS property the transition effect is for.
-   `transition-duration` - Specifies the duration of the transition. (can be in seconds or milliseconds)
-   `transition-timing-function` - Specifies the speed curve of the transition effect.
-   `transition-delay` - Specifies a delay (in seconds) for the transition effect.

For example:

```css
div {
    transition-property: background-color;
    transition-duration: 2s;
    transition-timing-function: ease;
    transition-delay: 1s;
}
```

is the same as:

```css
div {
    transition: background-color 2s ease 1s;
}
```

# Slide 8

## The Transition Timing Function

The only property that requires a little more discussion is the `transition-timing-function`. This property is used to specify the speed curve of the transition effect. The speed curve defines the speed and smoothness of the transition effect. There's a ton of options for this property, but the most common are:

-   `ease` - Specifies a transition effect with a slow start, then fast, then end slowly (this is default)
-   `linear` - Specifies a transition effect with the same speed from start to end
-   `ease-in` - Specifies a transition effect with a slow start
-   `ease-out` - Specifies a transition effect with a slow end
-   `ease-in-out` - Specifies a transition effect with a slow start and end

_Show examples of each_

# Slide 9

## So, we can trigger an animation when we trigger some event, but what if we want to trigger an animation without an event?

There's a specifc way to define the life cycle of an animation in CSS. This is done with the `@keyframes` rule. The `@keyframes` rule specifies the animation code. The animation is created by gradually changing from one set of CSS styles to another. During the animation, you can change the set of CSS styles many times.

# Slide 10

## Keyframes

The `@keyframes` architecture can be used to define the cycle of an HTML element in animation. It specifically controls the animation stage at each point in time.
Let's look at an example:

```css
@keyframes changeColor {
    0% {
        background-color: red;
    } /* The start of an animation */
    25% {
        background-color: yellow;
    } /* 1/4th into the life of the animation cycle */
    50% {
        background-color: blue;
    } /* 1/2 way through */
    75% {
        background-color: green;
    } /* 3/4 of the cycle completed */
    100% {
        background-color: red;
    } /* the end of the animation cycle */
}
```

Take note that typically, the end of the `@keyframes` cycle represents a return to the original state of the element.

# Slide 11

## Applying Keyframes

That's great and all, but how do we apply this to an element?
Any CSS selector pair can implement a specific `@keyframes` through referencing the name of it in the `animation-name` property.

```css
div {
    width: 100px;
    height: 100px;
    background-color: red;
    animation-name: changeColor;
    animation-duration: 4s;
}
@keyframes changeColor {
    0% {
        background-color: red;
    }
    25% {
        background-color: yellow;
    }
    50% {
        background-color: blue;
    }
    75% {
        background-color: green;
    }
    100% {
        background-color: red;
    }
}
```

# Slide 12

## All the Animation Properties

There are a few other properties that can be used to control the animation of an element. These include:

-   `animation-name` - Specifies the name of the `@keyframes` rule that defines the animation.
-   `animation-duration` - Specifies the duration of the animation.
-   `animation-timing-function` - Specifies the speed curve of the animation.
-   `animation-delay` - Specifies a delay for the start of an animation.
-   `animation-iteration-count` - Specifies the number of times an animation should be played.
-   `animation-direction` - Specifies whether an animation should be played forwards, backwards, or in alternate cycles.

# Slide 13

## All the Animation Properties, in a Shorthand

Just like the `transition` property, the `animation` property is a shorthand property for the six animation properties:

```css
.box {
    animation-name: changeColor;
    animation-duration: 4s;
    animation-timing-function: ease;
    animation-delay: 2s;
    animation-iteration-count: infinite;
    animation-direction: alternate;
}
```

is equivalent to:

```css
.box {
    animation: changeColor 4s ease 2s infinite alternate;
}
```

There are definitely pros and cons to using the shorthand. Shorthand looks clean and precise but not as intuitive or easy to read as its long counterpart.

# Slide 14

## The last CSS Property

The last CSS Property we will learn about this semester deals with direct manipulations of how an element is displayed on the screen, and it's predominantly used in animation-like settings.

# Slide 15

## The last CSS Property: transform

Allows you to apply various transformations to an element in 2D or 3D space. These transformations include rotations, translations (moving), scaling (resizing), and skewing (distorting).

translate - Moves the element both horizontally and vertically by the specified values.

`transform: translate(value1, value2);`

rotate - Rotates the element clockwise by the specified angle

`transform: rotate(angle);` [in degrees]

scale - Scales the element both horizontally and vertically by the specified factors.

`transform: scale(x, y);`

skew - Skews the element both horizontally and vertically by the specified angles.

`transform: skew(x-angle, y-angle);`

```css
.box {
    /* other visual styling properties */
    transition: all 2s ease;
}
.box:hover {
    transform: translate(5px, 10px) rotate(90deg) scale(5px, 10px) skew(120deg, 60deg);
}
```

# Slide 16

## Transition: review

Transition is used when triggered by an event, or interaction that CSS can identify. We’ve only used :hover in class so far, but there’s plenty more.

```css
.example {
    /* styling properties */
    transition: -property -duration -timing-function -delay;
}
.example:hover {
    width: 250px;
    background-color: #00000ff;
}
```

# Slide 17

## Animation: review

Animation is used when you want to animate an element without an event. It’s a way to control the life cycle of an element in CSS.

```css
.example {
    animation: -name -duration -timing-function -delay -iteration-count -direction;
}
@keyframes exampleKeyframe {
    0% {
        rotate: 0deg;
        background-color: red;
    }
    100% {
        rotate: 360deg;
        background-color: blue;
    }
}
```

# Slide 18

## Transform: review

Transform is used to manipulate the position, size, and shape of an element. It’s a way to control the visual appearance of an element in CSS.

```css
.example {
    transform: translate(value1, value2) rotate(angle) scale(x, y) skew(x-angle, y-angle);
}
```

When using transform, you can include one or more of any of the transformations in the same declaration.
