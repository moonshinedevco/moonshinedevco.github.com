---
layout: post
title: "YelpRoulette.com: Stop Arguing, Get Fed"
date: 2012-10-31 12:43
categories: [moonshinedevco, projects]
---
We all know the [drawbacks of having too many choices](http://www.amazon.com/The-Paradox-Choice-More-Less/dp/0060005696/).  One perfect example of group indecision brought about by the paradox of choice is the eternal question of what's for lunch.  I don't know, what do you want.  I don't know, what do you feel like.  I could eat anything.  Me too.  Where should we go?  I don't know - do you have any preference?  No, do you?  Blah blah blah and so on.

Larry Wall says this about the first great virtue of a programmer in [the Camel book](http://shop.oreilly.com/product/9780937175644.do):

<blockquote>
Laziness: The quality that makes you go to great effort to reduce overall energy expenditure. It makes you write labor-saving programs that other people will find useful, and document what you wrote so you don't have to answer so many questions about it. Hence, the first great virtue of a programmer.
</blockquote>

Naturally, this means that a program should be created to solve the eternal question once and for all.  We've called it [YelpRoulette.com](http://yelproulette.com).

At first, I tried to use the Yelp API, but when I requested access to more than 1K hits/day they sent me this:

<blockquote>
Hi Brian,<br />
Thanks for your interest, but this is a use case that we can't support. We're typically interested in use cases that are more complementary to than extensions or replications of the Yelp experience. We also ask that API partners refrain from using names that are confusingly similar to Yelp, such as yelproulette.com. Please refer to the Terms of Use and Display Requirements for more info.
<br /><br />
Regards,<br />
Nick<br />
Yelp Partner Relations
</blockquote>

There are so many things wrong with this (least of which is the implication that Yelp Roulette somehow replicates existing functionality) - but rather than fight it I figured I could just find a way around using the Yelp API.

Enter [the Google Places JavaScript API](https://developers.google.com/maps/documentation/javascript/places).  I can search for restaurants via JavaScript, randomly select a result, and then send the user along to the Yelp page.  The only last hurdle was trying to figure out what the Yelp page is going to be for a given establishment.  Thankfully, Google has already figured that out by crawling their entire site, so all I have to do is send a user to Google's "I'm Feeling Lucky" page with a specially crafted query, and the user is automagically sent along to the right page on Yelp.  Magic!  And I didn't even have to use the Yelp API.

So here's the one remaining question: Will Yelp thank me for the traffic or send me a take down notice?