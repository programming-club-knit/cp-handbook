
# Prefix and Suffix Sum
We are going to start with the Prefix Sum, also called cumulative sum or inclusive scan.
And when we have covered that we will move on to the Suffix Sum, instead of having the sum direction from left to right, it will be from right to left.







## Prefix Sum

Prefix sum, also known as cumulative sum, is a computational technique used in computer science and mathematics to efficiently calculate the sum of values in a sequence up to a certain position. The prefix sum array stores the cumulative sum of elements from the beginning of the sequence up to each index.

Here's a brief explanation of how prefix sum works:

1. To calculate the prefix sum of an array we just need to grab the previous value of the prefix sum and add the current value of the traversed array. 

2. Traverse through the original array and compute the cumulative sum of elements encountered so far. Store these cumulative sums in the prefix sum array.

3. Once the prefix sum array is constructed, it allows for fast computation of the sum of values within any range in the original sequence. This is because the sum of elements from index `i` to `j` in the original array can be calculated as `prefix_sum[j] - prefix_sum[i-1]`, provided `i > 0`.

4. This becomes really helpful because if you want to know what the total sum up to certain point is, you can just check for the value in the prefix sum array.

Prefix sum is particularly useful in scenarios where you need to repeatedly calculate sums of subarrays in an array. It reduces the time complexity from O(n^2) to O(n) for calculating the sum of elements in a subarray.

#### Here is the code implementation of the prefix sum in C++ language :-

```
// Fills prefix sum array.       
void fillPrefixSum(int arr[], int n, int prefixSum[])  
{  
    prefixSum[0] = arr[0];  
    // Adding present element with previous element  
    for (int i = 1; i < n; i++)  
        prefixSum[i] = prefixSum[i - 1] + arr[i];  
}  
```

### Sum of an array between indexes L and R using Prefix Sum:

We can approach this kind of problem in following steps:

1. Create the prefix sum array of the given input array.
2. Now for every query i.e. L and R :  
        1. If L is greater than 1 , ```then print prefixSum[R]- prefixSum[L-1];```.  
        2. else print `prefixSum[R]`.

#### Here is the code implementation in c++ language.

```
int main()
{
    int n = 6;
    int a[] = { 3, 6, 2, 8, 9, 2 };
    //Calculating prefix sum
    pf[0] = a[0];
    for (int i = 1; i < n; i++) {
        pf[i] = pf[i - 1] + a[i];
    }
   
    int q = 4;
      //Creating a 2D vector to store queries and display output
    vector<vector<int> > query
        = { { 2, 3 }, { 4, 6 }, { 1, 5 }, { 3, 6 } };
       
      //Printing sum from Queries
    for (int i = 0; i < q; i++) {
        int l = query[i][0], r = query[i][1];
        if (r > n || l < 1) {
            cout << "Please input in range 1 to " << n
                 << endl;
            continue;
        }
        if (l == 1)
            cout << pf[r - 1] << endl;
        else
            cout << pf[r - 1] - pf[l - 2] << endl;
    }
    return 0;
}
```

## Suffix Sum

Suffix Sum is a precomputation technique in which the sum of all the elements of the original array from an index i till the end of the array is computed.

For the Suffix Sum array, we will use a similar approach to the Prefix Sum, with the slight modification that we wil start from the end and go to the beginning of the array.

Therefore, this suffix sum array will be created using the relation: 

```
suffixSum[i] = ar[i] + ar[i+1] + ar[i+2]+ ....ar[n-1];
```

![this is how suffix sum looks like: ](https://media.geeksforgeeks.org/wp-content/uploads/20220211133915/suffixarray.png)

#### Heres the code implementation in c++ language:

```
vector<int> createSuffixSum(vector<int> arr, int n)
{
    // Create an array or vector to store the suffix sum

    vector<int> suffixSum(n, 0);// vector with size n and all elements equal to zero.
 
    // Initialize the last element of
    // suffix sum array with last element
    // of original array
    suffixSum[n - 1] = arr[n - 1];
 
    // Traverse the array from n-2 to 0
    for (int i = n - 2; i >= 0; i--)
 
        // Adding current element
        // with previous element from back
        suffixSum[i] = suffixSum[i + 1] + arr[i];
 
    // Return the computed suffixSum array
    return suffixSum;
}
```
##### Naive approach would have taken the time complexity of O(n*n).
But using suffix sum array this would take only O(n), time.
## Questions to practice

1. [Equilibrium point](https://www.geeksforgeeks.org/problems/equilibrium-point-1587115620/1?page=1&category=prefix-sum&sortBy=submissions)

2. [Array manipulation](https://www.hackerrank.com/challenges/crush/problem)

3. [Range sum Query](https://leetcode.com/problems/range-sum-query-immutable/description/)
