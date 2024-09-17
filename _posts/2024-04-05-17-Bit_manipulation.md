---
title: Bit Manipulation
---
# Bit Manipulation
Bit manipulation is the process of applying certain logical operations on a given sequence of bits to achieve the desired results. It can reduce the need to loop over a data structure and speed up the coding process as bit manipulations are processed in parallel.
The bits in the representation are indexed from right to left. 
We say that a certain bit is set, if it is one, and cleared if it is zero.
The binary number  (a<sub>k</sub>a<sub>k-1</sub>....a<sub>1</sub>a<sub>0</sub>)<sub>2</sub> represents the number 
	a<sub>k</sub>.2<sup>k</sup> + a<sub>k-1</sub>.2<sup>k-1</sup> + ... + a<sub>1</sub>.2<sup>1</sup> + a<sub>0</sub>.2<sup>0</sup> (in decimal)

### Pre-requisites:
## Binary Number System
 Binary Number System is a number system that is used to represent various numbers using only two symbols “0” and “1”. The word binary is derived from the word “bi” which means two. Hence, this number system is called Binary Number System. Thus, the binary number system is a system that has only two symbols.
There are generally various types of number systems and among them the four major ones are,
•	Binary Number System (Number system with Base 2)
•	Octal Number System (Number system with Base 8)
•	Decimal Number System (Number system with Base 10)
•	Hexa decimal Number System (Number system with Base 16

![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/c6306bab-eb64-4803-8635-6debb7c10f6e)

  In the Binary Number System, we have a base of 2. The base of the Binary Number System is also called the radix of the number system.
In a binary number system, we represent the number as,
•	(11001)2
In the above example, a binary number is given in which the base is 2. In a binary number system, each digit is called the “bit”. In the above example, there are 5 digits.

### Binary Number Table
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/37f7457d-bcef-4165-a185-664f1ea91f75)
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/74fd43c0-6c79-44f3-acfb-801531147073)

### Binary to Decimal Conversion
A binary number is converted into a decimal number by multiplying each digit of the binary number by the power of either 1 or 0 to the corresponding power of 2. Let us consider that a binary number has n digits, B = a<sub>n-1</sub>…a<sub>3</sub>a<sub>2</sub>a<sub>1</sub>a<sub>0</sub>. Now, the corresponding decimal number is given as
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/6e46fae3-4a4f-4211-83bd-f1f04355fd88)

##### Example: Convert (10011)<sub>2</sub> to a decimal number.
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/64b3b843-088e-4115-bf26-62691705e2ed)

### Decimal to Binary Conversion
A decimal number is converted into a binary number by dividing the given decimal number by 2 continuously until we get the quotient as 1, and we write the numbers from downwards to upwards.
###### Example: Convert (28)<sub>10/<sub> into a binary number.
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/08b90d65-76e7-47a1-b2d0-d9289cc1ddb5)

### Arithmetic Operations on Binary Numbers
We can easily perform various operations on Binary Numbers. Various arithmetic operations on the Binary number include,
•	Binary Addition
•	Binary Subtraction
•	Binary Multiplication
•	Binary Division

#### Binary Addition
The result of the addition of two binary numbers is also a binary number. To obtain the result of the addition of two binary numbers, we have to add the digit of the binary numbers by digit. The table added below shows the rule of binary addition.
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/80909ad1-2612-405e-9007-793f09d41ab8)

#### Binary Subtraction
The result of the subtraction of two binary numbers is also a binary number. To obtain the result of the subtraction of two binary numbers, we have to subtract the digit of the binary numbers by digit. The table added below shows the rule of binary subtraction.
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/4ee1ca3f-3d4a-49ec-867c-d438b28d44e6)

#### Binary Multiplication
The multiplication process of binary numbers is similar to the multiplication of decimal numbers. The rules for multiplying any two binary numbers are given in the table.
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/f3ea558b-af45-4e05-b1d2-a2cca3d9e375)

#### Binary Division
The division method for binary numbers is similar to that of the decimal number division method.
###### Example: Divide (101101)<sub>2</sub> by (110)<sub>2</sub>
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/f0553586-9165-4c10-9e9d-622f7463dd14)

### 1’s and 2’s Complement of a Binary Number
•1’s Complement of a Binary Number is obtained by inverting the digits of the binary number.
###### Example: Find the 1’s complement of (10011)<sub>2</sub>.
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/5b0095e6-1295-4f7b-a352-2e31766c8d2f)

•2’s Complement of a Binary Number is obtained by inverting the digits of the binary number and then by adding 1 to the least significant bit.
###### Find the 2’s complement of (1011)<sub>2</sub>.
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/0451cd4d-d0d1-4e37-ae72-6741463d12a7)

## BITWISE OPERATORS

