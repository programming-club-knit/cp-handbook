---
title: Set
---

# Introduction to Sets:

Sets are a type of associative container in which each element has to be unique because the value of the element identifies it. The values are stored in a specific sorted order i.e. either ascending or descending.

## Why do we need them?

Set data structures are commonly used in a variety of computer science applications, including algorithms, data analysis, and databases. The main advantage of using a set data structure is that it allows you to perform operations on a collection of elements in an efficient and organized way.

## Set and Unordered Set

The C++ standard library contains two set implementations: The structure `set` is based on a balanced binary tree and its operations work in $O(logn)$ time. The structure `unordered_set` uses hashing, and its operations work in $O(1)$ time on average.

| Set                                             | Unordered Set                                      |
| ----------------------------------------------- | -------------------------------------------------- |
| Set stores elements in a sorted order           | Unordered Set stores elements in an unsorted order |
| Set stores/acquire unique elements only         | Unordered Set stores/acquire only unique values    |
| Set uses Binary Search Trees for implementation | Unordered Set uses Hash Tables for implementation  |

## Implementation of Set

**Include the header file:** To use the set container, include the `set` header file in your C++ program. <br>
**Declare a set:** A set is declared using the `std::set` template class, specifying the type of elements it will contain. <br>
**Datatype :**
Set can take any data type depending on the values, e.g. `int`, `char`, `float`, etc.

### Syntax:

```C++
#include<iostream>
#include<set>

int main() {
    std::set<int> mySet; // Declare a set of integers
    return 0;
}
```

## Properties

- **Storing order** – The set stores the elements in sorted order.
- **Values Characteristics** – All the elements in a set have unique values.
- **Values Nature** – The value of the element cannot be modified once it is added to the set, though it is possible to remove and then add the modified value of that element. Thus, the values are _immutable_.
- **Search Technique** – Sets follow the Binary search tree implementation.
- **Arranging order** – The values in a set are unindexed.

## Basic Functions Associated with Set

- `begin()` – Returns an iterator to the first element in the set.
- `end()` – Returns an iterator to the theoretical element that follows the last element in the set.
- `size()` – Returns the number of elements in the set.
- `max_size()` – Returns the maximum number of elements that the set can hold.
- `empty()` – Returns whether the set is empty.

## Operations on Set

### Insert elements into the set:

You can insert elements into a set using the insert() function. This function returns a pair, where the first element is an iterator pointing to the inserted element, and the second element is a boolean value indicating whether the insertion was successful. If the element is already present in the set, the insertion is not performed, and the second element of the pair is false.

_Example:_

```C++
mySet.insert(5);
mySet.insert(3);
mySet.insert(7);
mySet.insert(2);
mySet.insert(5); // This element will not be inserted because it's already in the set
```

### Access elements in the set:

To access elements in a set, you can use iterators. The begin() function returns an iterator pointing to the first element in the set, and the end() function returns an iterator pointing to the “theoretical” element that is after the last element in the set.

_Example:_

```C++
for (auto it = mySet.begin(); it != mySet.end(); ++it) {
    std::cout << *it << " ";
}
// Output: 2 3 5 7
```

### Remove elements from the set:

You can remove elements from a set using the erase() function. This function can take either an iterator pointing to the element to be removed or the value of the element to be removed.

_Example:_

```C++
mySet.erase(3); // Remove the element with the value 3

// Remove all occurrences of the element 5
auto it = mySet.find(5);
while (it != mySet.end()) {
    mySet.erase(it++);
}
```

> **Note :**
> The time complexities for doing various operations on sets are : <br>
> Insertion of Elements – $O(log N)$ <br>
> Deletion of Elements – $O(log N)$

<br>

# Multisets

Multisets are a type of associative containers similar to the set, with the exception that multiple elements can have the same values.

## Basic Functions associated with Multiset:

- `begin()` – Returns an iterator to the first element in the multiset –> $O(1)$
- `end()` – Returns an iterator to the theoretical element that follows the last element in the multiset –> $O(1)$
- `size()` – Returns the number of elements in the multiset –> $O(1)$
- `max_size()` – Returns the maximum number of elements that the multiset can hold –> $O(1)$
- `empty()` – Returns whether the multiset is empty –> $O(1)$

