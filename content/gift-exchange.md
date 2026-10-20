+++
title = "The best way to exchange gifts"
date = 2024-02-15T23:46:57+08:00

[taxonomies]
tags = ["math"]
+++

It is common to exchange gifts in a Christmas party. Normally people would draw lots. But have anyone thought of a better method?

For n participants who would like to exchange gifts in a party, we know there are n! permutations of random orders of gifts. For some permutations, however, some participants get their own gifts instead of others’. In those cases, they are failed cases.

Assume the probability of getting our own gifts as 1/n. The probability of none of participants getting their own gifts is (1 - 1/n)^n. For n tends to infinity, the probability of that is 1/e , or on contrary, the probability of failed cases is 1 - 1/e.

To reduce effort, and not letting anyone knows the result first to ensure total randomness, an algorithm is needed for exchanging gifts.

The algorithm works like this: first all n participants with their own gifts get a random seat in a circle (it has (n-1)! combinations because of the circular arrangement). Then a random number from uniform distributed numbers from 1 to n-1 is picked and participants can pass their gifts clockwise according the number drawn. As a result, only one draw lot for random seats and one pick for a random number is needed.

This method can prevent participants getting their own gifts at the end of the party, and to speed up the gift exchange session. As long as there are participants in the party.
