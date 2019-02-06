# The Siruseri Singing Championship

(Zonal Computing Olympiad 2019)

The Siruseri Singing Championship is going to start, and Lavanya wants to figure out the outcome before the tournament even begins! Looking at past tournaments, she realizes that the judges care only about the pitches that the singers can sing in, and so she devises a method through which she can accurately predict the outcome of a match between any two singers.

She represents various pitches as integers and has assigned a lower limit and an upper limit for each singer, which corresponds to their vocal range. For any singer, the lower limit will always be less than the upper limit. If a singer has lower limit L and upper limit U (L < U), it means that this particular singer can sing in all the pitches between L and U, that is they can sing in the pitches {L, L+1, L+2, …, U}.

The lower bounds and upper bounds of all the singers are distinct. When two singers Si and Sj with bounds (Li, Ui) and (Lj, Uj) compete against each other, Si wins if they can sing in every pitch that Sj can sing in, and some more pitches. Similarly, Sj wins if they can sing in every pitch that Si can sing in, and some more pitches. If neither of these conditions are met, the match ends in a draw. In this problem, you can assume that no match ends in a draw.

N singers are competing in the tournament. Each singer competes in N-1 matches, one match against each of the other singers. The winner of a match scores 2 points, and the loser gets no points. But in case of a draw, both the singers get 1 point each.

You are given the lower and upper bounds of all the N singers. You need to output the total scores of each of the N singers at the end of the tournament.

## Solution hint
Since no match ends in a draw, for any pair of singers Si and Sj, one of their vocal ranges is strictly included in the other. Deduce that, across all singers, the vocal ranges form a sequence where each interval is strictly included in the previous one. You can then sort the starting points of the vocal ranges and determine how many matches each singer wins from the position of their starting point in this sorted sequence.

## Input format
The first line of of the input contains a single integer, N, which is the number of singers. N lines follow, the i-th of which contains two space-separated integers: Li and Ui, which correspond to the lower bound and upper bound of the i-th singer.

## Output format
Output a single line containing N space-separated integers, the i-th of which should be score of the i-th singer at the end of the tournament.

## Test data

```
2 ≤ N ≤ 105.
1 ≤ Li < Ui ≤ 109.
All the 2N integers (lower bounds and upper bounds) are distinct.
No matches end in a draw.
```

## Sample input 1
5
3 23
4 20
11 16
5 19
1 25

## Sample output 1

6 4 0 2 8
