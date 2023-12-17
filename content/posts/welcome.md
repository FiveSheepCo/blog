---
title: "Welcome"
date: 2022-03-01T22:59:30+01:00
draft: false
---

# Welcome to our blog!
We are FiveSheep (formerly known as Quintschaf), a small software engineering company based in Estonia.

## History
In 2020, shortly after the Covid pandemic started manifesting, we (Jann and Marco) founded our company: Quintschaf GbR.
This was a first for both of us, there were many things to figure out &mdash; for example how to get a business bank account &mdash; and finding a way to efficiently work together over a medium-large distance across Germany. Things weren't easy at the beginning, none of us knew how to manage multiple projects while keeping track of an always growing list of ToDos and still being able to ship well-rounded releases with a minimal amount of bugs. I'm happy to say that we've figured all of these things out and business is going better day by day.

### Our first app - NineList
The first app we released was a "smart" shopping list, called __9List__ (later renamed to NineList). We worked hard on this project and we believed that this app would be incredibly helpful to many people, especially during the pandemic. The app essentially used location-based notification triggers to show shopping list items on the lock-screen upon entering a supermarket.

People didn't have to remove their masks to unlock their phones and we saw this as a big opportunity, especially because it took Apple a long time to release their more mask-friendly iOS updates including the "Unlock using Apple Watch" functionality.

Sadly, the app flopped. We couldn't get any real visibility on the AppStore and we didn't have funds for marketing, so we gave up and and went back to the drafting board. A few years later we did release a few more quality of life updates, but the app never really took off. Anyway, we learned a lot from this experience and it was a great way to get started.

### Our biggest hit - MyKeyboard
Jann had been working on a Keyboard for iOS, called __OpenKeyboard__. It was a very interesting project &mdash; a fully customizable keyboard. Jann had been maintaining it in his free-time, it was a pretty technical app and the user base consisted mostly of tech-savvy people who knew their way around complex software. After talking about it for a few days we decided to migrate the project to Quintschaf.

We rewrote the app from scratch, added many more features and crafted a new user interface to make the app easy to use for the average person. We rebranded to __MyKeyboard__, published it on the AppStore and the sales started coming in. I wouldn't say that the app is a huge commercial success, but we have a very loyal and steadily growing user base. We're getting feedback and feature suggestions almost daily and our users are very happy with the app, which really makes us feel that our continued effort of improving the app is worth every single minute.

In the beginning we were focusing on iPhone only, with little consideration for iPad users. An analysis of the usage data provided by Apple showed that almost nobody was using the app on iPad anyway, so we spent our time on improving the experience on iPhone only. After a bit more than a year, this suddenly changed. We saw an influx of new iPad users and an increasing number of people contacted us directly to ask about (better) iPad support. Up to this point, the user interface was almost unusable on iPad, keyboard dimensions were weird and the whole experience just wasn't great.

So we sat down and started working on MyKeyboard 3. Two months and 100+ commits later, we shipped it. iPad support is great now, dimensions look and feel right, we introduced swipe-down support on keys to switch between alternate versions (like `2` and `@`) on the same key (similarly to the builtin iPad keyboard), and we made this feature available on iPhone too, because why not! We reworked the keyboard editor to be even more intuitive, added builtin support for more languages (Korean, Arabic, Chinese, ...), added both a split-screen and one-handed mode and fixed many bugs that accumulated over time.

Later, we even built and shipped our own auto-correct engine, because the builtin one was just not good enough, and we've gotten a lot of positive feedback about this change. Auto-correct is now much more reliable and although there are still a few issues, we're generally very happy with the results.

This whole experience has been amazing and we're looking forward to further improving MyKeyboard.

### Harder, better, faster, stronger
We had been working on MyKeyboard for a while now and we had learned a lot about software architecture, SwiftUI, and the AppStore. It was time to branch out some more, and so we started working on Chatalyzer, an analysis tool for WhatsApp, iMessage and Tinder chats. We released it in 2022, and by 2023 it had become our second biggest hit. We were clearly getting better at this, and things were slowly picking up speed.

### The year of prototypes
2023 rolled around and we had many ideas that we wanted to try out. We started moving fast and built many prototypes to see what would be worth pursuing. I think we scrapped at least 5 projects that year that never saw any public release, but a few of the prototypes stuck around. We built quite a few open source libraries, such as [MapItemPicker](https://github.com/FiveSheepCo/MapItemPicker), [Inspect](https://github.com/FiveSheepCo/SwiftUI-Inspect), [ChatView](https://github.com/FiveSheepCo/QSChatView), [SwiftUIElements](https://github.com/FiveSheepCo/SwiftUIElements) and [FoundationPlus](https://github.com/FiveSheepCo/FoundationPlus). Interestingly, we didn't release a single app that year, but we're working on a few that will be released early 2024.

## What's next?
We've got a few new ideas and prototypes up our sleeves that are almost ready for prime-time. Until then, we've got a few more blog posts in the works that might be interesting to Swift/SwiftUI developers and people interested in the field of software architecture.

See you soon!