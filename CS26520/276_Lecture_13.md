# CS26520 Lecture 13
## What is search?
__Monday, January 29th 2018__  
Lecture: mxw@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Myra Wilson](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=mxw).

## Introduction 

A simple thought experiment: when playing a game of noughts and crosses. 

- How many possible starting moves are there? 
    - Because of the symmetry of the board, there are three possible starting moves. 
- How do you reason about where to put an O or X? 
    - 
- How would you represent this in a computer? 

## Search 

Why do we need search techniques? 
 - Finite but very lage search spaces. For example, a game of chess is played on an 8*8 board, with 32 pieces, with different pieces moving in different ways. 
    - Just looking at the starting positions options - think of it as a tree strucutre. A single nodes with 32 different possible starting moves. 
    - From each of those starting moves, there is at least another 32 moves. Very quickly there is a large problem space to explore. 
- Infinite search spaces: 
    - If you don't remove the possibility of loops in the game (moving the queen back and forth, etc.) can give an infinite problem space. 

What do we want from a search?  
- We want a solution to our problem. 
- We don't always require the optimal solution 
    - Searching for holiday options on the internet. 
    - We usually settle on a good solution. 


## Defining the Problem 

1) Start state. 
2) Goal state. (In Tic-Tac-Toe, a board that has been played.)
3) State space. 
4) Operators for moving in the state space. 
5) Test function - has goal state been reached? 
6) Measurement function - calculate the path cost? 

## Example Problem Definition 

