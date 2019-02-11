---
layout: post
title: Entry 11 — Work it Out
description: >
 A note on the forward steps we've taken for Project D.
author: S00171013
---

Another busy week comes to an end, and it's clear that things will only heat up from here. Luckily, I've finally fixed
the long-standing phase issue that's been plaguing my test enemy. Now I can finally finish implementing its behaviour.

## A Fresh Start

As I mentioned last week, we planned to create a new repo for Project D and we have done so, in a way. What we've done
is empty out our existing repo completely and add a new blank Unity project to the repo. We each still have a copy of 
our prototype version on our PCs, which I've dubbed _Proto-Dissonance_. We can now add only what we want from Proto-D to our new
project. This can help us ensure our workspace remains uncluttered. (The amount of folders and files got a little out of hand
during the week of our presentation.)

As part of our new start in regards to the Unity project, we've also transitioned over to using GitKraken for Project D. This
new Git client should be a lot easier to work with than GitHub Desktop was, with it we can get a good overview of the project's
commit history at a glance. It also seems to have a much better diff viewer than Desktop. With GitKraken and our new knowledge
of how Git works with the .gitignore file, we shouldn't run into any more major Git issues. Hopefully! 

![GitKraken](/assets/img/concept_art/jack/semester_two/mistake.png){:.lead}
A new Git client should help us on our way.
{:.figure}

## Phase Issue Breakthrough

Well, I examined my enemy AI script in great detail last week. It turns out there was a number of issues with my code but I discovered
a particular one that was certainly the root of the problem. In my AI script, I have two primary phase variables: _enemyPhase_ and 
_previousPhase_. A phase is only updated once the _Update()_ method detects that the aforementioned two variables are not the same phase.
In my _SetPhase(enemyPhase newPhase)_ method, the previous phase becomes the current enemy phase first, then the enemy phase becomes
the new phase. What I soon realised was that the previous phase never became synced with the enemy phase again, so _Update()_ would detect the
two variables not being the same and therefore update the current phase constantly, which caused a lot of unwanted behaviour. Fixing this was
a simple enough affair:

![Syncing Phases](/assets/img/concept_art/jack/semester_two/mistake.png){:.lead}
Syncing the phases here has fixed the issue I mentioned in [Entry 09](https://itsgamedevteamy3.github.io/jack/2018-12-09-entry-nine/)).
{:.figure}

Now that I could transition to phases again, I was able to work on the SURVEY phase. This phase is where the enemy has reached a disturbance zone
and is now examining their surroundings. I had the idea to have the enemy look in four possible directions (up, down, left, right) when
surveying. To achieve this I gave the enemy invisible objects I called _Survey Points_. The enemy could look at one or more of these directions
with their weapon's flashlight. The idea being that they could turn and spot the unsuspecting player. I hard-coded a simple test where the enemy
would look left and then right. 

![Survey Points](/assets/img/concept_art/jack/semester_two/mistake.png){:.lead}
With these Survey Points (Purple orbs with yellow question marks), I might be able to implement some interesting behaviour. 
{:.figure}

I think I'm on the right track with this and I may be able to implement some cool behaviour here. Though I might
decide to leave it as it is for now and focus on implementing the enemy's ALERT phase, since it's an integral part of the game.
Finishing out all of the enemy's phases and ensuring it can transition between each will likely be my goal for this week. Wish
me luck!

'Til next time.
