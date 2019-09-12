# Amazons
## Setup
Initially, there are several queens in a chessboard. In this project, we will work with the following initial state:
<br>
<p align="center">
<img align = "center" src="https://raw.githubusercontent.com/pgmpablo157321/Amazons/master/initial.png">
</p>
<br>
A 6 x 6 chessboard with 2 white and 2 black queens positioned as shown in the picture. However, we could do slight modifications to the code and change the initial state of the game.

## Rules

The rules of the game are very simple. Two players (black and white) take turns until one of them cannot play anymore.
### Turn
##### Moving
At the beginning of the turn, the player moves one of his/her queens in the way they move in chess (vertically, horizontally or diagonally as many spaces as they want). However the queens can't go through another queen nor take any the enemy's queens as you can do in chess. For example, here are all the possible movements for one queen in the initial state:
<br>
<p align="center">
<img align = "center" src="https://raw.githubusercontent.com/pgmpablo157321/Amazons/master/move.png">
</p>



##### Blocking
<br>
After the player has moved a queen, he/she blocks a space in the board. But the player can only block the places where the queen that most recently moved can reach in one extra move. For example:
<br>
<p align="center">
<img align = "center" src="https://github.com/pgmpablo157321/Amazons/blob/master/block_options.png?raw=true">
</p>
<br>
Here the player has move one of the white queens, and can block any of the orange spaces.
In the next ilustration, the player has already blocked:
<br>
<p align="center">
<img align = "center" src="https://github.com/pgmpablo157321/Amazons/blob/master/block.png?raw=true">
</p>
<br>

##### Note
Notice that the next player cannot move through the blocked space nor the other queens.
<br>
<p align="center">
<img align = "center" src="https://github.com/pgmpablo157321/Amazons/blob/master/nextMove.png?raw=true">
</p>
<br>
The same rule applies to blocking

## Approach


## Heuristic
