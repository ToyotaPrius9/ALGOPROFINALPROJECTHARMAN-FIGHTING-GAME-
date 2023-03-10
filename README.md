Brief Description

“Jojo’s Bizarre Adventure: Heritage of the future” is a popular arcade style action fighting game in gaming consoles and has made its way to one of the most popular fighting games. Along with it’s games, Jojo’s bizarre adventure had also developed a very popular action-style show series. Jojo’s Bizarre Adventure was the last popular fighting game which had not switched to 3D style yet and kept its 2D fighting style unlike their competitors with high definition 3D graphics in the Playstation 3 era. I personally enjoy playing quick-paced fighting games such as Jojo's Bizzare Adventure: Heritage Of The Future and many more, so the thought of creating a replica of this particular game came to as a first choice to me. 

In a typical fighting game (in story/single player mode), a player would be fighting a bot in a 1 versus 1 match and the last man/bot standing wins, the game i have attempted in making for this project suits that category and shares the same theory as that. For this game, I have tried to make my own small copy of Jojo’s Bizarre Adventure: Heritage Of The Future, the similarities they share are the characters and some attack moves of the characters. 

This game contains three attacks for the boss and three attacks for the player, whereas the player gets a special ultimate attack.




-
-
-
-
-
-
-


Use-Case Diagram:

![image](https://user-images.githubusercontent.com/114371673/213071100-e52c69ee-5efb-4284-bcb8-5c827de3e1a0.png)

When the user launches the game, they will see the start screen wherein they can move around the player sprite and click to play the game. Once they play the game, the outcome will be the only result to either the player or the bot reaching 0 HP, when that outcome happens, they will be directed to the game over screen where they will see a message on the screen, if mouse clicked: it will exit the program.

-
-
-
-
-
-
-
-
-

Activity Diagram:

![image](https://user-images.githubusercontent.com/114371673/213071191-5a345c60-6a52-47d0-97bd-3a8e9f82aa9e.png)

-
-
-
-
-
-
-
-
-
-
-

Class Diagram:

![image](https://user-images.githubusercontent.com/114371673/213071354-6e81deec-4168-4fcb-b0ea-397779cab3fc.png)

The Arrows Connecting Represents The “Belongs To” Factor. Ora, Attack1, Attack2 belongs to Boss & pygame. Bullet, muda, Knives belongs to Player and pygame. Whereas Boss and Player belongs to Pygame. In the pygame class diagram we can see all classes under pygame, and for the rest of the classes we can see the functions defined under them. For instance, the class “Player” have the functions of player_input, apply gravity, animation_state and update. 



-
-
-
-
-
-
-
-
-
Modules:

Pygame: 
			This module is the core of this 
			Game. Pygame is a module which
			Exists for providing multiple 
			Convenient libraries for 2D game 
			Creations. Pygame was used for
			Multiple things ranging from 
			Loading models to playing sound
			to making a whole window.

Random:
			This module serves the purpose of 
			Creating random integers in any
			way or form factor desired, this 
			Module was used for the move-
			ment mechanics and attacking
 			mechanics of the boss.

Sys: 
			This module was used for its 
			Function to exit the program using
			sys.exit(). This module might’ve 
			Been unnecessary since pygame
			May already have something 
			Similar, but i did use this out of 
			pure self-preference.


Essential Algorithms:

StartScreen 
- If mouseclicked, move to GameLoop, If not mouseclicked, stay.

GameLoop
- If player stops time, change 
Background to yellow, if not stopped
Time, keep background image.

- If player health or boss health 
decreases, minus their health bar.

- If neither player or boss has 0 HP,
stay in the game loop.

- If either player or boss reaches 0 HP, move to EndScreen.



EndScreen
- If mouseclicked, close the program.
- If not mouseclicked, stay in EndScreen



Player2(class) 
- If user presses A and D at the Same time, movement speed is 0.
				
- If user holds G to the point of the
The ending animation index, time Stop status set to True.

- If only the player is on the ground, enable them to jump.

- If only the attack cooldown is 0, player may use their attack ability.

- If 10  seconds has passed after timestop ability, timestop is set to False.

- If user gets to the end of the Screen, keep making them stay in one place.



Boss(class)	
- Boss movements and attacks must only happen if timestop is False.
			
- Boss must jump to dodge the player’sBullet attack when it comes too close.

- Boss must move right at all costs if it Detects for itself to be at the left of the Player2(class)’s position.
	
- Boss must stay in position if detects it is going out of the screen.

- Ora(class) & Muda(class): Remove from screen if Went too far from Parent class’s attack position.
			




ScreenShots: 
- Start Screen

![image](https://user-images.githubusercontent.com/114371673/213073461-305d141e-21c2-4bba-bedd-90c3ab29ef52.png)


-Game Play Screen

![image](https://user-images.githubusercontent.com/114371673/213073460-33359128-c1e7-4684-8aa5-14a49eef7cfd.png)

-Game End Screen (Win)

![image](https://user-images.githubusercontent.com/114371673/213073524-324467b3-932e-420e-bca3-0e3b43b0a042.png)

-Game End Screen (Lose)

![image](https://user-images.githubusercontent.com/114371673/213073754-cd5337dd-9a5b-484f-8402-944be5bcca5a.png)


Lessons Learned:

Before the creation of this game, i was not too experienced with pygame sprites, i always did have a discomfort working with them since i used to find difficulties in obtaining certain values of sprites (inside of the game loop) but as i went deeper into the creation of this game, i found it really interesting on how sprite mechanics worked and learned useful knowledge on how to obtain desired values from sprites, these desired values include the constantly updating values of the sprite’s X position, or any variable stored inside of this sprite class, or even sprites which comes as a bunch of listed values (such as the bullet class for this matter). Another side-skill I have obtained is the functioning methods of implementing animation frames to the point that I can even enable a function to play when an animation reaches a certain point. 



Video Demo:



(lowering of volume is recommended)
https://drive.google.com/file/d/1AkZE0M6MS0OWjBRR_V36LK5QpVVHpas3






