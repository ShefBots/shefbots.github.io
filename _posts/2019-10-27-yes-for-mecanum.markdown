---
layout: post
title:  "Yes for Mecanum"
date:   2019-10-27 21:31:00 +0000
categories: meetings
---

At our meeting this past week, after a bit of discussion about rough ideas for electronics involving PPM, omni-directional cameras, and IMUs, we got down to the meat of focusing on the chassis design. Sadly, no progress on the gripper. :( We decided that to make the most effective use of our time designing electronics and software, that we really needed to get further in the hardware platform design process.

Robbie reported that our ideas about per-wheel suspension from our last meeting were impractical. Both he and Peter concluded that we needed to decide on a wheel - any wheel - to get further along in the design process. We knew we wanted mecanum wheels, but there are a lot of requirements to getting a good design that make mecanum wheels particularly complex to design from scratch. Chris spent some time working on wheel design and fabrication, even to the point of making a parametrised model and scale test prints, but didn't have something he was 100% confident in yet. But, he did have a spare chassis with the VEX mecanum wheels on it. After playing with that some, we have decided on using them. They're not crazy expensive, and would give us a solid starting point overcoming one of the biggest issues it looked like 3D printed wheels would have - traction.

![VEX Mecanum wheels]({{ site.url }}/assets/191027_sparechassis.jpg){: class="hight"}
{: class="centr"}

After looking at the VEX wheels, the obvious follow-up question was motors. We knew we wanted 25D motors with encoders (for precision driving), leaving us with the question of direct-drive or geared attachment? After much discussion about the width of the robot, manoeuvrability, and the maximum sizes, we felt that a geared attachment might be the only option. Robbie has done some work on a vertically stacked design, which we may consider, but for the moment it actually looks like direct drive will just fit within the size limits. (Provided the encoders aren't too big...)

![Geared motor mount]({{ site.url }}/assets/191027_gearing.png){: class="hight"} ![Direct drive fits]({{ site.url }}/assets/191027_justfit.png){: class="hight"}
{: class="centr"}

OK, OK, a little bit more about the electronics and sensors. Harry has been looking at 3S Li-Pos to go with 350 RPM 25D motors. This seems to be around the sweet spot of speed, current draw, and availability. Blayze is very excited about the idea of a 360-degree camera, and has plans to start doing simulations to train a neural network. High-tech! I'm feeling a lot more prosaic and really liking Harry's idea of an optical flow sensor - think like the pickup on a optical mouse. That and the IMU, or inertial measurement unit, I mentioned before to help keep track of where we've gone.

As for why we want mecanum wheels? Well, check out Chris' mini mecanum cruising sideways. TPU made all the difference...

![Man, it goes _sideways_!]({{ site.url }}/assets/191027_sideways.gif){: class="hight"}
{: class="centr"}


