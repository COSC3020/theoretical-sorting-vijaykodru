[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/9YUeXH71)
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.


With the blackbox implementation of the sorting algorithm, I would start by testing it first different set of arrays, such as randomly sorted array, reverse sorted array, already sorted array of same size and graph them with the attributes of time vs number of elements. I would try the same with multiple scenerios where the number of elements increases and decreases based on the input. And if the claims are really true, the graph should show a linear growth meaning the time it takes to sort the array that is randmoly sorted, reverse sorted and already sorted array of same size should take about the same time and this should stay the same as the number of elements increase as well. However, this cannot hold because in class, we learned that comparison-based sorting algorithms have a lower bound of $Ω(nlogn)$. This lower bound is based on the fact that, in the worst case, every comparison-based sorting algorithm must examine $log(n!)= Ω(nlogn)$ bits of information to correctly order all possible permutations of n elements.