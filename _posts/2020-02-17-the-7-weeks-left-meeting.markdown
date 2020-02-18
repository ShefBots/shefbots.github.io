---
layout: post
title:  "The 7 Weeks Left meeting"
date:   2020-02-17 21:22:00 +0100
categories: meetings
---

So last week was our oh-dear-there's-only-7-weeks-left meeting. The main topic of discussion was are we sure we can get the robot done and working in time? Should we withdraw? We went through each of our areas and had a very close look at our progress, how much we estimated was left to do, and how much time we realistically had available. The long story short is that we can get things done. Let's dive into a bit more detail.

On the hardware front, we admitted that progress had been slow, and there were still several tasks to complete. We've created a prioritised todo list that includes:
1. New motor driver electronics
2. Power delivery system
3. Chassis improvements
4. Attachments (gripper, turret, etc.)
5. Design and print a stand for the robot
6. Theme decorations

Chris has been making progress and has completed a good chunk of the chassis improvements (including improving the gear meshing), and nearly has the motor drive electronics finished (the in-progress stripboard layout is shown below). The plan is to pass the robot to Robbie and Harry for the final chassis improvements, camera and Pi mounts, and power systems on Tuesday. This is the minimum necessary for testing the software on real hardware. So next Monday/Tuesday I should be receiving the robot with hardware in a working state, giving Simon and I about a month to test/debug software on the real hardware. More on software development later.

![Improved gear meshing]({{ site.url }}/assets/200217_gears.jpg){: style="height: 14em;"} ![Strip board]({{ site.url }}/assets/200217_stripboard.png){: style="height: 14em;"}
{: style="text-align: center;"}

For the remaining attachments, we decided that we'll try and use a passive gripper sort of shaped like a giant C. There's a diagram of what this might look like below. We'd use it to push the barrels onto the zones, and then reverse away from them. An active gripper is still on the wish-list though if time allows. Robbie already has most of a turret built from a previous project we can use, and he can finish it up while we work on software.

![Diagram of a c-shaped gripper]({{ site.url }}/assets/200217_gripper.png){: style="height: 10em;"} 
{: style="text-align: center;"}

Unfortunately, the 360-degree camera that Blayze has been working on is the biggest casualty as his time is quite limited over the next few weeks. He doesn't have time to fully develop the neural network he was planning to use to extract angle and distance data from the captured images. We're still keeping the camera though, but instead of neural nets, we'll pivot to using traditional computer vision approaches to detect the presence of objects. The location of the object in the frame can then be used to identify the angle the object relative to the robot. This reduces the [bus factor](https://en.wikipedia.org/wiki/Bus_factor) of our sensor system and lets all of us contribute.

To compensate for the lack of distance data from the 360-degree camera, we're going with a two-camera approach. So where's the second camera going you ask? On the front of course! The front camera will also use traditional computer vision, and be used to detect when objects are close. The changes to the camera system are a little bit of a downgrade, but significantly easier to develop the code for. In fact, I've already created a mock-up of a front-mounted camera and started work.

![Forwards facing camera mockup]({{ site.url }}/assets/200217_forwards_camera.jpg){: style="height: 14em;"}
{: style="text-align: center;"}

Which brings us onto the software. At the start of the meeting, I was not confident about meeting the software requirements, especially given the relatively small window for testing on real hardware. Looking at the challenges, however, I realised I made a near-fatal error when considering the software - all my presuppositions about the time needed were predicated on the Ecodisaster challenge. Looking at it in detail, and discussing with the team, we decided that was the hardest challenge. The remaining AI challenges (line following, maze, and minesweeper) we expect to be easier to code for. I also realised that Simon and I weren't spending our time too effectively with both of us working on the Ecodisaster challenge.

So let's look at the prioritised software todo list then:
1. Lava Palava (line following)
2. Minesweeper
3. Escape route (maze)
4. Remote control
5. Eco-disaster
6. Turret control

We've put eco-disaster near to the bottom, but Simon will continue to work on this as we recognize it does require a large time investment. Just, in terms of the competition scoring, it's better to have software for the other challenges rather than putting all of our eggs in one basket. This also means that the piwarsimulator is going to be focused on just the Ecodisaster challenge, and other control programs developed for the other challenges. While that may not be good practice for software design if we were selling a real robot, as separate single-purpose programs severely limits future expandability, the separate programs will let us develop software much faster.

How much faster can we develop you ask? Well, you saw that I have a front-mounted camera mock-up. On the left below is a picture from the camera pointed at a line to follow. On the right is the MATLAB output from an algorithm to identify the line and decide what action the robot should take. This works for a variety of test photos. The next step is to port this algorithm to Python, run it on the Pi, and test with a video feed. Stay tuned for more detail on how this works in an upcoming blog post!

![A test photo]({{ site.url }}/assets/200217_line.jpg){: style="height: 14em;"} ![MATLAB output]({{ site.url }}/assets/200217_line_analysis.png){: style="height: 14em;"}
{: style="text-align: center;"}

We rounded off our meeting with a bit of light-hearted discussion on theming to get us motivated. We had an amazing idea, or at least we think it's pretty clever. The wheels are green. The LEDs on the motor encoders are green. What's green and a disaster? Something nuclear, so we're going all-in on a radioactive theme. We'll add some more green LEDs. Chris has done up a great design for ionizing radiation [trefoil](https://en.wikipedia.org/wiki/Trefoil) hub caps for the wheels that screw on, which we should fit yellow LEDs in if we have time.

![Hubcap render]({{ site.url }}/assets/200217_hubcap.png){: style="height: 14em;"} ![The hubcap unscrewed]({{ site.url }}/assets/200217_hubcap_unscrewed.jpg){: style="height: 14em;"}
{: style="text-align: center;"}

To wrap things off, check out the robot going in slow motion to see those sweet hubcaps spin!

![Going backwards in slow motion]({{ site.url }}/assets/200217_slowmo.gif){: style="height: 14em;"}
{: style="text-align: center;"}
