# CS2053 Concept Assignment 2
## Abhishek Haribasker

### Answers

**1** --
**| 1a**: Polling systems check every frame for a value and decides if we are there yet. Event-based systems register to relevant event which lets us know when we get there.

Polling models:-

void Update(float deltaTime)
{
 if (keyboard.IsKeyDown(SPACE))
 {
 player.Jump();
 }
}

Event-based models:-

void OnKeyPressed(KeyEvent e)
{
 if (e.key = SPACE)
 {
 player.Jump();
 }
}

**| 1b**: Polling: A CPU checking the status of a keyboard to see if a key has been pressed.
          Event-based: Instead of checking the mouse position, the browser waits for hardware to report a click.

**2** --
**| a**: The 4 values are Still Released, Just Pressed, Just Released, and Still Pressed. We should track the state for this frame and the last frame. We need to know when the key is pressed and released.
**| b**: Just Pressed: Clicking a flashlight button to switch the light on.
         Just Released: Clicking a flashlight button to switch the light on.
         Still Pressed: The flashlight stays switched on while we keep our finger on the button.
         Still Released: The flashlight stays switched off while we don't click the button at all.

**3** --
**| a**: In a first-person 3D game, the listener is at the camera because the player is the camera. In third-person games, the camera and the character occupy different spaces. The advantage would be that the sounds would feel real. The problem would be that even if we zoom in or zoom out, the audio volume won't change.
**| b**: If we imagine a character standing in a hallway with the camera in front of him. If an explosion happens behind the character and if the listener is on the character, the sound will be Behind them. But to the player (the camera), that explosion is actually at a different place. If the camera is rotated 180°, left for the character becomes right for the screen.

**4**: 
**| Reverb**: It does an echo.
**| Pitch shift**: It increases or decreases frequency.
**| Compressor**: It reduces dynamic range of sound volume levels.
**| Low-pass filter**: It reduces volume of high-pitch sounds.

**5**: To calculate how collision could be calculated between a rectangle and a circle, we fisst find the point on the rectangle closest to the center of the circle. Then, we check if the distance to that point is less than the circle's radius.

boolean checkCollision(Rect r, Circle c) {
    float closestX = Math.max(r.left, Math.min(c.x, r.right));
    float closestY = Math.max(r.top, Math.min(c.y, r.bottom));
    float dX = c.x - closestX;
    float dY = c.y - closestY;
    float dSq = (dX * dX) + (dY * dY);
    return dSq < (c.radius * c.radius);
}

**6** --
**| a**: The process of taking a 2D point (cursor position) and converting it into a 3D world space line segment is called Unprojection. A screen coordinate cannot be a single point because the 3D world has depth.
**| b**: Mouse Picking: Clicking an item in a 3D game to pick it up.
         RTS Orders: Clicking the ground in StarCraft to tell a unit where to move.
         Crosshair Aiming: In a 3D shooter game, determining exactly where you are aiming and shooting.

**7**: Your Answer

**8**: The idea and process behind natural selection genetic algorithms should be decided on the basis of how many are created, how we decide who wins or loses, and select the best ones. They were used to evolve complex behaviors or creature shapes that are hard to animate by hand. However, their drawback was that they were glitchy and predictable.

**9** --  
**| a**: The algorithm is a Heuristic search algorithm.
**| b**: The algorithm is not resource intensive.
**| c**: Its used more when you want to get done with it quicker than how accurate or correct it is.

**10**: I played a game called Valorant which had similar concepts used in it. It used 4-value KeyStates to distinguish between tapping a reload and holding to defuse a Spike. They used event-based triggers for one-tap Ultimates. 
Audio relies on placing the listener at the camera's coordinates to ensure a footstep heard matches the 3D world location. Crosshair Aiming is used in this game as well.
---

**Notes**
> [ If you have any notes or comments for the TA or Instructors, please leave them here! **Thanks**! ]
