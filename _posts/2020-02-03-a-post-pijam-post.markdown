---
layout: post
title:  "A post Pi Jam post involving a moving robot"
date:   2020-02-03 21:45:00 +0100
categories: meetings
---

Starting with the headline news... At the recent Sheffield Pi Jam, Chris debuted our robot moving under its own power! Well, it's own power in the sense that it was using test electronics for developing the software for the motor encoders and Teensy with no Pi involved, but moving nonetheless! This Jam ended up a bit robot-themed, and you can see ours below (bottom left), playing with its robot brethren controlled by [@jedifodder](https://twitter.com/jedifodder) (top) and [@red0brick](https://twitter.com/red0brick) (guess). A moving robot is a milestone for the team as it proves the platform is mechanically viable, although personally, I didn't catch on to this immediately as I still have a stack of software to write for high-level logic control...

![Playtime]({{ site.url }}/assets/200203_playtime.png){: style="height: 16em;"}
{: style="text-align: center;"}

Continuing onwards, Chris is working on the final version of the motor driver electronics now that he's completed the motor encoder and driver software. After a fair amount of driving, he's identified some slack in the gears and wobble around the wheel mounts that Robbie and Harry will be working on after their exams finish this week. (It's the last week of exams here at UniOf.) You can just about make out the wobble in the clip below as the Teensy in test mode executes driving a pre-programmed square.

![Wobble...]({{ site.url }}/assets/200203_wobbie.gif){: style="height: 14em;"}
{: style="text-align: center;"}

While talking about the EcoDisaster challenge at the last meeting we were pondering what to do if the barrel gets knocked over. Towards this end, we had the idea of using a hoop that goes down, rather than a gripper, to capture the barrels. This might also be mechanically simpler. Vaguely related, as in not at all - smooth segue I know, thanks Linus! - we realised that our best option to connect the Teensy controlling the motors (and other USB things) to the main control Pi will be to make our own USB cables. To that end, we've ordered some USB Type A plugs to go with the Micro USB plugs I've already got for that.

![Some assembly required]({{ site.url }}/assets/200203_assembly_required.png){: style="height: 7em;"}
{: style="text-align: center;"}

Blayze is continuing to work on the vision system and has come up with a few minor adjustments to the hardware to reduce glare and occlusion. Neural networking and renders abound, but he'll have to explain those himself at some point to do them justice. For our main control software, we're currently investigating a grid-based system for storing data, rather than a list of coordinates, to make implementing pathfinding around objects easier.

We've also now roughly worked out the serial protocol we'll be using to talk to the motor driver Teensy. This will probably consist of a two-byte header, a fixed number of data bytes, and a checksum. The checksum will ensure that we don't accidentally drive somewhere unintentional based on a corrupted data transfer. Our best idea for the moment to calculate a checksum is to calculate it as the remainder of the sum of our data bytes divided by 255. This is easy and fast to implement using integer overflows in C, and I've had good success with this in the past with my homemade Ambilight system. An example packet is shown below.

![What could be our packet format]({{ site.url }}/assets/200203_checksum.png){: style="height: 5em;"}
{: style="text-align: center;"}

The short term goal is to have everything assembled enough in the next two weeks to hook up the control Pi and test controlling the real hardware with our control software. That's not everything though, so it looks like as we get closer to PiWars we'll be getting busier and busier. We'll close out though with a clip of the robot scooting along to keep our spirits up!

<video height="640" width="360" style="margin-left: auto; margin-right: auto; width: 480px; height: 270px; display: block; border: solid 1px white; margin-top: 5px; margin-bottom: 5px" controls>
  <source type="video/mp4" src="{{ site.baseurl }}/assets/200203_scooch.mp4">
  <source type="video/webm" src="{{ site.baseurl }}/assets/200203_scooch.webm">
  <source type="video/ogg" src="{{ site.baseurl }}/assets/200203_scooch.ogv">
</video>

