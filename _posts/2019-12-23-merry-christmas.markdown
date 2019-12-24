---
layout: post
title:  "Merry Christmas!"
date:   2019-12-23 18:03:00 +0100
categories: meetings
---

This is going up right before Christmas, so Merry Christmas! Let's get straight into the year end update. As I've been struggling with a cold, I'm sad to say I haven't gotten much of anything done since my last post. The rest of the team also hasn't made much progress due to general year-end business. Blayze's work has been delayed due to a broken water-jet cutter, but progress continues on the camera design (more on this later). Harry and Chris have made some code improvements, on a library for PPM decoding and on code for adjusting speed and turning rate respectively.

Probably the best news is that we have a prototype chassis together! It's rough for the moment, and we've identified a few things to fix, but it's some great progress thanks to Robbie! You'll note the somewhat wonky wheels, which are temporary. Our actual mecanum wheels, kindly provided by Rapid Education, have since arrived in the post. The chassis has a bottom and upper layer, with the gearbox for the wheels inbetween. The bottom layer will host the heavier batteries, and the upper layer the electronics. It's made out of laser-cut wood, assembled with bolts.

![Our prototype chassis assembled]({{ site.url }}/assets/191223_chassis.jpg){: style="height: 14em;"}
{: style="text-align: center;"}

You'll notice on top of the chassis the first prototype of Blayze's 360 degree vision system. Below, you can see what the output from it looks like (apologies for a photo of a screen). Unfortunately, if you look closely you can see that the motors obscure a significant portion of the view, and so Robbie will be redesigning for the front motors to lay parallel to the chassis. To help minimise occlusion further, Blayze will also be redesigning the camera mount for thinner and fewer supports.

![Camera vision!]({{ site.url }}/assets/191223_camera.jpg){: style="height: 14em;"}
{: style="text-align: center;"}

Finally, I'm happy to announce that Simon has joined the ShefBots team to work on software! I was showing off my simulator at a recent Pi Jam, and he was quite interested in potential applications of things like the [A* path finding algorithm](https://en.wikipedia.org/wiki/A*) to solving the AI challenges. He's a CompSci graduate currently doing software dev work so we're pretty sure he's qualified! Simon, and the rest of us, will be continuing to work on the hardware, electronics, and software into the new year. We'll see you then!
