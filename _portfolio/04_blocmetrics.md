---
layout: post
title: Blocmetrics
thumbnail-path: "img/blocmetrics.png"
short-description: BlocMetrics is an analytics service and reporting tool that you can use with web apps to track user activity and report results.

---

{:.center}
![]({{ site.baseurl }}/img/blocmetrics.png)

[Github](http://github.com/iamkevinlowe/blocmetrics)

[Visit](http://iamkevinlowe-blocmetrics.herokuapp.com)

## Explanation

In this application I explored creating an API controller and some JavaScript for BlocMetrics to capture client-side events and display them for analytical purposes.

## Problem

The models in previous projects all lived and interacted within the application.  What's unique about BlocMetrics, I set up an API controller to listen for calls from an external JavaScript function.  Many of the other functionalities were introduced in previous projects.

## Solution

To receive information, the `API::EventsController` would listen for calls from the client-side JavaScript function.  If the url from the request matches that of a `RegisteredApplication`, it'll create a new `Event` and associate it to the `RegisteredApplication`.

On the client-side web application, a JavaScript function gets called wherever a user wants tracking.  A string is passed in as an event name and a HTTP Request gets made to BlocMetrics where the `API::EventsController` receives the incoming event.

When the user accesses the BlocMetrics application and signs in, they'll see a list of their registered applications.  Opening the link will show a pie chart comparing all the events and their relative frequencies as well as a line graph that represents activity over time.

## Results

Although this application was relatively simple in that it doesn't have a lot of models or views, the usefulness is quite large when you use it with an external web application to automate tracking of events.  The hardest part was making sure the JavaScript funtion was passing the correct information to the right place, and having the controller understand and parse the data.

#Conclusion

The fascinating part of this is being able to listen for incoming calls from an external source.  Linking this to work with a web application doesn't require a lot.  It's literally copying a JavaScript function to an application and calling it wherever you want an event tracked.

Because of the elegance in its simplicity, I've used BlocMetrics as an analytics tool for some of the other applications that I've built.