---
layout: post
title: Entry 04 — Quiet Week
description: >
  A quick rumination on how I want an enemy in the game to behave.
author: S00171013
---

With this week being study week at the college, and the fact that my family and I were set
 to visit relatives in Spain from November 1st to 6th, I'm afraid I didn't make any concrete progress
 on Project D. With the prior weekend taken up by volunteer work for Sligo Live, I decided to spend the few days
 I had before the 1st catching up on other assignments.

Despite that, in place of a progress report, I'll quickly go through what I want for the enemy object
I am to create for Project D.

## The Basis

My primary basis for the enemy AI in this game is that of the enemy soldiers in [Metal Gear Solid 2: Sons of Liberty](https://en.wikipedia.org/wiki/Metal_Gear_Solid_2:_Sons_of_Liberty).
 To me, it is one of the most impressive examples of AI in a stealth game. 
 
A few examples of their intelligence:

*   Upon spotting the player, instead of attempting to take the player on by themselves, they will run to a safe location and radio for backup first.
*   They notice and investigate signs of the player's presence, be it an empty weapon magazine on the floor or the player's shadow.
*   They work as a team to find the player when they are alerted, e.g. a pair of soldiers would stand back to back as they move through a hallway, one would check hiding spots while the other keeps watch on the room's entrance.

While the AI I manage to implement by the end will very likely be less sophisticated than the MGS2 guards,
 they will serve as a great reference for when I think about how an enemy should react to a certain situation.

## The Minimum of What I Want to Achieve

I want the enemy I create to at least be capable of:

*  Following a patrol pattern, stopping briefly at certain points to allow the player to sneak by them or take them out.
*  Investigating any source of disturbance (a noise, seeing the player from afar) effectively, returning to their patrol route if they find nothing.
*  Upon spotting the player, they will rush to to another enemy if there is one nearby to attack the player as a group. If no enemy is nearby, they will fight the player themselves. They could also try to raise a nearby alarm.

Above all, I want the enemies to act as naturally as possible. Next week is where I begin my work on the enemy AI.

'Til next time.