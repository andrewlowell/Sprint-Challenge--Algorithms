Add your answers to the Algorithms exercises here.

Exercise I

a)

This while loop will run up to n^3 times, but a increments by n^2, so you could say that the loop happens n^3 / n^2 times, so it runs in O(n) time.

b)

My first hunch is n^4 because there are 4 nested loops, but the number of loops the inner loops has to do decreases each time, but is that decrease just a constant so it doesn't count? So really there would be some log n in there or something, but I'm just going to say O(n^4) because you drop all of the lower-order terms :)

c)

This function will spawn n-1 function calls and nothing too complicated is happening inside, all O(1) stuff, so it runs in O(n) time.



Exercise II

One potential option would be to start either at the highest or lowest floor and just try each floor, which would work, and it would be O(n) time, but we can do better. If we cut the number of floors in half and try the middle one, then we will have eliminated half the floors after just one test, instead of eliminating just one floor after one test. So we can choose the f // 2 floor and if the egg breaks, we'll know we have to try lower, and if it doesn't, we have to try higher. We can also cut the remaining floors in half, try the middle floor, and we will have eliminated another half of the half we eliminated before, and so and and so forth until we find the cutoff point with the fewest number of eggs :) So if an egg from f // 2 breaks, we then try the middle from from the range first floor to (f // 2) floor, so (f // 2) // 2, etcetera until we find the right ones.

Complexity: O(log n)