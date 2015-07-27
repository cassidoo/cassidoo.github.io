---
layout: post
title: "Making the Whitney Houston API."
date: 2015-07-26 10:30:00
summary: I made a Whitney Houston API. Because why not.
categories: technical
---

I'm a Whitney Houston fan.  Anyone who's known me for more than a [moment in time](https://www.youtube.com/watch?v=c84ogrNEds0) would know that (see, making references already, agh I'm so funny).

Anyway, I took a nap the other day and I dreamt that I made a Whitney Houston API.  So obviously I had to make one.

But, I had never made an API before.  [I had nothing](https://www.youtube.com/watch?v=FxYw0XPEoKE).  But I had to try.

First, I had to get all of the songs she ever recorded.  Wikipedia came to save the day.  I scraped [the article of all of her songs](https://en.wikipedia.org/wiki/List_of_songs_recorded_by_Whitney_Houston) with a Python script, and then got to work on parsing it.  Let me tell you, it was not fun.  The HTML in Wikipedia tables is a pain in the BUTT to deal with.  Sure, I *could* do it, but I wouldn't wish that mess on anyone.  So, I said to myself, [it's not right, but it's okay](https://www.youtube.com/watch?v=6J538b-OLRU), I'll get through this.
Once I filtered out a lot of crap (like stripping out the links and the special characters) and broke it down into something readable, it looked more like this:

    "Could I Have This Kiss Forever"
    Whitney Houston and Enrique Iglesias
    Diane Warren
    Whitney: The Greatest Hits and Enrique
    2000
    |-

So, it had the title of the song, the artists who sang (most of these were just Whitney), the writer(s), the albums on which the song appeared, and the year it was released.

