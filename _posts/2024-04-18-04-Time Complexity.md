---
title: Time Complexity
---

# Introduction to Time Complexity:

An important part of competitive programming is learning the concepts of time constraints and complexities. Time Complexity refers to the estimated time an algorithm is going to take for complete execution for the given input. It can be said as a measure of efficiency of a program against the size of input or parameters. Time Complexity is an important topic because a large part of Competitive Programming is dependent on increasing efficiency of your code and that can only be accomplished by writing optimized code. Knowledge of this concept will help in finding out the most efficient method withoust applying the hit and trial method and hoping to stumble upon the solution.

## Notations of Time Complexity:

There are three main ways of representation of Complexity of a program:

1. **Big-Omega Notation $(Ω)$** - This form of representation gives the best-case time complexity. Omega Notation represents the lower bound of running time of an algorithm.

2. **Big-Theta Notation $(Θ)$** - This gives the average-case time complexity. It is a representation of the lower and upper bound of an algorithm.

3. **Big-O Notation $(O)$** - This is the worst-case time complexity and it is the most used form in competitive programming. It is the Upper limit time complexity of an algorithm. In other words, this represents the maximum time taken by an algorithm in the worst case.

**Additional Resources:**
- GFG Article: [Types of Asymptotic Notations in Complexity Analysis of Algorithms](https://www.geeksforgeeks.org/types-of-asymptotic-notations-in-complexity-analysis-of-algorithms/)
## Calculation Of Time Complexity

Knowledge of complexities of frequently used data structures and methods will certainly help in avoiding time limit exceeds

## i) Simple Loop
```cpp
for(int i=1;i<=n;i++){
    //code
}
```
The Time Complexity of simple loops is $O(n)$ because it is iterating from 1 to n.

## ii) Nested Loop-
```cpp
for(int i=1;i<=n;i++){
		for(int j=1;j<=n;j++){
			//code
		}
	}
```
The time complexity of nested loops is $O(n^2).$ The more the number of nested loops, more is the time complexity. If there were three nested loops, the complexity would have been $O(n^3).$ Thus, for i nested loops, the time complexity becomes $O(n^ⅈ).$

## iii) Multiple Loops-
```cpp
for(int i=1;i<=n;i++){
	//code
}
for(int i=1;i<=n;i++){
    //code
}

for(int i=1;i<=27;i++){
	//code
}
```
The time complexity in this case is $O(n)+O(n)+O(27) = O(2*n+27).$ In this case, the complexity can simply be written as O(n). A general rule that can be helpful is that all lower order terms with respect to the biggest term can be ignored. Also, one can ignore all leading coefficients.

For Example - 
1. $O(5n) --> O(n)$   { Leading coefficient Ignored }
2. $O(3n+25) --> O(n)$  { lower order term(25) ignored and coefficient also ignored }
3. $O(5n^2+2n+6) --> O(n^2)$  { both lower order terms(2n and 6) are ignored and $coefficient(5)$ is also ignored }

## iv) Multiple Variables-
```cpp
for(int i=1;i<=n;i++){
	for(int j=1;j<=m;j++){
		//code
	}
}
```
Time Complexity – $O(n*m)$

# Time Complexities of Algorithms

These are the most common and most used time complexities used to represent an algorithm. Another point to note is that higher a complexity is on the list, the better it is.

## 1. Constant-Time – $O(1)$

A constant operation does not depend on the input size. Basic operations like addition, subtraction, division etc. fall in this category.

## 2. Logarithmic Time – $O(log n)$

For an algorithm exhibiting logarithmic time complexity, the size of the target array or vector decreases by a factor of 2. The most Important example of Logarithmic Algorithm is –
- **Binary Search**
  - [GFG Article](https://www.geeksforgeeks.org/binary-search/)
  - [Video Tutorial](https://youtu.be/fDKIpRe8GW4?si=BfF5vFq6GpcOHgcZ)

## 3. Square Time – $O(√n)$

This lies between the complexities exhibited by Linear Algorithms[ $O(n)$ ] and Logarithmic Algorithms[ $O(log(n))$ ]. One of the most used examples is finding out prime numbers. This method will not be asked directly in any question but will be used extensively in many intermediate steps of many problems.

## 4. Linear Time – $O(n)$

Algorithms with linear time complexity go through the array or vector and its examples include iterating through the array or vector for a specific element.
### Resources:
- [GFG Article](https://www.geeksforgeeks.org/linear-search/)
- [Video Tutorial](https://youtu.be/246V51AWwZM?si=jUsQ2v90cfqESrpd)

## 5. Linearithmic Time – $O(nLogn)$

This complexity is used in complex sorting algorithms like Merge Sort, Quick Sort, and Heap Sort.
### Examples:
- **Merge Sort**
  - [GFG Article](https://www.geeksforgeeks.org/merge-sort/)
  - [Video Tutorial](https://youtu.be/4VqmGXwpLqc?si=Ma4vAO5slqHIv4F6)
- **Quick Sort**
  - [GFG Article](https://www.geeksforgeeks.org/quick-sort/)
  - [Video Tutorial](https://youtu.be/Hoixgm4-P4M?si=Wv_qA9RCsNRU_hU4)

## 6. Quadratic Time – $O(n^2)$

This is used in relatively simpler sorting algorithms like bubble sort, selection sort, etc.
### Resources:
- [Selection Sort](https://www.geeksforgeeks.org/selection-sort/)
- [Bubble Sort](https://www.geeksforgeeks.org/bubble-sort/)
- [Insertion Sort](https://www.geeksforgeeks.org/insertion-sort/)
### Video Tutorials:
- [Selection Sort](https://youtu.be/xli_FI7CuzA?si=6BJ06Qlc0zEtVw7g)
- [Bubble Sort](https://youtu.be/g-PGLbMth_g?si=AB4Eh7gbN2ATfPUp)
- [Insertion Sort](https://youtu.be/JU767SDMDvA?si=IeNCKpFvQU8JOdms)

## 7. Polynomial Time Complexity – $O(n^k)$

Algorithms with polynomial time constraints have runtime proportional to input raised to the power of $k$, where $k$ is positive. An example can be nesting of loops $k$ times.

## 8. Exponential Complexity – $O(2^n)$

Algorithms with exponential complexity have a rapidly increasing runtime as input increases. Recursive Algorithms generally exhibit this complexity and its many calls are responsible for its complexity.

## 9. Factorial Time Complexity – $O(n!)$

Runtime increases factorially with respect to input size. Permutations and brute-force algorithms have this type of complexity.

# Estimation Of Problem Before Solving

Estimating time complexity of an algorithm before implementation can help in finding out if the solution is optimized or efficient enough to pass the test cases or not. For a particular problem, it can be said that an online compiler has the capability of running $10^7$ iterations (this is an estimation, not an exact figure) in one second. So, if the input is of the range of $10^5$ and $O(η^2)$ is used with a 1 second time limit, the algorithm will perform $10^5*10^5 =  10^{10}$ operations, which is outside the permissible time limit.

The following table contains some useful estimates for solving problems on online coding websites:

| Size Of Input | Time Complexity |
|---------------|-----------------|
| $n ≤ 10$       | $O(n!)$           |
| $n ≤ 20$        | $O(2^n)$          |
| $n ≤ 500$       | $O(n^3)$          |
| $n ≤ 5000$     | $O(n^2)$         |
| $n ≤ 10^4$     | $O(nLogn)$       |
| $10^4 ≤ n ≤ 10^6$ | $O(n)$          |
| $n ≥ 10^6$     | $O(Logn)$        |

These are not the exact figures because a quadratic expression can also perform some linear tasks and that is not included in the calculation of the time complexity. Similarly, any higher order function can have many lower order functions which increase its complexity even though they are not considered in the calculations.
