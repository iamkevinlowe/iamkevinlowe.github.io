---
layout: post
title: Blocitoff
thumbnail-path: "img/blocitoff.png"
short-description: Build a self-destructing to-do list application.

---

{:.center}
![]({{ site.baseurl }}/img/blocitoff.png)

## Explanation

The second Rails project taught by Bloc.  This further developed how Rails applications are built.

## Problem

To-Do lists often horde items that potentially become unmanaged and make the list undesirable to use.  Blocitoff will create To-Do items that will expire in 7 days.

## Solution

Users are allowed to complete items in the list and have them removed.  Items that become older than 7 days will be considered no longer important and be automatically removed.  To get this to work, an item must determine the difference between the current time and when the item was created.

## Results

Blocitoff showed how much you could do with only a couple models and controller actions.

## Conclusion

This was easy to create but often times, it's these apps that are intuitive and useful.