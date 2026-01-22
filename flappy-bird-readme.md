FLAPPY BIRD UNDERSTANDING REPORT
---';
jkghjhjjhjhhh
bjj
1. Project setup in Unity:
First I created a 2D project model in Unity, I set the camera to 2D mode and adjusted the screen size to mobile resolution. Then I added basic game objects like background, bird, pipes. All sprites are imported with correct setting so that they look clear.
2. Bird setup and movement (BirdController script):
The bird is the player obj added Rigidbody 2D to the bird do that the gavity can pull it down naturally, even added collider2D so it can detect collision with pipes and ground. In script- 
•	The bird jumps up when the player taps or clicks.
•	Gravity pulls the bird down when there is no input.
•	Sound plays when the bird flaps.
•	The bird dies when it hits a pipe or the ground.
Logics : Rigidbody2D.AddForce() to make the bird jump , OnCollisionEnter2D() to detect bird ,Bird movement is diables before the game starts using rb.simulated=false;( sure the bird stays still on the start screen and moves only after pressing Play)
---

3. Pipe system  and movement :
Pipes are obstacles in game, created a pipe prefab with top and bottom pipes and gap in btw ,then added PipeMovement script to move pipes from right to left, Pipes moves using transform. Translate().Random gap positions are generated so the game feels different each time. This created continuous moving obstacles for the bird.
4. PipeSpawner System :
Created a Pipespawner obj that spawns pipes at regular time interval, In the script – Pipes are spawned only when the game is active ,pipes are hidden at the start  screen and after game gets over. It means pipes apper only during game play.
---
5.Score System  :
 In this when the bird passes through pipes the scre increase by 5,  score is updated  using TextMeshPro .Here score increses smootly and displays correctly on screen. I even added   highestscore where  the score will be check with pervious score and which has highest value that will be considered as hightest score and later player have to target the highest score and beat that.
6. Game Manager:
Here in this I created a gamemanager to control the main game flow, it shows play button then start the game when the play button is on.Stop the game on game over (bird dies),even show the game over text and restart button, hides  bird and pipes before game begins. This script controls when objects appear and disappear.

7. UI Setup(Canvas) : 
UI elemenst are been added here like play button ,game over text, restart button , flappy bird title text ,Score text and these are connect to Gamemanager function and in the inspector.
8. Gameover and restart button : 
When the bird collides with a pipe:
•	Game stops.
•	Pipe spawning stops.
•	Bird movement stops.
•	Game Over text and Restart button appear.
When Restart is pressed:
•	Scene reloads.
•	Score resets.
•	Game starts fresh. This gives a clean restart experience.

9. Audio System : 
Added sound effects for:
•	Bird flap
•	Bird death, an AudioSource is attached to the bird.
10. Final result and outcome :
The final Flappy Bird game works smoothly with a proper start screen, scoring system, obstacles, sounds, and restart option.



