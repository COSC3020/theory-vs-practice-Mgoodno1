# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
  1. The assumption of inputs normally being large: Asymptotic analysis typically assumes that input is large often approaching infinity. However, real world problems can typically involve finite input sizes, and some times those inputs are not large enough for asymptotic analysis to be fully realized. For instance, an algorithm that has a time complexity of O(n^2) may have similar performance when compared to O(n log n) when the input is small. Large inputs refering to values in the thousands or millions while small inputs refering to relatively small like 100 elements.

  2. Hidden Constants/ Lower-Order terms: Typically Asymptotic analysis ignores these which can play an important part in actual peformance causing it to be slower.

  3. Hardware factors: Factors like CPU cache behavior, memory access patterns, and paralleism can affect performance of an algorithm, but Asymptotic analysis does not account for them. Causing problems within predictions and performance.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  My first thought is that the program takes 5 seconds to find an element within 1,000 elements, so if it is now 10,000 elements it should take 50 seconds. However, that seemed impractical so I looked at it again with logarithmic and determined it to be around 6 - 7 seconds. So the runtime should be around 7 seconds for a tree with 10,000 assuming the tree is balanced and no other limiing factors. The typical complexity of a balanced binary search tree is O(log n).


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.
  
  1. Poor tree structure/ Data distribution: The distribution of data within a tree could cause it to perform worse than expected at times. So if the data inserted is not uniformly distributed or if the tree is built in a non optimal way, causing a skewed structure to take form. Which can lead to one side of the tree being significantly deeper than the other, but the tree still appears to be balanced which could result in longer search times. While data clustering could lead to longer search paths because of an uneven depth causing longer search paths. So in theory it could lead to such a big search time difference, but it would have to be an extreame imbalance. It is instead more likely that this appears with other problems (such as other answers) which makes it even worse times.

  2. Inefficient implementation/ algorithm: The binary tree itself or the code which finds the elements within the tree can inefficiences not accounted for. Such as poor memory access patters, inefficient balancing algorithms, and some others which can impact performance making the search take longer. A poor implementation may show slightly slower performance for small inputs, but will become much more noticeable as the input grows. This is because larger inputs will have higher cost of inefficiencies with the size of the data. Meaning more iterations, computions, and memory being used which will amplify the inefficiencies much more than a smaller input could sinc they will do less.

  3. System fators: Although it can be rare it does happen like memory bottlenecks, limited CPU power, and more which could significantly impact the search time. Asymptotic analysis assumes ideal conditions that could not be true on the actual system. These are more likely to appear at a larger scale, but it can affect smaller inputs as well, especially since the system will have less resources than normal. With larger inputs more resources will have to be used accordingly which will cause more issues/inefficiencies to occur and become more obvious.

Add your answers to this markdown file.
