---
layout: post
title: Blocipedia
thumbnail-path: "img/blocipedia.png"
short-description: Build a production quality SaaS app that allows users to create their own wikis.

---

{:.center}
![]({{ site.baseurl }}/img/blocipedia.png)

[Github](http://github.com/iamkevinlowe/blocipedia)

[Visit](http://iamkevinlowe-blocipedia.herokuapp.com)

## Explanation

Building a replica of something we all know is a great way to understand what happens behind what the user sees on their screen.  Blocipedia allows users to create their own wikis.

## Problem

Make a web application for collaborative modification of content.  Although each wiki is created by a user, other users can add to or change the content.  Incorporate a payment system to allow users to upgrade their account for premium features.

## Solution

Blocipeda begins with a backbone similar to previous Rails projects that I've built.  The idea of making a particular wiki private was the most challenging.  In order to do this, the user must have an upgraded account.  [Stripe](https://stripe.com/) is implemented to receive payment to upgrade a users account.  Private wikis would then be viewable and modifiable to only those who are added as contributors.  If the creator downgrades to a standard account, their private wikis will then be changed to public.

## Results

Getting a deep understanding of the association between models really helped building Blocipedia.  Private wikis relied on collaborators to associate users to wikis.  This application made building my [Capstone Project](http://iamkevinlowe.github.io/projects/photochamp) possible.

## Conclusion

Unique applications are often built from first understanding how existing applications work.  Then by taking apart those elements and combining them with something new, the possibilities can be limitless.