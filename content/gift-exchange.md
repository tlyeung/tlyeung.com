+++
title = 'Gift Exchange'
date = 2024-02-15T23:46:57+08:00
draft = true
+++

It is common to exchange gifts in a Christmas party. Normally people would draw lots. But have anyone thought of a better method?

For $n$ participants who would like to exchange gifts in a party, we know there are $n!$ permutations of random orders of gifts. For some permutations, however, some participants get their own gifts instead of other's. In those cases, they are **_failed gift exchange cases_**. Failing to exchange gifts in a party breaks children's hearts.

For permutations of $n$ participants, we can work out that the combinations of _**failed gift exchange cases**_ is related to the number of participants, i.e.

#### [$a(n) = (n-1) * (a(n-1) + a(n-2))$](https://oeis.org/A002467)


|$n$|$a(n)$	|$n!$	|$\%$ of failed cases||
|---|---|---|---|-|
|1|1	|1	|1.0|too bad, no one wants to party with you|
|2|1	|2	|0.5|
|3|4	|6	|0.6666666666666666|
|4|15	|24	|0.625|
|5|76	|120	|0.6333333333333333|
|6|455	|720	|0.6319444444444444|
|7|3186	|5040	|0.6321428571428571|
|8|25487	|40320	|0.6321180555555556|
|9|229384	|362880	|0.632120811287478|
|10|2293839	|3628800	|0.6321205357142857|
|11|25232230	         |39916800	         |0.6321205607663941|
|12|302786759	         |479001600	         |0.6321205586787184|
|13|3936227868	       |6227020800  	     |0.6321205588393088|
|14|55107190151	       |87178291200	       |0.6321205588278381|
|15|826607852266	     |1307674368000	     |0.6321205588286029|
|16|13225725636255	   |20922789888000	   |0.632120558828555 |
|17|224837335816336	   |355687428096000	   |0.6321205588285578|
|18|4047072044694047	 |6402373705728000	 |0.6321205588285577|
|19|76894368849186894	 |121645100408832000 |0.6321205588285577|
|20|1537887376983737879|2432902008176640000|0.6321205588285577|


On the other hand, we also can simulate this by assuming the probability of getting our own gifts as $\frac 1 n$. The probability of none of participants getting their own gifts is $(1 - \frac 1 n)^n$. For $n$ tends to infinity, we can get the probability of that is $\frac 1 e$ , or on contrary, the probability of **_failed gift exchange cases_** is $1 - \frac 1 e$ , which is equivalent to $a(n) = (n-1) * (a(n-1) + a(n-2))$ when $n$ is large.

To reduce effort, and not letting anyone knows the result first to ensure total randomness, thus an algorithm is needed for exchanging gifts. 

The algorithm works like this: first all $n$ participants with their own gifts get a random seat in a circle (it has $(n-1)!$ combinations because of the circular arrangement). Then a random number from uniform distributed numbers from $1$ to $(n-1)$ is picked and participants can pass their gifts clockwise according the number drawn. As a result, only one draw lots for random seats and one pick for a random number is needed.

This method can prevent participants getting their own gifts at the end of the party, and to speed up the gift exchange session, and to make it funnier.
