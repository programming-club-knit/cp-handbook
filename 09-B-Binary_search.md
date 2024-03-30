# Binary Search
Binary Search is defined as a searching algorithm used in a sorted array by repeatedly dividing the search interval in half. The Idea of Binary search is to use the information that the array is sorted and reduce the time complexity to $O(log N)$.

It a powerful tool in various problems as it can be used in a versatile way to find Lower bound, upper bound, search on arbitrary predicate, Binary Search on answer etc.

### Conditions:
```
1.	Data structure Must be Sorted.
2.	Access to any element of the data structure takes constant time.
```

## Basic Binary Search Algorithm

Given an array $A$ of $n$ elements with $a_0,a_1,a_2, ...,a_{n-1}$ sorted such that $a_0 \le a_1 \le a_2 \le a_3 \le .... \le a_{n-1},$ a key value $k$. Then Following steps are taken to Search $k$ in $A$.
<br>
1. Set $L$ to 0 and $R$ to $n-1$.
2. If $L > R$ , the search terminates as unsuccessful.
3. Set $m$ (the position of the middle element) to the floor of $\frac{L+R}{2}$.
4. if $a_m < k$, set $L$ to $m+1$ and go to step 2.
5. if $a_m > k$, set $R$ to $m-1$ and go to step 2.
6. Now $a_m = k$, The search is done; return $m$.


The iterative procedure keeps track of the search boundaries with the two variables $L$ (Lower Boundary) and $R$ (Upper Boundary). 

## Implementation
There are two ways to implement the binary search, Iteratively and Recursively. 
We here take Iterative approach : 

```cpp
// C++ program to implement iterative Binary Search
#include <bits/stdc++.h>
using namespace std;
 
// An iterative binary search function.
int binarySearch(int arr[], int l, int r, int x)
{
    while (l <= r) {
        int m = l + (r - l) / 2;
 
        // Check if x is present at mid
        if (arr[m] == x)
            return m;
 
        // If x greater, ignore left half
        if (arr[m] < x)
            l = m + 1;
 
        // If x is smaller, ignore right half
        else
            r = m - 1;
    }
 
    // If we reach here, then element was not present
    return -1;
}
 
// Driver code
int main(void)
{
    int arr[] = { 2, 3, 4, 10, 40 };
    int x = 10;
    int n = sizeof(arr) / sizeof(arr[0]);
    int result = binarySearch(arr, 0, n - 1, x);
    (result == -1)
        ? cout << "Element is not present in array"
        : cout << "Element is present at index " << result;
    return 0;
}
```

#### Output
```
Element is present at index 3
```
The Iterative approach is used most of the time as they are easy to debug and work with.

#### Recursive approach:
<details><summary>For Recursive Approach Click Here</summary>
  
  ```cpp
  // C++ program to implement recursive Binary Search
#include <bits/stdc++.h>
using namespace std;
 
// A recursive binary search function. It returns
// location of x in given array arr[l..r] is present,
// otherwise -1
int binarySearch(int arr[], int l, int r, int x)
{
    if (r >= l) {
        int mid = l + (r - l) / 2;
 
        // If the element is present at the middle
        // itself
        if (arr[mid] == x)
            return mid;
 
        // If element is smaller than mid, then
        // it can only be present in left subarray
        if (arr[mid] > x)
            return binarySearch(arr, l, mid - 1, x);
 
        // Else the element can only be present
        // in right subarray
        return binarySearch(arr, mid + 1, r, x);
    }
 
    // We reach here when element is not
    // present in array
    return -1;
}
 
// Driver code
int main()
{
    int arr[] = { 2, 3, 4, 10, 40 };
    int x = 10;
    int n = sizeof(arr) / sizeof(arr[0]);
    int result = binarySearch(arr, 0, n - 1, x);
    (result == -1)
        ? cout << "Element is not present in array"
        : cout << "Element is present at index " << result;
    return 0;
}
  ```
</details>

<br>


## Complexity  Analysis

 - ### TimeComplexity: 
    - **Best Case**: $O(1)$
    - **Average Case**: $O(log N)$
    - **Worst Case**: $O(log N)$
- **Auxiliary Space**: $O(1)$, If recursive stack is considered then auxiliary space will be $O(log N)$.


We have seen Basics of Binary Search now its Applications.

## Lowerbound 

Lowerbound is defined as the position of the first element that is not less than $k$.
Where $k$ is the key.

CPP already has  STL function [`lower_bound()`](https://www.geeksforgeeks.org/lower_bound-in-cpp/) for finding lower bound in an already sorted data structure. But one should implement it on there own for better standing :
        
[Problem : Find the Lowerbound in $O(log N)$ time](https://leetcode.com/problems/search-insert-position/solutions/15371/my-understanding-of-lower-boundupper-bound-binary-search-in-c-thanks-to-two-post/)

## UpperBound 

In an sorted datastructure upperbound of $k$ is the position of the first element that is greater than $k$ . Where $k$ is the key.

similar to [`lower_bound()`](https://www.geeksforgeeks.org/lower_bound-in-cpp/) there is [`upper_bound()`](https://www.geeksforgeeks.org/upper_bound-in-cpp/) function, but one should try to implement it first on their own before using it in CP.

[Problem : Find upper and lower bound of . . . . . . . . .](https://www.hackerearth.com/problem/algorithm/binary-search-basic/)

## Advanced topics
- [Overview on all Topics](https://cp-algorithms.com/num_methods/binary_search.html)
- [Binary Search On Answer](https://www.geeksforgeeks.org/binary-search-on-answer-tutorial-with-problems/)
- [Binary Search On Predicate](https://www.geeksforgeeks.org/binary-search-intuition-and-predicate-functions/)

## Practice Problems
These cover almost all binary search topics :
- [LeetCode - Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
- [LeetCode - Search Insert Position](https://leetcode.com/problems/search-insert-position/)
- [LeetCode - First Bad Version](https://leetcode.com/problems/first-bad-version/)
- [LeetCode - Valid Perfect Square](https://leetcode.com/problems/valid-perfect-square/)
- [LeetCode - Find Peak Element](https://leetcode.com/problems/find-peak-element/)
- [LeetCode - Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- [LeetCode - Find Right Interval](https://leetcode.com/problems/find-right-interval/)
- [Codeforces - Interesting Drink](https://codeforces.com/problemset/problem/670/D1)
- [Codeforces - Magic Powder - 1](https://codeforces.com/problemset/problem/670/D1)
- [Codeforces - Another Problem on Strings](https://codeforces.com/problemset/problem/165/C)
- [Codeforces - Frodo and pillows](https://codeforces.com/problemset/problem/760/B)
- [Codeforces - GukiZ hates Boxes](https://codeforces.com/problemset/problem/551/C)
- [Codeforces - Enduring Exodus](https://codeforces.com/problemset/problem/645/C)
- [Codeforces - Chip 'n Dale Rescue Rangers](https://codeforces.com/problemset/problem/590/B)

