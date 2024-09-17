---
title: COMBINATORICS
---

# Introduction to Combinatorics:

**What is combinatorics:** Combinatorics is a branch of mathematics
primarily concerned with counting and certain properties of finite
structures.

It deals with the study of enumeration, combination, and permutation of
sets of elements and the mathematical relations that characterize their
properties.

In other word we can also that Combinatorics is all about number of ways
of choosing some objects out of a collection and/or number of ways of
their arrangement. For example suppose there are five members in a club,
let's say there names are A, B, C, D, and E, and one of them is to be
chosen as the coordinator. Clearly any one out of them can be chosen so
there are 5 ways. Now suppose two members are to be chosen for the
position of coordinator and co-coordinator. Now, we can choose A as
coordinator and one out of the rest 4 as co-coordinator. Similarly we
can choose B as coordinator and one of out the remaining 4 as
co-coordinator, and similarly with C, D and E. So there will be total 20
possible ways.

**<u>Basic Combinatorics Rules:</u>**

Suppose there are two sets A and B.

The basic rules of combinatorics one must remember are:

1.  **The Rule of Product**:  
    The product rule states that if there are X number of ways to choose
    one element from A and Y number of ways to choose one element
    from B, then there will be X×Y number of ways to choose two
    elements, one from A and one from B.

2.  **The Rule of Sum**:  
    The sum rule states that if there are X number of ways to choose one
    element from A and Y number of ways to choose one element from B,
    then there will be X+Y number of ways to choose one element that can
    belong to either A or to B.

3.  **Rule of Inclusion-Exclusion :**

> The principle of inclusion-exclusion says that in order to count only
> unique ways of doing a task, we must add the number of ways to do it
> in one way and the number of ways to do it in another and then
> subtract <img src="./assets/images/image1N.png"
> style="width:2.53472in;height:1.65486in" />the number of ways to do
> the task that are common to both sets of ways. The principle of
> inclusion-exclusion is also known as the **subtraction principle**.
>
> For any set A and B,
>
> \|A U B\| = \|A\| + \|B\| - \|A $`\cap`$ B\|.

These rules can be used for a finite collection of sets.

**Examples:**

**Example 1** – In how many ways can 3 winning prizes be given to the
top 3 players in a game played by 12 players?

**Solution** – We have to distribute 3 prizes among 12 players. This
task can be divided into 3 subtasks of assigning a single prize to a
certain player.

Giving out the first prize can be done in 12 different ways. After
giving out the first prize, two prizes remain and 11 players remain.
Similarly, the second prize and third prize can be given in 11 ways and
10 ways. The total number of ways by the product rule is 12 \* 11 \* 10
= 1320.

**Example 2** – How many distinct license plates are possible in the
given format- Two alphabets in uppercase, followed by two digits then a
hyphen, and finally four digits. Sample- AB12-3456.

**Solution** – There are 26 possibilities for each of the two letters
and 10 possibilities for each of the digits. Therefore, the total number
of possibilities is – 26 \* 26 \* 10 \* 10 \* 10 \* 10 \* 10 \* 10 =
676000000.

**Example 3** – How many variable names of length up to 3 exist if the
variable names are alphanumeric and case-sensitive with the restriction
that the first character has to be an alphabet?

**Solution** – Let N1, N2, and N3 denote the number of possible variable
names of lengths 1, 2, and 3. Therefore, the total number of variable
names is N1 + N2 + N3.

For N1, there are only 52 possibilities since the first character has to
be an alphabet.

For N2, there are 52 \* 62 = 3224 possibilities.

For N3, there are 52 \* 62 \* 62 = 199888 possibilities.

Therefore, total number of variable names = 52 + 3224 + 199888 = 203164

**Example 4** – How many binary strings of length 8 either start with a
‘1’ bit or end with two bits ’00’?

**Solution** – If the string starts with one, there are 7 characters
left which can be filled in 2^7 = 128 ways. If the string ends with ’00’
then 6 characters can be filled in 2^6 = 64 ways. Now if we add the
above sets of ways and conclude that it is the final answer, then it
would be wrong. This is because there are strings with start with ‘1’
and end with ’00’ both, and since they satisfy both criteria they are
counted twice. So we need to subtract such strings to get a correct
count. Strings that start with ‘1’ and end with ’00’ have five
characters that can be filled in 2^5 = 32 ways.

So by the inclusion-exclusion principle we get –

Total strings = 128 + 64 – 32 = 160.

