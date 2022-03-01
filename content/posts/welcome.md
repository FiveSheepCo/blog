---
title: "Welcome"
date: 2022-03-01T22:59:30+01:00
draft: false
---

# Welcome to our blog!
We are Quintschaf, a small software engineering company from Germany.

## History
In 2020, shortly after the Covid pandemic started manifesting, we (Jann and Marco) founded our company.
This was a first for both of us, there were many things to figure out &mdash; for example how to get a business bank account &mdash; and finding a way to efficiently work together over a medium-large distance across Germany. Things weren't easy at the beginning, none of us knew how to manage multiple projects while keeping track of an always growing list of ToDos and still being able to ship well-rounded releases with a minimal amount of bugs. I'm happy to say that we've figured all of these things out and business is going better day by day.

### 9List
The first app we released was a "smart" shopping list, called __9List__. We worked hard on this project and we believed that this app would be incredibly helpful to many people, especially during the pandemic. The app essentially used location-based notification triggers to show shopping list items on the lock-screen upon entering a supermarket.

People didn't have to remove their masks to unlock their phones and we saw this as a big opportunity, especially because it took Apple a long time to release their more mask-friendly iOS updates including the "Unlock using Apple Watch" functionality.

The app flopped, to this day we've made maybe 5 sales and almost nobody uses it. 9List works well and I personally still use it, but the shopping list space is incredibly saturated. We couldn't get any real visibility on the AppStore and we didn't have funds for marketing, so we let the app die and went back to the drafting board.

### MyKeyboard
Jann had been working on a Keyboard for iOS, called __OpenKeyboard__. It was a very interesting project &mdash; a fully customizable keyboard. Jann had been maintaining it in his free-time, it was a pretty technical app and the user base consisted mostly of tech-savvy people who knew their way around complex software. After talking about it for a few days we decided to migrate the project to Quintschaf.

We rewrote the app from scratch, added many more features and crafted a new user interface to make the app easy to use for the average person. We rebranded to __MyKeyboard__, published it on the AppStore and the sales started coming in. I wouldn't say that the app is a huge commercial success, but we have a very loyal and steadily growing user base. We're getting feedback and feature suggestions almost daily and our users are very happy with the app, which really makes us feel that our continued effort of improving the app is worth every single minute.

In the beginning we were focusing on iPhone only, with little consideration for iPad users. An analysis of the usage data provided by Apple showed that almost nobody was using the app on iPad anyway, so we spent our time on improving the experience on iPhone only. After a bit more than a year, this suddenly changed. We saw an influx of new iPad users and an increasing number of people contacted us directly to ask about (better) iPad support. Up to this point, the user interface was almost unusable on iPad, keyboard dimensions were weird and the whole experience just wasn't great.

So we sat down and started working on MyKeyboard 3. Two months and 100+ commits later, we shipped it. iPad support is great now, dimensions look and feel right, we introduced swipe-down support on keys to switch between alternate versions (like `2` and `@`) on the same key (similarly to the builtin iPad keyboard), and we made this feature available on iPhone too, because why not! We reworked the keyboard editor to be even more intuitive, added builtin support for more languages (Korean, Arabic, Chinese, ...), added both a split-screen and one-handed mode and fixed many bugs that accumulated over time.

This whole experience has been amazing and we're looking forward to further improving MyKeyboard.

## What's next?
While we're committed to further improving MyKeyboard, we also got a few new ideas up our sleeves and one of them is almost ready for prime-time. Once it's ready for the big reveal, you'll hear about it here first! Until then, we've got a few more blog posts in the works that might be interesting to Swift/SwiftUI developers and people interested in the field of software architecture.

See you soon!

{{ template "_internal/disqus.html" . }}