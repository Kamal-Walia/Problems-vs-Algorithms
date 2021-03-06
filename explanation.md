# Project Explanation
Explanation of the different project submodules

## Problem 1
First, if the number is 0 or 1 simply return it and avoid further calculations. Otherwise, create a list of numbers from 1 to the number passed as the argument. Then, take the halfway point or middle of the list.

Looking at this middle number, square it and if the answer is larger than the number keep halving your index to find a smaller result. After exiting this while loop, do the reverse and slowly work your way up, incrementing the index by 1 until the square is less than the number.

If the square of the found number at nums[index] equals the number, return the result. Otherwise, return the very next number in your list, as the square root is thereby some fraction.

### Time and Space complexity:
The time complexity is O(log(n)) since you are halving the array as you search for the number, and incrementing up is far less than O(n) since you are looking at a smaller segment of the main list of numbers. The space complexity is O(1) as you are merely making one list and a variable index used to search for the answer.

## Problem 2
The principle employed in this algorithms is based directly in the _binary search_ algorithms, differently, to this 
implementations, in its structure, it has been decided to be employed a __more divide approach__, rather than
computationally expensive on previous levels to _spare_ some division; e.g. when the lists are of size 2, both values
could have been checked (though this would have increased our __time complexity__). 

### Time and Space complexity
The time complexity being an algorithm based on binary search is __O(log(n))__.  The number of iterations we perform,
i.e. recursive depth, follows the rule of _recursive_depth^2 = n_. Thus if we isolate the number of iterations in
relation to the __input space__ (n), we obtain __log(n) = recursive_depth__. As for the space complexity, it is 
__independent of the input__, requiring solely pointers to different array locations; __O(1)__.

## Problem 3
This problem, as stated to be solved in _time complexity_ of __O(n*log(n))__, has given the clue to be tackled by a 
variation of the __merge sort__ algorithm. Indeed, it is a _merge sort_ algorithm, except for the particular treatment 
if gives to the comparison of results coming from the previous recursion, if we are on the _first level_ of the
recursion. In this case, it does the _comparison_, as usual, but then starts saving the results on 
__alternative lists__, which are then returned as the results. 

The usage of this _alternative list saving_ is due to the fact that having the list perfectly sorted, if we start from
the index[0] and give alternatively a value to each list, occupying this value an increasing digit position, we 
__always__ obtain a combination that satisfies the condition of having a __maximum sum of two numbers__ and __maximum a
digit of difference between them__.  

### Time and Space complexity 
As the base of the algorithm is the __merge sort__, having a time complexity of __O(n*log(n))__, and there have been no
substantial modifications to the algorithm; just the addition of __O(1)__ operations, the time complexity remains 
_equal_. As for the space complexity, if we hold the assumption that python gets automatically rid of each previous 
step auxiliary created arrays, then the space complexity is of __O(n)__ (we have always arrays tat amount to the 
length of the input array).

## Problem 4
This problem is tackler as the construction of a output list, issue form a single transverse of the elements. By using,
several pointers, it is possible on a __single transverse__ to properly order the provided array.

### Time and Space complexity
In this case the _time complexity_ is precisely, __O(n)__. Analyzing the _space complexity_, due to the non usage of 
__auxiliary tables__ (only a few pointers), it is of order __O(1)__ (excluding the input space).

## Problem 5
This problem is focused on the development of the of a __trie__ a data structure derived from a _tree_, suited for a
 good ratio between _time and space_ complexity.

### Time and Space complexity
For the __trie__, time complexity of **searching and inserting** from a trie depends on the length of the word **a** 
that’s being searched for, inserted, and the number of total words, **n**, making the runtime of these operations
 __O(a*n__). Looking into the space complexity of a __trie__, the worst case, would be when we have a word (or words),
 with no common characters between them, hence having, a node for each letter. Resulting in a _space complexity_ of 
 __O(n)__.

## Problem 6
This problem focuses on __finding max and min values__ from an unsorted array, we are not required to nothing extra 
and here _lies the key_, not being required to sort anything, we can solve the problem with a single transversal and
 two placeholders, as reference for _min_ and _max_ values.

### Time and Space complexity
In this case, we perform a __single transverse__ of the whole input, being the time complexity of __O(n)__. In respect 
to the _space complexity_, we have just a pair of pointers, hence, it is independent from _input size_; __O(1)__.

## Problem 7 
It is similar to __problem 5__, except for the _edge cases_, like "root handler", and working with a __hierarchy of 
web pages__ instead of strings. This problem is focused on the development of the of a __trie__ a data structure 
derived from a _tree_, suited for a good ratio between _time and space_ complexity.

### Time and Space complexity
For the __trie__, time complexity of **searching and inserting** from a trie depends on the length of the path **n**
that’s being searched for, inserted, making the runtime of these operations __O(n)__. Looking into the space 
complexity of a __trie__, the worst case, would be when we have a path (or paths), with no common folders between them,
hence having, a node for each _path block_ (path between forward slashes). Resulting in a _space complexity_ of  
__O(n)__.
