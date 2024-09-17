# Introduction to Strings
The concept of strings in C++ provides us the facility to deal with the textual data in our programs.
Strings can be understood as a collection of charachters in an Array.
## Difference Between C-style Strings and C++ Strings:
C-style strings are arrays of characters terminated by a null character (‘\0’). They are just like any other type of arrays like integer arrays.<br>
C++ strings are objects that provide more flexibility and functionality for string manipulation.
You will learn more about [objects and classes in the OOPS concept in CPP.](https://www.geeksforgeeks.org/object-oriented-programming-in-cpp/)

## C++ String Class
The string class in C++ provides many functionalities to manipulate strings.

 It is part of the Standard Template Library (STL) and have various member functions for string operations.
-	Dynamic resizing.
-	Built-in functions for string manipulation.

**Tutorial:** [GeeksforGeeks –>GFG complete strings tutorial](https://www.geeksforgeeks.org/strings-in-cpp/) 

## String Input and Output
### Inputting Strings 
Use `cin` to take single word string and use `getline()` member function of string to take multiword string input.

**Example:**
```cpp
#include <iostream>
#include <string>
using namespace std; 
/* if you write this statement here in the starting then you don’t have to
 write std:: with different objects and member functions of string class.*/

int main() 
{
    string str1 = "hello"; 
    // predefining the string (string is written within “ “)
    string str2;
    string str3;

    cin>>str2;      // single word string input
    getline(cin,str3);    // multiword string input

    cout<<str1<<endl<<str2<<endl<<str3<<endl;       
    return 0;
}
```
<br>
<br>

```
Recommendation:
 Try each and every operations by doing some modifications by yourself to get better understanding of the functions discussed below and always try to think about the answer by yourself before running the program to get a better understanding.
 ```

## String Operations  
- Concatenation
- Searching 
- Insertion
- Deletion,etc.

1. **Concatenation of Strings:**<br>
Strings can be concatenated using the `+` operator or the `append()` function.
<br><br>
2. **Finding the Length of a String:**<br>
The `length()` function can be used to find the length of a string.

#### [Practice Problem(LeetCode)->  Add Binary - Click_Here](https://leetcode.com/problems/add-binary/description/)

```cpp
// code demonstrating above operations is given below.

#include <iostream>
#include <string>
using namespace std;

int main() {
    string str = "Hello";
    str = str + " World";      // Concatenation using + operator
    str.append(“ World ”);    // Concatenation using append function
    int string_length = str.length() ;  // finding length of str  (try to guess the answer)
    cout<<str<<endl;
    cout << "Length of the string: " << string_length << endl;
    return 0;

}
```

-------------------------
<br><br>
3. **Searching Within Strings:**<br>
String searching can be done using functions like `find()` or `find_first_of()`.

```cpp
// Demonstratiion of string’s find() function
#include<iostream>
#include<string>
using namespace std;

int main()
{
string str = "hello world";
cout<<str.find("o");   
return 0;
}
```

 For more functionalities related to searching in strings refer to the link given below.<br>
[String find in C++](https://www.geeksforgeeks.org/string-find-in-cpp/)

--------------------------
<br><br>
4. **String Comparison:**

- Strings can be compared using relational operators like `==`, `!=`, `>=` etc.<br>
- Using `compare()`: The `compare()` function can be used for lexicographical comparison of strings.

```cpp
// Demonstration given below
#include <iostream>
#include <string>
using namespace std;
int main() {
    string str1 = "Hello";
    string str2 = "World";
    
    if (str1 == str2) {
       cout << "Strings are equal" <<endl;
    } else {
       cout << "Strings are not equal" <<endl;
    }
    
    return 0;
}
```

#### [Practice Problem(LeetCode)->  Valid Anagram](https://leetcode.com/problems/valid-anagram/description/)
----------------------------
<br><Br>
5. **String Iteration:**<br>
Iterating Through Characters of a String:
Strings can be iterated through using loops or iterators.<br><br>
- Using Iterators:Iterators provide a more flexible way to traverse strings.

```cpp
    // Code 
    #include <iostream>
    #include <string>
    using namespace std;
    int main() {
        std::string str = "Hello";
        for (char ch : str) {
            std::cout << ch << std::endl;
        }
        return 0;
    }
```
---------------------------
<Br><br>
6. **String Conversion**

-	Converting Strings to Numerical Types:
               Strings representing numbers can be converted to numerical types using functions like `stoi()`.

-   Converting Numerical Types to Strings:
        Numerical types can be converted to strings using functions like `to_string()`.

```cpp
// Demonstration given below:-

#include <iostream>
#include <string>
using namespace std;
int main() {
    string str = "123";
    int num = stoi(str); // String to Integer
    num = num+1;
    cout << "Converted integer: " << num << endl;

    int num2 = 456;
    string str2 = to_string(num2); // Integer to String
    str2 = str2+'7';
    cout << "Converted string: " << str2 << endl;

    return 0;
}
```
- For more conversion related functions of string refer to the links given below:-<br>
    - [Convert String to int in C++](https://www.geeksforgeeks.org/convert-string-to-int-in-cpp/)
    - [Converting Number to String in C++](https://geeksforgeeks.org/converting-number-to-string-in-cpp/)

#### [Practice Problem: LeetCode - Integer to Roman](https://leetcode.com/problems/integer-to-roman/description/)
----------------------------
<br><br> 
7. **Copying a string to another**<br>
       We have `strcpy()` function to copy one string into another string with replacement of dataPresent in the string to which the another string is being copied.

```NOTE -> This function only works with C-style strings but not with CPP strings, in cpp strings we can use assignment operator ‘=’ directly or assign() member function.```      

```cpp
// code demonstrating the use of strcpy() function, copying C-style strings.                                                       
#include <iostream>
#include <cstring>
using namespace std;
int main() {
    char str1[] = "Hello";
    char str2[10];
    strcpy(str2, str1); 
    cout << "Copied string: " << str2 << endl;
    return 0;
}
```
-----------------------------
<br><br>

8.**Reversing a String**<br>
Strings can be reversed by many different methods like using loops,etc. But Cpp string class have its inbuilt `reverse()` member function.

```cpp
// Code implementation given below:-
#include <iostream>
#include<string>
using namespace std;
int main()
{
    string str = "hello world";
    reverse(str.begin(), str.end());
// str.begin() gives iterator pointing to the first element of the string
    cout << str;
    return 0;
}
```

- For other methods to reverse string refer to the link given below:-<br>
[Different Methods to Reverse a String in C++](https://www.geeksforgeeks.org/reverse-a-string-in-c-cpp-different-methods/)<br>

#### [Practice problem(leetcode) -> Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/description/) 

- For more operations like insertion,deletion, and other manipulation in strings do refer the tutorial link.<br>
[Tutorial Link -> Basic String Operations with Implementation](https://www.geeksforgeeks.org/basic-string-operations-with-implementation/)
-------------------------
<br><br>

## [Important Practice problems leetcode links collection](https://leetcode.com/discuss/interview-question/2001789/collections-of-important-string-questions-pattern)
[Collections of Important String questions Pattern - LeetCode Discuss.html](https://leetcode.com/discuss/interview-question/2001789/collections-of-important-string-questions-pattern)







