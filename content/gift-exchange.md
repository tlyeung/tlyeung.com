+++
title = 'The best way to exchange gifts'
date = 2024-02-15T23:46:57+08:00
tags = ['🧮Math']
+++

It is common to exchange gifts in a Christmas party. Normally people would draw lots. But have anyone thought of a better method?

For _*n*_ participants who would like to exchange gifts in a party, we know there are _*n!*_ permutations of random orders of gifts. For some permutations, however, some participants get their own gifts instead of others'. In those cases, they are **failed cases**.

Assume the probability of getting our own gifts as _1/n_. The probability of none of participants getting their own gifts is _(1 - 1/n)^n_. For _n_ tends to infinity, the probability of that is _1/e_ , or on contrary, the probability of **_failed cases_** is _1 - 1/e_.


To reduce effort, and not letting anyone knows the result first to ensure total randomness, an algorithm is needed for exchanging gifts. 

The algorithm works like this: first all _n_ participants with their own gifts get a random seat in a circle (it has _(n-1)!_ combinations because of the circular arrangement). Then a random number from uniform distributed numbers from _1_ to _n-1_ is picked and participants can pass their gifts clockwise according the number drawn. As a result, only one draw lot for random seats and one pick for a random number is needed.

This method can prevent participants getting their own gifts at the end of the party, and to speed up the gift exchange session. As long as there are participants in the party.