| Operator | Name and Function of Operator | 
| -------- | ----------------------------- |
| & | Bitwise AND: The bitwise AND operator compares each bit of its first operand with the corresponding bit of its second operand. If both bits are 1, the corresponding result bit is set to 1. Otherwise, the corresponding result bit is set to 0. |
| | | Bitwise OR: The bitwise inclusive OR operator compares each bit of its first operand with the corresponding bit of its second operand. If one of the two bits is 1, the corresponding result bit is set to 1. Otherwise, the corresponding result bit is set to 0. |
| ~ | One’s complement / NOT: The bitwise complement (NOT) operator flips each bit of a number, if a bit is set the operator will clear it, if it is cleared the operator sets it. |
| ^ | Bitwise XOR: The bitwise exclusive OR (XOR) operator compares each bit of its first operand with the corresponding bit of its second operand. If one bit is 0 and the other bit is 1, the corresponding result bit is set to 1. Otherwise, the corresponding result bit is set to 0. |
| << | Left shift: Shifts a number to the left by appending zero digits. A left shift by k represents a multiplication by  2^k. |
| >> | Right shift: Shifts a number to the right by removing the last few binary digits of the number. Each shift by one represents an integer division by 2, so a right shift by k represents an integer division by 2^k. |


## Get the bit at a specific position
To find the bit at position i in a given number N, you can perform a bitwise AND operation between N and 2 raised to the power of i (represented as (1 << i)). This operation checks whether the bit at position i is set or unset. If the resulting value is 1, then the bit at position i is set. Otherwise, it is unset.
```
bool getBit(int num, int i)
{
    // Return true if the bit is
    // set. Otherwise, return false
    return ((num & (1 << i)) != 0);
}
```

## Set the bit at a specific position:
To set a specific bit at position i in a given number N, you can perform a bitwise OR operation between N and 2 raised to the power of i (represented as (1 << i)). This operation effectively sets the bit at position i in N. 
```
int setBit(int num, int i)
{
    // Sets the ith bit and return
    // the updated value
    return num | (1 << i);
}
```

## Clear the bit at a specific position:
To clear a specific bit at position i in a given number N, you can perform a bitwise AND operation between N and the complement of 2 raised to the power of i (represented as ~(1 << i)). This operation effectively clears the bit at position i in N. If the resulting value is 1, then the bit at position i was initially set. Otherwise, it was already clear.
```
int clearBit(int num, int i)
{
 
    // Create the mask for the ith
    // bit unset
    int mask = ~(1 << i);
 
    // Return the updated value
    return num & mask;
}
```

## Brian Kernighan’s algorithm for counting the total number of set bits in a binary number:
The idea is to subtract n by 1 to invert all the bits after the rightmost set bit of n (including the rightmost set bit). Then use n & (n-1) expression to clear the rightmost set bit. The number of times we clear the rightmost set bit until the number becomes zero will be the set bit count. 
```
int countSetBits(int n)
    {
        int count = 0;
        while (n) {
            n &= (n - 1);
            count++;
        }
        return count;
    }
```

## Flip the bit at a specific position:
Left shift given number 1 by k-1 to create a number that has only set bit as kth bit temp = 1 << (k-1)). Return bitwise XOR of temp and n.  Since temp has only kth bit set, doing XOR would flip only this bit. 
```
int toggleKthBit(int n, int k)
{
    return (n ^ (1 << (k-1)));
}
```

## Find the position of the rightmost set bit:
To find the position of the first set (1) bit in a given number, you can initialize a variable m to 1 and perform a bitwise XOR operation between m and the given number, checking from the rightmost bit. You left shift m by one position until you encounter the first set bit. This operation effectively isolates the position of the first set bit in the given number because the first set bit encountered in the XOR operation indicates where the given number and m differ. In other words, by repeatedly left-shifting m and performing XOR operations, you can determine the position of the first set bit in the given number. 
```
int PositionRightmostSetbit(int n)
{
    if (n == 0)
        return 0;
    // Position variable initialized with 0
    // m variable is used to check the set bit
    int position = 0;
    int m = 1;
 
    while (!(n & m)) {
 
        // left shift
        m = m << 1;
        position++;
    }
    return position;
}
```

## Clear the rightmost set bit in a given number:
To clear the rightmost set bit in a given number n, you can subtract 1 from n, which flips all the bits after the rightmost set bit (including the set bit). Then, performing a bitwise AND operation between n and n-1 will result in the desired output. This operation effectively clears the rightmost set bit in n while leaving other bits unchanged. 
```
int clearRightmostSetBit(unsigned int n) 
{ 
    return n & (n - 1); 
} 
```

