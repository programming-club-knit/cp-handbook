---
title: Linear Search
---

# Linear Search

Linear Search is a searching algorithm that starts at one end and goes through each element of a list until the desired element is found. Otherwise, the search continues until the end of the dataset. It is also known as sequential search.

## Basic Algorithm

Given an Array $A$ of $n$ elements as $a_0, a_1, a_2, ..., a_{n-1}$ and there is a key value K which has to be searched in array A. i is the current index. We use the following steps:

1. Set $i$ to $0$.
2. If $a_i = K$, the search terminates successfully; return $i$.
3. Increase $i$ by $1$.
4. If $i$ < $n$, go to step $2$. Otherwise, The Search terminates unsuccessfully.

The above algorithm takes linear time to find the element, if it exists.

## Implementation In C++

```cpp
#include <iostream>
using namespace std;

// Function to perform linear search
int linearSearch(int arr[], int n, int key) {
    for (int i = 0; i < n; ++i) {
        if (arr[i] == key)
            return i; // Key found, return index
    }
    return -1; // Key not found
}

// Driver code
int main() {
    int arr[] = {10, 20, 30, 40, 50};
    int key = 30;
    int n = sizeof(arr) / sizeof(arr[0]);
    int result = linearSearch(arr, n, key);
    if (result != -1)
        cout << "Element found at index: " << result;
    else
        cout << "Element not found";
    return 0;
}
```
Output:
```
Element found at index: 2
```

## Properties Of Linear Search

1. **Complexity**: It is the simplest form of search to understand and implement.

2. **Time Complexity**:
   - **Best Case**: In the best case, Key is found at the first index. So Best case complexity is $O(1)$.
   - **Worst Case**: In the worst case, the key might be present at the end of the array, hence taking $O(n)$.
   - **Average Case**: $O(n)$

3. **Auxiliary Space**: The Linear Search uses no extra space but only one variable and the original array. $O(1)$.

4. **No Order Needed**: Linear Search is suitable for unsorted data structures.

5. **Not Suitable for Large Data Sets**: $O(n)$ is very expensive when it comes to large data sets and repetitive searches.

## Practice Problems

1. **Hacker Earth - [Find Mex](https://www.hackerearth.com/practice/algorithms/searching/linear-search/practice-problems/algorithm/find-mex-62916c25/_)**
2. **Hacker Earth - [Equal Strings](https://www.hackerearth.com/practice/algorithms/searching/linear-search/practice-problems/algorithm/equal-strings-79789662-4dbd707c/)**
3. **Hacker Earth - [Count Mex](https://www.hackerearth.com/practice/algorithms/searching/linear-search/practice-problems/algorithm/count-mex-8dd2c00c/)**
4. **Codeforces - [Effective Approach](https://codeforces.com/problemset/problem/227/B)**
5. **LeetCode - [Kth Missing Number](https://leetcode.com/problems/kth-missing-positive-number/description/)**

## Also See
- **[How to Effectively Practice CP](https://codeforces.com/blog/entry/116371)**
