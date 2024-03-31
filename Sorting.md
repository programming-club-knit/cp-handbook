> **[Sorting]{.underline}**
>
> A Sorting Algorithm is used to rearrange a given array or list of
> elements according to a comparison operator on the elements.
>
> Many efficient algorithms use sorting as a subroutine, because it is
> often easier to process data if the elements are in a sorted order.
>
> For example, the problem "does an array contain two equal elements?"
> is easy to solve using sorting. If the array contains two equal
> elements, they will be next to each other after sorting, so it is easy
> to find them.
>
> There are many ways to sort but let's learn some sorting algorithms-

**[Selection Sort --]{.underline}**

-   
-   
-   

***Selection sort** is a simple and efficient sorting algorithm that
works by repeatedly selecting the smallest (or largest) element from the
unsorted portion of the list and moving it to the sorted portion of the
list. *

*The algorithm repeatedly selects the smallest (or largest) element from
the unsorted portion of the list and swaps it with the first element of
the unsorted part. This process is repeated for the remaining unsorted
portion until the entire list is sorted*

## [Selection Sort Algorithm]{.underline}

*Lets consider the following array as an example: **arr\[\] = {64, 25,
12, 22, 11}***

## For C++ -

+-----------------------------------------------------------------------+
| // C++ program for implementation of                                  |
|                                                                       |
| // selection sort                                                     |
|                                                                       |
| #include \<bits/stdc++.h\>                                            |
|                                                                       |
| using namespace std;                                                  |
|                                                                       |
|                                                                       |
|                                                                       |
| // Function for Selection sort                                        |
|                                                                       |
| void selectionSort(int arr\[\], int n)                                |
|                                                                       |
| {                                                                     |
|                                                                       |
|     int i, j, min_idx;                                                |
|                                                                       |
|                                                                       |
|                                                                       |
|     // One by one move boundary of                                    |
|                                                                       |
|     // unsorted subarray                                              |
|                                                                       |
|     for (i = 0; i \< n - 1; i++) {                                    |
|                                                                       |
|                                                                       |
|                                                                       |
|         // Find the minimum element in                                |
|                                                                       |
|         // unsorted array                                             |
|                                                                       |
|         min_idx = i;                                                  |
|                                                                       |
|         for (j = i + 1; j \< n; j++) {                                |
|                                                                       |
|             if (arr\[j\] \< arr\[min_idx\])                           |
|                                                                       |
|                 min_idx = j;                                          |
|                                                                       |
|         }                                                             |
|                                                                       |
|                                                                       |
|                                                                       |
|         // Swap the found minimum element                             |
|                                                                       |
|         // with the first element                                     |
|                                                                       |
|         if (min_idx != i)                                             |
|                                                                       |
|             swap(arr\[min_idx\], arr\[i\]);                           |
|                                                                       |
|     }                                                                 |
|                                                                       |
| }                                                                     |
|                                                                       |
|                                                                       |
|                                                                       |
| // Function to print an array                                         |
|                                                                       |
| void printArray(int arr\[\], int size)                                |
|                                                                       |
| {                                                                     |
|                                                                       |
|     int i;                                                            |
|                                                                       |
|     for (i = 0; i \< size; i++) {                                     |
|                                                                       |
|         cout \<\< arr\[i\] \<\< \" \";                                |
|                                                                       |
|         cout \<\< endl;                                               |
|                                                                       |
|     }                                                                 |
|                                                                       |
| }                                                                     |
|                                                                       |
|                                                                       |
|                                                                       |
| // Driver program                                                     |
|                                                                       |
| int main()                                                            |
|                                                                       |
| {                                                                     |
|                                                                       |
|     int arr\[\] = { 64, 25, 12, 22, 11 };                             |
|                                                                       |
|     int n = sizeof(arr) / sizeof(arr\[0\]);                           |
|                                                                       |
|                                                                       |
|                                                                       |
|     // Function Call                                                  |
|                                                                       |
|     selectionSort(arr, n);                                            |
|                                                                       |
|     cout \<\< \"Sorted array: \\n\";                                  |
|                                                                       |
|     printArray(arr, n);                                               |
|                                                                       |
|     return 0;                                                         |
|                                                                       |
| }                                                                     |
|                                                                       |
|                                                                       |
+=======================================================================+
+-----------------------------------------------------------------------+

> Time Complexity: The time complexity of Selection Sort is O(N^2^).

# 

# 

# [Bubble Sort -- Data Structure and Algorithm Tutorials]{.underline}

