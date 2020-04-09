---
layout: post
title:      "Fridgeroo, a Sinatra MVC app."
date:       2020-04-09 10:02:52 +0000
permalink:  fridgeroo_a_sinatra_mvc_app
---



Welcome to my first MVC app, Fridgeroo, that is a fridge which keeps track of your items and their expiration date.

***Model*** - the one who is responsible with all the processes and the relationships between the objects
***View*** - the one that shows you the result
***Controller*** - the one who makes the model-view communication possible

My app has 3 models, all interconnected to each other. They are engaged in model relationships :D Luckily, in programming there's rarely any relationship drama...

**My 3 models**

* Fridge
* Item
* User

Using relationship associations like `has_many`, "`has_many, through`" and "`belongs_to`" I succesfully connected everything together. The idea behind this way of building associations is that it will be easier for you to find a user based on an item, an item based on a fridge and so on, using automatically generated IDs. 
Instead of writing methods for my models, which can be fun but can easily get overwhelming and tedious, I used ActiveRecord which facilitates the creation and use of objects, and it also helps with performing database operations.

**Controllers**

Imagine a console controller(Playstation 4 for example), that you use to tell the console how to display things on the screen. Well my controllers do a similar job having the application controller setting some basic rules like in which folder to find my views, to enable sessions - those are used to keep track on which user is currently logged in and to secure the session.

The fridge controller is mostly responsible with creating a new fridge and its attributes, creating, editing items and deleting them, adding expiry dates and it works simultaneously with the User, Item and Fridge models.

The users controller is mostly responsible with creating a user, logging them in and deleting them if needed. I used some helper methods to make the code more readable and my life easier and with those helper methods (that receive an arument of the current session), I can check if a user is logged in `Helpers.is_logged_in?(session)` or to target the current user `Helpers.current_user(session)`


**Views**

Here you'll find a few more files. The views in my project use the data pulled from the models through controllers in order to display it.
The .erb extension allows me to use ruby and html in the same file so if I need to loop over the list of users and display them, I can do that with an each loop or something similar, applied to the collection of users and capture the username or other details I need to display.


This is in big lines my first MVC application and I'd like to invite you to check the code [here](http://https://github.com/Swishyfishie/sinatra_test) or watch the video here!

