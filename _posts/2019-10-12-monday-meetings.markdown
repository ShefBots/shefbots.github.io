---
layout: post
title:  "Monday Meetings"
date:   2019-10-12 14:11:00 +0100
categories: meetings
---

Well. The semester has started and everyone's back in Sheffield, so it's time to get moving. This past Monday we had our first in person meeting after forming our team via Discord and occasional discussion. I've seen tweets and posts about other #PiWars bots under construction, so I know we have a lot to catch up on, but I'm feeling optimistic. Let's take a look at what we discussed on Monday.

Before exciting discussions about robots, we had to take care of a bit of admin type stuff. The short version is that Blayze missed the meeting feeling poorly, we're going to keep a regular fortnightly meeting schedule, and continue using Discord for discussions. (We've setup channels for different aspects of robot design, there's more below.)

After the admin, we spent a fair amount of time going through each challenge to work out a list of robot requirements. It was pretty encouraging that upon reviewing everything, our original idea of a mecanum wheel based robot still looked like a good idea. What we hadn't agreed on previously was a robot size, sensor suite, and attachment requirements. Considering the manoeuvring strength the mecanum wheels give us, and the size of the spaces available in the maze and eco-disaster challenges, we're going to aim for something on the smaller side, around 175 mm wide.

Considering we're entering in the advanced category, we have to compete in several challenges autonomously. The smaller size will give us larger margins on movement, which should be to our advantage. To make the most of these margins, we're looking at using time of flight sensor data (on a servo?) to complement a camera video feed and a 9 or 6 DOF package. For attachments, a largish gripper feels like a bad good idea right now - just see it in our current logo! We haven't really decided on the attachment for the moment. This will take on more detail after we've played around with chassis design some.

We discussed a lot about what motors and electronics we might use in the robot, but no firm decisions yet. We're definitely planning on DC motors in the 400-1000 RPM range, probably with encoders. To drive that we're looking at an Arduino micro-controller, that will communicate over serial to the Pi, which will carry out the high-level logic. Another Arduino might be used to interface with sensors, which would include a PPM RF receiver for remote control.

We decided to form two/three person groups to specialise on the robot design. Broadly, we have three sub-teams focusing on Design & Construction, Electronics, and AI & Software. At the moment most of the work is being carried out by the Design & Construction team:

![A chassis design idea]({{ site.url }}/assets/191009_chassis.png)
{: style="text-align: center;"}

Still, the rest of us are thinking in the background, pondering such questions as "Where are the flashing LEDs going to go?" - and I've just finished this blog post! Stay tuned for more soon.
