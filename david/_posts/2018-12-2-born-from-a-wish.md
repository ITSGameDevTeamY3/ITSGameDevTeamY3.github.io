---
layout: post
title: Born From A Wish
description: >
  A few late nights before it's show time. We got brand spankin' new t-shirts too!
author: s00172994
image: /assets/img/user/david/posts/t-shirts.jpg
---

With our current setup, I have managed to finally get the first draft of our main character modelled in **Maya LT**.
Let me talk you through the rest of the process, continuing from the blog post on _18/11/2018_.

## Extruding The Body

In order to create symmetry, I used a technique of creating an _'instance'_ of the player's other body half.

![Protagonist Body Half](/assets/img/user/david/posts/protagonist-half-body-select.jpg){:.lead}
Any changes I make to one half of the model is mimicked in the instance on the opposite half.
{:.figure}

![Protagonist Body Half Perspective View](/assets/img/user/david/posts/protagonist-half-body.jpg){:.lead}
When I have finished modelling one half, I delete the instance of the half and mirror an actual duplicate on the other side to 
complete the body. Here, I have finished the legs.
{:.figure}

## The Finished Mesh

For the arms, I had a look at a few references to help me get the sizes even more precise than my sketch. Unfortunately, I had 
my arms drawn in an A-pose shape where a T-pose would be more appropriate and will allow for easier rigging later on.

![Protagonist Full Body Color](/assets/img/user/david/posts/protagonist-full-body-color.jpg){:.lead}
This is the character with its arms attached and colored. As discussed in a prior blog post I am using flat colors instead of textures
for a more low-poly look and to allow for sharper edges. The colors here are straight from my 2D renders of the protagonist.
{:.figure}

![Protagonist's Back](/assets/img/user/david/posts/protagonist-rig.jpg){:.lead}
Here I took inspiration from Dead Space in designing a RIG-like system on the protagonist's back. Perhaps this will display and indicate the 
player's health or status.
{:.figure}

## UV Mapping

For the eyes, I was heavily inspired by older PS2 model aesthetics which have eyes that are drawn on. To me it feels nostalgic, Square Enix 
used this technique of switching higher and lower poly models, the latter with drawn on features as textures instead of polygons.

![Protagonist UV Mapping](/assets/img/user/david/posts/protagonist-uv-mapping.jpg){:.lead}
First I go into **UV Editing** in Maya LT. I then create a _Planar_ of the model in the _Z-Axis_.
{:.figure}

![Protagonist UV Cut](/assets/img/user/david/posts/protagonist-uv-cut.jpg){:.lead}
Next I cut out the edges and verts that I will use for texturing, here I cut out one of the eyes. Maya LT 2018 allows you to _3D cut and 
sow_ in the perspective view, it's really neat and useful!
{:.figure}

## In Paint Tool SAI

![Drawing In Paint Tool SAI](/assets/img/user/david/posts/protagonist-sai.jpg){:.lead}
After exporting a _UV snapshot_, I draw the eyes in **Paint Tool SAI** using my _Wacom Bamboo_ tablet.
{:.figure}

## Back Into Maya LT

![Protagonist Texture Assign](/assets/img/user/david/posts/protagonist-applied-uv-texture.jpg){:.lead}
I create a new _material_ and assign the image to the _color_ and _ambient color_ properties. The _UV Shells_ for the eyes then 
use the newly created texture I made.
{:.figure}

![Protagonist With Eyes](/assets/img/user/david/posts/protagonist-eyes.jpg)

The result.
