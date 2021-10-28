---
description: Coderbyte & CLR
---

# Matrix Chain Multiplication

Have the function MatrixChains(**arr**) read the array of positive integers stored in **arr** where every pair will represent an NxM matrix. For example: if **arr** is \[1, 2, 3, 4] this means you have a 1x2, 2x3, and a 3x4 matrix. So there are N-1 total matrices where N is the length of the array. Your goal is to determine the least number of multiplications possible after multiplying all the matrices. Matrix multiplication is associative so (A\*B)\*C is equal to A\*(B\*C).\
\
For the above example, let us assume the following letters represent the different matrices: A = 1x2, B = 2x3, and C = 3x4. Then we can multiply the matrices in the following orders: (AB)C or A(BC). The first ordering requires (1\*2\*3) = 6 then we multiply this new 1x3 matrix by the 3x4 matrix and we get (1\*3\*4) = 12. So in total, this ordering required 6 + 12 = 18 multiplications. Your program should therefore return **18** because the second ordering produces more multiplications. The input array will contain between 3 and 30 elements.\


**Examples**

Input: new int\[] {2, 3, 4}\
Output: 24

Input: new int\[] {1, 4, 5, 6, 8}\
Output: 98

{% hint style="info" %}
bottom up

****[**video for Matrix Chain**](https://www.youtube.com/watch?v=GMzVeWpyTN0)****
{% endhint %}

```java
  public static int MatrixChains(int[] arr) {
    //code goes here  
    int N = arr.length;
    int[][] dp = new int[N][N];

    for(int i = 0; i < N; i++){
      for(int j = i + 2; j < N; j++){
        dp[i][j] = Integer.MAX_VALUE;
      }
    }
    for(int j = 0; j < N; j++){
      for(int i = j - 2; i >= 0; i--){
        for(int  v = i + 1; v < j; v++){
          dp[i][j] = Math.min(dp[i][j], dp[i][v] + dp[v][j] + arr[i] * arr[v] * arr[j]);
        }
      }
    }
    return dp[0][N - 1];
  }
```

{% hint style="info" %}
top down
{% endhint %}

```java
  public static int MatrixChains(int[] arr) {
    // code goes here  
    return MatrixChainOrder(arr, 1, arr.length - 1);
    // return arr[0];
  }

  static int MatrixChainOrder(int p[], int i, int j) 
  { 
      if (i == j) 
          return 0; 
      int min = Integer.MAX_VALUE; 
      // place parenthesis at different places between 
      // first and last matrix, recursively calculate 
      // count of multiplications for each parenthesis 
      // placement and return the minimum count 
      for (int k = i; k < j; k++)  { 
          int count = MatrixChainOrder(p, i, k) 
                      + MatrixChainOrder(p, k + 1, j) 
                      + p[i - 1] * p[k] * p[j]; 
          if (count < min) min = count; 
      } 
      // Return minimum count 
      return min; 
  } 
```
