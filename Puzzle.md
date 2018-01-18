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