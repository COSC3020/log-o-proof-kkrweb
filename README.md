# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$


//


Name: Kane Kriz

Date Started: 13 Feb 2025

Last Edited: 9 April 2025


//


Response, Proof:


Definition of big-O - $T(n) \in O(f(n)) \iff \exists c > 0, \exists n_0 \in \mathbb{N}, \forall n \geq n_0 : T(n) \leq c * f(n)$.




(Start of actual proof below)



Theorem: $O(\log_2 n) = O(\log_5 n)$.

Proof:

First, we need to prove $O(\log_2 n) \subseteq O(\log_5 n)$. 

Assume $T(n) \in O(\log_2 n)$. 

By definition, there exists constant value c such that $c > 0$ and $n_0 \in \mathbb{N}$ such that for all $n \geq n_0$, $T(n) \leq c \log_2 n$.

Using change of base of logs, $\log_2 n = \frac{\log_5 n}{\log_5 2}$, this can be rewritten as:

$T(n) \leq c * \frac{\log_5 n}{\log_5 2}$. 

//

This proves $T(n) \in O(\log_5 n)$.

Next, we need to demonstrate $O(\log_5 n) \subseteq O(\log_2 n)$. 

Assume $T(n) \in O(\log_5 n)$. 

Then there exists $c > 0$ and $n_0 \in \mathbb{N}$ with $T(n) \leq c \log_5 n$ for all $n \geq n_0$.

Applying the identity $\log_5 n = \frac{\log_2 n}{\log_2 5}$, we obtain $T(n) \leq c * \frac{\log_2 n}{\log_2 5}$. 

//

Since it has been shown that both $O(\log_2 n) \subseteq O(\log_5 n)$, and $O(\log_5 n) \subseteq O(\log_2 n)$, it is proven that $O(\log_2 n) = O(\log_5 n)$.


Q.E.D.


//


Plagiarism Acknowledgement: I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.


Citations:

Provided: https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions

