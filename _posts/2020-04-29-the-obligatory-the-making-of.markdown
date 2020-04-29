---
layout: post
title:  "The obligatory The Making Of"
date:   2020-04-29 20:20:00 +0000
categories: updates
---

Hi all! It's the week after Virtual PiWars! I admit I was disappointed events conspired to make postponing PiWars necessary, but I really had fun with Virtual PiWars! I'm so glad everyone managed to come together for it, organising and making videos for it. I had a lot of fun with Virtual PiWars, both seeing everyone's robots and leading up to it. I thought it'd be fun to spread some of the joy I had leading up to the event and share a bit of the behind the scenes of our video entry. Here we go.

Pretty much immediately after Chris shared the event announcement with the team, I was on board with doing a video. Largely because I immediately knew the type of video I wanted to make. Let's take a look at my primary inspiration:

<iframe width="853" height="480" src="https://www.youtube.com/embed/6i-nMWgBUp0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Thanks, Cave, that was lovely. Leading up to the release of Portal 2, Valve Software released [a](https://www.youtube.com/watch?v=0qcED35LL8I) [set](https://www.youtube.com/watch?v=AZMSAzZ76EU) [of](https://www.youtube.com/watch?v=6i-nMWgBUp0) [four](https://www.youtube.com/watch?v=wX9Sc88qreg&t=7s) of these quick, snappy, trailers detailing some of the technology of Aperature Science. At the time I really adored these, I enjoyed how well they flowed and the minimalistic style. Having started playing around with video editing the last year or so, I didn't think to replicate this style was beyond me. This type of video (although a bit more serious) has also been quite common in crowd-funding campaigns. So if we're going to show off our robot, why not try and do it in a fun way that tries to "sell" our robot?

The first half of the script pretty much wrote itself, around the idea of a spinning model of our robot. To the extent that I have typed "Hi, we at ShefBots are here to tell you today about our all-purpose search-and-rescue robot, the ShefBot Mark 1b." off the top of my head. It's not exactly what's in the script, but it's pretty close. When I wrote it out originally, I just carried on from that, listing out the 1b's features in my head, with that sort of calm voice with a bit of extra inflexion. What you'll have heard (or will hear later on in this post) recorded for the video is pretty much how I wrote it originally, said the same way as I heard it in my head.

![The script, pretty much unchanged]({{ site.url }}/assets/200429_script.png){: style="height: 14em;"}
{: style="text-align: center;"}

The second half of the script was a bit harder as to write, as this was to be the section on the real-world demonstrations. *Which I didn't have any footage of at the time I wrote the first half.* I knew vaguely what I wanted to demonstrate - line following and minesweeper - as I had working code for these. The rest our robot's software is kind of half-finished. We had planned to finish the code up in the two or three weeks before the competition in some fun collaborative hackathon sessions, but as the competition was delayed that took a back seat to more pressing matters. I was a bit worried about how I was going to take up an estimated 2 or 3 minutes with only two demos, but I hit upon the idea of explaining in a bit more detail how things worked. Eventually. It took a while to think of, so in the end, I took the day off of work the Friday before the competition to clear as much floor space in my room as possible, film the demonstrations, write the descriptions around them, and finish all of the recording and video editing. Friday was a very long day, but the video was finished in the early morning hours of Saturday.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Welp, done at last. Stay tuned tomorrow (later today) for hearing about our <a href="https://twitter.com/hashtag/ShefBots?src=hash&amp;ref_src=twsrc%5Etfw">#ShefBots</a> robot at Virtual <a href="https://twitter.com/hashtag/PiWars?src=hash&amp;ref_src=twsrc%5Etfw">#PiWars</a>. Thanks for your help <a href="https://twitter.com/ZodiusInfuser?ref_src=twsrc%5Etfw">@ZodiusInfuser</a>, <a href="https://twitter.com/Blayzeing?ref_src=twsrc%5Etfw">@Blayzeing</a>, <a href="https://twitter.com/harrymerckel?ref_src=twsrc%5Etfw">@harrymerckel</a>, <a href="https://twitter.com/morphashark?ref_src=twsrc%5Etfw">@morphashark</a>, <a href="https://twitter.com/RobbieKinghorn?ref_src=twsrc%5Etfw">@RobbieKinghorn</a>, &amp; <a href="https://twitter.com/ShefRoboteers?ref_src=twsrc%5Etfw">@ShefRoboteers</a>. <a href="https://t.co/OrpBFYjF2e">pic.twitter.com/OrpBFYjF2e</a></p>&mdash; Fred (@theguruofthree) <a href="https://twitter.com/theguruofthree/status/1253869198348091397?ref_src=twsrc%5Etfw">April 25, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Why a 3D model instead of real footage of the robot? Basically, while I have the robot at my house at the moment, my hands are not steady and lighting in my room is not good, leading to blurry footage I wouldn't want to watch. If I don't want to watch it, I don't want to force anyone else to watch it either. I also couldn't figure out a way to shoot footage for a good background. But we have a Fusion 360 model of entire robot that looks great! Of course, I was worried about rendering the model as I haven't really been involved with our Fusion 360 model at all and don't know how to use it very well. Harry assured me however he could do (and did do) a spinning render of our model, which to my mind was all we really needed. I could start and stop the spin, speeding up or slowing down the footage to get the transitions we needed.

