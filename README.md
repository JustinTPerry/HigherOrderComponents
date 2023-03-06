# HigherOrderComponents

Working with Higher Order Components in React. Created with CRA (Create React App).

## Step 1

First, I created the application using CRA, as stated above.

## Step 2

The application was then given a header containing the mock restaurant's name, Little Lemon Restaurant.

### **Aside**

The Prerequiste understanding for this mock restaurant is the following:

> The Little Lemon Restaurant & its chef debuted several new pizzas. After a few days of sales, the restaurant notices that one pizza in particular is not selling as much. As a result, the restaurant asks you, the developer, to implement mouse tracking on the web application. The hope is that the restaurant is able to use the analytics to determine why the pizza is not selling as well.
>
> > **Spoiler Alert:** There was a blurry photo for the pizza on the web app, causing customers to find no interest in the selection.

## Step 3

The _PointMouseLogger_ Component was created which displays the mouse's x and y coordinates within the window using simple parenthetical notation (x , y).

## Step 4

The _PanelMouseLogger_ Component was created which displays the mouse position coordinates within a pan format as follows:

> Mouse Position: <br>
> x: 0 y: 0

Within a simple solid border.

## Step 5

1. The functionality is implemented with a Higher Order Component, named _withMousePosition_ which takes a deconstructed parameter of _WrappedComponent_
2. The HOC contains a state, _mousePosition_.
3. The HOC also has a side effect which takes an empty array as its dependency array. This is because the side effect adds an event listener on mouse movement which calls a function within the side effect called _handleMousePositionChange_ when the event is fired. Additionally, the side effect has cleanup for the event listener.
4. The HOC returns the _WrappedComponent_ with its props spread back in and adding a _mousePosition_ prop with the value of the _mousePosition_ state.

## Step 6

Before the _App_ functional component, two const variables are created, _PointMouseTracker_ (_PointMouseLogger_ with super powers.) and _PanelMouseTracker_ (_PanelMouseLogger_ with super powers.) these are created by invoking the _withMousePosition_ HOC and passing the respective Component to the HOC.

## Finally,

With a little CSS I was able to reset margins, padding, etc. Allowing me to freely style the components in a simple, symmetrical way.
