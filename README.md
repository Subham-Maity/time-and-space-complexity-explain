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