## Operations on Multiset :

- `insert(x)` – Inserts the element x in the multiset –> $O(log n)$
- `clear()` – Removes all the elements from the multiset –> $O(n)$
- `erase(x)` – Removes all the occurrences of x –> $O(log n)$

Removing Element From Multiset Which Have Same Value:
- `a.erase()` – Remove all instances of element from multiset having the same value
- `a.erase(a.find())` – Remove only one instance of element from multiset having same value

<br>

> **Note:** The time complexities for doing various operations on Multisets are : <br>
Inserting Elements – $O(log N)$ <br>
Accessing Elements – $O(log N)$ <br>
Deleting Elements – $O(log N)$ <br>

### Example :
```C++
// CPP Program to demonstrate the implementation of multiset
#include <iostream>
#include <iterator>
#include <set>
using namespace std;

int main() {
	// empty multiset container
	multiset<int, greater<int> > mSet1;

	// insert elements in random order
	mSet1.insert(40);
	mSet1.insert(30);
	mSet1.insert(60);
	mSet1.insert(20);
	mSet1.insert(50);

	// 50 will be added again to the multiset unlike set
	mSet1.insert(50);
	mSet1.insert(10);

	// printing multiset mSet1
	multiset<int, greater<int> >::iterator itr;
	cout << "\nThe multiset mSet1 is : \n";
	for (itr = mSet1.begin(); itr != mSet1.end(); ++itr) {
		cout << *itr << " ";
	}
	cout << endl;

	// assigning the elements from mSet1 to mSet2
	multiset<int> mSet2(mSet1.begin(), mSet1.end());

	// print all elements of the multiset mSet2
	cout << "\nThe multiset mSet2 \n"
			"after assign from mSet1 is : \n";
	for (itr = mSet2.begin(); itr != mSet2.end(); ++itr) {
		cout << *itr << " ";
	}
	cout << endl;

	// remove all elements up to element with value 30 in mSet2
	cout << "\nmSet2 after removal \n"
			"of elements less than 30 : \n";
	mSet2.erase(mSet2.begin(), mSet2.find(30));
	for (itr = mSet2.begin(); itr != mSet2.end(); ++itr) {
		cout << *itr << " ";
	}

	// remove all elements with value 50 in mSet2
	int num;
	num = mSet2.erase(50);
	cout << "\nmSet2.erase(50) : \n";
	cout << num << " removed \n";
	for (itr = mSet2.begin(); itr != mSet2.end(); ++itr) {
		cout << *itr << " ";
	}

	cout << endl;

	// lower bound and upper bound for multiset mSet1
	cout << "\nmSet1.lower_bound(40) : \n"
		<< *mSet1.lower_bound(40) << endl;
	cout << "mSet1.upper_bound(40) : \n"
		<< *mSet1.upper_bound(40) << endl;

	// lower bound and upper bound for multiset mSet2
	cout << "mSet2.lower_bound(40) : \n"
		<< *mSet2.lower_bound(40) << endl;
	cout << "mSet2.upper_bound(40) : \n"
		<< *mSet2.upper_bound(40) << endl;

	return 0;
}
```
**Output :**
```terminal
The multiset mSet1 is : 
60 50 50 40 30 20 10 

The multiset mSet2 
after assign from mSet1 is : 
10 20 30 40 50 50 60 

mSet2 after removal 
of elements less than 30 : 
30 40 50 50 60 
mSet2.erase(50) : 
2 removed 
30 40 60 

mSet1.lower_bound(40) : 
40
mSet1.upper_bound(40) : 
30
mSet2.lower_bound(40) : 
40
mSet2.upper_bound(40) : 
60
```

## Practice Questions :
- https://www.geeksforgeeks.org/problems/unique-rows-in-boolean-matrix/1
- https://www.geeksforgeeks.org/problems/smaller-on-left20360700/1
- https://leetcode.com/problems/merge-similar-items/
- https://www.geeksforgeeks.org/problems/jays-apples2724/1
- https://www.geeksforgeeks.org/problems/set-operations/1
- https://www.geeksforgeeks.org/problems/pair-sum-existence/1
- https://www.geeksforgeeks.org/problems/sum-the-common-elements/1
