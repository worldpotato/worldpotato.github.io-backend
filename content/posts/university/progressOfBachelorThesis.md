---
title: "Progress of my bachelor thesis"
date: 2020-04-15T22:58:15+02:00
draft: false
tags: ["University", "Bachelor Thesis", "ROS", "Matlab", "Python", "CUDA"]
---

My last post is some time ago.
Mostly because I had no motivation to write a new post and I don't want that blog to be a "I have to do that"-thing.
Actually I started to write a new post but never finished it and now it is really outdated so let me start again.

Let me start with the thermal camera.
It's an Optris PI400 and the ROS node is on GitHub and the driver is easy to download and install.
The ROS node works well and everything is nice so that I can close the first issues.
*Yeah!*
Nevertheless, I think there is some space for improvement.
Which leads me to creating a pull request.

The second sensor is the ZED cam.
That's a stereo cam from StereoLabs which can provide a 3D-Pointcloud.
To calculate the pointcloud the driver uses CUDA cores and that would cause some trouble.
But that is a topic for later.
Installing and running the ROS node was pretty easy and smooth.
Also the documentation is excellent and should be a prototype to others.
*KUDOS to StereoLabs on that point!*

After installing the two cameras and running the ROS nodes the next step would be to project the thermal image on the pointcloud.
With the RVIZ Plugin "Depth Cloud" makes is easy to show a image on a pointcloud.
But that's only the visualization and does not result in reliable merged data.
That's an important fact and good to know.
But it doesn't bother me at all since ROS should only be used to collect the sensor data.
And RVIZ should only be used to get an idea of the acquired data.
At least in the first run.
The depth cloud plugin needs the image in the same resolution as the point cloud.
What means I need a node to resize the image or add some pixels.
I decided to write a python script because I never wrote a python node and thought python would be good for that purpose.
And that was not wrong.
After some minutes the first prototype was ready and did his job.
Sure.
I tinkered around afterwards and improved the node and played around with different values and so on...

Let's do a little sum up here.
To this point I had the drivers running and also the ROS nodes.
Together with my own node I had a nice visualization.
But I had to start these tree nodes in separated terminals and RVIZ in an fourth terminal and adding the plugin and so on.
As a lazy developer I knew I have to automate this process.
So I wrote a `*.launch` file where I start every node including rviz with the right configuration.
What an awesome feeling to launch all that with only one command!

As a small time reference, that was the time where Corona comes to Germany.
Nearly every company tries to establish home office and it was just a question of time until the lockdown got launched.
But fortunately I can record a Rosbag and play that at home.
As I mentioned before, the ZED camera needs CUDA cores to work and I don't have a Nvidia graphic card at home.
So I can't only play the bags for future work.

Well, OK. After moving all the sensors at home and preparing my home office it just took one day until we go the lockdown.

So, welcome to the home office!
The next step was to connect the xsens IMU to ros.
Sounds easy.
I threw "xsens ROS node" to [duckduckgo.com](duckduckgo.com) and found a GitHub link.
Yes! But no.
It was a deprecated node.
Well, quick look at the xsens homepage showed me that the ROS node is not on GitHub anymore.
Whoever wants to use the node needs to download a package full with other software and copy the node to the workspace.
What if they release a new version?
Download the full package again, copy it, apply your changes and hope that everything is fine.
How do you know what they changed?
Hope that everything is in the changelog.
Git is a nice tool.
You just need to use it.
But OK.
I installed the driver, copied the ROS node and build it.
That works nearly flawless.
So let's check the published messages.
And what should I say?
Only the current orientation is published.

Actually, the IMU is the less important sensor in my setup.
So lets move to the lidar.
I did not tried that one before the IMU because it needs a external power supply and the power supply was located at an other building of the university.
Fortunately my Professor knows someone who has authorization to go into the buildings during the lockdown, so that he was able to bring me the power supply.
After managing to power on the lidar it was very easy to get the ROS node running.
But the visualisation was not correct.
I thought it may be because I pulled it from GitHub some weeks ago at the beginning of my work.
So I just did a `git pull`, got the lasted release and after building it the whole node works perfect!
That's how I like it!

After talking to my professor we decided to let the xsens be the xsens and go over to the matlab part.
My love/hate relationship to MatLab is an other story, but let me say that I really hate matlab sometimes.
But sometimes MatLab is really nice.
For example if you want to create a GUI application in a short time.
It took me some hours of finding a elegant way to get the last message at certain timestamp of a message.
Mostly because I didn't see a implicit cast from double to uint16.

And that is my current state.
It took me some time to write it together but it's nice to recap the own doing.
And hopefully I can manage it to do it a little bit more often.


