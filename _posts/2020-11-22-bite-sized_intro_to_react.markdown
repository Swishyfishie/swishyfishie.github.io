---
layout: post
title:      "Bite-sized intro to React"
date:       2020-11-22 10:54:30 +0000
permalink:  bite-sized_intro_to_react
---


Sometimes we come across tutorials that seem great because we're building something, and that's ok.

The main issue with some of these tutorials is that they are focused on you building something, and not actually, teaching you what's going on inside of what you've built, so at the end of an udemy course you might find yourself having coded 3 full stack applications and have no idea how to manipulate an array.

I'll try to take a different approach with this article and instead of focusing on building, we're going to dissect something which was already built following examples from www.reactjs.com and www.w3schools.com

I'm going to explore the following questions.

1. What is a component? (and what is going on inside it)

2. What are the props? (and what is *this*)

3. What is the state?


> Note: the HTML you see in React is not actually HTML, it's a way of writing JavaScript and HTML. You are not required to know JSX in order to build a React app, but it's definitely the easiest way. 
> 

### What is a component?

A component is a piece of code that is (ideally) reusable code, that is (*again, ideally*) independent from the other pieces of code that you wrote.

This is a component: 

![react component](https://i.imgur.com/8lSW63U.png)
> Reference: https://reactjs.org/


Now, let's break down what's going on in here. 

On line 1 we're using the ES6 Class syntax to define the "TodoList" class, that is extending the React.Component which basically means that TodoList class is a React.Component child, therefore inheriting React.Component's methods.

On line 2, we're looking at a ***render***  function, that (on line 3) *** returns*** HTML.

Line 4 is an *UL* opening tag, that closes on line 8,  and line 5 and 6 are the display of JSX's power. 

Curly braces allow you to process javascript inside the HTML, you can think of it like when you're using template literals in javascript, where in order to have javascript code in your string, you need to surround the string with back-ticks and wrap your code around ${ }. It's mostly the same principle.

Coming back to line 5 and 6.
We're going to talk about `this` and `props` soon, but for now you just need to know that we're mapping over the this.props.items array and returning a *LI* html element that has a key and a content of `item.text`.


### What are the props?

Props are properties of a react component. They are similar to what arguments are in a javascript function and they're passed down from a parent component.

![car compoent](https://i.imgur.com/MGn9WhG.png)
> Reference: https://www.w3schools.com/

On this example you can see how there are two components, Car and Garage. If we're thinking about the hierarchy of things, a Garage can store Cars so we can say that Garage is the parent of Car. 

In the Garage component you can see how the `<Car />` component is invoked and there's the prop passed in as brand="Ford" which is essentially a HTML attribute. 

The Car component can access it through `props` and in our case, through `this.props.brand` 

`this` refers to the object it belongs to so `this.props.brand` could be pseudocoded like:

this object . props . the attribute 

### What is the state?

The state of an object refers to what that object is like, and its attributes.

A state of a Car object can be an object that holds some attributes such as `color:red`, `working:true`, `wheels:4` and so on.

The magic of it is the fact that we can change this information and update it in the user view without much trouble. 

We could theoretically build a function that detects changes in the wheels number and when it's less than 4, we could change `this.state.working` to `false`. However we'd have to do it through a function named `setState` so the code will look like this:

`this.setState({working:false})`

Here is an example of how the Car's color will be changed through setState, using an event listener bound to a button:

![car component changes state](https://i.imgur.com/HPkYUeU.png)
> Reference: https://www.w3schools.com/


I hope that this bite-sized article made you curious about what's going on in some simple React code. 

For more information please check the https://reactjs.org/ and really work your way through it. Study properly, don't just copy the code and you'll find yourself progressing way faster than coding along from udemy or youtube. 

All the best!








