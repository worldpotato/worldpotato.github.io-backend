---
title: "First Heroku App"
date: 2020-02-01T09:57:42+01:00
draft: false
tags: ["development", "heroku", "django", "python", "hello world"]
---

Yesterday was a day full of procrastination.
I should learned Machine Learning but instead I created a Heroku app.
Actually it's just a Hello World site, but I's hones work.

Since I want to learn python I use python as programming language and Django as framework.
Mostly because Django is part of the "Heroku with python" tutorial.
Actually the tutorial was no problem.
The test page works great.
But I don't want to start my app from scratch and not with all the unknown things from the tutorial application and I want to host the source on [Github](https://github.com/worldpotato/shiftpotato)

So after creating the Github repository, the development and deploy branch I created my first Django site.
Committed the new files and just before I pushed it I recognised a "SECURE_KEY" in the settings file.
I felt like "I should not push that in a public repository".
So I used an environment variable to set it.
Append the changes to the former commit and it's done.

Nope. You also need to create a app.
But that's also covered by the Django tutorial.
Committing, pushing and merging the feature branch, and finally merging it to the protected deploy branch is done by some commands and clicks.
It's time to configure the Heroku app.

I created an app in the web interface, added a buildpack and connected Github to the app.
So everything should work fine, right?
Nope!
Sure, I forgot to set the environment variable at Heroku.
A quick [duckduckgo](duck.com) search brought me the correct command to add it.
So now!
`App not compatible with buildpack` Dough!
OK, I forgot something, but what?
Again a [duckduckgo](duck.com) search helped.
There must be a `Procfile` and `requirements.txt` file.
So creating them, committing, merging and wait for the deploy just take some minutes.

And look! My first Heroku app runs! You can see it under [shiftpotato.herokuapp.com](shiftpotato.herokuapp.com).

Like you may think. I want to build a open source shiftplaner. Mostly for the treetopadventure park where I work from time to time.

I'll work on it in the next weeks. Maybe we can actually use it.

