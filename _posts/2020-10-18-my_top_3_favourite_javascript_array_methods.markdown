---
layout: post
title:      "My Top 3 Favourite JavaScript Array Methods"
date:       2020-10-18 06:45:28 -0400
permalink:  my_top_3_favourite_javascript_array_methods
---



In this tutorial I will be working in the **Google Chrome dev tools** console, so feel free to follow along.


![](https://i.imgur.com/j3GVn2O.png)



We will create an array of strings and we will go through each of those methods to see what they are used for in an array.

`let myTutorials = ['Python','JavaScript','Ruby']`

![](https://i.imgur.com/YgF6e8y.png)

### Starting with .forEach()

For each calls a function for each element of the array, in order so basically it loops over the array, and I mostly use `.forEach()` when I want to render something in the dom.

`myTutorials.forEach(tutorial => document.write(`I love ${tutorial}. `))`

![](https://i.imgur.com/hfCWAzB.png)

> Please be careful when you're working with objects, as forEach is an **array method**, and if you try to use it it will throw the following error

![](https://i.imgur.com/c9UFgKH.png)


### The next array method is called .filter() 

Filter it will create an array with the items that pass a certain condition which is provided as a function.

Let's create an array of numbers: `let arrayOfNumbers = [2, 53, 3, 81, 31, 5, 12, 66, 199, 34, 81, 19]`

In the following image you can see how the filter method is easy to apply when you know what you want to filter, in this case, I want to filter out numbers that are higher than 50

![](https://i.imgur.com/JT3XcXD.png)

### And last but not least, your soon-to-be best friend, .map() .

> Map will execute a function over all the elements it loops through, and create a new array of them. 

> Map will not change the initial array and we're calling this a non-destructive behaviour. 

Let's say I want to change something on every element of my previously initialized tutorials array

`let myTutorials = ['Python','JavaScript','Ruby']`

You can see here how I changed each element individually

![](https://i.imgur.com/WznO5af.png)

And here, I could even introduce a conditional statement to display my love for a certain language.

![](https://i.imgur.com/UpffdI0.png)


This bite-sized article is meant to quickly show you how you could use those 3 methods. I hope you enjoyed it and fount it useful.







