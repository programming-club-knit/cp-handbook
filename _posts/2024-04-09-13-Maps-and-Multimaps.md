---
title: Maps
author: Deepak Singh
---

# Introduction to Maps:

In C++, a "map" is a data structure that stores a collection of key-value pairs. It's like having a dictionary where you can look up a word (the key) and find its definition (the value).

## Some key points related to maps

In C++, the map is a type of associative container that stores elements formed by a combination of a key and a mapped value. Here are some key properties of map

1. **Key-Value Pair Storage**: Each element in a map is a key-value pair. The key is used to uniquely identify the element, and the mapped value is the associated data.

2. **Ordered Collection**: By default, elements in a map are stored in a specific order based on the keys. This order is usually determined by a comparison function applied to the keys. This means you can iterate through the elements in a specific order, like alphabetical order if the keys are strings.

3. **Fast Lookup**: map provides fast lookup times for accessing elements based on their keys. The underlying data structure of a map is typically a balanced binary search tree, which ensures efficient search operations.

4. **Unique Keys**: Each key in a map must be unique. Attempting to insert a duplicate key will replace the existing value associated with that key.

5. **Ordered Insertion**: When inserting elements into a map, they are inserted in the correct order based on their keys. This ensures that the elements remain in the desired order when iterating through the map.

6. **Dynamic Size**: map can grow or shrink dynamically as elements are inserted or removed. It automatically manages memory allocation and deallocation.

7. **Accessing Values**: We can access value of a key using `[]` operator. 

These properties make `std::map` a versatile and efficient container for storing key-value pairs, especially when ordered traversal or fast lookup based on keys is required. However, it's essential to be mindful of the performance characteristics and overhead associated with maintaining the order and balancing the underlying binary search tree.

## Creating a map :-
A map can be created by the following syntax

map<_keyDataType_, _ValueDataType> _mapName_;

Example:-
```bash
map<int,int>m;
```
The above map will map the keys of integer datatype to values of integer datatype.
The datatypes of both keys and values may or may not be same. 

## Usage

```c++
# include<bits/stdc++.h>;
using namespace std;

int main() {
    map<string, int> ageMap;

    // Adding key-value pairs
    ageMap["Alice"] = 30;
    ageMap["Bob"] = 25;
    ageMap["Charlie"] = 40;

    // Accessing values
    cout << "Alice's age: " << ageMap["Alice"] << std::endl;

    // Modifying values
    ageMap["Bob"] = 26;

    return 0;
}


```
## Iterating in maps
Iteration in maps can be done can be done using iterators. Iterators are like pointers which points to the elements of the STL container in this case map.

Below is an example showing iteration in maps
```c++
# include<bits/stdc++.h>
using namespace std;

int main() {
    // Creating a map
    map<int, string> myMap;

    // Inserting elements into the map
    myMap.insert(pair<int, string>(1, "One"));
    myMap.insert(pair<int, string>(2, "Two"));
    myMap.insert(pair<int, string>(3, "Three"));

    // Iterating through the map and printing its elements
    cout << "Map elements:" << endl;
    for (auto it = myMap.begin(); it != myMap.end(); ++it) {
        cout << it->first << ": " << it->second << endl;
    }

    return 0;
}

```
## Ouput 
```
Map elements:
1: One
2: Two
3: Three
```
## Alternate method to iterate
```c++
for(auto it:mp){
    cout<<it.first<<" "<<it.second<<" ";
}
//mp is the map
```
# Important Map Functions
**begin()** – Returns an iterator to the first element in the map.  
**end()** – Returns an iterator to the theoretical element that follows the last element in the map.
**size()** – Returns the number of elements in the map.    
**empty()** – Returns whether the map is empty.  
**insert(keyvalue, mapvalue)** – Adds a new element to the map.  
**erase(iterator position)** – Removes the element at the position pointed by the iterator.
**erase(const g)**– Removes the key-value ‘g’ from the map.  
**clear()** – Removes all the elements from the map.

