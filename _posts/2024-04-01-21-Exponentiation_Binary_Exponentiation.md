---
title: Exponentiation and Binary Exponentiation
---

# Introduction to Exponentiation and Binary Exponentiation:

**Binary exponentiation**, also known as exponentiation by squaring, is a technique used to efficiently compute large powers of a number modulo another number. It is particularly useful in computer science and cryptography where large numbers are involved.

## What is Binary Exponentiation?

Binary Exponentiation or Exponentiation by squaring is the process of calculating a number raised to the power another number (AB) in Logarithmic time of the exponent or power, which speeds up the execution time of the program.


NORMAL EXPONENTIATION:

3<sup>6</sup>=3X3X3X3X3X3

3<sup>6</sup>=9X3X3X3X3

3<sup>6</sup>=27X3X3X3

3<sup>6</sup>=81X3X3

3<sup>6</sup>=243X3

3<sup>6</sup>=729

Number of iterations to calculate 3<sup>6</sup> was 6 complexity O(n)
where n is the power of base 3.

BINARY EXPONENTIATION:

3<sup>6</sup> = (3<sup>2</sup>)<sup>3</sup>

3<sup>6</sup>=(9)<sup>3</sup>

3<sup>6</sup>=(9)<sup>2</sup>X9

3<sup>6</sup>=81X9

3<sup>6</sup>=729

Number of iterations to calculate 3<sup>6</sup> was 3 complexity
O(log(n)) where n is the power of base 3.

**GENERAL FORMULA OF BINARY EXPONENTIATION**

<img src="./assets/images/image1.png" style="width:6.26806in;height:1.63547in"
alt="A math problem with numbers and symbols" />





# C++ code for binary exponentiation both iterative and recursive

```cpp
#include <iostream>
using namespace std;

// Iterative approach
long long binary_exponentiation_iterative(long long base, long long exponent) {
    long long result = 1;

    while (exponent > 0) {
        if (exponent & 1) // Check if current bit of exponent is set
            result *= base;
        base *= base;
        exponent >>= 1; // Shift exponent to the right by 1 bit
    }

    return result;
}

// Recursive approach
long long binary_exponentiation_recursive(long long base, long long exponent) {
    if (exponent == 0)
        return 1;

    long long temp = binary_exponentiation_recursive(base, exponent / 2);
    long long result = temp * temp;

    if (exponent % 2 == 1)
        result *= base;

    return result;
}

int main() {
    long long base = 5;
    long long exponent = 13;

    cout << "Iterative result: " << binary_exponentiation_iterative(base, exponent) << endl;
    cout << "Recursive result: " << binary_exponentiation_recursive(base, exponent) << endl;

    return 0;
}
```





# Modulo arithmetic in binary exponentiation

Lets say we have a number of order 10<sup>18</sup> and modulo also
having value 10<sup>18</sup>+7 now for our binary exponentiation we have
to multiply two values of order 10<sup>18</sup> which is the nearly
largest range of values in c++ so multiplying two values of order
10<sup>18</sup> will give us a number of order 10<sup>36</sup> which
cannot be stored by any data type in c++ giving an overflow
error(largest value storing data type has range nearly 10<sup>19</sup>
in c++) here the problem arises how are we going to mod it?

Long long a=(10<sup>18</sup>X10<sup>18</sup>)%mod gives overflow error
will return trash value

To deal with this problem we have yet another technique called binary
multiplication using the math here is.

If c=10<sup>2</sup>

Then we can write c also like this

c = 10+10+10+10+10+10+10+10+10+10

now applying this same technique in above problem we have

a is of order 10<sup>18</sup>

if we need to multiply aXa

we can write it like this a+a+a+a+a……………………..+a

now (a+a)=2X10<sup>18</sup> we can do the mod of this number without
getting any trash value and overflow errors.

(a<sup>b</sup>%mod)=(a%mod)<sup>b</sup>%mod

So if we do mod each time after calculating the sums of a it would not
have any effect on our final answer.

Since we have done binary multiplication + binary exponentiation the
time complexity of our code turns out to be O(log power X log a) hence
can be written simply as O((log(t))<sup>2</sup>).

# C++ code for applying binary multiplication in binary exponentiation and to calculate mod

```cpp
// Source Code Here  

#include <iostream>
using namespace std;

// Function to perform binary multiplication
long long binaryMultiply(long long a, long long b, long long mod) {
    long long result = 0;
    a %= mod;
    while (b) {
        if (b & 1)
            result = (result + a) % mod;
        a = (2 * a) % mod;
        b >>= 1;
    }
    return result;
}

// Function to perform binary exponentiation with modulo
long long binaryExponentiation(long long base, long long power, long long mod) {
    long long result = 1;
    base %= mod;
    while (power > 0) {
        if (power & 1)
            result = binaryMultiply(result, base, mod);
        base = binaryMultiply(base, base, mod);
        power >>= 1;
    }
    return result;
}

int main() {
    long long base, power, mod;
    cout << "Enter base: ";
    cin >> base;
    cout << "Enter power: ";
    cin >> power;
    cout << "Enter modulo value: ";
    cin >> mod;

    long long result = binaryExponentiation(base, power, mod);
    cout << "Result of (" << base << "^" << power << ") % " << mod << " = " << result << endl;

    return 0;
}
```

**<u>Use Cases of Binary Exponentiation in Competitive
Programming:</u>**

1.  Matrix multiplication

2.  Fast calculation of n th Fibonacci number

3.  Compute a large number modulo

4.  Apply permutations of a given sequence large number of times

Practice problem set for binary exponentiation:

1.  <https://www.geeksforgeeks.org/problems/padovan-sequence2855/1>

2.  <https://leetcode.com/problems/fibonacci-number/description/>

(do it in log n complexity)

3.  <https://www.geeksforgeeks.org/problems/geometric-progression3042/1>

4.  <https://www.geeksforgeeks.org/problems/matrix-exponentiation2711/1>

5.  <https://www.geeksforgeeks.org/problems/leftmost-divisor3822/1>

6.  <https://leetcode.com/problems/powx-n/description/>

7.  <https://www.geeksforgeeks.org/problems/ncr-mod-m-part-10038/1>

8.  <https://www.geeksforgeeks.org/problems/generalised-fibonacci-numbers1820/1>
