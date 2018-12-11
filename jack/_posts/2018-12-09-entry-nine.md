---
layout: post
title: Entry 09 — Aftermath
description: >
 A quick recap of the week of our project 300 presentation.
author: S00171013
---

As I predicted, it's been a long and stressful week, but our demo is behind us now and we can afford to de-stress ourselves a bit!

## Preparation

On the Monday of this past week, I worked closely with Donnacha on importing his assets into a new scene, while he took the time to layout the level, I worked on the enemy AI.
 On Tuesday, myself and Donnacha worked on adding certain features to the game that would help us demo it. We added a spawn point, a pitfall boundary that would spawn the player
 at the aforementioned point, as well as a goal point that, for now, restarts the level. Donnacha also added lighting to the scene and improved existing lighting. On Tuesday night,
 I managed to finally fix the enemy rotation issue I've been having for weeks now. As I fix one issue however, another rears its ugly head. Now I've got an 
 issue where the enemy's phases are out of their proper sync. For example, when the enemy is in their INVESTIGATE phase, the Update() method will still reach PATROL code when it shouldn't.

On Wednesday, the eve before the presentation, we came together to put everything in its place. We looked at the enemy phase issue but it was clear that it was a problem that would have to wait.
 Apart from that, we put a moving player into the scene with a camera that follows them. Using this player, we could traverse the level and show off the different features in the game, like
 the AI, the SFX, the assets and the lighting. Despite the phase issue, I had the PATROL, HALT and INVESTIGATE phases to show off the next day. Myself and Adrian also printed out
 copies of a presentation schedule to hand out on the day. This can still be seen on our GitHub repo for Project D, it's called "presentation.md". On Wednesday evening we rehearsed our presentation
 and decided how to approach it. Obviously, it would have been better to have started rehearsing it a week in advance but we instead focused on getting as much ready for the demo as possible.

## Presentation Day

![In the Spotlight](/assets/img/concept_art/jack/screenshots/in_the_spotlight.png){:.lead}
Our hero finds himself in the presentation spotlight this week.
{:.figure}

At 9AM on Thursday the 6th of December, we came in and set up the laptop we borrowed from our supervisor. We downloaded our project and made sure everything worked, we then made sure our FMOD stuff
 was working. Our presentation was scheduled for 12PM that day. We went in to the presentation room and set up the laptop and monitor an hour beforehand, which involved myself and Adrian running 
 around the college looking for an extension cord, which we eventually found. Unbeknownst to us, another group had their PRJ300 presentation in the same room before us, at 11:30AM. We stood outside
 the room for a half hour, uneasy. We encountered an issue with FMOD before we had to leave the room, unfortunately we didn't think to take the laptop with us.

When we finally got into the room, we were forced to fix what we could on-the-spot and power through the presentation despite certain issues distracting us. We got the music working for the main menu, 
 but the volume sliders weren't working as intended, and I believe the SFX wasn't working as intended either. No doubt thanks to FMOD's frustrating behaviour when moved from PC to PC. Our presentation
 certainly had its hiccups as result of these factors as well as a few others, but I believe it could have gone worse. At the end of the day, we still showed off the game and were able to answer any 
 questions thrown at us.

## What Next?

My next priority is to clean up the project a little, since a rush always leaves files and folders in a messy state. As part of this cleanup, I want to find a better method of integrating GitHub with Unity,
 our current system will not work. GitHub desktop does not ignore files that it should ignore. For example, opening a scene in Unity generates thousands of auto-generated changes alone. Changes that must 
 either be synced or discarded. At least, the pressure is lessened a bit for this coming week. It'll soon be Christmas after all.

'Til next time!