**<u>Factorials:</u>**

Factorial of a number n is defined as a product of all positive
descending integers, Factorial of n is denoted by n!. Factorial can be
calculated using the following recursive formula where the recursive
call is made to a multiplicity of all the numbers lesser than the number
for which the factorial is computed as the formula to calculate
factorial is as follows:

n! = n \* \[(n-1)!\]

i.e factorial of n - (n!) = n \* (n-1) \* ......\* 3 \* 2\* 1.

**Note**: Factorial of 0 is 1.

1.  Factorial Program using Loop:

<img src="./assets/images/image2.tmp" style="width:5.30347in;height:2.97986in"
alt="Factorial Program in C++ - javatpoint - Brave" />

2.  <img src="./assets/images/image3.tmp" style="width:5.63125in;height:4.44722in"
    alt="Factorial Program in C++ - javatpoint - Brave" />Factorial
    Program using Recursion:

**<u>Permutation</u>**

Permutation is defined as a mathematical calculation that tells us the
way a particular set of data are arranged in a particular way. In simple
word we can say that permutation is the number of ways objects can be
ordered and arranged.

If n objects are available and we arrange all, then every arrangement
possible is called a permutation. In other words, arranging some objects
in a specific order is called permutation. For example, we need to
choose two numbers out of {1, 2, 3}, then there can be 6 ways in which
we can do the same. (1, 2), (2, 1), (2, 3), (3, 2), (1, 3), and (3, 1).
As we can see here both (1, 2) and (2, 1) are two different
permutations, unlike combinations where (1, 2) and (2, 1) are the same
combination.

**Representation of Permutation:**

- P(n, r)

<!-- -->

- nPr

- Pn,k

**Permutation Formula ( nPr ):**

P(n, r) = n! / (n-r)!

where,

- **n** is the Number of Total Objects

<!-- -->

- **r **is the Number of Objects Chosen at Once

<!-- -->

- 0 ≤ r ≤ n

**Types of Permutation:**

In the study of permutation, there are some cases such as:

- Permutation with Repetition

<!-- -->

- Permutation without Repetition

<!-- -->

- Permutation of Multi-Sets

<!-- -->

- **Permutation With Repetition:**

> This is the simplest of the lot. In such problems, the objects can be
> repeated. Let’s understand these problems with some examples.
>
> **Example**: How many 3-digit numbers greater than 500 can be formed
> using 3, 4, 5, and 7?
>
> Since a three-digit number, greater than 500 will have either 5 or 7
> at its hundredth place, we have 2 choices for this place.
>
> There is no restriction on repetition of the digits, hence for the
> remaining 2 digits we have 4 choices each
>
> So the total permutations are,
>
> 2 × 4 × 4 = 32

- **Permutation Without Repetition:**

> In this class of problems, the repetition of objects is not allowed.
> Let’s understand these problems with some examples.
>
> Example: How many 3-digit numbers divisible by 3 can be formed using
> digits 2, 4, 6, and 8 without repetition?
>
> For a number to be divisible by 3, the sum of it digits must be
> divisible by 3.
>
> From the given set, various arrangements like 444 can be formed but
> since repetition isn’t allowed we won’t be considering them.
>
> We are left with just 2 cases i.e. 2, 4, 6 and 4, 6, 8
>
> Number of arrangements are 3! in each case
>
> Hence the total number of permutations are: 3! + 3! = 12

- Permutation of Multi-Sets:

> Permutation when the objects are not distinct
>
> This can be thought of as the distribution of n objects into r boxes
> where the repetition of objects is allowed and any box can hold any
> number of objects.
>
> 1st box can hold n objects
>
> 2nd box can hold n objects
>
> 3rd box can hold n objects
>
> . .
>
> . .
>
> . .
>
> rth box can hold n objects
>
> Hence total number of arrangements are,
>
> n × n × n . . . (r times) = nr
>
> Example: A police officer visits the crime scene 3 times a week for
> investigation. Find the number of ways to schedule his visit if there
> is no restriction on the number of visits per day?
>
> Number of ways to schedule first visit is 7 (any of the 7 days)
>
> Number of ways to schedule second visit is 7 (any of the 7 days)
>
> Number of ways to schedule third visit is 7 (any of the 7 days)
>
> Hence, the number of ways to schedule first and second and third visit
> is
>
> 7 × 7 × 7 = 7<sup>3</sup> = 343.

Programs for permutations coefficient:

1.  Using the factorial:

