# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
  1. Real world conditions/ algorithm implementation: Asymptotic analysis focuses on the growth rate of an algorithm and its performance as the input size increases. However it normally does not account for pratical implementation details that can arise in real world conditions so it does not factor in potential inefficiencies that may arise in these scenarios. For example, an algorithm can be influenced by factors like cache behavior or actual input distribution which are often not captured in asymptotic analysis. Which could cause a theoretically worse asymptotic complexity to outperform another with a much better complexity due to optimizations or favorable conditions.

  2. Hidden Constants/ Lower-Order terms: Typically Asymptotic analysis ignores these which can play an important part in actual peformance causing it to be slower.

  3.Hardware factors: Factors like CPU cache behavior, memory access patterns, and paralleism can affect performance of an algorithm, but Asymptotic analysis does not account for them. Causing problems within predictions and performance.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  My first thought is that the program takes 5 seconds to find an element within 1,000 elements, so if it is now 10,000 elements it should take 50 seconds. However, that seemed impractical so I looked at it again with logarithmic complexity and determined it to be around 6 - 7 seconds. So the runtime should be around 7 seconds for a tree with 10,000 assuming the tree is balanced and no other limiing factors. The typical complexity of a balanced binary search tree is O(log n). Assuming the tree is balanced, the number of comparisons required to find an element will be determined by how many levels the tree has (log n). Hence a logarithmic approach is more appiorate for prediciting the performance more accurately.


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  
  1. External interferance or contention: The difference in time could result from resource contention due to other tasks running on the system. If other processes (update, background applications) are consuming resources (CPU, memory, ...) it can lead to a significant slow down to the algorithm that is running. This type of interference is not often captured by asymptotic analysis, but can have real world impact on the algorithm.


  2. Inefficient implementation/ algorithm: The binary tree itself or the code which finds the elements within the tree could have inefficiences not accounted for. Such as poor memory access patters, inefficient balancing algorithms, and some others which can impact performance making the search take longer. A poor implementation may have a slight impact on performance with smaller inputs, but the effect becomes much more noticable as the input size increases. Larger inputs will require more iterations, operations, and memory usage which can amplify the inefficiencies and slow down execution more noticeablly compared to smaller inputs.

  3. System fators: Although rare, system specific issues like memory bottlenecks, limited CPU capacity, or other hardware restraints can significantly impact the search time. Asymptotic analysis assumes ideal conditions that could not be true on the actual system. These system limitations may be more prenounced with larger inputs, but they can also affect smaller inputs as well. Especially if the system is under heavy load or lacking sufficient resources (such as processing power/memory). As input size increases, the algorithm could require more memory or processing power, making thesee system related inefficiencies more noticeable.

Add your answers to this markdown file.


Sources:
Used chatGpt to generate some ideas for the last section, specifically answer 1 due to running around the same answer and was struggling to find another approach.
Also the use of notes and lectures from the class.
