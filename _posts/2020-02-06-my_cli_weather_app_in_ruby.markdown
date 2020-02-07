---
layout: post
title:      "My CLI Weather APP in Ruby"
date:       2020-02-07 02:03:21 +0000
permalink:  my_cli_weather_app_in_ruby
---

So here I am, a couple of months in the bootcamp and done with my first project. Yay! 
Let's get to the point!

In this APP I've been using an API called [Weatherbit](https://www.weatherbit.io/api) and object oriented Ruby.

In big lines, an API is a database containing specific information - in this case, weather information; that is shared for free (or for money) by its creator.

In order to work with an API, you need a key that is unique to you; usually you get that upon registration on their website but there are also a lot of free public APIs that don't require a key. Once you get the key, it's time to make an API call so we can get some information going. 

A call for my app is done through nice gem called [HTTParty](https://rubygems.org/gems/httparty/versions/0.13.7) and it includes details like the city name, the country name and the units of measurment. 

The information received is a hash that is processed upon the initialization using attr_accessors (setter and getter methods).

These methods are used in the controller which is responsible for "puts"-ing out the information that the user requests such as the temperature, the wind speed or any weather alerts going on.

After tying everything together in the environment.rb file, I can run my app from the bin/run executable.

Simple and clean! 



