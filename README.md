[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/8KYthzwp)
# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

expand to find pattern

$T(\frac{n}{13})+5$

$T(\frac{n}{169})+10$

$T(\frac{n}{13^i})+5i$

let $i = \log_{13}n$

=> $T(\frac{n}{n})+5(\log_{13}n)$ -> $T(1)+5(\log_{13}n)$

=> $T(n) = \theta(logn)$ because we can ignore the constant and the log base as proven in logO proof





2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

expand to find pattern

$13T(\frac{n}{13}) + 5$

$13(13T(\frac{n}{169})+5)+5$ -> $169T(\frac{n}{169}+65+5)$

=> $13^iT(\frac{n}{13^i})+5(13^(i-1))+5$



3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$
