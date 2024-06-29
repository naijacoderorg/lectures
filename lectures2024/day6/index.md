Day 6: Growth of Functions
===========================

Morning
-------

### Reflection from Last Day:
* Answer questions about for objects, libraries in Python
* Discuss exercises from previous day

Understanding the growth of functions and asymptotic notation is crucial in analyzing the efficiency of algorithms and data structures. These concepts help in quantifying how the runtime or space requirements of algorithms change with input size. Let's delve into each of these concepts:

### Growth of Functions

In computer science, the growth of a function refers to how its runtime (or space) increases as the size of the input grows. This growth is typically measured in terms of the input size $n$.

#### Example of Growth Functions:

Consider two functions:
- $f(n) = 2n + 1$
- $g(n) = n^2 + 3n$

As $n$ increases:
- $f(n)$ grows linearly $O(n)$ because the dominant term is $n$.
- $g(n)$ grows quadratically $O(n^2)$ because the dominant term is $n^2$.

### Asymptotic Notation

Asymptotic notation provides a formal way to describe the limiting behavior (as $n$ becomes very large) of a function:

1. **Big O Notation (O)**:
   - **Definition**: Represents the upper bound of the function's growth rate. It describes the worst-case scenario.
   - **Example**: Intuition is that $O(n^2)$ means the function grows no faster than $n^2$.

2. **Omega Notation ($\Omega$)**:
   - **Definition**: Represents the lower bound of the function's growth rate. It describes the best-case scenario.
   - **Example**: Intuition is that $\Omega(n)$ means the function grows at least as fast as $n$.

3. **Theta Notation ($\Theta$)**:
   - **Definition**: Represents both the upper and lower bounds, providing a tight bound on the function's growth rate.
   - **Example**: Intuition is that $\Theta(n)$ means the function grows exactly like $n$.

In mathematical terms, Big O notation $O(f(n))$ is used to denote an upper bound on the asymptotic growth rate of a function $f(n)$ as $n$ becomes large. Here's the mathematical definition of Big O notation:

### Definition

Given two functions $f(n)$ and $g(n)$:

$$f(n) = O(g(n))$$

This statement means that there exist constants $c > 0$ and $n_0 \geq 0$ such that for all $n \geq n_0$, the function $f(n)$ is bounded above by $c \cdot g(n)$:

$$|f(n)| \leq c \cdot |g(n)| \quad \text{for all } n \geq n_0$$

### Key Points

- **Upper Bound**: Big O notation provides an upper bound on the growth rate of $f(n)$.
- **Constant Factors**: It ignores constant factors and lower-order terms, focusing on the dominant term that contributes most significantly to the growth rate as $n$ increases.
- **Asymptotic Behavior**: Big O notation describes the long-term behavior of functions as $n$ approaches infinity.

### Example Interpretation

If $f(n) = 2n + 1$, we say $f(n) = O(n)$ because for sufficiently large $n$, $2n + 1$ is bounded above by $cn$ for some constant $c$. Specifically, for $c = 3$ and $n_0 = 1$, $2n + 1 \leq 3n$ holds for all $n \geq 1$.

### Practical Use

In algorithm analysis, Big O notation is widely used to characterize the time complexity (and sometimes space complexity) of algorithms. It helps in comparing the efficiency of algorithms and predicting how they will perform with larger inputs.

In mathematical terms, Big Omega notation $\Omega(f(n))$ is used to denote a lower bound on the asymptotic growth rate of a function $f(n)$ as $n$ becomes large. Here's the mathematical definition of Big Omega notation:

### Definition

Given two functions $f(n)$ and $g(n)$:

$$f(n) = \Omega(g(n))$$

This statement means that there exist constants $c > 0$ and $n_0 \geq 0$ such that for all $n \geq n_0$, the function $f(n)$ is bounded below by $c \cdot g(n)$:

$$|f(n)| \geq c \cdot |g(n)| \quad \text{for all } n \geq n_0$$

### Key Points

- **Lower Bound**: Big Omega notation provides a lower bound on the growth rate of $f(n)$.
- **Constant Factors**: Similar to Big O notation, it ignores constant factors and lower-order terms, focusing on the dominant term that contributes most significantly to the growth rate as $n$ increases.
- **Asymptotic Behavior**: Big Omega notation describes the long-term behavior of functions as $n$approaches infinity.

### Example Interpretation

If $f(n) = n^2 + 3n$, we say $f(n) = \Omega(n^2)$ because for sufficiently large $n$, $n^2 + 3n$ is bounded below by $cn^2$ for some constant $c$. Specifically, for $c = 1$ and $n_0 = 1$, $n^2 + 3n \geq n^2$ holds for all $n \geq 1$.

### Practical Use

Big Omega notation is used similarly to Big O notation in algorithm analysis. It helps in characterizing the lower bounds of algorithms' time complexity (and sometimes space complexity), providing insight into their performance guarantees for large inputs.

### Comparison with Big O Notation

- **Big O vs. Big Omega**: While Big O provides an upper bound on the growth rate of a function $f(n)$, Big Omega provides a lower bound. Together, they can give a more complete picture of an algorithm's complexity by indicating both its worst-case and best-case scenarios.

In mathematical terms, Big Theta notation $\Theta(f(n))$ is used to denote a tight bound on the asymptotic growth rate of a function $f(n)$ as $n$ becomes large. Here's the mathematical definition of Big Theta notation:

