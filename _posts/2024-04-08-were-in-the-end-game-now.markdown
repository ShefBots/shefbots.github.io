---
layout: post
title:  "We're in the End Game now"
date:   2024-02-03 19:50:00 +0000
categories: [updates]
---

It's been a hectic few months - we've struggled at times to be motivated and get things done - but we're back in action and working our way through integration heck to pull everything together.

Chris is pulling together our final styling:

![The robot from the front]({{ site.url }}/assets/240408_style1.jpg){: class="hight"} ![The robot from the side]({{ site.url }}/assets/240408_style2.jpg){: class="hight"} ![The robot rear]({{ site.url }}/assets/240408_style3.jpg){: class="hight"}
{: class="centr"}

Blayze is working on the final neural network training for the vision system:

![A render from the vision system]({{ site.url }}/assets/240408_vision.jpg){: class="hight"} 
{: class="centr"}

Robbie is handling the design of our final launcher attachment:

![A render of the in design launcher]({{ site.url }}/assets/240408_launcher.jpg){: class="hight"} 
{: class="centr"}

At the moment every challenge I've programmed the simulator for can be solved and with Chris' effort on the sensor board we've started integration testing. A fun few issues were had with trying to use the gripper crashing the software stack - we had bugs in both our codes! (Too frequent polling on my end and a missing global on Chris'.) Some great progress on the Escape Route though:

<video height="480" width="960" class="centrvideo" controls>
  <source type="video/mp4" src="{{ site.baseurl }}/assets/240408_simulator.mp4">
</video>
<video height="480" width="854" class="centrvideo" controls>
  <source type="video/mp4" src="{{ site.baseurl }}/assets/240408_reality.mp4">
</video>

How well everything integrates together in  practice is up for grabs. Maybe it'll be great, or maybe wishful thinking. Whatever the outcome, we've had a fair bit of fun working on our robot and we're all looking forward to Cambridge in a couple weeks time to share our work with everyone and see what everyone else has done as well!
