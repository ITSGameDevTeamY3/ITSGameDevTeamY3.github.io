---
layout: post
title: Entry 05 — AI Foundations
description: >
 Here I recount my first week working on implementing AI for the enemies in Project D.
author: S00171013
---

This week was my first week working on AI for the enemies. I think I've made a good start,
 but it's clear that a lot more work needs to be done to make this AI convincing. I'll detail what
 I've been up to in more detail below.

## Compatibility Issues

The first challenge I came across has made me aware of the issues that can occur when one is working off of
 two different versions of Unity. When I added the NavMesh Components to the project at home, I installed
 the "2018.2" version since my Unity editor was "2018.2.9f1". Upon opening the project at the IT,
 the components were incompatible as the Unity editor at the college was version "2018.1.6f1" 
 and such would only support the "2018.1" NavMesh Components.

Due to a lack of admin rights, I am unable to update the Unity editor at college to match my home version.
 To rectify the compatibility I removed the ".2" components and replaced them with their ".1" counterpart.
 This allowed me to use the NavMesh freely in college. When I got home however, I realized that Unity
 automatically upgrades all components when opened in a newer version, thus I would run into the same
 issues again when I resumed work at college. Eventually, I gave in and decided to install 
 "Unity 2018.1.6f1" at home so that I'd be working on a version identical to the college version.
 I have since instructed the other team members to do the same for their home versions.
 Thankfully we are now free of those particular issues.

## The Initial NavMeshes

After much research, I finally starting baking NavMeshes into the scene this week. I had to do this a couple
 of times over thanks to the compatibility issues I mentioned above. Currently, I have two different Nav Meshes
 set up for the Protomap, one for regular "grunt" enemies to navigate and another for "Elite" enemies that are 
 more nimble and can reach certain heights. These meshes are certainly subject to change over the weeks, but here's
 a couple of screenshots. (Any blue area is navigable by the enemy type it was made for.)

![Grunt NavMesh](/assets/img/concept_art/jack/navMesh_grunt.png){:.lead}
This is a bird's eye view of where run-of-the-mill grunt enemies can move.
{:.figure}

![Elite NavMesh](/assets/img/concept_art/jack/navMesh_elite.png){:.lead}
The elite enemies can traverse a lot more of the landscape. Notice that they will be able to jump on top of certain buildings or plateaus, unlike regular enemies.
{:.figure}

## The Enemy So Far

So far, I have my test enemy patrolling a number of specified "Patrol Points", a prefab I made that can be used again and again for the scene, they are invisible in-game.
 When the enemy reaches a patrol point, I have it so that they briefly pause, this is common in stealth games as it gives players a chance to sneak up on them. The length 
 of their pause in seconds can be changed in the Unity Inspector. I've implemented a simple boolean method that takes a number of seconds passed in and returns true when
 that amount of time has passed. I've placed this in a "TimeManager" class that can be re-used whenever it is needed. It will see much use, I feel, as time is a major 
 element in game programming.

![Patrol](/assets/video/jack/patrol.webm)

As a test for the enemy's pathfinding, I've implemented a script that sends them to any location that you have clicked on in the scene, assuming you clicked on an object.
This is to simulate the enemy investigating a disturbance (e.g. a noise or a glimpse of the player from afar.), the click will be replaced by something more natural later on.
Of course, right now this functionality is very rudimentary. Upon the click, the enemy halts for a specified time before moving to the click area to investigate. I have them
stop a certain distance in front of the click to make their investigation seem more natural. After they've reached the area, they promptly resume their previous patrol.
A lot more work is needed for this investigation functionality. Adrian informed me that if you click on top of an obstacle, the enemy walks into the obstacle and is 
sent flying back, unable to move properly afterwards. It's humorous, but it's obviously an issue. My first move is to mark it as a "NavMesh Obstacle" and work on 
ironing it out from there. I will continue my work on the enemy this coming week.

This week, I want to improve the enemy so that it:

*  Avoids crashing into obstacles and going berserk.
*  Looks around its surroundings naturally at each patrol point.
*  Turns naturally to face the source of a disturbance before moving toward it.
*  Looks around it's surroundings at a source of disturbance before moving back to its patrol area.

Hopefully the enemy behaves a little more realistically come next week. Wish me luck!

'Til next time.