### Definition

Given two functions $f(n)$ and $g(n)$:

$$f(n) = \Theta(g(n))$$

This statement means that there exist constants $c_1 > 0$, $c_2 > 0$, and $n_0 \geq 0$ such that for all $n \geq n_0$, the function $f(n)$ is bounded both above and below by $c_1 \cdot g(n)$ and $c_2 \cdot g(n)$, respectively:

$$c_1 \cdot |g(n)| \leq |f(n)| \leq c_2 \cdot |g(n)| \quad \text{for all } n \geq n_0$$

### Key Points

- **Tight Bound**: Big Theta notation provides a tight or asymptotically tight bound on the growth rate of $f(n)$. It means $f(n)$ grows at the same rate as $g(n)$ within constant factors, asymptotically speaking.
  
- **Constant Factors**: Similar to Big O and Big Omega notations, Big Theta ignores constant factors and lower-order terms, focusing on the dominant term that contributes most significantly to the growth rate as $n$ increases.
  
- **Asymptotic Behavior**: Big Theta notation describes the long-term behavior of functions as $n$approaches infinity, indicating that $f(n)$ and $g(n)$ grow at the same rate.

### Example Interpretation

If $f(n) = n^2 + 3n$, and $g(n) = n^2$, we say $f(n) = \Theta(n^2)$ because there exist constants $c_1 = 1$, $c_2 = 1$, and $n_0 = 1$ such that $n^2 \leq n^2 + 3n \leq n^2$ holds for all $n \geq 1$.

### Practical Use

Big Theta notation is particularly useful in algorithm analysis as it provides a precise description of an algorithm's asymptotic behavior. It indicates both the upper and lower bounds of the growth rate of algorithms' time complexity (and sometimes space complexity), giving a clear understanding of their efficiency across different input sizes.

### Comparison with Big O and Big Omega Notations

- **Big O vs. Big Omega vs. Big Theta**: 
  - Big O provides an upper bound on the growth rate of $f(n)$.
  - Big Omega provides a lower bound on the growth rate of $f(n)$.
  - Big Theta provides both upper and lower bounds, indicating that $f(n)$ grows asymptotically at the same rate as $g(n)$.



Afternoon
---------

In mathematical analysis, small o $o(f(n))$ and small omega $\omega(f(n))$ notations are used to describe the asymptotic behavior of functions in terms of limits. Here’s how they are defined using limits:

### Small o Notation $o(f(n))$

Small o notation $o(f(n))$ denotes that a function $g(n)$ grows asymptotically slower than $f(n)$ as $n$ approaches infinity.

#### Definition:

$$g(n) = o(f(n)) \quad \text{if and only if} \quad \lim_{n \to \infty} \frac{g(n)}{f(n)} = 0$$

In simpler terms, $g(n)$ is in $o(f(n))$ if for every positive constant $c > 0$, there exists a constant $n_0 \geq 0$ such that for all $n \geq n_0$, $|g(n)| < c \cdot |f(n)|$.

### Small Omega Notation $\omega(f(n))$

Small omega notation $\omega(f(n))$ denotes that a function $g(n)$ grows asymptotically faster than $f(n)$ as $n$ approaches infinity.

#### Definition:

$$g(n) = \omega(f(n)) \quad \text{if and only if} \quad \lim_{n \to \infty} \frac{g(n)}{f(n)} = \infty$$

In other words, $g(n)$ is in $\omega(f(n))$ if for every positive constant $c > 0$, there exists a constant $n_0 \geq 0$ such that for all $n \geq n_0$, $|g(n)| > c \cdot |f(n)|$.

### Key Points:

- **Asymptotic Behavior**: Small o notation $o(f(n))$ indicates that $g(n)$ grows slower than $f(n)$ as $n$ becomes large, while small omega $\omega(f(n))$ indicates that $g(n)$ grows faster than $f(n)$.
  
- **Limits**: Both notations are defined using limits to formalize the concept of growth rate in asymptotic analysis.
  
- **Precision**: These notations provide a more precise characterization of asymptotic relationships compared to Big O and Big Omega, especially in contexts where exact growth rates are important.


Exercises
---------

### Exercise 1: Identifying Notations

For each pair of functions $f(n)$ and $g(n)$, determine whether $f(n)$ is in Big O, Small o, Big Theta, Small omega, or Big Omega relative to $g(n)$.

1. $f(n) = 2n + 1$, $g(n) = n$
2. $f(n) = n^2$, $g(n) = 3n^2$
3. $f(n) = \log n$, $g(n) = \sqrt{n}$
4. $f(n) = n^{0.5}$, $g(n) = n^{0.4}$
5. $f(n) = n \log n$, $g(n) = n$

### Exercise 2: Verifying Limits

Determine whether the following statements are true (T) or false (F):

1. $n^2 = O(n^3)$
2. $n^2 = o(n^3)$
3. $n^2 = \Theta(n^2)$
4. $n^2 = \omega(n)$
5. $n^2 = \Omega(n^2)$

### Exercise 3: Matching Functions

Match each function $f(n)$ with the appropriate notation (Big O, Small o, Big Theta, Small omega, Big Omega) describing its asymptotic behavior:

1. $f(n) = n^2$
2. $f(n) = \log n$
3. $f(n) = 3n + 5$
4. $f(n) = n^{0.5}$
5. $f(n) = 2^n$

