# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
  1. The assumption of inputs normally being large: Asymptotic analysis typically assumes that input is large like growing to infinity. However, inputs can varie which can behave differently making it not align with predictions causing performance issues.
  2. Hidden Constants/ Lower-Order terms: Typically Asymptotic analysis ignores these which can play an important part in actual peformance causing it to be slower.
  3. Hardware factors: Factors like CPU cache behavior, memory access patterns, and paralleism can affect performance of an algorithm, but Asymptotic analysis does not account for them. Causing problems within predictions and performance.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  My first thought is that the program takes 5 seconds to find an element within 1,000 elements, so if it is now 10,000 elements it should take 50 seconds. However, that seemed impractical so I looked at it again with logarithmic and determined it to be around 6 - 7 seconds assuming the tree is balanced and there are no problems.


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  
  1. Unbalanced Tree: If the binary tree is unbalanced it would significantly change the time trying to find elements raising the search time.
  2. Inefficient implementation/ algorithm: The binary tree itself or the code which finds the elements within the tree can inefficiences not accounted for. Such as poor memory access patters, inefficient balancing algorithms, and some others which can impact performance making the search take longer.
  3. System fators: Although it can be rare it does happen like memory bottlenecks, limited CPU power, and more which could significantly impact the search time. Asymptotic analysis assumes ideal conditions that could not be true on the actual system.

Add your answers to this markdown file.