![Yes, it does spin General]({{ site.url }}/assets/200429_rotate.gif){: style="height: 14em;"}
{: style="text-align: center;"}

Uh oh! Our model wasn't up to date! Several changes had been made by hand that hadn't been reflected in the model. This is largely the reason our video was made the weekend before Virtual PiWars. Everyone was busy! Chris eventually got the time to update the model though, including textures, to make the model look really good. Fantastic job Chris!

![Chris' very nice render]({{ site.url }}/assets/200429_goodrender.png){: style="height: 14em;"}
{: style="text-align: center;"}

It was around the time Chris was working on the model that I remembered seeing [this video](https://www.youtube.com/watch?v=_3loq22TxSc) about programming in PowerPoint. As in, Turing complete programming. But the thing I was really interested in was the second half of this video, where a feature of PowerPoint called the Morph transition is discussed, and how on slide changes it smoothly animates between objects in the slides. And another feature of PowerPoint - to embed 3D models! - is discussed. Could I embed the model of our robot, and animate everything using PowerPoint? The *nix user in me shuddered, but the practical part of me was thinking "gosh, that would save a lot of time". Chris had some problems getting Fusion 360 to export texture information, but eventually through the power of Blender (no surprise there!) got something exported that at least had colour. It all came together perfectly. Here's a test we did, with the model animating in PowerPoint.

![Yes, PowerPoint can render a model]({{ site.url }}/assets/200429_ppttest.gif){: style="height: 14em;"}
{: style="text-align: center;"}

It was also around the time of Chris working on the model that I admit I went off the rails a little bit. I started browsing through the [YouTube Audio Library](https://www.youtube.com/audiolibrary/music) for background music, and searching for "calm" or "tranquil" or some such, and came across the track "Same Time" by Spence. And then things went off the rails for a bit. I questioned everything. Because I discovered our script... also worked as a rap. See below.

<iframe width="849" height="472" src="https://www.youtube.com/embed/O9Tngrmnd08" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

I laughed for a good solid 5 minutes after I recorded this. Sadly, I realised this would be almost impossible to animate to in the time I had left. Also, the rest of the team, while enjoying wasn't quite as enthused at making this our face to the world, so it was off to PowerPoint.

Making the video ended up largely similar to just making a presentation. At least half of my time was making a slide and animating it. The new bit in PowerPoint for me was timing the slide and adding transitions between the slides. There was also a fair bit of fiddling with camera settings for the 3D model. After enough slides, I then recorded the voice over. Then jiggered with all of the timings and re-recorded the voice over. Check out how it turned out.

<iframe width="853" height="480" src="https://www.youtube.com/embed/BlXzRxTyxiw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Overall I'm really pleased. It's 20 or so hours of my life I'll never get back, but I learned some new things about PowerPoint, timing, recording, editing, and YouTube. I had a blast making the video and I've really enjoyed my friend's reactions to it.

I never got things quite perfect anywhere in my opinion. I think the closest I got was about 20 seconds in where the 1b goes forward, rotates, and strafes. Everything came together there, and I can hear the smile on my face every time I listen to it. In general, for the first half of the video, I find the voice over is really well recorded and much more polished from more practice reading it, but the slide timings are too fast and I rushed a bit. By the time I was working on the second half of the video, I was better at timing things, but as it was Friday evening I was rushed rushed. I had just written the things I was reading out, and I didn't get the microphone quite placed correctly which is why how I sound changes halfway through. There are also more takes clipped together in the second half. The final crossfade at the end to the blooper has too much delay. That really annoys me now actually.

I also realised on competition day that I'd pretty much completely ignored the attachments, and we had time for it. I believe I forgot them because they're the bits of the robot I don't have - they're still at various team member's houses. I'll definitely be remembering to include the attachments time. Again, I learned a fair bit doing this and had a lot of fun. And again, thanks to everyone who helped organise and participated in Virtual PiWars! I look forward to finding out the results this weekend.

PS. Why the mark 1b? Because it's the second revision of the main chassis of course.
