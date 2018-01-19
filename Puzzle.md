Puzzle Links \
[Lawrence Puzzles](https://www.teamten.com/lawrence/puzzles/)

# Airplane Seats Puzzle

## Description
100 passengers in line, boarding an airplane 100 seats, one at a time. There are no particular order. 
Each one has his own seat assigned on the ticket. The first guy is drunk and can sit whichever seat. 
Any one of the rest passengers follows this rule:

1. If his seat is unoccupied, sit on it.
2. If his seat is occupied, sit on a random one.

Question: what is the probability that the last person sits in his own seat.


## Idea
WLOG, number the 100 passengers from 1 to 100. If the first passenger sit on 1 or 100th, the answer is straightforward. The next discussion
exclude these two scenarios.
Suppose he sit on n-th seat:
1. for 2th to (n-1)-th psg, they have their own seats.
2. for n-th passenger, he has actually "3" choices: sit on 1st seat, sit on 100th seat, and sit on other seats.
3. if he sits on 1-st seat, everyone in the following will have their own seat; if he sits on 100th seats, everyone except the last person
have their own seats; if he sits on any other seat, say k, then k-th person will face the exactly same situation as he does.
4. As long as the key question is still hanging on there (the 100th seat is not occupied yet), any passenger who found his seat occupied 
has three choices: 1st, 100th, or "others". The "others" are transient state (recall the markove chain), and we are only concerned 
whether 1st or 100th is chosen by him. By symmetry, the answer is straightforward.


# Picture Boards

## Description
A company keeps two corkboards in the lobby to  displays the pictures of current exployees. The pictures are ordered by start day of
the employee, putting the most senior in the upper-left of the first corkboard, filling it up, and then starting on the second corkboard.
When an employee quits, his picture is removed and everyone else shifts over.\
\
You just started, and the two boards are full, with 150 pictures on each board. You observe that one person starts per week and one person quits per week. Currently you are on the lower-right on the 2nd board, how long will you wait on average to get on the first board.  

## Idea
For each shift, the time it takes follows a negative-binomial distriution based on the current position.


# Two Marbles

## Description
Puzzle: You are given two marbles and a 100 story building. There’s a floor where dropping a marble from that floor or any floor above it will cause the marble to break, but dropping a marble from any floor below it will not cause breakage. You want to devise an algorithm that will minimize the maximum number of drops needed to find that floor. With one marble, you can do no better than 100, but with two it is easy to improve on that. What is the fewest number of drops of the two marbles that will find the break floor, not knowing in advance where it is between 1 and 100?
