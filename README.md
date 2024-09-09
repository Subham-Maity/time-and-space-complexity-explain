# Time & Space Complexity  

- [Concept:](#concept)
- [Easy Big O Calculation Rules:](#easy-big-o-calculation-rules)
- [How to calculate program's time complexity](#how-to-calculate-programs-time-complexity)
## Concept:
![img1](./img/1.png)
![img2](./img/2.png)
![img3](./img/3.png)
![img4](./img/4.png)
![img5](./img/5.png)
![img6](./img/6.png)


## Easy Big O Calculation Rules:
1. Ignore lower degree terms
2. Ignore constants

Corrected and formatted calculations:

1. f(n) = 2n² + 3n → O(n²)

2. f(n) = 4n⁴ + 3n³ → O(n⁴)

3. f(n) = n² + log n → O(n²)

4. f(n) = 3n³ + 2n² + 5 → O(n³)

5. f(n) = n³/300 → O(n³)

6. f(n) = 5n²/log n → O(n²)

7. f(n) = n/4 → O(n)

8. f(n) = (n+4)/4 → O(n)

Key points:
- The highest degree term determines the Big O notation.
- Constant coefficients (like 2, 3, 4, 1/300, etc.) are ignored.
- Lower degree terms (like n² when n³ is present) are ignored.
- Logarithmic terms are considered lower order than polynomial terms.
- Division by a constant (like /4) doesn't affect the Big O notation.
- Division by a logarithmic term (like /log n) doesn't change the polynomial degree in Big O notation.


## How to calculate program's time complexity
Here's an improved and cleaner version of your explanation for calculating time complexity:

---

## How to Calculate Time Complexity

### 1. Print Array
```cpp
void printArray(int arr[], int n) {
    for(int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
}
```
- **Explanation**: The loop runs from 0 to `n`, meaning it iterates `n` times.
- **Time Complexity**: O(n)

### 2. Reverse an Array
```cpp
void reverse(int arr[], int n) {
    int start = 0;
    int end = n - 1;
    while (start <= end) {
        swap(arr[start], arr[end]);
        start++;
        end--;
    }
}
```
- **Explanation**: The loop swaps elements from both ends until the middle. This results in approximately `n/2` swaps. Since constants are ignored in Big-O notation, it simplifies to O(n).
- **Time Complexity**: O(n)

### 3. Linear Search
```cpp
int linearSearch(int arr[], int n, int x) {
    for (int i = 0; i < n; i++) {
        if (arr[i] == x) {
            return i; 
        }
    }
    return -1;
}
```
- **Explanation**: In the worst case, we may have to check every element of the array, which requires `n` comparisons.
- **Time Complexity**: O(n)

### 4. Separate Loops
```cpp
int a = 0, b = 0;
for (int i = 0; i < N; i++) {
    a = a + rand();
}
for (int j = 0; j < M; j++) {
    b = b + rand();
}
```
- **Explanation**: The first loop runs `N` times and the second loop runs `M` times. Since these are independent loops, their complexities add up.
- **Time Complexity**: O(N) + O(M) = O(N + M)

### 5. Nested Loop with Independent Loop
```cpp
int a = 0, b = 0;
for (int i = 0; i < N; i++) {
    for (int j = 0; j < N; j++) {
        a = a + j;
    }
}

for (int k = 0; k < N; k++) {
    b = b + k;
}
```
- **Explanation**: The first part has a nested loop that runs `N * N` times, so it has a time complexity of O(N²). The second part has a single loop that runs `N` times.
- **Time Complexity**: O(N²) + O(N) = O(N²)

### 6. Nested Loop with Varying Inner Loop
```cpp
int a = 0;
for (int i = 0; i < N; i++) {
    for (int j = N; j > i; j--) {
        a = a + i + j;
    }
}
```
- **Explanation**: The outer loop runs `N` times. The inner loop runs `N - i` times, which decreases as `i` increases. This results in a quadratic time complexity because the total number of iterations is proportional to the sum of a series.
- **Time Complexity**: O(N²)

### 7. Get Minimum and Maximum from Array
```cpp
#include<iostream>
using namespace std;

int getMin(int num[], int n) {
    int min = INT_MAX;
    for(int i = 0; i < n; i++) {
        if(num[i] < min) {
            min = num[i];
        }
    }
    return min;
}

int getMax(int num[], int n) {
    int max = INT_MIN;
    for(int i = 0; i < n; i++) {
        if(num[i] > max) {
            max = num[i];
        }
    }
    return max; 
}
```
- **Explanation**: Both `getMin` and `getMax` iterate through the array exactly once, performing a comparison at each step.
- **Time Complexity**: O(n) for both functions.