> <img src="./assets/images/image4.tmp" style="width:3.64097in;height:3.91944in"
> alt="Online C++ Compiler - Brave" />

2.  Just using the formula:

> <img src="./assets/images/image5.tmp" style="width:4.61458in;height:3.82569in"
> alt="Online C++ Compiler - Brave" />

3.  Using dynamic programming:

<img src="./assets/images/image6.tmp" style="width:6.15208in;height:5.98264in"
alt="Online C++ Compiler - Brave" />

**<u>Combination</u>**

Combination is a way of choosing items from a set, such as (unlike
permutations) the order of selection doesn’t matter. In smaller cases,
it’s possible to count the number of combinations. Combination refers to
the mixture of n things taken k at a time without repetition. To know
the combinations in the case where repetition is allowed, the terms like
k-selection or k-combination along with repetition are often used. For
instance, if we’ve two elements A and B, then there’s just one way to
select two items, we select both of them.

Combination is the choice of selecting r things from a group of n things
without replacement and where the order of selection is not important.

Number of combinations when ‘r’ elements are selected out of a complete
set of ‘n’ elements is denoted by nCr.

**Representation of Combination:**

- C(n, r)

<!-- -->

- nCr

- Cn,k

**Combination Formula ( nCr ):**

C(n, r) = n! / ((n-r)! \* r!)

where,

- **n** is the Number of Total Objects

<!-- -->

- **r **is the Number of Objects Chosen at Once

<!-- -->

- 0 ≤ r ≤ n

**Example:**

1.  Handshaking problem:

Handshaking problem is one of the most interesting problems in
combination. It is used to find that in a room full of people how many
handshakes are required for everybody to shake everybody else’s hand
exactly once.

Basically when there are 2 people there will be one handshake and if
there are three people there will be 3 handshakes and so on. This many
people we can count but let’s suppose there are thousands of people in a
hall then we can’t count each handshake here the need for the
combination arises.

<img src="./assets/images/image7.tmp" style="width:4.64301in;height:4.09236in"
alt="Combinations - Definition, Formula, Solved Examples, FAQs - Brave" />

To see the people present, and consider one person at a time. The first
person will shake hands with n – 1 other people. The next person will
shake hands with n-2 other people, not counting the first person again.
Following this, it will give us a total number of

(n – 1) + (n – 2) + … + 2 + 1

= n(n – 1)/ 2 handshakes.

- ***Total Number of Handshakes = n × (n – 1)/2***

<!-- -->

- ***Total Number of Handshakes = nC2***

**Properties of combination coefficient:**

1.  ⁿCr = ⁿCn-r.

2.  ⁿCx = ⁿCy, then either x = y or x + y = n.

3.  Recursive formula for combination:

> ⁿ<sup>-1</sup>Cr + <sup>n-1</sup>Cr<sub>-1</sub> = ⁿCr

4.  ⁿCr + ⁿCr<sub>+1</sub> = ⁿ<sup>+1</sup>Cr<sub>+1</sub>

**Programs for combination coefficient:**

1.  Using factorial function:

> <img src="./assets/images/image8.tmp" style="width:4.62069in;height:4.13422in"
> alt="Online C++ Compiler - Brave" />

2.  Using formula directly:

> <img src="./assets/images/image9.tmp" style="width:4.24713in;height:4.06873in"
> alt="Online C++ Compiler - Brave" />

**<u>Binomial coefficient</u>**

A binomial coefficient C(n, k) can be defined as the coefficient of x^k
in the expansion of (1 + x)^n.

A binomial coefficient C(n, k) also gives the number of ways,
disregarding order, that k objects can be chosen from among n objects
more formally, the number of k-element subsets (or k-combinations) of a
n-element set.

(1+x)<sup>2</sup> = 1 + 2x + x<sup>2</sup> = <sup>2</sup>C<sub>0</sub> +
<sup>2</sup>C<sub>1</sub> x+ <sup>2</sup>C<sub>2</sub> x<sup>2</sup>

(1+x)<sup>3</sup> = 1 + 3x + 3x<sup>2</sup> + x<sup>3</sup> =
<sup>3</sup>C<sub>0</sub> + <sup>3</sup>C<sub>1</sub> x+
<sup>3</sup>C<sub>2</sub> x<sup>2</sup> + <sup>3</sup>C<sub>3</sub>
x<sup>3</sup>

..

..

So on.

Thus, we can see that combinations are only the binomial coefficients.

**Example:**

