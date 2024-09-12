# EXPONENTIATION AND BINARY EXPONENTIATION

**<u>BINARY EXPONENTIATION</u>**
**Binary exponentiation**, also known as exponentiation by squaring, is a
Binary exponentiation, also known as exponentiation by squaring, is a
technique used to efficiently compute large powers of a number modulo
another number. It is particularly useful in computer science and
cryptography where large numbers are involved.

**<u>What is Binary Exponentiation?</u>**

***Binary Exponentiation **or **Exponentiation by squaring **is the
process of calculating a number raised to the power another number (AB)
in **Logarithmic **time of the exponent or power, which speeds up the
execution time of the program.*

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





C++ code for binary exponentiation both iterative and recursive

<img src="./assets/images/image2.png" style="width:6.26806in;height:6.88194in"
alt="A screenshot of a computer program" />





**Modulo arithmetic in binary exponentiation**

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

**C++ code for applying binary multiplication in binary exponentiation
and to calculate mod**

<img src="./assets/images/image3.png" style="width:5.76042in;height:7.04861in"
alt="A computer screen shot of a program code Description automatically generated" />

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
