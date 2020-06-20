---
layout: post
title:      "A mediocre way of building a Ruby on Rails app"
date:       2020-06-20 01:02:04 +0000
permalink:  a_mediocre_way_of_building_a_ruby_on_rails_app
---

 Life's too short to be feel pressured that you have to be exceptional, so let's dive into a realistic way of how an average person builds a Ruby on Rails project.


### Any prior knowledge?
This being my third project at Flatiron School, it's quite safe to say that I have at least some basic Ruby knowledge. My Sinatra project (the previous one) helped me understand better the RESTful conventions and how a MVC app works. Apart from this, I knew some HTML and CSS. 
Out of the last two, I'd recommend focusing on HTML more than CSS. While you may not be focused on the design when writing a backend of an app, you still have to visualise it somehow. It doesn't have to be pretty(CSS), but it has to have a visual output of some sort but we'll talk about how Rails handles the visual("views") part in a moment.

TLDR: Ruby, HTML and CSS

### Where did I started from?

https://guides.rubyonrails.org/getting_started.html

I started there. 

That rails guide has a nice way of holding your hand (up to a point :D ) and showing you what the conventions are.

After I've set up my project with `rails new projectname` I started drawing up my associations. 

What are those? Well...good question. 

They're basically the relationships between your models.

What are the models?

### Models

Oh...ummm....the models are Ruby classes. They talk with the database, validate data, connect with other classess (e.g. the `Person` class connecting with `Book` class in an app that wants to track a person's books).

### Relationships

So back to the relationships. That `Person` class needs to connect with the `Book` class (notice that the models are named with a singular form regardless if we have one or more of that class's instance). A person can have more than one books, but a book can only belong to a person at one time. 

What if the `Person` joins a book club? They'd have a `Meeting` and this meeting would have many `Person`s and the `Person` could have many `Meeting`s as they'd RSVP to more than one.

These are the relationships you're looking at when thinking how your app will function. 

https://guides.rubyonrails.org/association_basics.html this is the thing to go at when you're planning it. 

### Migrations

I like to write my migrations. 

You can use generators to write them, but I like to get my hands dirty.

The migrations are a feature of Rails' Active Record that helps you keep your database structure flexible and updated to your needs.

![A migration looks like this](https://i.imgur.com/XGXlFrE.png)

This is how a migraton looks like. It creates a table in your database that is named like the plural of your model (`:books`) and please notice the `person_id` field that will connect the book to the person.

### Controllers 

Oooh boy. Here's where the magic happens. 

In a decent app that has authentication forms, displays some information and allows the user(read) also to create, update and destroy you need to know a few things.

![Controller](https://i.imgur.com/rJWen72.png)

Here's how a controller looks like. Oh and it needs to also be the plural of your model (Books). 

So quick recap on what the "defs" are doing: 

1. new - Shows the form to create a new instance of your model
2. index - Shows all instances of your model
3. create - Creates new instance from new form
4. show - Shows an individual instance of your model
5. edit - Shows the form to edit a specific instance
6. update - Actually edits the specific instance
7. destroy - I'll let you guess this one. 

Basically knowing these will help you figure out what you're supposed to write in the controllers. But don't beat yourself too hard if you don't get it the first time. Or the 100th time. It's fine. I'm still trying to figure out the best way to write logic and I always have this opened in a nearby tab https://guides.rubyonrails.org/action_controller_overview.html

### The views

Ok so remember when I said that it's important to know some HTML?

Ruby uses its own tool to pull information from the controller (that pulls it out from the database) and display it to you. 
It's called ERB and it stands for Embedded Ruby, which is basically a HTML file that knows how to read Ruby code if you write it in this syntax `<%= %> or <% %>`.



### Result

You can see my result here and what I'm talking about.

* Here's the video: 

* And here's the repository: https://github.com/Swishyfishie/Tellcode


If you read until here, you might have noticed that this is not your standard "how to- technical article". And my mission was not to teach you something that other people managed to do it brilliantly in the guides I posted above. 

I have also not included a lot of steps that were mandatory (e.g how to build a form and connect it to your object instances) and this is because I wanted to show you how I, an average person, starts building a project. It has a lot of flaws and this is the normal process. 

The key aspect here is to ask questions like "How do I even send information to the database?".

It's the process of answering questions that will build your project, and in time, those questions will be answered in the planning phase. 



 
