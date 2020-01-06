---
layout: post
title:  "How we ended up with 4 wheels"
date:   2020-01-06 19:26:00 +0100
categories: details chassis
---

With Christmas and the New Year out the way (Happy 2020!), our team is back and ready to progress with our entry! As you can imagine we didn't make much progress over the break, so rather than post a very light update (and to give Fred a rest), I though I would step in and share the story of how we arrived at our proposed PiWars robot.

When we submitted our application back at the end of September 2019, our proposal was for a 4 mecanum-style wheeled robot. You may be interested to hear this wasn't our first idea. In fact we had quite lengthy discussions online about different chassis ideas, including trikes and tanks. One particularly promising option that stayed with us for a while was that of a 6-wheeled chassis with independent feedback-driven control for each axle. Below you can see our first concept design.

![First robot concept]({{ site.url }}/assets/200106_6wheelconcept.png){: style="height: 14em;"}
{: style="text-align: center;"}

In theory this style of chassis would have given our robot the widest range of locomotion options possible, by swapping what was attached to it for each challenge. For example, it could've had regular wheels or tracks for speed challenges, mecanums for navigation challenges, or whegs for rough terrain challenges. For those who've never heard of them, Whegs or wheel-legs are wheels that are only in contact with the ground for part of their rotation, with the rest of the rotation allowing them to clear obstacles like legs can. The particular style we were interested in was that of the [Boston Dynamics RHex](https://www.youtube.com/watch?v=ISznqY3kESI), but there are more spoke-like styles such as what Fred comically tried on one of his [ant-weight robots](https://twitter.com/i/status/1197996851632463872).

Speaking of legs, we, well I, even talked about using the axles as the first joints of fully articulated spider legs as a "stretch goal", seeing as I was preparing a [PiWars Mini Conference](https://piwarsmc.org/) talk about walking robots at the time. I even simulated it in my [Walker Simulator](https://github.com/ZodiusInfuser/TrueWalkSimulator).

<video height="640" width="360" style="margin-left: auto; margin-right: auto; width: 320px; height: 180px; display: block; border: solid 1px white; margin-top: 5px; margin-bottom: 5px" controls>
  <source type="video/mp4" src="{{ site.baseurl }}/assets/200106_walker.mp4">
  <source type="video/webm" src="{{ site.baseurl }}/assets/200106_walker.webm">
  <source type="video/ogg" src="{{ site.baseurl }}/assets/200106_walker.ogv">
</video>

Needless to say, the "stretch goal" was quickly shot down as it introduced a lot of complexity and restrictions on the size and weight of our robot without providing much benefit beyond its cool factor. We also began questioning how valuable the RHex-style whegs would be, as they were the only movement capability remaining that required our robot to have 6 axles. Around this time, challenge details were coming through from the PiWars organisers, and unlike 2019 that had a rough terrain challenge in the form of "Spirit of Curiousity", no such dedicated challenge exists for 2020. Therefore our team agreed to drop wheg support, leading us to settle on the regular 4-axled arrangement.

Going for 4 axles still left us with a choice of what to mount on them though. This is where Harry's previous experience of competing in PiWars with his KEITH robots became hugely valuable! He told us that "getting tracks right is a fair challenge in itself", so recommended we go for "something as close to holonomic as possible" instead. Holonomic for ground robots essentially means that for each of the movements possible by a robot in two-dimensions e.g. drive, strafe, rotate, it needs at least that many independently controllable wheels. Mecanum wheels were the obvious choice for this, as they allow for this movement in any direction whilst having the axles be arranged like a car, giving us the option to switch to regular wheels or tracks should we need to. Also, mecanum robots have seen success at previous year's competitions so we knew from a hardware standpoint that they were capable. I personally watched PiDER 3.0 tackle several of the 2019 courses when I visited as a spectator, and know that Tigerbot and X-Bot did well the year before.

![PiDER 3.0 at PiWars 2019]({{ site.url }}/assets/200106_pider2019.png){: style="height: 14em;"}
{: style="text-align: center;"}

There's the story of how we ended up with our robot proposal for PiWars 2020. There is more I can cover about our exploration of mecanum wheels and their control, but I'll leave that for another week.