## Reversing the order of bits in a given number:
To reverse the bits of a given number, we start by initializing a variable called "res" to 0. Then, if the input number is greater than 0, we enter a loop. Within this loop, we multiply "res" by 2 and add 1 to "res" if "num" is odd. After each iteration, we divide "num" by 2. This process continues until "num" becomes greater than 0. Finally, we return the value of "res," which now holds the reversed bits of the original number. This method efficiently reverses the order of bits in the given number.
```
int reverseBits(int num) 
{ 
    int rev = 0;
    // traversing bits of num from the right 
    while (num > 0)
    { 
        // bitwise left shift res by 1 
        res <<= 1;     // multiply res by 2
        // if current bit is 1 or num is odd
        if (num & 1 == 1) 
            res ^= 1; 
  // Convert 0 to 1
        // bitwise right shift num by 1 
        num >>= 1;     // divide num by 2
    }
    return res; 
} 
```

## Check if a number is power of 2 : 
If the & operation between the given number n and given number minus one n-1 gives us 0, it is a power of 2. Otherwise, it is not.
```
#include <iostream>
using namespace std;

int main() {
  int n;
  // reading value of n from user
  cin >> n;

  if (n > 0) {
    // & operation between n and n - 1
    int i = n & (n - 1);

    // check if n is a power of 2
    if (i == 0) {
      cout << n << " is a power of 2";
```

## How to swap two numbers without using a third variable?
The bitwise XOR operator can be used to swap two variables. The XOR of two numbers x and y returns a number that has all the bits as 1 wherever bits of x and y differ. For example, XOR of 10 (In Binary 1010) and 5 (In Binary 0101) is 1111, and XOR of 7 (0111) and 5 (0101) is (0010). 
```
#include <bits/stdc++.h>
 
using namespace std;
 
int main()
{
    int x = 10, y = 5;
    // Code to swap 'x' (1010) and 'y' (0101)
    x = x ^ y; // x now becomes 15 (1111)
    y = x ^ y; // y becomes 10 (1010)
    x = x ^ y; // x becomes 5 (0101)
    cout << "After Swapping: x =" << x << ", y=" << y;
    return 0;
}
```

# Bit Tricks for Competitive Programming
In competitive programming or in general, some problems seem difficult but can be solved very easily with little concepts of bit magic.
##### One-Liner Hacks of Bit Manipulation:
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/23f41165-8579-4db4-b13b-e04f7c27c132)
![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/b00219fb-6a6d-4c58-8aee-11a207b320dc)

### Playing with Kth bit:
1) Turn Off kth bit in a number:

   ![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/b6a368d9-73f8-4f0d-ab0f-05b0fef40008)

3) Turn On kth bit in a number:

   ![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/04154241-1c9d-4e29-aa1d-cf73cf29e099)

5) Check if kth bit is set for a number:
   
   ![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/5abb8caf-3558-4933-a374-8f9e6c9c16dd)

7) Toggle the kth bit:
   
   ![image](https://github.com/29SagunSingh/bitmanipulation/assets/143775654/984dcd9a-24b3-42dd-89dd-21a201cd7230)


# Questions for Practice:
## Basic Level Questions
1. Check whether K-th bit is set or not
https://www.naukri.com/code360/problems/check-whether-k-th-bit-is-set-or-not_5026446?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

2. Check if the number is odd or not 
https://www.naukri.com/code360/problems/odd-even_7993579?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

3. Check if a number is power of 2 or not
https://www.naukri.com/code360/problems/power-of-two_893061?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

4. Count the number of set bits
https://www.naukri.com/code360/problems/count-total-set-bits_784?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

5. Set/Unset the rightmost unset bit
https://www.naukri.com/code360/problems/set-the-rightmost-unset-bit_8160456?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

6. Swap two numbers
https://www.naukri.com/code360/problems/swap-two-numbers_1380853?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

7. Divide two integers without using multiplication, division and mod operator
https://www.naukri.com/code360/problems/-divide-two-integers_1112617?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

## Interview Problems : 
1. Count number of bits to be flipped to convert A to B
https://www.naukri.com/code360/problems/flip-bits_8160405?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

2. Find the number that appears odd number of times
https://www.naukri.com/code360/problems/one-odd-occurring_4606074?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

3. Power Set 
https://www.naukri.com/code360/problems/subsequences-of-string_985087?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

4. Find xor of numbers from L to R
https://www.naukri.com/code360/problems/l-to-r-xor_8160412?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

5. Find the two numbers appearing odd number of times
https://www.naukri.com/code360/problems/two-numbers-with-odd-occurrences_8160466?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

## Advanced Maths : 
1. Print Prime Factors of a Number
https://www.naukri.com/code360/problems/prime-factorisation_1760849?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

2. All Divisors of a Number
https://www.naukri.com/code360/problems/print-all-divisors-of-a-number_1164188?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

3. Sieve of Eratosthenes
https://www.naukri.com/code360/problems/prime-factorisation_1760849?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

4. Find Prime Factorizaton of a number using Sieve 
https://www.naukri.com/code360/problems/prime-factorisation_1760849?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

5. Power(n, x)
https://www.naukri.com/code360/problems/power-of-numbers_8157729?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf

