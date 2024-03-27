## INTRODUCTION
Let’s understand the concept of arrays using an analogy. Consider a situation in which we have 20 students in a class and we have been asked to write a program that reads and prints the marks of all the 20 students. In this program, we will need 20 integer variables with different names.
Now to read the values of these 20 variables, we must have 20 read statements. Similarly, to print the value of these variables, we need 20 write statements. If it is just a matter of 20 variables, then it might be acceptable for the user to follow this approach. But would it be possible to follow this approach if we have to read and print the marks of students,
in the entire course (say 100 students),
in the entire college (say 500 students),
in the entire university (say 10,000 students).
The answer is no, definitely not! To process a large amount of data, we need a data structure known as an array.

![Need of Array Illustration](./assets/images/array-need.png)

## ARRAY
Array can be defined as **a collection of similar data types that are stored at contiguous memory locations**.

![Array](./assets/images/array.png)

### Array Declaration
Declaring an array means specifying the following:
- Data type - the kind of values it can store, for example, int, char, float, double.
- Name - to identify the array.
- Size - the maximum number of values that the array can hold.

Array can be declared using the following syntax:

`type name[size]`;
```cpp
int arr[8];
```