## Example of above functions
```c++
# include<bits/stdc++.h>

using namespace std;

int main() {
    // Creating a map
    map<int, string> myMap;

    // Inserting elements into the map
    myMap.insert(pair<int, string>(1, "One"));
    myMap.insert(pair<int, string>(2, "Two"));
    myMap.insert(pair<int, string>(3, "Three"));

    // Using begin() and end() to iterate through the map
    cout << "Map elements:" << endl;
    for (auto it = myMap.begin(); it != myMap.end(); ++it) {
        cout << it->first << ": " << it->second << endl;
    }

    // Using size() to get the number of elements in the map
    cout << "Number of elements in the map: " << myMap.size() << endl;

    // Using empty() to check if the map is empty
    cout << "Is the map empty? " << (myMap.empty() ? "Yes" : "No") << endl;

    // Using erase(iterator) to remove an element from the map
    auto it = myMap.find(2);
    if (it != myMap.end()) {
        myMap.erase(it);
    }

    // Using erase(const key) to remove an element by key
    myMap.erase(3);

    // Using clear() to remove all elements from the map
    myMap.clear();

    // Checking if the map is empty after clearing
    cout << "Is the map empty after clearing? " << (myMap.empty() ? "Yes" : "No") << endl;

    return 0;
}

```
## Output
```
Map elements:
1: One
2: Two
3: Three
Number of elements in the map: 3
Is the map empty? No
Is the map empty after clearing? Yes

```
# Unordered maps in c++:
**Hash-Based:** unordered_map is a hash table-based associative container that stores key-value pairs. It provides fast retrieval of elements based on keys using hashing.  
**No Order:** Unlike map, the elements in unordered_map are not stored in a specific order based on keys. Instead, they are stored based on the hash values of keys, resulting in faster lookup times but no guaranteed order.  
**Unique Keys:** Each key in an unordered_map must be unique. Attempting to insert a duplicate key will replace the existing value associated with that key.  
**Complexity:** Insertion, deletion, and search operations in unordered_map have an average time complexity of O(1) under the assumption of a good hash function.   
They have same functions as of maps.
 
Example:
```c++
# include<bits/stc++.h>
using namespace std;
int main() {
    unordered_map<string, int> umap;
    umap["one"] = 1;
    umap["two"] = 2;
    umap["three"] = 3;

    for (auto pair : umap) {
        std::cout << pair.first << ": " << pair.second << endl;
    }

    return 0;
}

```
# Multimaps in c++
**Ordered Collection:** multimap is an associative container that stores multiple key-value pairs where keys can have duplicate values.  
**Allows Duplicates:** Unlike map, multimap allows duplicate keys. Each key-value pair is inserted independently, and multiple pairs with the same key can exist in the multimap.  
**Ordered Insertion:** Elements in multimap are stored in a specific order based on keys. This order is maintained using the comparison function provided when creating the multimap.  
**Complexity:** Insertion, deletion, and search operations in multimap have a logarithmic time complexity O(log n), where n is the number of elements in the multimap.  
it also have all the functions as of a map and unordered map except erase() function which deletes all the occurences 
```c++
#include <iostream>
#include <map>

int main() {
    std::multimap<int,string> mmap;
    mmap.insert(pair<int, string>(1, "one"));
    mmap.insert(pair<int, string>(2, "two"));
    mmap.insert(pair<int, string>(1, "uno")); // Duplicate key

    for (const auto& pair : mmap) {
        std::cout << pair.first << ": " << pair.second << std::endl;
    }

    return 0;
}

```
## Practice questions:
- [https://www.geeksforgeeks.org/problems/twice-counter4236/1](https://www.geeksforgeeks.org/problems/twice-counter4236/1)  
- [https://codeforces.com/problemset/problem/525/A](https://codeforces.com/problemset/problem/525/A)
- [https://codeforces.com/problemset/problem/4/C](https://codeforces.com/problemset/problem/4/C)
- [https://www.hackerrank.com/challenges/cpp-maps/problem](https://www.hackerrank.com/challenges/cpp-maps/problem)
- [https://www.geeksforgeeks.org/tag/cpp-map/](https://www.geeksforgeeks.org/tag/cpp-map/)
- [https://leetcode.com/problems/single-number-ii/description/](https://leetcode.com/problems/single-number-ii/description/)
- [https://www.hackerrank.com/challenges/cpp-maps/problem](https://www.hackerrank.com/challenges/cpp-maps/problem)
- [https://www.geeksforgeeks.org/problems/find-the-frequency/1](https://www.geeksforgeeks.org/problems/find-the-frequency/1)
- [https://www.geeksforgeeks.org/problems/twice-counter4236/1](https://www.geeksforgeeks.org/problems/twice-counter4236/1)
- [https://www.geeksforgeeks.org/problems/word-with-maximum-frequency0120/1](https://www.geeksforgeeks.org/problems/word-with-maximum-frequency0120/1)