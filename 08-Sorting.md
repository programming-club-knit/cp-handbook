
**Sorting**

A Sorting Algorithm is used to rearrange a given array or list of elements according to a comparison operator on the elements.

Many efficient algorithms use sorting as a subroutine, because it is often easier to process data if the elements are in a sorted order.

For example, the problem ”does an array contain two equal elements?” is easy to solve using sorting. If the array contains two equal elements, they will be next to each other after sorting, so it is easy to find them.

There are many ways to sort but let’s learn some sorting algorithms-

**Selection Sort –**

***Selection sort** is a simple and efficient sorting algorithm that works by repeatedly selecting the smallest (or largest) element from the unsorted portion of the list and moving it to the sorted portion of the list.* 

*The algorithm repeatedly selects the smallest (or largest) element from the unsorted portion of the list and swaps it with the first element of the unsorted part. This process is repeated for the remaining unsorted portion until the entire list is sorted*

## **Selection Sort Algorithm-**

*Lets consider the following array as an example: **arr[] = {64, 25, 12, 22, 11}***

## **For C++ -**

#include <iostream>

void selectionSort(int array[], int size) {

`    `for (int i = 0; i < size; ++i) {

`        `int min\_index = i;

`        `for (int j = i + 1; j < size; ++j) {

`            `if (array[j] < array[min\_index]) {

`                `min\_index = j;

`            `}

`        `}

`        `// Swap the minimum element with the current index's element

`        `int temp = array[i];

`        `array[i] = array[min\_index];

`        `array[min\_index] = temp;

`    `}

}

int main() {

`    `int arr[] = {64, 25, 12, 22, 11};

`    `int size = sizeof(arr) / sizeof(arr[0]);

`    `selectionSort(arr, size);

`    `std::cout << "The array after sorting in Ascending Order by selection sort is:" << std::endl;

`    `for (int i = 0; i < size; ++i) {

`        `std::cout << arr[i] << " ";

`    `}

`    `std::cout << std::endl;

`    `return 0;

}

Time Complexity: The time complexity of Selection Sort is O(N<sup>2</sup>).
#
#
# **Bubble Sort –**


***Bubble Sort** is the simplest [sorting algorithm](https://www.geeksforgeeks.org/sorting-algorithms/) that works by repeatedly swapping the adjacent elements if they are in the wrong order. This algorithm is not suitable for large data sets as its average and worst-case time complexity is quite high.*
##
##
## **Bubble Sort Algorithm**

*In Bubble Sort algorithm,* 

- *traverse from left and compare adjacent elements and the higher one is placed at right side.* 
- *In this way, the largest element is moved to the rightmost end at first.* 
- *This process is then continued to find the second largest and place it and so on until the data is sorted.*

Let us understand the code of bubble sort with the help of the following problem:

***Input:** arr[] = **{64, 34, 25, 12, 22, 11, 90}***



||
| :- |
## **For C++ -**

#include <iostream>

int main() {

`    `int arr[] = {64, 34, 25, 12, 22, 11, 90};

`    `int N = sizeof(arr) / sizeof(arr[0]);

`    `bool swapped;

`    `for (int i = 0; i < N - 1; ++i) {

`        `swapped = false;

`        `for (int j = 0; j < N - i - 1; ++j) {

`            `if (arr[j] > arr[j + 1]) {

`                `// Swap the elements

`                `int temp = arr[j];

`                `arr[j] = arr[j + 1];

`                `arr[j + 1] = temp;

`                `swapped = true;

`            `}

`        `}

`        `// If no swaps occurred in this pass, the array is already sorted

`        `if (!swapped) {

`            `break;

`        `}

`    `}

`    `std::cout << "Sorted array:" << std::endl;

`    `for (int i = 0; i < N; ++i) {

`        `std::cout << arr[i] << " ";

`    `}

`    `std::cout << std::endl;

`    `return 0;

}



Time Complexity: Time Complexity of Bubble sort is O(N<sup>2</sup>).


# **Insertion Sort –** 
#
***Insertion sort** is a simple sorting algorithm that works similarly to the way you sort playing cards in your hands. The array is virtually split into a sorted and an unsorted part. Values from the unsorted part are picked and placed in the correct position in the sorted part.*
##
## **Insertion Sort Algorithm**

*To sort an array of size N in ascending order iterate over the array and compare the current element (key) to its predecessor, if the key element is smaller than its predecessor, compare it to the elements before. Move the greater elements one position up to make space for the swapped element.*
##
## **Working of Insertion Sort algorithm**
*Consider an example: arr[]: **{64, 34, 25, 12, 22, 11, 90}***

Below is the implementation of the iterative approach:

##
## **For C++ -**
#include <iostream>

int main() {

`    `int arr[] = {64, 34, 25, 12, 22, 11, 90};

`    `int N = sizeof(arr) / sizeof(arr[0]);

`    `for (int i = 1; i < N; ++i) {

`        `int key = arr[i];

`        `int j = i - 1;

`        `// Move elements of arr[0..i-1] that are greater than key

`        `// to one position ahead of their current position

`        `while (j >= 0 && arr[j] > key) {

`            `arr[j + 1] = arr[j];

`            `j = j - 1;

`        `}

`        `arr[j + 1] = key;

`    `}

`    `std::cout << "Sorted array:" << std::endl;

`    `for (int i = 0; i < N; ++i) {

`        `std::cout << arr[i] << " ";

`    `}

`    `std::cout << std::endl;

`    `return 0;

}


Time Complexity: Time Complexity Insertion Sort is O(N<sup>2</sup>).

#
#
#
#
# **Sort() in C++ STL-**

*C++ STL provides a similar function sort that sorts a vector or array (items with random access)*

*It generally takes two parameters, the first one being the point of the array/vector from where the sorting needs to begin and the second parameter being the length up to which we want the array/vector to get sorted. The third parameter is optional and can be used in cases such as if we want to sort the elements lexicographically.*

***By default, the sort() function sorts the elements in ascending order.***

*Below is a simple program to show the working of sort().* 

## **For C++ -**

#include <iostream>

#include <algorithm> // Include the STL header

int main() {

`    `int arr[] = {1, 5, 8, 9, 6, 7, 3, 4, 2, 0};

`    `int n = sizeof(arr) / sizeof(arr[0]);

`    `std::sort(arr, arr + n); // Sort the array

`    `std::cout << "Array after sorting using default sort is:\n";

`    `for (int i = 0; i < n; ++i)

`        `std::cout << arr[i] << " ";

`    `return 0;

}

**Output**

Array after sorting using default sort is :

0 1 2 3 4 5 6 7 8 9 

**Time Complexity:** O(N log N)

Since you've all caught up with the above algos, let's solve some problems to get more understanding it ... 

Follow the link below for problems based on sorting--

<https://www.codechef.com/problems/TSORT>

<https://www.codechef.com/problems/LOCKDRAW>

<https://www.codechef.com/problems/JOHNY>

<https://codeforces.com/problemset/problem/405/A>

<https://codeforces.com/problemset/problem/141/A>

<https://codeforces.com/problemset/problem/230/A>

