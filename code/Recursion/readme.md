## Recursion 

https://recursion.vercel.app

Recursion is a technique in which a function calls itself, breaking problems down into simpler instances of the same problem. It's fundamental in solving problems like tree traversals and combinatorial tasks.

- Head Recursion
- Tail Recursion

## How do check if a Coding Problem can be solved using Recursion?

*The best thing is to break the problem into a smaller set and see if the smaller problem is the same as the original problem or not like in order to calculate a factorial of 5, does it helps to calculate a factorial of 4? This may be a guide to see if Recursion can be used or not.*

## Steps to solve a Coding problem using Recursion

Once you have identified that a coding problem can be solved using Recursion, You are just two steps away from writing a recursive function.

  1. Find the base case
  2. Finding how to call the method and what to do with the return value.

### Top Questions to Practice for Recursion

| Sr. No. | Problems | code
| --------| ---------|------|
| 01. | Factorial & Fibonacci |
| 02. | Power |
| 03. | Product of Array |
| 04. | Palindrome Check |
| 05. | Tower of Hanoi | 
| 06. | Catalan Numbers |
| 07. | Merge Sort |
| 08. | Quick Sort |
| 09. | Combination Sum |
| 10. | Combination Sum II | 
| 11. | Subset Sum |
| 12. | Subset Sum II |
| 13. | Print all Combinations of a String/Array |
| 14. | Palindrome Partitioning |
| 15. | Phone Keypad Problem |
| 16. | Rat in a Maze Problem |
| 17. | Height of a Binary Tree |
| 18. | Sort an Array/Stack |
| 19. | Delete middle element of a Stack |
| 20. | Reverse a Stack |
| 21. | Kth Symbol in Grammar |
| 22. | Print Subsets/Power Sets/Print Subsequences |
| 23. | Print Unique Subsets and Variations |
| 24. | Permutation with Spaces |
| 25. | Permutation with Case Change |
| 26. | Letter Case Permutation |
| 27. | Generate all Balanced paranthesis |
| 28. | Print N-bit binary numbers having more 1’s than 0’s for any prefix |
| 29. | Josephus Problem | 
| 30. | Greatest Common Division GCD using Euclid’s algorithm |
| 31. | Nine Queen problem in chess using Recursion | 
| 32. | Minimum Cost path in a Matrix |
| 33. | Word Search |
| 34. | Tiling Problem |
| 35. | Friends Pairing Problem |



### Solution to Top Problems in Recursion 


//POWER SOLUTION
```js
function power(base, exponent){
    if(exponent === 0) return 1;
    return base * power(base,exponent-1);
}
```

//FACTORIAL SOLUTION
```js
function factorial(x){
   if (x < 0 ) return 0;
   if (x <= 1 ) return 1;
   return x * factorial(x-1);
}
```

//PRODUCT OF ARRAY SOLUTION
```js
function productOfArray(arr) {
    if(arr.length === 0) {
        return 1;
    }
    return arr[0] * productOfArray(arr.slice(1));
}
```
//RECURSIVE RANGE SOLUTION
```js
function recursiveRange(x){
   if (x === 0 ) return 0;
   return x + recursiveRange(x-1);
}
```

//FIBONACCI SOLUTION
```js
function fib(n){
    if (n <= 2) return 1;
    return fib(n-1) + fib(n-2);
}
```
