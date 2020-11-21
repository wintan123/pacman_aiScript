
#Pac-Man Algorithm Script
The project builds a Pac-Man AI script based on a variant of Dijkstra's algorithm.<br>
The script is written in ai.c which is based on the heuristic.<br>

##Program Execution
To run the project, clone the repository and compile using the make file by the command: *make*

<br>

The program runs by the command : *./pacman <level> <ai/ai pause> <max/avg> <budget>*
<br>
where
<br>
* level is 0-9 for standard levels, or the path to a file.dat level
* ai pause calls your algorithm and pauses the game to allow playing one step at a time.
* <max=avg> is either max or avg, to select the 2 options for propagating scores
* <budget> is an integer number indicating the budget of your search.

---
The code is injected to the Pac-Man game who is created by the original owner as below.
---

Pacman For Console
------------------
Okay, so basically, I got tired of enabling flash on my browser so that I could play Pacman.
That, and I was extremely bored one night. So I decided to make my own Pacman... for Console.

Licenseing Information
----------------------
See COPYING for details on the GNU/GPL

Compile/Install
---------------
To make... gee... let's see. type 'make'
To install... type 'make install'
To run...type 'pacman [level_#]'          where # is 1-9, for a premade level
    OR   type 'pacmac [level_file_name]'  for a custom level you made
To uninstall... type 'make uninstall'
    i.e.:
        make && su -c "make install"
        pacman 3                                        # Start @ level 3
        pacman /usr/share/pacman/Levels/level07.dat     # Play only level 7
        echo ":-( I don't like it." && make uninstall   # Uninstall :-(

The ASCII art:
--------------
C	-	Pacman - That's you.
&	-	Ghosts - Boo.
.	-	Pellet - Yummy. Collect all of them to pass to the next level.
*	-	Power pellet - Makes you invincible for a short while.
	-	Wall - No one can walk through it.
	-	Blocker - A.K.A. Ghost wall. Only the Ghosts can walk through this.


13 Basics Playing Rules
-----------------------
In case you don't know the rules of Pacman (rules I programmed in), here are most of them
1) Pacman must collect all the pellets of food in the maze. 1 point per pellet.
2) Big pellets make Pacman invincible for a short amount of time.
3) If Pacman touches a ghost without being invincible, he dies and loses 1 life.
4) If Pacman touches a ghost while invincible, the ghost is sent back to its starting point.
5) Points are awarded for each ghost eaten in a row while invincible: 20, 40, 80, 160 (10*2^x).
6) Pacman cannot go through the Ghost Walls (Blockers).
7) Ghosts cannot turn completely around unless there is no other option.
8) While Pacman is invincible, Ghosts will be a bit slower and tend to stay away from him.
9) While Pacman is NOT invincible, Ghosts will tend to come toward him.
10) Pacman starts with 3 extra lives, once all three are gone, the game is over.
11) Extra lives are awarded at 1000 points, 2000, 4000, 8000... (500*2^x).
12) If any character reaches a border of the maze, it will be transported to the opposite side.
13) Each character can only go in one X or Y direction at a time.

To make your own levels, see Levels/README

Contact Information
-------------------
Send comments and levels you have made to: michaelbillars@gmail.com
I would love to include more levels.