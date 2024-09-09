---
layout: page
title: Pasta Fever
description: Click here to learn more!
img: assets/img/PastaMakerAppIcon.png
importance: 2
category: Twenty Games
justified: true
---

<div>
    <img src="{{ '/assets/img/PastaMakerAppIcon.png' | relative_url }}" alt="Pasta Fever Icon" style="float: left; width: 30%; margin-right: 20px; border-radius: 8px;">
    <p>
        <a href="https://apps.apple.com/us/app/pasta-fever/id1642532274" target="_blank"><strong>Click Here To Download</strong></a><br><br>
        Pasta Fever's game idea came from our game designer when I was working as a product owner. He showed me a video of a real pasta machine and asked if we could gamify it. The decision was instant.<br><br>
        Initial test results were like a dream: $0.20 CPI, >50% D1 Ret, 40+ min PT. Yet, hyper-casual idle clicker games lacked a key component that generates profit: D7 Retention. We worked hard with Rollic and within ourselves to find solutions to overcome this obstacle. We implemented daily missions, daily rewards, new items, new levels, etc. Unfortunately, in the end, Pasta Fever couldn't make a global hit, only reaching 500k+ downloads. However, it created a vacuum in the hyper-casual scene and made a lot of studios follow its lead. 
    </p>
</div>

<div style="clear: both;"></div>

**Some interesting stuff about game economy in idle games**

If you've ever encountered an idle game, either by playing or developing, you'll notice the currency inflation happens pretty fast. This situation leads to dealing with enormously large numbers which neither 32-bit Int nor 64-bit Double can handle. In order to solve this problem, there exists a concept called [Double-precision floating-point format](https://en.wikipedia.org/wiki/Double-precision_floating-point_format). I have integrated famous [BreakInfinity's C# port](https://github.com/Razenpok/BreakInfinity.cs) in our game Pasta Fever, which uses this concept at its core. 

Moreover, to keep users engaged over long periods, idle games start off easy, where you can buy upgrades quickly and progress fast. But as time goes on, the time between each upgrade drastically increases, forcing us to "prestige" to multiply their production rate. This concept is brilliantly explained by Anthony Pecorella in his [blog in Kongregate](https://blog.kongregate.com/the-math-of-idle-games-part-i/). He summarizes it as, "_At the most basic level, idle games are a seesaw between production rates and costs. Early on in a run, your production will exceed costs while eventually costs will become prohibitive. This is typically accomplished by having costs grow exponentially while production grows at a linear or polynomial rate._"

I followed a similar pattern in Pasta Fever's economy, where income increases linearly with some jumps, while costs increase exponentially. Progression resets (prestige) occur between levels. [Here you can view](https://docs.google.com/spreadsheets/d/16ECoMlERrznnzbfsfYxkAdYJEFKa5tcz/edit?usp=drive_link&ouid=113882831359149382032&rtpof=true&sd=true) the file we prepared in Excel, where we try to estimate the total seconds between levels given the current costs of upgrades and income sources. _(Note: Region settings should be in English(U.S.))_

**Here is the most watched CPI video**

<iframe width="315" height="560"
src="https://youtube.com/embed/Xr-7v0vsAQo?si=13Mx8C4q4bwsKfGY"
title="YouTube video player" frameborder="0"
allow="accelerometer; autoplay; clipboard-write; encrypted-media;
gyroscope; picture-in-picture;
web-share"
allowfullscreen></iframe>