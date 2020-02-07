---
layout: post
title:      "My CLI Weather APP in Ruby"
date:       2020-02-06 21:03:22 -0500
permalink:  my_cli_weather_app_in_ruby
---

So here I am, a couple of months in the bootcamp and done with my first project. Yay! 
Let's get to the point!

In this APP I've been using an API called [Weatherbit](https://www.weatherbit.io/api) and object oriented Ruby.

In big lines, an API is a database containing specific information - in this case, weather information; that is shared for free (or for money) by its creator.

In order to work with an API, you need a key that is unique to you; usually you get that upon registration on their website but there are also a lot of free public APIs that don't require a key. Once you get the key, it's time to make an API call so we can get some information going. 

A call for my app is done through nice gem called [HTTParty](https://rubygems.org/gems/httparty/versions/0.13.7) and it includes details like the city name, the country name and the units of measurment.

These details are submitted by the user, which is prompted to do so through `puts` questions that capture their answers with `gets` methods.
Once this process is complete, the answers are stored in a hash used to instantiate a new API class through the `get_weather` method.

The information received from the API is a hash that is processed upon the initialization using the `.send` method on it that allows the program to set methods for accessing the particular data (temperature, wind, etc).
In this particular case, I have looked in the API hash response to pick the names for my attr_accessors as they have to match with the key names.

So basically the attr_accessors make sure that the `.send` methods can write the key-value information over them and later on, making it available for reading and using along the app.

The control flow has a key role in verifying the validity of the user input.
In the `options` method the app asks the user what would they like to find out: Temperature, wind speed or if there is a weather alert going on by typing out commands like `temp`, `wind`, `alert` or `exit` if they wish to abort the whole process and exit the app.

The app doesn't like to have any errors so if the user types in something else rather than the accepted inputs, it will display an error message `INVALID INPUT` and will run the `options` method,  prompting them again for one of the correct commands.

This is done through an if statment that verifies the input and if any of the input is correct, the program will execute the appropriate method (e.g.`get_temperature` for temp) and will re-execute the `options` method so that the user would be able to find more information.
 
After tying everything together in the environment.rb file, I can run my app from the bin/run executable.

Simple and clean! 



