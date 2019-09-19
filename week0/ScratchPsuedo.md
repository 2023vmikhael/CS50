Title: STARFISH SPRITE

<br>When green flag is clicked;
	Set size to [70]<br>

When [space key] clicked;
	Wait [1.5] seconds;
	Go to x: -192 y: -126;
		Switch costume to [Starfish-a];
		Wait [0.05] seconds;
	Switch costume to [Starfish-b]

When I recieve [hide when you win screen is recieved];
	Forever (loop);
	Hide 

When green flag is clicked;
	Hide

When I recieved [show everything]; 
	Show 

When [right arrow] key is pressed; 
	Change x by 10

When [left arrow] key is pressed; 
	Change x by -10

When green flag is clicked;
	Hide;
	Show variable [score];
Wait [2.5] seconds;
Show;
Set score to [0]

When green flag is clicked;
Go to x -192 y: -126

When I recieve [start game];
Forever (loop); 
If [key space pressed?] then (loop); 
Repeat [10] (loop); 
	Change x by 13.5;
	Change y by 13.5;
Repeat [10] (loop); 
	Change x by 13.5;
	Change y by -13.5;
[Forever (loop), If/Then (loop), and Repeat (10) (loop) close]

When I recieve [you win]; 
	Hide

When I recieve [game over];
	Hide

When green flag is clicked;
	If (not [touching shark] then;
	Wait 1 [second] 

Title: SHARK SPRITE <br>

When green flag is clicked;
	Set size to [47]%

When green flag is clicked;
	Go to x: 0 y:-145;
	Show

When green flag is clicked;
Forever (loop);
 	If (touching [starfish]?) then;
Broadcast [game over];
	Switch backdrop to [game over]
	If/Then (loop closed);
Forever (loop closed) 

When I recieve [game over];
	Hide 

When green flag is clicked;
	Hide;
Wait [1.5] seconds;
Show

When I recieve [new shark];
Forever (loop);
Hide;
Wait [1.5] seconds;
Forever (loop closed)

When [space] key is clicked;
	Change score by [1];
	Broadcast [new shark]

When I recieve [new shark];
	Forever (loop);
	Show;
Wait [1] second;
	Hide;
Wait [1] second;
Show;
Set x to [240];
Set y to [-160];
Glide [1] secs to x: 0 y: -145
When green flag is clicked;
Forever (loop);
If ([score] =  [10]) then;
Wait [1] seconds;
	Switch backdrop to [Light];
	Broadcast [hide when you recieve you win screen];
Forever (loop closed);
	If/Then (loop closed)

Define [maximum score 10];
	If [score=10] then;
	Broadcast [you win]

When I recieve [hide when you win screen is recieved];
	Forever (loop);
	Hide;
Forever (loop closed)

When I recieve [you win];
Hide

When I recieve [you win];
If [score=10] then;
Switch backdrop to [Light];
Hide;
Maximum score [10]

Title: BACKDROP CODING <br>

When green flag is clicked;
	Switch backdrop to [start game] and wait;
	Broadcast [start game]

When I recieve [you win];
	Switch backdrop to [Light]

When stage is clicked; 
	Switch backdrop to [underwater 1];
	Broadcast [show everything]

When I recieve [show everything];
	Switch backdrop to [underwater 1]
