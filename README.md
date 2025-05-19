# Bayesian-Network-Notebooks
### **Maths behind Naive Bayes:**

As we know, 

$$
P(A \mid B) = \frac{P(A \bigcap B)}{P(B)}
$$

and, from Bayes Theorem :

$$
P(A \mid B) P(B) = P(B \mid A) P(A)
$$

Let $X = \{x_1 ...  x_n\}$ be the Dataset (Feature Vector) with $y$ as the output.

Then, 

$$
P(y \mid x_1, x_2 .. x_n) = \frac{P(x_1 \mid y)P(x_2 \mid y)...P(x_n \mid y) * P(y)}{P(x_1) P(x_2) . . . P(x_n)}
$$

$$
\implies P(y \mid x_1, x_2 .. x_n) = [\prod_{i = 1}^n p(x_i \mid y)] \cdot \frac{P(y)}{[\prod_{i = 1}^n p(x_i)]}
$$

$$
\implies P(y \mid x_1, x_2 .. x_n) = k \cdot p(y) \cdot \prod_{i = 1}^n p(x_i \mid y)
$$

Hence, 

$$
y = argmax_y [p(y) \cdot \prod_{i = 1}^n p(x_i \mid y)]
$$
