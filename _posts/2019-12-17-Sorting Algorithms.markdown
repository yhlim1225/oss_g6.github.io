---
layout: post
title:  "Sortings!!"
date:   2019-12-18 12:03:36 +0530
categories: Sorting
---
A sorting algorithm is an algorithm made up of a series of instructions that takes an array as input, performs specified operations on the array, sometimes called a lhtml to markdownto introduce other key computer science topics like [Big-O notation](https://brilliant.org/wiki/big-o-notation), [divide-and-conquer](https://brilliant.org/wiki/divide-and-conquer) methods, and data structures such as [binary trees](https://brilliant.org/wiki/binary-search-trees), and [heaps](https://brilliant.org/wiki/binary-heap). There are many factors to consider when choosing a sorting algorithm to use.

### Sorting Algorithms

In other words, a sorted array is an array that is in a particular order. For example, \[a,b,c,d\] is sorted alphabetically, \[1,2,3,4,5\] is a list of integers sorted in increasing order, and \[5,4,3,2,1\] is a list of integers sorted in decreasing order.

A sorting algorithm takes an array as input and outputs a permutation of that array that is sorted.

There are two broad types of sorting algorithms: **integer sorts** and **comparison sorts**.

**Comparison Sorts**

Comparison sorts compare elements at each step of the algorithm to determine if one element should be to the left or right of another element.

Comparison sorts are usually more straightforward to implement than integer sorts, but comparison sorts are limited by a lower bound of O(*n*log*n*), meaning that, on average, comparison sorts cannot be faster than O(*n*log*n*). A lower bound for an algorithm is the worst-case running time of the best possible algorithm for a given problem. The "on average" part here is important: there are many algorithms that run in very fast time if the inputted list is already sorted, or has some very particular (and overall unlikely) property. There is only one permutation of a list that is sorted, but *n*! possible lists, so the chances that the input is already sorted is very unlikely, and on average, the list will not be very sorted.


Proof

The running time of comparison-based sorting algorithms is bounded by Ω(*n*log*n*).

A comparison sort can be modeled as a large binary tree called a decision tree where each node represents a single comparison. 
Because the sorted list is some permutation of the input list, for an input list of length nn, there are n!n! possible permutations of that list. 
This is a decision tree because each of the n! is represented by a leaf, and the path the algorithm must take to get to each leaf is the series of comparisons and outcomes that yield that particular ordering.

At each level of the tree, a comparison is made. 
Comparisons happen, and we keep traveling down the tree; until the algorithm reaches the leaves of the tree, there will be a leaf for each permutation, so there are n!n! leaves.

Each comparison halves the number of future comparisons the algorithm must do (since if the algorithm selects the right edge out of a node at a given step, it will not search the nodes and paths connected to the left edge). 
Therefore, the algorithm performs O(log *n*!) comparisons. Any binary tree, with height hh, has a number of leaves that is less than or equal to 2^h.

From this,
> 2^*h* ≥ *n*!

Taking the logarithm results in
> *h* ≥ log( *n*! ).

From Stirling's approximation,
> *n*! > ( *n* / *e* )^*n*.

Therefore,
> *h* ≥ log( *n* / *e* )^*n* 
>
>    = *n* log( *n* / *e* )^*n*
>
>    = *n* log *n* − *n* log *e*
>
>    = Ω(*n* log *n*).

**Integer Sorts**

Integer sorts are sometimes called counting sorts (though there is a specific integer sort algorithm called counting sort). Integer sorts do not make comparisons, so they are not bounded by Ω(*n*log*n*). Integer sorts determine for each element​ *x* how many elements are less than *x*. If there are 14 elements that are less than *x*, then *x* will be placed in the 15th slot. This information is used to place each element into the correct slot immediately—no need to rearrange lists.

Sorting Algorithms. Brilliant.org. Retrieved 15:04, December 19, 2019, from [https://brilliant.org/wiki/sorting-algorithms/](https://brilliant.org/wiki/sorting-algorithms/)