![Godot Logo](../../images/godot-game-engine-logo.svg)

# Learn GDScript From Zero

- [Learn GDScript From Zero](#learn-gdscript-from-zero)
  - [Overview](#overview)
  - [Process Function](#process-function)
  - [Time Delta](#time-delta)
  - [2D Vectors](#2d-vectors)

## Overview

- X

## Process Function

- Godot has special functions that we can customize or add to, such as `_process(delta)`. The process function gets its name because it does calculations or continuous actions.
- Almost every thing in the game has its own _process function and any changes made to that function will run on every frame. If the game runs at 60 frames per second, the process function will run 60 times every second.

## Time Delta

- Time Delta is the amount of seconds passed since the previous frame finished processing & the next frame started processing. Less than 1 second (milliseconds) is a negative decimal value & more than 1 second is a positive decimal value.
- Frames take verying amounts of time to calculate/display which means the game will run faster/slower depending on how fast frames are processed. This means on lower end PCs, the game will run very slowly and can stutter, while on high end PCs the game will go too fast & can be jerky. This is where a time delta is useful.
- Without taking delta into account, an item will move over a constant distance every frame which can cause the item to move too fast or too slow or even stutter. Using a time delta will ensure the item moves at a fixed speed & move smoothly.
- To use a delta, you can multiply the item's movement speed by the delta & that will smooth out the speed so it's always the same speed in all frames.
- For example: Say your character moves 10 pixels every single frame. At 60fps, your character moves 600 pixels per second. (10 x 120fps). At 30fps, your character moves 300 pixels per second. (10 x 30fps). That's double the distance which makes a big difference considering low end PCs may not be able to hit 60fps, & high end PCs can go reach hundreds of FPS.
- To make it consistent across all PCs, you can multiply the speed by a time delta which will increase/decrease the speed depending on how fast the game runs.
- For example: If the difference between frame 1 & frame 2 is 200 milliseconds, the character's move speed over the next frame will be decreased by 200 milliseconds. If the difference between frame 2 & 3 is 1.2 seconds, the character's move speed over the next frame will be increased by 1.2 seconds.
- This ensures the character moves over a set timeframe which will smooth out the speed. This will make the character "faster" on a low end PC and "slower" on a high end PC which will be the same speed for both PCs.

## 2D Vectors

- A vector, in physics, is a quantity with a magnitude and a direction. For example, a force applied to some object, the velocity (speed and direction) of a character, etc.
- Scale is a common vector that determines the size of the sprite. It does this by calculating how far on the x & y axis the sprite needs to be enlarged/shrunk.
- Position is a common vector that determines the location of the sprite. It does this by calculating how far on the x & y axis the sprite needs to move.
- Vectors are essential in video games because they allow you to represent 
