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
The same rule applies to blocking.

For more in depth description of the rules of the game, click [here](https://en.wikipedia.org/wiki/Game_of_the_Amazons)

## Approach
We will aproach this problem by using a minimax algorithm and by making it more efficient with an alfa-beta prunning. For a description of these: [minimax](https://en.wikipedia.org/wiki/Minimax) and [alfa-beta prunning](https://en.wikipedia.org/wiki/Alpha%E2%80%93beta_pruning)

Notice that the [tree of the game](https://en.wikipedia.org/wiki/Game_tree) at the beggining is very large (particularly very wide). In fact, the first player has 468 possible moves for her/his first turn! That is kind of a problem since we can't see very far in the tree. However notice that as the game progresses the number of possible moves tends to shrink, since there are more blocked spaces (meaning less spaces where to move!). So the final algorithm that plays the game will call the minimax algorithm with a depth in function of the number of not blocked space in the game.

## Heuristic
In order to use the minimax algorithm, we need a good heuristic to evaluate how good is a state of the game. After a lot games played, the following heuristic was proposed:

The main goal of the heuristic is to recognize which spaces of the board "belong" to each player. The player with more spaces will be able to make more moves than the other player and will win the game. To achieve that, we define the following funtion: $F(T,Q,x,y)$
\frac{\sigma}{\mu}
