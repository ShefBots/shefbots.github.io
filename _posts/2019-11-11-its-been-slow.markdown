---
layout: post
title:  "It's been slow..."
date:   2019-11-11 20:45:00 +0000
categories: meetings
---

...but slow and steady wins the race. It's time for that fortnightly update again, but as the title hints, things have been a bit slow the since the last post. Why? It's not the entire reason, but it doesn't help that Peter's poor laptop died, came to life, and then died again in the middle of a meeting with his supervisor. Not just a blue screen of death, but a blue screen of awkward - leaving Peter without a functioning computer for design work. And as Peter is half of our primary hardware design team, it's been down to Robbie to make progress. Which he has!

In the last post I mentioned working on gearing to connect the 25D motors we want to use to VEX mecanum wheels. Robbie continued to tackle the problem and has produced a bevel gear design to attach the motors to the wheels at a right angle. As you can see below, this allows for a smaller footprint, which we think will make navigating the AI challenges easier. Robbie plans to test print this design to verify it works mechanically. (We'll apparently need to find some ball-bearings somewhere?) If it checks out we plan to go with this. Robbie has also now placed the order for the motors and encoders. We've established ourselves a rough budget for the robot of £300, which we think is reasonable.

![Bevel gear motor mount]({{ site.url }}/assets/191111_bevel.png){: class="hight"} ![A smaller footprint]({{ site.url }}/assets/191111_smallerfootprint.png){: class="hight"}
{: class="centr"}

We have some more research type results rather than built it or wrote it down type results for our slower progress elements. Chris was planning to work on testing out encoders and working on the software for that, but only had time to work on the design and says it should be easy. Hopefully not famous last words! Harry got some testing with a radio receiver and an oscilloscope done and is confident he can read the receiver output with an Arduino that we can then interface via USB to the Pi to provide remote control. We're planning to connect what we can to the Pi via USB to avoid any potential timing issues from the hardware buses (TTY, I2C, SPI, etc.).

I've done some research on tracking the position of the robot. Looking at IMUs, inertial measurement units, something called [a complementary filter](https://www.pieter-jan.com/node/11) can be used to combine the readings from an accelerometer and gyroscope to get a reliable reading of heading. I also looked at optical flow sensors, like the sensor from a mouse. This would provide dead-reckoning of the robot position. Unfortunately it looks like most of the available literature on these sensors is more academic than hobbyist. Given this, their cost, and potential difficulties with tracking over different surfaces, I've recommended to the rest of the team that we just estimate position using the encoders instead. Or use an old ball mouse. (Or Chris suggested [lighthouse tracking](https://www.triadsemi.com/steamvr-tracking/) like the use for VR?!)

![Old-school mouse style...]({{ site.url }}/assets/191111_mouse.gif){: class="nothight"}
{: class="centr"}

The coolest progress since our last update has been made by Blayze. His 360-degree camera idea involves pointing a camera up at a largish bearing ball (or similar) used as a convex mirror, like they sometimes have at blind street corners. The bearing ball would sit at the top of our robot and hence we want a smaller footprint for a smaller blind spot. A potential problem with Blayze's idea though is that bearing balls are imperfect - how can we make sense of a potentially distorted reflection? Blayze is treating this to the old machine learning approach. To generate training data, he's started writing an algorithm for a ray-tracing simulator (RTX on!) that will simulate what the camera would see. My understanding is a bit vague, but mumble something de-warped mumble objects mumble (my notes on this bit aren't good enough!). If this sounds kind of complicated it is, but to be fair it's also related to Blayze's in progress PhD. He should be providing all of us with a more detailed explanation of how it's all going to work at some point in the future. More prosaically, he's also working on how to hold the bearing ball in place and we should soon expect to see a model for this.

![Physics A-level style drawing of 360 camera setup]({{ site.url }}/assets/191111_360.png){: class="hight"}
{: class="centr"}

For future steps, we're still not sure about suspension, but we've just remembered we also need to keep attachments in mind. So Peter will be working on our gripper attachment idea while his laptop is repaired. Chris and Harry will continue working on encoders and control, and I'm still on blog writing and looking at the IMU. I plan to write some test code to help give us a better idea of what we could use one for. After the hardware is down, we're planning to start by software development around the [eco-disaster](https://piwars.org/2020-competition/challenges/eco-disaster/) challenge as it looks like we can take a fairly mechanistic approach to tackling that problem. Overall I'm pleased at the progress we're making!