***Bubble Sort** is the simplest [sorting
algorithm](https://www.geeksforgeeks.org/sorting-algorithms/) that works
by repeatedly swapping the adjacent elements if they are in the wrong
order. This algorithm is not suitable for large data sets as its average
and worst-case time complexity is quite high.*

## Bubble Sort Algorithm

*In Bubble Sort algorithm, *

-   *traverse from left and compare adjacent elements and the higher one
    > is placed at right side. *

```{=html}
<!-- -->
```
-   *In this way, the largest element is moved to the rightmost end at
    > first. *

```{=html}
<!-- -->
```
-   *This process is then continued to find the second largest and place
    > it and so on until the data is sorted.*

Let us understand the code of bubble sort with the help of the following
problem:

***Input:** arr\[\] = {6, 3, 0, 5}*

## For C++ -

+-----------------------------------------------------------------------+
| // Optimized implementation of Bubble sort                            |
|                                                                       |
| #include \<bits/stdc++.h\>                                            |
|                                                                       |
| using namespace std;                                                  |
|                                                                       |
|                                                                       |
|                                                                       |
| // An optimized version of Bubble Sort                                |
|                                                                       |
| void bubbleSort(int arr\[\], int n)                                   |
|                                                                       |
| {                                                                     |
|                                                                       |
|     int i, j;                                                         |
|                                                                       |
|     bool swapped;                                                     |
|                                                                       |
|     for (i = 0; i \< n - 1; i++) {                                    |
|                                                                       |
|         swapped = false;                                              |
|                                                                       |
|         for (j = 0; j \< n - i - 1; j++) {                            |
|                                                                       |
|             if (arr\[j\] \> arr\[j + 1\]) {                           |
|                                                                       |
|                 swap(arr\[j\], arr\[j + 1\]);                         |
|                                                                       |
|                 swapped = true;                                       |
|                                                                       |
|             }                                                         |
|                                                                       |
|         }                                                             |
|                                                                       |
|                                                                       |
|                                                                       |
|         // If no two elements were swapped                            |
|                                                                       |
|         // by inner loop, then break                                  |
|                                                                       |
|         if (swapped == false)                                         |
|                                                                       |
|             break;                                                    |
|                                                                       |
|     }                                                                 |
|                                                                       |
| }                                                                     |
|                                                                       |
|                                                                       |
|                                                                       |
| // Function to print an array                                         |
|                                                                       |
| void printArray(int arr\[\], int size)                                |
|                                                                       |
| {                                                                     |
|                                                                       |
|     int i;                                                            |
|                                                                       |
|     for (i = 0; i \< size; i++)                                       |
|                                                                       |
|         cout \<\< \" \" \<\< arr\[i\];                                |
|                                                                       |
| }                                                                     |
|                                                                       |
|                                                                       |
|                                                                       |
| // Driver program to test above functions                             |
|                                                                       |
| int main()                                                            |
|                                                                       |
| {                                                                     |
|                                                                       |
|     int arr\[\] = { 64, 34, 25, 12, 22, 11, 90 };                     |
|                                                                       |
|     int N = sizeof(arr) / sizeof(arr\[0\]);                           |
|                                                                       |
|     bubbleSort(arr, N);                                               |
|                                                                       |
|     cout \<\< \"Sorted array: \\n\";                                  |
|                                                                       |
|     printArray(arr, N);                                               |
|                                                                       |
|     return 0;                                                         |
|                                                                       |
| }                                                                     |
+=======================================================================+
+-----------------------------------------------------------------------+

Time Complexity: Time Complexity of Bubble sort is O(N^2^).

# [Insertion Sort --]{.underline} 

-   
-   
-   

***Insertion sort** is a simple sorting algorithm that works similarly
to the way you sort playing cards in your hands. The array is virtually
split into a sorted and an unsorted part. Values from the unsorted part
are picked and placed in the correct position in the sorted part.*

## 

## Insertion Sort Algorithm

*To sort an array of size N in ascending order iterate over the array
and compare the current element (key) to its predecessor, if the key
element is smaller than its predecessor, compare it to the elements
before. Move the greater elements one position up to make space for the
swapped element.*

## 

## Working of Insertion Sort algorithm

*Consider an example: arr\[\]: **{12, 11, 13, 5, 6}***

Below is the implementation of the iterative approach:

## For C++ -

## 

+-----------------------------------------------------------------------+
| // C++ program for insertion sort                                     |
|                                                                       |
|                                                                       |
|                                                                       |
| #include \<bits/stdc++.h\>                                            |
|                                                                       |
| using namespace std;                                                  |
|                                                                       |
|                                                                       |
|                                                                       |
| // Function to sort an array using                                    |
|                                                                       |
| // insertion sort                                                     |
|                                                                       |
| void insertionSort(int arr\[\], int n)                                |
|                                                                       |
| {                                                                     |
|                                                                       |
|     int i, key, j;                                                    |
|                                                                       |
|     for (i = 1; i \< n; i++) {                                        |
|                                                                       |
|         key = arr\[i\];                                               |
|                                                                       |
|         j = i - 1;                                                    |
|                                                                       |
|                                                                       |
|                                                                       |
|         // Move elements of arr\[0..i-1\],                            |
|                                                                       |
|         // that are greater than key,                                 |
|                                                                       |
|         // to one position ahead of their                             |
|                                                                       |
|         // current position                                           |
|                                                                       |
|         while (j \>= 0 && arr\[j\] \> key) {                          |
|                                                                       |
|             arr\[j + 1\] = arr\[j\];                                  |
|                                                                       |
|             j = j - 1;                                                |
|                                                                       |
|         }                                                             |
|                                                                       |
|         arr\[j + 1\] = key;                                           |
|                                                                       |
|     }                                                                 |
|                                                                       |
| }                                                                     |
|                                                                       |
|                                                                       |
|                                                                       |
| // A utility function to print an array                               |
|                                                                       |
| // of size n                                                          |
|                                                                       |
| void printArray(int arr\[\], int n)                                   |
|                                                                       |
| {                                                                     |
|                                                                       |
|     int i;                                                            |
|                                                                       |
|     for (i = 0; i \< n; i++)                                          |
|                                                                       |
|         cout \<\< arr\[i\] \<\< \" \";                                |
|                                                                       |
|     cout \<\< endl;                                                   |
|                                                                       |
| }                                                                     |
|                                                                       |
|                                                                       |
|                                                                       |
| // Driver code                                                        |
|                                                                       |
| int main()                                                            |
|                                                                       |
| {                                                                     |
|                                                                       |
|     int arr\[\] = { 12, 11, 13, 5, 6 };                               |
|                                                                       |
|     int N = sizeof(arr) / sizeof(arr\[0\]);                           |
|                                                                       |
|                                                                       |
|                                                                       |
|     insertionSort(arr, N);                                            |
|                                                                       |
|     printArray(arr, N);                                               |
|                                                                       |
|                                                                       |
|                                                                       |
|     return 0;                                                         |
|                                                                       |
| }                                                                     |
+=======================================================================+
+-----------------------------------------------------------------------+

Time Complexity: Time Complexity Insertion Sort is O(N^2^).

# sort() in C++ STL

*C++ STL provides a similar function sort that sorts a vector or array
(items with random access)*

*It generally takes two parameters, the first one being the point of the
array/vector from where the sorting needs to begin and the second
parameter being the length up to which we want the array/vector to get
sorted. The third parameter is optional and can be used in cases such as
if we want to sort the elements lexicographically.*

***By default, the sort() function sorts the elements in ascending
order.***

*Below is a simple program to show the working of sort(). *

## For C++ -

## 

+-----------------------------------------------------------------------+
| // C++ program to demonstrate default behaviour of                    |
|                                                                       |
| // sort() in STL.                                                     |
|                                                                       |
| #include \<bits/stdc++.h\>                                            |
|                                                                       |
| using namespace std;                                                  |
|                                                                       |
|                                                                       |
|                                                                       |
| int main()                                                            |
|                                                                       |
| {                                                                     |
|                                                                       |
|     int arr\[\] = { 1, 5, 8, 9, 6, 7, 3, 4, 2, 0 };                   |
|                                                                       |
|     int n = sizeof(arr) / sizeof(arr\[0\]);                           |
|                                                                       |
|                                                                       |
|                                                                       |
|     /\*Here we take two parameters, the beginning of the              |
|                                                                       |
|     array and the length n upto which we want the array to            |
|                                                                       |
|     be sorted\*/                                                      |
|                                                                       |
|     sort(arr, arr + n);                                               |
|                                                                       |
|                                                                       |
|                                                                       |
|     cout \<\< \"\\nArray after sorting using \"                       |
|                                                                       |
|             \"default sort is : \\n\";                                |
|                                                                       |
|     for (int i = 0; i \< n; ++i)                                      |
|                                                                       |
|         cout \<\< arr\[i\] \<\< \" \";                                |
|                                                                       |
|                                                                       |
|                                                                       |
|     return 0;                                                         |
|                                                                       |
| }                                                                     |
+=======================================================================+
+-----------------------------------------------------------------------+

**Output**

Array after sorting using default sort is :

0 1 2 3 4 5 6 7 8 9

**Time Complexity: **O(N log N)

Since you\'ve all got the above algos, let\'s solve some problems to get
hold on what you\'ve caught up till now\...

Follow the link below for problems based on sorting\--

🔗https://leetcode.com/tag/sorting/
