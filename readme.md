Sudoku solver (reason for creating this program is basic understand of go concept)

Backtracking is an algorithm for finding all (or some) of the solutions to a problem that incrementally builds candidates to the solution(s).


Build:
go build sudoku.go

Run:
./sudoku ...1.5.68......7.19.1....3...7.26...5.......3...87.4...3....8.51.5......79.4.1...

Explanation:

![Sudoku](https://hackernoon.com/hn-images/1*dFNtAnfevAa9wP-VQ10oXQ.png)

1. Define empty coordinates (x,y) ((1,2) (2,2) (2,3) (3,1) (3,2))

2. Select first empty spot (1,2) 
3. Add first possible value  (1) - and verify (it's match)
4. Go to the next empty spot (2,2)
5. Add first possible value (1) - verify (not matched) - then second (2) - match)

![Sudoku](https://hackernoon.com/hn-images/1*-ZfNe5ATHjC5ew08rlKweg.png)

6. Go to next empty spot (2,3) - 1 - 2 and 3 is not valid - so if every values not working than back to (2,2)

7. Fill 3 in (2,2) - then 2 to (2,3)

![Sudoku](https://hackernoon.com/hn-images/1*6QuUVfx8BLw9XeaiTCCR8Q.png)

8.Repeating that process until will either reach the goal or we hit one of the termination conditions.

______

Works in animation in bigger scale:

![Sudoku](https://upload.wikimedia.org/wikipedia/commons/8/8c/Sudoku_solved_by_bactracking.gif)


sources:
https://github.com/nticaric/sudoku-solver