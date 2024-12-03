# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
  1. Real world conditions/ algorithm implementation: Asymptotic analysis assumes as ideal scenario where the algorithm is implemented effciently and the input size is large enough for the asymptotic behavior to dominate. However, various real world factors can lead to deviations from the predicted performance. For example, an algorithm can perform differently on inputs due to issues like input distribution, caching behaviors which are not normally captured. In some cases, an algorithm with a worse asymptotic complexity may outperform one with a better complexity for certain input sizes due to optimizations in the implementation or favorable data patterns.

  2. Hidden Constants/ Lower-Order terms: Typically Asymptotic analysis ignores these which can play an important part in actual peformance causing it to be slower.

  3. Hardware factors: Factors like CPU cache behavior, memory access patterns, and paralleism can affect performance of an algorithm, but Asymptotic analysis does not account for them. Causing problems within predictions and performance.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  My first thought is that the program takes 5 seconds to find an element within 1,000 elements, so if it is now 10,000 elements it should take 50 seconds. However, that seemed impractical so I looked at it again with logarithmic complexity and determined it to be around 6 - 7 seconds. So the runtime should be around 7 seconds for a tree with 10,000 assuming the tree is balanced and no other limiing factors. The typical complexity of a balanced binary search tree is O(log n).


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  
  1. Hidden Constants/ Lower-Order terms: Typically asymptotic complexity focuses on the growth rate of an algorithm as the input size increase. However, it often overlooks constant factors and lower-order terms which can significantly impact actual runtime. For example, an algorithm with a time complexity of O(n^2) might still perform poorly for small inputs if there is a large hidden constant factor. If the constant factor is large, the algorithm could take much longer to process the 10,000 elements even though asymptotic complexity suggests a faster time.


  2. Inefficient implementation/ algorithm: The binary tree itself or the code which finds the elements within the tree could have inefficiences not accounted for. Such as poor memory access patters, inefficient balancing algorithms, and some others which can impact performance making the search take longer. A poor implementation may have a slight impact on performance with smaller inputs, but the effect becomes much more noticable as the input size increases. Larger inputs will require more iterations, operations, and memory usage which can amplify the inefficiencies and slow down execution more noticeablly compared to smaller inputs.

  3. System fators: Although rare, system specific issues like memory bottlenecks, limited CPU capacity, or other hardware restraints can significantly impact the search time. Asymptotic analysis assumes ideal conditions that could not be true on the actual system. These system limitations may be more prenounced with larger inputs, but they can also affect smaller inputs as well. Especially if the system is under heavy load or lacking sufficient resources (such as processing power/memory). As input size increases, the algorithm could require more memory or processing power, making thesee system related inefficiencies more noticeable.

Add your answers to this markdown file.
