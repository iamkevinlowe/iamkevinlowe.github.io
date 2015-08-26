---
layout: post
title: Heroku vs Digital Ocean with Capistrano
---

As an introduction to getting an app up and running on the web, Heroku and its toolbelt makes it easy.  It was simple to set up by signing up for a **free** [Heroku Account](https://signup.heroku.com/identity), downloading the [Heroku Toolbelt](https://toolbelt.heroku.com) and entering your credentials by running the command `heroku login`.  After that, running `heroku create <app name>` creates a new application in Heroku.  To deploy to Heroku, all there is to it is the command `git push heroku master`.

[Heroku](https://heroku.com) has a graphic interface showing each app and their settings, tools, and add-ons.  It certainly makes it easy for a beginner.  For the advanced user who needs more control and customizability, with the help of my [Bloc](https://bloc.io) mentor we set up a [Digital Ocean](https://www.digitalocean.com) cloud server and deployed [PhotoChamp](http://104.131.155.142) using [Capistrano](http://capistranorb.com).

*By no means am I experienced enough to make a proper comparison.  This is from my point of view as a student.*

Getting this set up took more effort but by doing so, I learned a lot about the world of DevOps.  Ever heard of learning from your mistakes?  Well, add in some Google and StackOverflow and that sums up the process of hosting an app on [Digital Ocean](https://www.digitalocean.com), not to discourage anyone.  The first step of creating a "Droplet", a Digital Ocean cloud server, really shows how much granular control you have by allowing you to choose one of six operating systems to run.  Digital Ocean's support center has a lot of helpful tutorials to get things working.  After finishing, adding the [Capistrano](http://capistranorb.com) gem to your app and configuring the deploy settings allows it to push the app to your Digital Ocean droplet.  After a lot of trial and error (and destroying everything and starting over), you get things right.  Calling `cap production deploy` will push your app to your droplet and gets the server running.  Since hosting on Digital Ocean isn't free and their servers run on SSD storage, the performance is blazing fast.

To get started with $10 in your account, you can sign up with my [referral link](https://www.digitalocean.com/?refcode=d61dd007c7b7).

Although [Digital Ocean](https://www.digitalociean.com) required a lot more work, the whole process showed me how much flexibility and control you really have.  The most amount of time actually only went into configuration.  You're behind the wheel and you get to take the car anywhere you want- you just need to learn to drive first.  The struggles of getting one part right and inching forward before having to fix another error made finally succeeding feel a whole lot sweeter.