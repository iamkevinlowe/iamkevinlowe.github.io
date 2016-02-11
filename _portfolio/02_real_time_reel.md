---
layout: post
title: Real Time Reel
thumbnail-path: "img/real_time_reel.png"
short-description: Create a slideshow from an Instagram hashtag.

---

{:.center}
![]({{ site.baseurl }}/img/real_time_reel.png)

[Github](http://github.com/iamkevinlowe/real_time_reel)

[Visit](http://real-time-reel.herokuapp.com)

## Explanation

A simple to use Instagram slideshow creator that auto updates as images are being shared on Instagram.

## Problem

The idea for this came from the question, "How can I make weddings more fun?".  Nowadays, most people document everything on social media.  Instagram is a great application for users to capture and share moments.  At weddings, phones are almost always out capturing the Groom as he patiently waits for his love, the Bride as she walks down the aisle, their first kiss, and all the other special moments.  Most of the time, there's too much going on for people to stop what they're doing and flip through what's posted on Instagram.

## Solution

Real Time Reel, literally creates a real-time slideshow of hash-tagged images.  It connects to Instagram's API to retrieve the most recent photos and queues them up in line.  As a new photo gets shared, RTR gets the data as soon as it's uploaded to Instagram and queues the photo to display next in line.  This makes it fun for guests at events to participate and see their photos displayed, and in return more memories are created.

## Results

I've yet to use this in a large-scale event, but those who've used it say it's a great application that works!

## Conclusion

Building RTR was great, mainly because of the tools I learned to create the real-time aspect of it.  I used [Socket.io](http://socket.io/), a websocket service, to create a subscription to an Instagram hashtag and listen for updates from their server.  Each ping from their server will have RTR retrieve the new data and inserts it in the queue.

By developing with websockets, I'm able to see a huge opportunity in its potential to build future applications.