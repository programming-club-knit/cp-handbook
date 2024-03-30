
# Modular Arithmetic

Modular Arithmetic is an important topic in Competitive Programming. Some questions involve such big numbers that they can’t even fit in any of the data types. So, modular arithmetic is a method to avoid data overflow.


## [Quotient Remainder Theorem](https://www.geeksforgeeks.org/quotient-remainder-theorem/)
It states that, for any pair of integers a and b (b is positive), there exist two unique integers q and r such that:

$a = b * q + r$  
$0 \le r < b$


## Need for Usage

The largest data type in C++ is unsigned long long int, which is of 64-bits and can handle integers from 0 to $2^{64}-1$. But sometimes, the computations are so big that this data type cannot handle such big computations. And if overflow happens, it does not generate an error in most cases and just returns a garbage value. So, knowledge of this topic becomes a must to remedy the error if it arises.

Generally, the question statement mentions if modulo needs to be used. The statement that prompts the usage of modulo is:

"Print the answer modulo $10^9+7$."


## Rules Governing Usage of Modulo

Modulo cannot be simply used for arithmetic operations and follows certain rules. The rules are as follows:

- #### $(a + b)$ % $mod = ((a$ % $mod) + (b$ % $mod))$ % $mod$
- $(a * b)$ % $mod = ((a$ % $mod) * (b$ % $mod))$ % $mod$
- $(a - b)$ % $mod = ((a$ % $mod) - (b$ % $mod) + mod)$ % $mod$


The difference from the general pattern in the case of subtraction can be understood by the following example:

$a = 9, b = 6, mod = 4$

$(9-6)$ % $4 = ((9$ % $4)-(6$ % $4)+4)$ % $4$

$3$ % $4 = (1-2+4)$ % $4$

$3 = 3$

$LHS=RHS.$

##

### [Modular Inverse](https://cp-algorithms.com/algebra/module-inverse.html) 

It can be proven that this formula is valid for all values of \(a\) and \(b\).

- $(a / b)$ % $mod = (a * (inverse\ of\ b\ if\ it\ exists))$ % $mod$

Inverse of b exists only when b and mod are co-primes, that is-

$Gcd( b , mod ) = 1$

I would recommend you to read [this article](https://cp-algorithms.com/algebra/module-inverse.html) for in depth understanding of [Modular Inverse](https://cp-algorithms.com/algebra/module-inverse.html)
<br>

## Practice Problems 
    
- [Xor Equality](https://www.codechef.com/problems/XOREQUAL)
- [Array Modification](https://www.codechef.com/problems/MARM)
- [Word Counding](https://www.codechef.com/problems/WCOUNT)
- [Koxia and number Theory](https://codeforces.com/problemset/problem/1770/C)

### Also See

[Precomputation Techniques for Competitive Programming](https://www.geeksforgeeks.org/precomputation-techniques-for-competitive-programming/)


    
    