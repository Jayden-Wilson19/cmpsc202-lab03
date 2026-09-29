# Lab 3: Asymptotic Analysis

This lab focuses on understanding and analyzing the asymptotic behavior of algorithms. We will explore concepts such as Big-O, Big-$\Theta$, and Big-$\Omega$ notations, and apply them to various algorithmic problems to determine their efficiency and scalability.

**Instructions:** To complete this lab, you may work in groups, but you must write your solutions yourself. Once you have completed the lab, push your changes to your forked repository.

## Problem 1

Suppose $T(n)$ is the worst case running time of an algorithm with input size $n$, and we know that $T(n)$ is $\mathcal{O}(n^3)$ and $\Omega(n^2)$. For each of the following statements, determine whether it must be true, must be false, or could be either true or false. Give a brief justification for each. 

1. $T(n)$ is $\mathcal{O}(n^2)$. Could be either. Could be Θ(n^2) which is the same as O(n^2). It could also be Θ(n^3) which is not the same as O(n^2).
2. $T(n)$ is $\Theta(n^3)$. Could be either. O(n^3) allows to include Θ(n^3), however it is not required.
3. $T(n)$ is $\Omega(n)$. Must be true. Since T(n) = Ω(n^2) and n^2 grows faster than n, this statement is true.
4. $T(n)$ is $\Theta(n^{1.5})$. Must be false. The lower bound is n^2. Θ(n^1.5) is not Ω(n^2) since it goes slower than the lower bound.
5. $T(n)$ is $\mathcal{O}(n)$. Must be false. Since n grows slower than n^2, T(n) = O(n) cannot also be Ω(n^2).
6. $T(n)$ is $\Theta(n^2 \log n)$. Could be either. n^2logn is normally shown between n^2 and n^3. It satisfies both lower and upper bound.


## Problem 2
Consider the following algorithm where $f(A, i, j)$ is an unknown algorithm that takes as input an array $A$ and two indicies $i$ and $j$ and returns a number. 

```
Mystery Algorithm
Input: An array of int $A$ of length $n$.
Output: int sum
    n = |A|
    sum = 0
    for i = 1 to n:
        for j = 1 to n:
            sum += f(A, i, j)
```

Without knowing anything about $f$, what can we say about the running time of the Mystery Algorithm in terms of $n$? Justify your answer. 
