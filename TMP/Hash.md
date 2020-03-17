# Hash

> - just implement a complicate fuction to map the initial value to another value (specific location in the hardware to avoiding conflicting in the memory)
> - $Hash\_Function(\text{your value})=\text{new value (avoiding the scenario that after hashing, two different values have same output)}$

## Hash table

> - Search Insert Delete
>   - $O(1)$ 
>   - Worst: $O(n)$
> - Like bottom img, but when it meets conflicting, it would automatically search for next available space, if that partial is free, then inserting current value into it, elsewise, keeps going down.

## Hash list

> - Search Insert Delete
>   - $O(1)$ 
>   - Worst: $O(n)$
> - Simplier case, if the Hash value is the same with previous one, just append it to the end of the list
> - ![image-20200316180149869](/Users/jiadao/Library/Application Support/typora-user-images/image-20200316180149869.png)

# Time complexity

> - $O(1)$
>   - Since you know the hash function, given an Input, you could easliy compute the $Output=Hash\_function(Input)$
>   - But, what if, all of your $n$ data have the same hash Output? The worst case is $O(n)$. Another cause is, if using hash table, what if the program only gave out 10 free memory space but having the $11th$ input? Thus you have generate a new free larger hash table and re-do the same things. (Rehashing)
>   - As you recall, since we want to avoiding hashing conflicting, the important case is to design a good Hash Function.
> - $O(1)$ $=$ $O(constant)$
>   - Is the best time complexity
>   - ![Image result for algorithm complexity](https://miro.medium.com/max/631/1*iEbD3x2S5KOiEI6ZOltp9w.png)

