---
title: "I started my bachelor thesis"
date: 2020-02-20T09:31:29+01:00
draft: false
tags: ["University", "Student life", "Bachelor Thesis", "ROS"]
---

I just got my grades but the semester is not over.
Yesterday I started my bachelor thesis.
Well, in fact I talked with my professor about the topic, the process of the whole bachelor thesis and he gave me some materials.
I also organized the access to the labors.

The bachelor thesis will be about capturing data from an thermal camera and a 3D sensor, visualize them and safe them in a format which can be played without the sensors.
With my small experience I think ROS is a good tool to handle that.
So my plan is to write some publisher for the sensors, using rviz to visualize and writing some subscriber.
I'm not sure about the programming language I should use.
I think I will decide that after I know more about the sensors itself.
But it would be C++ or Python.
Only the subscriber needs to be in Matlab because the data should be used in an existing project which uses Matlab.
I'm really curious how that works.

The former project gets the data from the sensors and merges them to one 3D point cloud with thermal data for each point.
But getting the data there is a little bit "hacky" and should be more reliable.
And it's not possible to work on that project without having the sensors connected to the computer.

So my target is to build a basis for future projects.
With that comes a big responsibility to make a clean solution with good documentations.

I will track my work with issues in the GitLab instance from the LRZ [(Leibnitz-Rechenzentrum)](https://www.lrz.de/).
But I will mirror the repository to GitHub because I want my work to be public accessible.
Maybe somebody can use it.

Bests!
