## Chapter 2 Divide & Conquer

### Lesson 3 Recursive functions

- Factorial: $O(n)$
- Fibonacci
- Ackermann Function
- Integer Partion
- Tower of Hanoi: $O(2^{n})$

### Lesson 4 Concept of D&C

#### D&C

- Design Philosophy
- Applicable Conditions (Properties)
  - sub-problems with small input size
  - can be divided into k subproblems
  - solutions can be merged to give the final solution
  - sub-problems mutually independent
    - no common sub-subproblems
- Basic Steps
- Computation Complexity

#### Algorithms & Problems

- Binary Search ($O(\log{n})$)

- Merge Sort ($O(n\log{n})$)

- Quick Sort ($O(n\log{n})$)
  - Worst: $O(n^2)$
  - Average : $O(n\log{n})$
  
- Chessboard Coverage
  - number of L-shaped dominoes: $\frac{4^k-1}{3}$
  - $T(n)=O(4^k)$

  <img src="Chapter 2 Divide & Conquer.assets\image-20201018142655568.png" alt="image-20201018142655568" style="zoom:67%;" />

### Lesson 5 D&C Algorithms

#### Algorithms

- Element Selection: $O(n)$
  - Worst: $O(n^2)$
  - Average: $O(n)$
- Selection in Expected Linear Time
  - $\lceil{n/5}\rceil$ medians
  - find median $x$ in the medians
  - $\frac{3(n-5)}{10}$ elements < $x$
    - reduce at least 1/4
- Closest Pair of Points: $O(n\log{n})$
- Large Integer Multipication: $O(n^2)\rightarrow O(n^{1.59})$

- Strassen ALG: $O(n^{\log{7}})\rightarrow O(n^{2.81})$