Consider expanding (x+2)<sup>5</sup> :

(x+2)<sup>5</sup>=(x+2)(x+2)(x+2)(x+2)(x+2)

One quickly realizes that this is a very tedious calculation involving
multiple applications of the distributive property. The binomial theorem
provides a method of expanding binomials raised to powers without
directly multiplying each factor:

(x+y)<sup>n</sup> = <sup>n</sup>C<sub>0</sub> x<sup>n</sup>
y<sup>0</sup> + <sup>n</sup>C<sub>1</sub> x<sup>n-1</sup>
y<sup>1</sup> + <sup>n</sup>C<sub>2</sub> x<sup>n-2</sup> y<sup>2</sup>
+….. .. . . . .+ <sup>n</sup>C<sub>n-1</sub> x<sup>1</sup>
y<sup>n-1</sup> + <sup>n</sup>C<sub>n</sub> x<sup>0</sup> y<sup>n</sup>

More compactly we can write,

(x+y)<sup>n</sup>= $`\sum_{k = 0}^{n}{}`$ <sup>n</sup>C<sub>k</sub>
x<sup>n-k</sup> y<sup>k</sup>

**Program to find binomial coefficient:**

1.  **Recursively:**

The formula for recursively solving binomial coefficients.

C(n, k) = C(n-1, k-1) + C(n-1, k)

C(n, 0) = C(n, n) = 1

<img src="./assets/images/image10.tmp" style="width:4.24097in;height:3.90139in"
alt="Online C++ Compiler - Brave" />

2.  Using factorial by direct formula:

<sup>n</sup>Cr = n! / ( (n-r)! \* r!)

<img src="./assets/images/image11.tmp" style="width:4.47126in;height:4.17616in"
alt="Online C++ Compiler - Brave" />

**<u>Pascal’s Triangle</u>**

<img src="./assets/images/image12.png" style="width:4.35069in;height:3.925in"
alt="enter image description here" />

The image above is pascal’s triangle.

This is nothing but the coefficients of the terms of binomial expansion
for different powers.

Pascal’s triangle is a never-ending equilateral triangle of numbers that
follow a rule of adding the two numbers above to get the number below.
Two of the sides are “all 1's” and because the triangle is infinite,
there is no “bottom side.”

<img src="./assets/images/image13.jpeg" style="width:5.90805in;height:3.93131in"
alt="The numbers of Pascal’s triangle match the number of possible combinations (nCr) when faced with having to choose r-number of objects among n-number of available options." />

**Approach for program for pascal’s triangle:**

The number of entries in every line is equal to line number. For
example, the first line has “1“, the second line has “1 1“, the third
line has “1 2 1“,.. and so on. Every entry in a line is value of a
Binomial Coefficient. The value of ith entry in line number line is
C(line, i). The value can be calculated using following formula.

C(line, i) = line! / ( (line-i)! \* i! )

**Program for pascal’s triangle:**

<img src="./assets/images/image14.tmp" style="width:5.22361in;height:5.35069in"
alt="Online C++ Compiler - Brave" />

**<u>Problems to practice for combinatorics:</u>**

1.  <https://leetcode.com/problems/isomorphic-strings/description/?envType=daily-question&envId=2024-04-02>

2.  <https://leetcode.com/problems/sum-of-all-subset-xor-totals/description/>

3.  <https://leetcode.com/problems/distribute-candies-among-children-i/description/>

4.  <https://leetcode.com/problems/count-sorted-vowel-strings/description/>

5.  <https://codeforces.com/problemset/problem/1743/A>

6.  <https://codeforces.com/problemset/problem/1855/B>

7.  <https://codeforces.com/problemset/problem/478/B>

8.  <https://leetcode.com/problems/find-triangular-sum-of-an-array/description/>

9.  <https://leetcode.com/problems/distribute-candies-among-children-ii/description/>

10. <https://codeforces.com/problemset/problem/1840/C>

11. <https://codeforces.com/problemset/problem/1539/A>

12. <https://codeforces.com/problemset/problem/630/C>

13. <https://codeforces.com/problemset/problem/1328/B>

14. <https://codeforces.com/problemset/problem/1931/D>

15. <https://leetcode.com/problems/unique-paths/description/>

16. <https://leetcode.com/problems/poor-pigs/description/>

17. <https://leetcode.com/problems/probability-of-a-two-boxes-having-the-same-number-of-distinct-balls/description/>

18. <https://leetcode.com/problems/kth-smallest-instructions/description/>
