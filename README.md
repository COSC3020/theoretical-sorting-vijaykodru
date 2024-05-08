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

To verify the claim of a sorting algorithm achieving $O(n)$ time complexity based on comparisons of two elements at a time, I would try the following with the blackbox implementation of the sorting algorithm:

Test Cases: I would generated various test cases encompassing different input sizes and characteristics. These test cases included:

-Randomly ordered arrays
-Reverse sorted arrays
-Already sorted arrays
-Arrays with nearly all elements identical
-Arrays with many duplicates
-Arrays with a few unique elements
-Arrays with different data types (numbers, strings, custom objects)

Measure Time: Utilizing the black-box implementation of the sorting algorithm, I would try sorting each test case multiple times to ensure consistency and measure the execution time for each sorting operation.

Analyze Results: I would plot the execution times against the input size for each type of test case. I would expect it to show a general trend of $O(n)$ time complexity, as claimed. Specifically, I would look for linear growth in execution time as the input size increased. Along with this I would look for any sudden changes in the execution times which tells me that there is a weakness in the code. As we've learned, these algorithms have a lower bound of $Ω(n\log n)$ because they need to examine $log(n!)= Ω(nlogn)$ bits of information in the worst-case scenario to sort all permutations of elements accurately. Consequently, any assertion that a comparison-based sorting algorithm achieves $O(n)$ time complexity would directly challenge this lower bound, unless the algorithm functions beyond the constraints of the conventional comparison-based model.

references:

theoretical-sorting-IshitaPatel18

theoretical-sorting-ross223

https://tildesites.bowdoin.edu/~ltoma/teaching/cs231/fall07/Lectures/sortLB.pdf