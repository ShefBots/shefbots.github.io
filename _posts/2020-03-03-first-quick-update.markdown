---
layout: post
title:  "The first quick update"
date:   2020-03-02 23:27:00 +0000
categories: meetings
---

So a quick recap of our now weekly catch-up meetings. This is a bit light on details to save time, so I may have missed a bit, but I've got the highlights here for you if nothing else. We started out with a catch up and risk assessment on the health situation. We're happy that Pi Wars is keeping us up to date, and we'll be following along with their, university, and DHSC guidance. We currently think the risk is low and are happy to attend under the current conditions. We've now got our hotel and travel sorted.

In hardware news, the power system is now installed, although a little bit of final tweaking is needed (good work Chris and Harry over the weekend). Harry is working on the final electronics. That is, the Teensy LC control and interface board, which will connect to the Pi via USB. It'll control 2x servos, 2x ESCs, and interface with the RC receiver, 2x ultrasonic modules, a protractor, and WS2812b RGB LEDs. The decision on the ultrasonics and protractor are a late addition after our discussions on the maze.

![The battery mount is a bit...]({{ site.url }}/assets/200303_battery.jpg){: class="hight"}
{: class="centr"}

So the maze. We were talking about the software to tackle it. Ideally, we can use solely a camera, but due to the walls being low, and black like the floor, there would likely be some annoying challenges in horizon detection. So instead we discussed using the camera to look at the entire course (as it'll be quite high anyway) and then design and execute a pre-programmed route. We think this is a bit more feasible, but we have had some issues with the robot turning exactly 90 degrees, so some ultrasonic sensors to confirm the route and avoid wall collisions make sense. It may also be possible to do the course entirely based on ultrasonics. Much testing is in the future.

![Ultrasonics to be installed]({{ site.url }}/assets/200303_ultrasonics.jpg){: class="hight"}
{: class="centr"}

The last thing we discussed was, for a change, a technical Linux discussion. With two Teensy boards acting as USB serial devices... How do we tell them apart in software? One idea would be to use udev, and it seems you can [distinguish devices by the physical USB port](https://askubuntu.com/questions/49910/how-to-distinguish-between-identical-usb-to-serial-adapters). But to confirm, we're baking an ID request into the serial protocol to be able to double-check in software, that we are not going to accidentally control the motors when we try and query the ultrasonics...
