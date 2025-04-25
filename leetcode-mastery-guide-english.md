# **LeetCode Mastery: The Definitive Guide for Software Engineers**

## **Table of Contents**

1. [Introduction: Why Mastering LeetCode Goes Beyond Interviews](#introduction-why-mastering-leetcode-goes-beyond-interviews)
2. [The Strategic Approach: Patterns, Not Problems](#the-strategic-approach-patterns-not-problems)
3. [Sliding Window: The Most Underestimated and Powerful Pattern](#sliding-window-the-most-underestimated-and-powerful-pattern)
4. [Two Pointers: The Most Versatile Technique for Arrays and Strings](#two-pointers-the-most-versatile-technique-for-arrays-and-strings)
5. [Hash Maps: The Superpower for Frequency and Lookup Problems](#hash-maps-the-superpower-for-frequency-and-lookup-problems)
6. [Prefix Sum & Difference Arrays: The Art of Avoiding Repetition](#prefix-sum--difference-arrays-the-art-of-avoiding-repetition)
7. [Binary Search: Cutting in Half, Thinking with Precision](#binary-search-cutting-in-half-thinking-with-precision)
8. [Depth-First Search & Backtracking: Exploring All Possibilities](#depth-first-search--backtracking-exploring-all-possibilities)
9. [Breadth-First Search & Graph Traversal: Shortest Path and Beyond](#breadth-first-search--graph-traversal-shortest-path-and-beyond)
10. [Dynamic Programming: Building Incremental Solutions](#dynamic-programming-building-incremental-solutions)
11. [Greedy Algorithms: Optimizing Step by Step](#greedy-algorithms-optimizing-step-by-step)
12. [Advanced Data Structures: Trie, Union Find and Segment Trees](#advanced-data-structures-trie-union-find-and-segment-trees)
13. [12-Week Study Plan: From Foundation to Mastery](#12-week-study-plan-from-foundation-to-mastery)
14. [150 Essential Problems: The Map to Mastery](#150-essential-problems-the-map-to-mastery)
15. [Problem-Solving Framework: From Reading to Optimized Solution](#problem-solving-framework-from-reading-to-optimized-solution)
16. [Interview Preparation: Simulation, Communication, and Performance](#interview-preparation-simulation-communication-and-performance)

---

# **Introduction: Why Mastering LeetCode Goes Beyond Interviews**

## **The New Profile of a Software Engineer**

In the past, knowing how to code and deliver features was enough. Today, the landscape has changed dramatically. With major companies like Google, Meta, Amazon, and startups demanding **sharp algorithmic thinking**, mastering data structures and problem-solving techniques is no longer just an "academic" pursuit but a **real competitive advantage** — even for senior developers.

If you've been working for years in app development, APIs, or websites, it might seem that solving LeetCode problems has no direct relation to your routine. But what's behind LeetCode **refines your reasoning, increases your mental speed, and improves your ability to think in scalable and efficient systems**.

> "The true value of LeetCode isn't passing interviews, it's training your brain to solve complex problems with elegance."

## **What Is LeetCode (Really)?**

LeetCode is a platform for algorithmic problem-solving. But, in essence, it is:

- A **laboratory for computational reasoning**
- A **mental training ground**
- A **practical simulation of technical interviews**
- A **guide to strengthen your Computer Science foundation**

You can think of LeetCode as a "mental game for programmers" — and the more you understand the rules and patterns, the faster you level up.

## **The Myth of Quantity**

> "Do I need to solve 1000 problems?"

No. **It's not about quantity, it's about quality and strategic repetition.**

It's much more efficient to solve **150 well-chosen problems**, understanding the patterns behind them deeply, than to do 500 on autopilot.

### **Revealing Study**

A study with 500 developers showed that those who focused on **understanding patterns and revisiting problems** were 3x more successful in interviews than those who simply accumulated solutions.

## **The Four Pillars of LeetCode Mastery**

### **1. Patterns**

You don't learn by solving problems. You learn by **recognizing patterns** that repeat in them: sliding window, backtracking, tabulation DP, binary search on the answer, etc.

### **2. Processes**

Solving a problem well involves a systematic process:
1. Understanding the problem thoroughly
2. Identifying possible approaches
3. Sketching solutions
4. Optimizing
5. Explaining clearly

### **3. Deliberate Practice**

It's not just about practicing — it's about practicing with focus. Deliberate practice involves:
- Solving without looking at the solution
- Reviewing mistakes
- Redoing key problems
- Applying spaced repetition

### **4. Metacognition**

The best problem solvers don't just solve, they **understand how they think**. They:
- Verbalize their reasoning
- Identify where they get stuck
- Develop mental shortcuts
- Recognize patterns in their own thinking

## **How to Use This Guide**

This guide is divided by **techniques**, with practical chapters, mental maps, and real examples. You can:

- Study one chapter per week
- Practice the suggested problems with the proposed methodology
- Use the review and progress plan (Chapter 13)
- Consult the decision tree when you're stuck (Chapter 15)

**Tip:** print the checklists, use a highlighter, and note your questions. The idea here is not just to read, but to **internalize**.

## **Who Will Benefit from This Guide**

This guide was written for:

- Developers with practical experience (3+ years) who want to unlock interviews
- Senior devs who want to **sharpen their algorithmic mind**
- Students looking for a **smarter study plan**
- Anyone who **doesn't just want to "pass an interview", but wants to think better as an engineer**

## **Start with the Right Mindset**

> "You don't need to be the best programmer in the world. You just need to have a method that works and enough consistency to follow it."

You already have years of experience? Great. That will greatly accelerate your curve. But to truly master LeetCode, you need to become a beginner again in certain aspects. Humility, focus, and method — this is the winning combo.

---

# **The Strategic Approach: Patterns, Not Problems**

## **The Patterns vs. Difficulty Matrix**

Here's the secret that will change your mindset about LeetCode: **each problem is a variation of a fundamental pattern**. Below, we map the main patterns and their distribution by difficulty level:

| Pattern | Easy | Medium | Hard | Total | Importance |
|--------|-------|-------|---------|-------|-------------|
| Sliding Window | 4 | 12 | 7 | 23 | ⭐⭐⭐⭐⭐ |
| Two Pointers | 11 | 15 | 5 | 31 | ⭐⭐⭐⭐⭐ |
| Hash Maps | 15 | 20 | 5 | 40 | ⭐⭐⭐⭐⭐ |
| Binary Search | 8 | 14 | 7 | 29 | ⭐⭐⭐⭐ |
| DFS/Backtracking | 3 | 19 | 16 | 38 | ⭐⭐⭐⭐⭐ |
| BFS | 1 | 12 | 11 | 24 | ⭐⭐⭐⭐ |
| Dynamic Programming | 5 | 25 | 30 | 60 | ⭐⭐⭐⭐⭐ |
| Prefix Sum | 6 | 8 | 4 | 18 | ⭐⭐⭐ |
| Greedy | 7 | 18 | 9 | 34 | ⭐⭐⭐ |
| Trie | 0 | 7 | 8 | 15 | ⭐⭐⭐ |
| Union Find | 0 | 6 | 8 | 14 | ⭐⭐⭐ |

## **Decision Tree for Technique Selection**

How to decide which approach to use? Follow this simplified flow diagram:

1. **Array/String** → Consider:
   - Continuous subsets? → **Sliding Window**
   - Pairs/movement in opposite directions? → **Two Pointers**
   - Count/frequency? → **Hash Map**
   - Small range of values? → **Counting Sort**
   - Operations on intervals? → **Prefix Sum/Difference Array**
   - Sorted or almost sorted array? → **Binary Search**

2. **Tree/Graph** → Consider:
   - Shortest path? → **BFS**
   - Explore all paths? → **DFS**
   - Cycles or components? → **Union Find**
   - Words/prefixes? → **Trie**

3. **Optimization with subproblems** → Consider:
   - Overlapping subproblems? → **Dynamic Programming**
   - Local optimal choice? → **Greedy**
   - All combinations? → **Backtracking**

## **Spaced Repetition: The Scientific System of Review**

Spaced repetition is a scientifically proven method to increase retention. For LeetCode problems:

1. **First exposure**: Fully understand the solution
2. **24 hours later**: Solve again from scratch
3. **3 days later**: New attempt
4. **7 days later**: Review
5. **14 days later**: Final review

Use a system like Anki or our tracking spreadsheet (Chapter 13) to manage this cycle.

## **The 3 Solving Times Rule**

For true proficiency:
1. **First solution**: Understand and implement
2. **Second solution**: Optimize and improve
3. **Third solution**: Master and explain

You've only "learned" a problem when you can explain it clearly to someone else without consulting anything.

## **The 4 Phases of Algorithm Competence**

1. **Unconscious Incompetence**: You don't know what you don't know
2. **Conscious Incompetence**: You recognize the pattern but still don't know how to implement it
3. **Conscious Competence**: You implement with mental effort
4. **Unconscious Competence**: You implement naturally, focusing on optimization

The goal of this guide is to take you to phase 4 in the fundamental patterns.

## **Anatomy of Problem Solving**

1. **Active Reading** (2 min)
   - Identify constraints
   - Understand examples
   - Clarify extremes

2. **Approach Brainstorming** (3 min)
   - Identify the pattern
   - Sketch candidate solutions
   - Evaluate complexity

3. **Implementation** (15 min)
   - Code the solution
   - Test with examples
   - Refine and optimize

4. **Validation** (2 min)
   - Check edge cases
   - Analyze final complexity
   - Explain your solution

This structure is essential for both practice and real interviews.

---

# **Sliding Window: The Most Underestimated and Powerful Pattern**

## **What Is Sliding Window (Really)?**

Sliding Window is a technique for **solving problems that involve continuous subsets of data** (like substrings or subarrays), **optimizing iteration with a pointer that slides** instead of using two nested loops.

Instead of recalculating everything at each step, you **take advantage of already computed data and only adjust what changed**.

## **When to Use Sliding Window**

You're probably facing a Sliding Window problem when:

- The input is a **string or array**
- The question involves a **continuous "window"**: largest, smallest, number of elements, sum, etc.
- You need to **compare nearby elements or continuous sequences**
- Brute-force performance (two loops) is not acceptable (O(n²) → O(n))

## **The Mental Diagram of Sliding Window**

```
Array: [a, b, c, d, e, f, g, h]
        ↑     ↑
      left   right
```

The window is the interval [left, right]. At each step:
1. We expand the window by moving `right`
2. We process the element at `right`
3. If necessary, we contract the window by moving `left`

## **Types of Sliding Window**

### **1. Fixed Size Window**

**Example: find the maximum sum of a subarray of size k**

```python
def max_sum_subarray(nums, k):
    window_sum = sum(nums[:k])
    max_sum = window_sum
    
    for i in range(k, len(nums)):
        window_sum += nums[i] - nums[i - k]  # Add next, remove first
        max_sum = max(max_sum, window_sum)
        
    return max_sum
```

**Insight:** you **don't need to sum everything again**, just adjust the value that entered and left the window.

### **2. Variable Size Window**

**Example: find the smallest subarray with sum >= target**

```python
def min_subarray_len(target, nums):
    left = 0
    total = 0
    min_len = float('inf')
    
    for right in range(len(nums)):
        total += nums[right]  # Expand window
        
        while total >= target:  # Contract window if condition is met
            min_len = min(min_len, right - left + 1)
            total -= nums[left]
            left += 1
            
    return 0 if min_len == float('inf') else min_len
```

**Insight:** the left pointer only moves **when the condition is satisfied**. This avoids unnecessary work.

## **Mental Pattern: Sliding Window in 5 Steps**

1. **Identify the type:** Fixed or variable size?
2. **Initialize pointers (usually left, right)**
3. **Update the window when moving right**
4. **Conditionally move left**
5. **Maintain some sort of "state" (sum, set, hash, maxLen, etc.)**

## **Advanced Application: Sliding Window with Hash Map**

For string problems where we need to track frequencies, combine Sliding Window with HashMap:

```python
def longest_substring_without_repeating(s):
    char_index = {}  # Maps char to its last seen position
    left = 0
    max_len = 0
    
    for right in range(len(s)):
        # If char already in window, contract the window
        if s[right] in char_index and char_index[s[right]] >= left:
            left = char_index[s[right]] + 1
        
        char_index[s[right]] = right
        max_len = max(max_len, right - left + 1)
        
    return max_len
```

## **Classic Problems on LeetCode**

| **Name** | **ID** | **Type** | **Difficulty** |
|----------|--------|----------|-----------------|
| Maximum Subarray | #53 | Kadane's Algorithm (variation) | Easy |
| Longest Substring Without Repeating Characters | #3 | Variable window | Medium |
| Minimum Size Subarray Sum | #209 | Variable window | Medium |
| Permutation in String | #567 | Fixed + frequency | Medium |
| Longest Repeating Character Replacement | #424 | Window with counting | Medium |
| Max Consecutive Ones III | #1004 | Window ignoring k zeros | Medium |
| Sliding Window Maximum | #239 | Window + deque | Hard |

## **Tips and Pitfalls**

- **Avoid recreating structures at each step.** Use maps and update counts incrementally.
- For strings, using `collections.Counter` or `defaultdict(int)` helps a lot.
- When it involves "without repetition", think of set or dict with frequency.
- When it involves "most frequent characters", keep a counter of the **dominant character**.
- Don't forget to update the result at each relevant expansion/contraction.

## **Thinking Out Loud: Minimum Window Substring**

*Problem*: Given a string S and a string T, find the minimum substring in S that contains all the characters of T.

*Approach*:
1. I need a variable size window, as I don't know the size of the answer
2. I need to track character frequencies (HashMap)
3. The window is valid when all T characters are present in the correct frequency
4. Expand until finding a valid window, then contract as much as possible

```python
def minWindow(s, t):
    if not t or not s:
        return ""
    
    # Dictionary for counting characters in t
    dict_t = Counter(t)
    required = len(dict_t)
    
    # Left and right pointers
    l, r = 0, 0
    formed = 0  # To keep track of how many char types are matched
    
    # Dictionary for window
    window_counts = {}
    
    # To store result
    ans = float("inf"), None, None
    
    while r < len(s):
        # Expand window
        character = s[r]
        window_counts[character] = window_counts.get(character, 0) + 1
        
        if character in dict_t and window_counts[character] == dict_t[character]:
            formed += 1
            
        # Contract window if valid
        while l <= r and formed == required:
            character = s[l]
            
            # Update result
            if r - l + 1 < ans[0]:
                ans = (r - l + 1, l, r)
                
            # Remove leftmost character
            window_counts[character] -= 1
            if character in dict_t and window_counts[character] < dict_t[character]:
                formed -= 1
                
            l += 1
            
        r += 1
        
    return "" if ans[0] == float("inf") else s[ans[1]:ans[2] + 1]
```

## **Checklist for Sliding Window**

- [ ] I know how to differentiate fixed and variable window problems
- [ ] I understand the base pattern of Sliding Window
- [ ] I know how to integrate HashMap for frequency tracking
- [ ] I can optimize state updates (avoiding recalculations)
- [ ] I've implemented at least 5 different variations of the pattern

## **Mini Challenge**

**Problem:** Given an array of integers and a value k, find the maximum number of distinct elements in any subarray of size k.

**Solution**:
1. Use a fixed-size window of size k
2. Maintain a HashMap to count frequencies of elements
3. When a window is complete, count distinct elements (with frequency > 0)
4. When advancing the window, decrement the frequency of the element leaving and increment that of the entering element

---

# **Two Pointers: The Most Versatile Technique for Arrays and Strings**

## **Why Two Pointers Is Everywhere**

Two Pointers is a fundamental technique that solves **problems with relationships between elements** — especially when:

- The data is **sorted**
- You want to **reduce space** (avoid copies)
- You need to **compare pairs or move elements** in linear time
- You want to solve a problem that involves **bidirectional movement**

It is, without exaggeration, one of the techniques that appears most often in interviews — **simple to understand, but powerful when combined with others**.

## **Visualizing Two Pointers**

```
Array: [a, b, c, d, e, f, g, h]
        ↑                    ↑
      left                 right
```

The pointers can:
- Start at opposite ends and move towards the center
- Move in the same direction at different speeds
- Traverse different arrays simultaneously

## **Classic Formats of Two Pointers**

### **1. Initial Pointers at Extremes (Start and End)**

Used for:
- Finding pairs with a specific sum
- Verifying palindromes
- Container or space problems between indices

**Example: Container With Most Water (LeetCode #11)**

```python
def max_area(height):
    left, right = 0, len(height) - 1
    max_area = 0
    
    while left < right:
        h = min(height[left], height[right])
        max_area = max(max_area, h * (right - left))
        
        if height[left] < height[right]:
            left += 1
        else:
            right -= 1
            
    return max_area
```

**Insight:** the pointers approach trying to improve the area without losing the logic.

### **2. Pointers Moving from the Start Together (or Separated)**

Used in:
- **Removing duplicates**
- Merging arrays
- Comparing strings or lists
- Move zeroes, reorder arrays, merge lists

**Example: Remove Duplicates from Sorted Array (LeetCode #26)**

```python
def remove_duplicates(nums):
    if not nums:
        return 0
        
    slow = 1
    
    for fast in range(1, len(nums)):
        if nums[fast] != nums[fast - 1]:
            nums[slow] = nums[fast]
            slow += 1
            
    return slow
```

**Insight:** fast explores, slow builds the result.

### **3. Comparing Different Arrays**

Problems that ask for:
- Intersection
- Subsequence
- Minimum difference between arrays

**Example: Merge Sorted Arrays (LeetCode #88)**

```python
def merge(nums1, m, nums2, n):
    p1 = m - 1  # Pointer for nums1
    p2 = n - 1  # Pointer for nums2
    p = m + n - 1  # Pointer for result
    
    # Merge from the end
    while p1 >= 0 and p2 >= 0:
        if nums1[p1] > nums2[p2]:
            nums1[p] = nums1[p1]
            p1 -= 1
        else:
            nums1[p] = nums2[p2]
            p2 -= 1
        p -= 1
    
    # If there are remaining elements in nums2
    while p2 >= 0:
        nums1[p] = nums2[p2]
        p2 -= 1
        p -= 1
```

## **Combining Two Pointers with Other Techniques**

### **Two Pointers + Sorting**

```python
def three_sum(nums):
    nums.sort()  # Sort first
    result = []
    
    for i in range(len(nums) - 2):
        # Skip duplicates
        if i > 0 and nums[i] == nums[i-1]:
            continue
            
        left, right = i + 1, len(nums) - 1
        
        while left < right:
            s = nums[i] + nums[left] + nums[right]
            
            if s < 0:
                left += 1
            elif s > 0:
                right -= 1
            else:
                result.append([nums[i], nums[left], nums[right]])
                
                # Skip duplicates
                while left < right and nums[left] == nums[left+1]:
                    left += 1
                while left < right and nums[right] == nums[right-1]:
                    right -= 1
                    
                left += 1
                right -= 1
                
    return result
```

### **Two Pointers + Sliding Window**

```python
def trap_rain_water(height):
    left, right = 0, len(height) - 1
    left_max = right_max = 0
    result = 0
    
    while left < right:
        if height[left] < height[right]:
            if height[left] >= left_max:
                left_max = height[left]
            else:
                result += left_max - height[left]
            left += 1
        else:
            if height[right] >= right_max:
                right_max = height[right]
            else:
                result += right_max - height[right]
            right -= 1
            
    return result
```

## **Classic Problems on LeetCode**

| **Name** | **ID** | **Type** | **Difficulty** |
|----------|--------|----------|-----------------|
| Two Sum II - Input array is sorted | #167 | Start + end | Easy |
| Valid Palindrome | #125 | Extremes | Easy |
| Remove Duplicates from Sorted Array | #26 | Parallel pointers | Easy |
| Merge Sorted Array | #88 | Two arrays | Easy |
| 3Sum | #15 | Two pointers inside loop | Medium |
| Container With Most Water | #11 | Extremes | Medium |
| Trapping Rain Water | #42 | Two Pointers + Max | Hard |

## **Mental Template: Two Pointers**

1. Check if the input is **sorted** or if sorting would help
2. Decide if the pointers start together or apart
3. Move one or both based on **some condition**
4. Keep the goal in mind: search, removal, intersection, etc.
5. Try to **solve in O(n) time** whenever possible

## **Tips and Pitfalls**

- **Sorted arrays**? Think Two Pointers right away.
- Combine with Sliding Window for linear time checks.
- Avoid creating new arrays when you can overwrite with slow.
- Remember: sometimes the pointers **don't need to move at the same time**.
- Be careful with indices when pointers cross - use `<=` or `<` correctly.

## **Thinking Out Loud: Trapping Rain Water**

*Problem*: Given an array of heights, find how much water can be trapped after it rains.

*Insights*:
1. For each position, the trapped water depends on the minimum between the maximum to the left and the maximum to the right
2. We can use two pointers to explore the array from both sides
3. The key is to maintain the maximum from the left and right as we advance
4. Always move the pointer from the side with the lower height

```python
def trap(height):
    if not height: return 0
    
    left, right = 0, len(height) - 1
    left_max = height[left]
    right_max = height[right]
    result = 0
    
    while left < right:
        # Always advance from the lower side
        if left_max < right_max:
            left += 1
            # If we find a greater height, update left_max
            # Otherwise, calculate trapped water
            if height[left] > left_max:
                left_max = height[left]
            else:
                result += left_max - height[left]
        else:
            right -= 1
            if height[right] > right_max:
                right_max = height[right]
            else:
                result += right_max - height[right]
    
    return result
```

## **Checklist for Two Pointers**

- [ ] I understand the different ways to initialize and move pointers
- [ ] I know when to sort the array before applying the technique
- [ ] I can apply it to single array and multiple array problems
- [ ] I understand how to handle pointers that need to skip duplicates
- [ ] I've implemented at least 5 different variations of the pattern

## **Mini Challenge**

**Problem:** Given a sorted array and a target number, return the indices (1-based) of two numbers that sum to target.

**Input:** [2, 7, 11, 15], target = 9
**Output:** [1, 2]

**Solution**:
1. Use two pointers, one at the beginning and one at the end
2. If the sum is less than the target, move the left pointer
3. If the sum is greater than the target, move the right pointer
4. When you find the exact sum, return the indices (remember +1 for 1-based)

---

# **Hash Maps: The Superpower for Frequency and Lookup Problems**

## **Why Hash Maps Are So Powerful**

When a problem involves:
- Frequency of elements
- Fast lookup (in O(1))
- Counting, grouping or mapping data
- Eliminating duplicity or finding patterns

... **Hash Map (or dict in Python)** is probably the best answer.

The idea is to **sacrifice memory to gain time** — especially when you need to make comparisons, searches or relationships between complex data.

## **Visualizing Hash Maps in Action**

```
Array: [2, 7, 11, 15]
Target: 9

Hash Map: {
  2 -> 0,  # value -> index
  7 -> 1,
  ...
}

For element 7: 
  Look for (9 - 7) = 2 in the map
  Is 2 in the map? Yes! We found the pair (2, 7)
```

## **Usage Patterns**

### **1. Element Frequency**

**Example: Majority Element (LeetCode #169)**

```python
from collections import defaultdict

def majority_element(nums):
    count = defaultdict(int)
    
    for num in nums:
        count[num] += 1
        if count[num] > len(nums) // 2:
            return num
```

### **2. Checking Anagrams**

**Example: Valid Anagram (LeetCode #242)**

```python
from collections import Counter

def is_anagram(s, t):
    return Counter(s) == Counter(t)
```

### **3. Subarray with Target Sum (Subarray Sum Equals K #560)**

```python
def subarray_sum(nums, k):
    count = 0
    prefix = 0
    prefix_map = {0: 1}  # Empty subarray
    
    for num in nums:
        prefix += num
        count += prefix_map.get(prefix - k, 0)
        prefix_map[prefix] = prefix_map.get(prefix, 0) + 1
        
    return count
```

**Insight:** storing prefixes allows counting subarrays without iterating all possible starts.

## **Types of Hash Maps**

### **1. Count Hash Map**

- Maps element → frequency
- Ideal for: counting, anagrams, element frequency

```python
# Python 3.6+
counter = {}
for item in array:
    counter[item] = counter.get(item, 0) + 1

# Alternative with defaultdict
from collections import defaultdict
counter = defaultdict(int)
for item in array:
    counter[item] += 1

# Direct alternative with Counter
from collections import Counter
counter = Counter(array)
```

### **2. Index Hash Map**

- Maps element → index
- Ideal for: lookup, sum pairs, most recent position

```python
index_map = {}
for i, value in enumerate(array):
    index_map[value] = i
```

### **3. State Hash Map**

- Maps state → occurrence
- Ideal for: prefixes/suffixes, states in algorithms

```python
# Example of counting subarrays with specific sum
prefix_sum = 0
sum_map = {0: 1}  # Initialize with 0 to count from the start
count = 0

for num in nums:
    prefix_sum += num
    if prefix_sum - k in sum_map:
        count += sum_map[prefix_sum - k]
    sum_map[prefix_sum] = sum_map.get(prefix_sum, 0) + 1
```

## **Strong Combinations with Other Techniques**

### **Sliding Window + Hash Map**

```python
def longest_substring_k_distinct(s, k):
    char_count = {}
    left = 0
    max_len = 0
    
    for right in range(len(s)):
        # Add current character to window
        char_count[s[right]] = char_count.get(s[right], 0) + 1
        
        # Shrink window if we have more than k distinct chars
        while len(char_count) > k:
            char_count[s[left]] -= 1
            if char_count[s[left]] == 0:
                del char_count[s[left]]
            left += 1
            
        max_len = max(max_len, right - left + 1)
        
    return max_len
```

### **Prefix Sum + Hash Map**

```python
def subarray_sum_equals_k(nums, k):
    prefix_sum = 0
    result = 0
    sum_map = {0: 1}  # For empty subarray
    
    for num in nums:
        prefix_sum += num
        
        # Check if there was a previous sum that creates a subarray of sum k
        if prefix_sum - k in sum_map:
            result += sum_map[prefix_sum - k]
            
        # Update the frequency of current sum
        sum_map[prefix_sum] = sum_map.get(prefix_sum, 0) + 1
        
    return result
```

## **Classic Problems on LeetCode**

| **Name** | **ID** | **Type** | **Difficulty** |
|----------|--------|----------|-----------------|
| Two Sum | #1 | Direct lookup | Easy |
| Valid Anagram | #242 | Count hash | Easy |
| Group Anagrams | #49 | Count hash | Medium |
| Subarray Sum Equals K | #560 | Prefix + hash | Medium |
| Longest Consecutive Sequence | #128 | Hash + DFS | Medium |
| Isomorphic Strings | #205 | Char-char map | Easy |
| LRU Cache | #146 | HashMap + DLL | Medium |

## **Ninja Tips**

- Use `collections.defaultdict(int)` or `Counter` to simplify.
- In string problems, **sorting is not always efficient**, using a count hash may be better.
- Be careful with mutable dict as value — clone if comparing snapshots.
- Store **indices or positions** in addition to values, to reconstruct answers.
- When dealing with prefix/partial sums, think of a hash map storing the state.

## **Thinking Out Loud: Longest Consecutive Sequence**

*Problem*: Given an unsorted array of integers, find the length of the longest consecutive sequence.

*Example*: Input: [100, 4, 200, 1, 3, 2] → Output: 4 (sequence [1, 2, 3, 4])

*Insights*:
1. Sorting would be O(n log n), we can do better with hash
2. For each number, check if it's the beginning of a sequence (n-1 doesn't exist)
3. If it's a start, begin counting consecutive using hash

```python
def longest_consecutive(nums):
    if not nums:
        return 0
        
    num_set = set(nums)  # O(1) lookup
    max_length = 0
    
    for num in num_set:
        # Only check sequences from the start
        if num - 1 not in num_set:
            current_num = num
            current_streak = 1
            
            # Count consecutive elements
            while current_num + 1 in num_set:
                current_num += 1
                current_streak += 1
                
            max_length = max(max_length, current_streak)
            
    return max_length
```

## **Checklist for Hash Maps**

- [ ] I know how to implement and use count maps with defaultdict and Counter
- [ ] I understand how to use prefixes with hash maps
- [ ] I can store complex states in hash maps
- [ ] I know when to use set vs. dict for optimization
- [ ] I've implemented at least 5 different variations with maps

## **Mini Challenge**

**Problem:** Check if two strings are isomorphic (same pattern of 1-to-1 mapping between characters).

**Example:**
- egg → add ✅ (e→a, g→d)
- foo → bar ❌ (f→b, o→a, o→r: o tries to map to two characters)

**Solution**:
1. Use two maps: one for s→t and another for t→s
2. Check if each character has a unique mapping in both directions
3. Ensure the mapping is consistent

---

# **Prefix Sum & Difference Arrays: The Art of Avoiding Repetition**

## **Why Use Prefix Sum?**

When you need to calculate **sums in ranges repeatedly**, prefix sum is your best friend.

Imagine: You want to know the sum of the interval arr[2:5] multiple times. Instead of manually summing, you use prefixes:

sum[2:5] = prefix[5] - prefix[1]

You transform an **O(n)** operation into **O(1)**.

## **Visualizing Prefix Sum**

```
Original: [3, 1, 4, 1, 5, 9, 2, 6]
Prefix:   [0, 3, 4, 8, 9, 14, 23, 25, 31]
          ↑   ↑
         [0] [1] = sum of 0 elements = 0
             ↑   ↑
            [1] [2] = sum of arr[0] = 3
                 ↑   ↑ 
                [2] [3] = sum of arr[0:1] = 3+1 = 4
```

To find the sum of arr[2:5]: prefix[6] - prefix[2] = 23 - 4 = 19

## **Creating Prefix Sums**

```python
def build_prefix(nums):
    prefix = [0]  # Start with 0 for empty subarray
    
    for num in nums:
        prefix.append(prefix[-1] + num)
        
    return prefix
```

Now prefix[i] represents the sum of nums[0] through nums[i-1].

## **Common Applications**

### **1. Subarray with Specific Sum**

**Problem:** Subarray Sum Equals K (#560)

We've seen this in Chapter 4, but we reinforce it here as it's the essence of Prefix + Hash Map.

```python
def subarray_sum(nums, k):
    prefix = 0
    count = 0
    prefix_map = {0: 1}  # Empty subarray
    
    for num in nums:
        prefix += num
        count += prefix_map.get(prefix - k, 0)
        prefix_map[prefix] = prefix_map.get(prefix, 0) + 1
        
    return count
```

### **2. Range Sum Query**

```python
class NumArray:
    def __init__(self, nums):
        self.prefix = [0]
        for num in nums:
            self.prefix.append(self.prefix[-1] + num)
            
    def sumRange(self, left, right):
        return self.prefix[right + 1] - self.prefix[left]
```

### **3. Difference Array: Interval Updates**

You want to add +10 from arr[2] to arr[5] **without iterating**? Use a difference array:

```python
def range_update(arr, updates):
    diff = [0] * (len(arr) + 1)
    
    for start, end, val in updates:
        diff[start] += val
        diff[end + 1] -= val
        
    # Reconstruct the original array with the updates
    for i in range(1, len(arr)):
        diff[i] += diff[i - 1]
        
    return [arr[i] + diff[i] for i in range(len(arr))]
```

## **Prefix Sum in 2D Arrays**

For 2D matrices, prefix sum allows calculating the sum of any sub-rectangle in O(1):

```python
def build_2d_prefix(matrix):
    if not matrix or not matrix[0]:
        return [[]]
        
    rows, cols = len(matrix), len(matrix[0])
    prefix = [[0] * (cols + 1) for _ in range(rows + 1)]
    
    for r in range(1, rows + 1):
        for c in range(1, cols + 1):
            prefix[r][c] = matrix[r-1][c-1] + prefix[r-1][c] + prefix[r][c-1] - prefix[r-1][c-1]
            
    return prefix

def get_sub_matrix_sum(prefix, r1, c1, r2, c2):
    return prefix[r2+1][c2+1] - prefix[r2+1][c1] - prefix[r1][c2+1] + prefix[r1][c1]
```

## **Real and Creative Applications**

- Accumulated frequency histogram
- Server load balancing (simulated problems)
- Task scheduling (intervals with impact)
- Trend analysis in time series

## **Classic Problems on LeetCode**

| **Name** | **ID** | **Technique** | **Difficulty** |
|----------|--------|-------------|-----------------|
| Range Sum Query - Immutable | #303 | Prefix Sum | Easy |
| Subarray Sum Equals K | #560 | Prefix + Hash | Medium |
| Maximum Size Subarray Sum Equals k | #325 | Prefix Sum | Medium |
| Corporate Flight Bookings | #1109 | Difference Array | Medium |
| Car Pooling | #1094 | Difference Array | Medium |
| Range Sum Query 2D - Immutable | #304 | 2D Prefix Sum | Medium |

## **Proficiency Tips**

- Store the prefix of **position zero** as 0 to avoid edge cases.
- Use dict for prefix sums if the array is very large and you want optimized space.
- For range update problems, Difference Array saves time and space.
- For 2D matrices, remember the formula: rect_sum = prefix[r2+1][c2+1] - prefix[r2+1][c1] - prefix[r1][c2+1] + prefix[r1][c1]

## **Thinking Out Loud: Car Pooling**

*Problem*: There is a car with capacity. You are given trips where trips[i] = [num_passengers, start, end] represents a trip with num_passengers from point start to end. Determine if it's possible to complete all trips.

*Insights*:
1. I can use difference array to track additions and removals of passengers
2. At each start point, add passengers; at each end point, remove them
3. Reconstruct the difference array to check if it exceeds capacity

```python
def car_pooling(trips, capacity):
    # Find the furthest point
    last_location = 0
    for _, _, end in trips:
        last_location = max(last_location, end)
        
    # Create the difference array
    diff = [0] * (last_location + 1)
    
    # Register boardings and departures
    for num_passengers, start, end in trips:
        diff[start] += num_passengers  # Boarding
        diff[end] -= num_passengers    # Departure
        
    # Check if any point exceeds capacity
    current = 0
    for passengers in diff:
        current += passengers
        if current > capacity:
            return False
            
    return True
```

## **Checklist Prefix/Diff**

- [ ] I know how to calculate sums in ranges with prefix sum
- [ ] I know how to do range updates with difference array
- [ ] I understand how to apply prefix sum in 2D matrices
- [ ] I've combined prefix with hash map to check patterns
- [ ] I've implemented at least 3 solutions using these techniques

## **Mini Challenge**

**Problem:** Given an array of range updates, like:
updates = [[1, 3, 2], [2, 4, 3], [0, 2, -2]]

Return the final array after applying all the updates on an array of size 5, initially with zeros.

**Solution**:
1. Create a difference array of size n+1
2. For each update [start, end, val], add val at diff[start] and subtract val from diff[end+1]
3. Reconstruct the original array through the difference array by cumulatively summing

---

# **Binary Search: Cutting in Half, Thinking with Precision**

## **Why Binary Search Is An Elite Weapon**

Binary Search goes far beyond finding elements in arrays. It's a technique for solving **problems with a monotonicity property**, where we can divide the search space in half at each iteration.

That's what makes it a legendary tool for transforming an O(n) problem into O(log n).

## **Visualizing Binary Search**

```
Array: [1, 2, 3, 4, 5, 6, 7, 8, 9]
        ↑           ↑           ↑
       left        mid         right

Looking for 7:
mid = 5 (value 6)
6 < 7, so left = mid + 1

Array: [1, 2, 3, 4, 5, 6, 7, 8, 9]
                        ↑   ↑   ↑
                      left mid right

mid = 7 (value 8)
8 > 7, so right = mid - 1

Array: [1, 2, 3, 4, 5, 6, 7, 8, 9]
                        ↑ ↑
                      left,right

mid = 6 (value 7)
7 == 7, found!
```

## **The Basic Pattern**

```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    
    while left <= right:
        mid = (left + right) // 2
        
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
            
    return -1  # Not found
```

This pattern can be adapted to **find bounds, specific positions, or optimize values**.

## **Important Variations**

### **1. Lower Bound Search**

```python
def lower_bound(arr, target):
    left, right = 0, len(arr)
    
    while left < right:
        mid = (left + right) // 2
        
        if arr[mid] < target:
            left = mid + 1
        else:
            right = mid
            
    return left
```

Finds the first element >= target.

### **2. Upper Bound Search**

```python
def upper_bound(arr, target):
    left, right = 0, len(arr)
    
    while left < right:
        mid = (left + right) // 2
        
        if arr[mid] <= target:
            left = mid + 1
        else:
            right = mid
            
    return left
```

Finds the first element > target.

### **3. Binary Search on Answer Space**

```python
def min_capacity(weights, D):
    def can_ship(capacity):
        days = 1
        total = 0
        
        for w in weights:
            if total + w > capacity:
                days += 1
                total = 0
            total += w
            
        return days <= D
    
    left = max(weights)   # Minimum possible capacity
    right = sum(weights)  # Maximum possible capacity
    
    while left < right:
        mid = (left + right) // 2
        
        if can_ship(mid):
            right = mid
        else:
            left = mid + 1
            
    return left
```

## **Where to Apply Binary Search**

| **Problem Type** | **Binary Search Application** |
|----------------------|--------------------------------|
| Search for value | In sorted arrays |
| Find first/last occurrence | Binary Search with adjustments |
| Optimize a number | Binary Search on answer space |
| Check if possible | Use an isValid(mid) function to guide |

## **Practical Cases**

### **1. Search Insert Position**

**LeetCode #35**

```python
def searchInsert(nums, target):
    left, right = 0, len(nums) - 1
    
    while left <= right:
        mid = (left + right) // 2
        
        if nums[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
            
    return left
```

➡️ When not found, returns where the value should be.

### **2. Find First and Last Position of Element**

**LeetCode #34**

```python
def searchRange(nums, target):
    def find_first():
        left, right = 0, len(nums) - 1
        result = -1
        
        while left <= right:
            mid = (left + right) // 2
            
            if nums[mid] == target:
                result = mid
                right = mid - 1  # Continue searching to the left
            elif nums[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
                
        return result
        
    def find_last():
        left, right = 0, len(nums) - 1
        result = -1
        
        while left <= right:
            mid = (left + right) // 2
            
            if nums[mid] == target:
                result = mid
                left = mid + 1  # Continue searching to the right
            elif nums[mid] < target:
                left = mid + 1
            else:
                right = mid - 1
                
        return result
        
    return [find_first(), find_last()]
```

### **3. Find Minimum in Rotated Sorted Array**

**LeetCode #153**

```python
def findMin(nums):
    left, right = 0, len(nums) - 1
    
    while left < right:
        mid = (left + right) // 2
        
        if nums[mid] > nums[right]:
            left = mid + 1
        else:
            right = mid
            
    return nums[left]
```

## **Crucial Concepts in Binary Search**

### **1. Overflow When Obtaining Mid**

In languages like C/C++, using:
```cpp
int mid = (left + right) / 2;  // Can overflow
```

Better approach:
```cpp
int mid = left + (right - left) / 2;  // Prevents overflow
```

### **2. Descending to the Correct Element**

Depending on the problem:
- If `left <= right`: search ends when pointers cross
- If `left < right`: search ends when pointers meet

### **3. Monotonicity**

The fundamental property: the search space must be divided into two distinct regions where the condition changes exactly once.

```
[F, F, F, T, T, T, T]
          ↑
     Change point
```

## **Ninja Tips**

- Binary Search is about **values, not just indices**
- It can work on **virtual or infinite arrays**
- **Don't just rely on the template**: understand the monotonicity!
- For optimizations, create an isValid() function and look for the smallest/largest value that satisfies it
- Draw the case to visualize the behavior of the pointers

## **Classic Problems to Master**

| **Problem** | **LeetCode ID** | **Difficulty** |
|--------------|-----------------|-----------------|
| Binary Search | #704 | Easy |
| Search Insert Position | #35 | Easy |
| First Bad Version | #278 | Easy |
| Find First and Last Position | #34 | Medium |
| Koko Eating Bananas | #875 | Medium |
| Find Minimum in Rotated Sorted Array | #153 | Medium |
| Search in Rotated Sorted Array | #33 | Medium |
| Median of Two Sorted Arrays | #4 | Hard |

## **Thinking Out Loud: Koko Eating Bananas**

*Problem*: Koko loves eating bananas. There are N piles of bananas, the i-th pile has piles[i] bananas. The guard will come back in H hours. Koko can eat bananas at a speed of K per hour. Given that she can only eat from one pile per hour, find the minimum K for her to eat all bananas before the guard returns.

*Insights*:
1. The minimum limit of K is 1
2. The maximum limit of K is the maximum of the piles (eat the largest pile in 1 hour)
3. For each value of K, I can calculate how many hours Koko takes
4. I'll search for the smallest K that satisfies the condition

```python
def minEatingSpeed(piles, h):
    def hours_to_eat(k):
        return sum((pile + k - 1) // k for pile in piles)  # Ceiling division
        
    left, right = 1, max(piles)
    
    while left < right:
        mid = (left + right) // 2
        
        if hours_to_eat(mid) <= h:
            right = mid  # Try to reduce the speed
        else:
            left = mid + 1  # Need to increase the speed
            
    return left
```

## **Checklist Binary Search**

- [ ] I can implement classic binary search without errors
- [ ] I understand the variations of lower/upper bound
- [ ] I know how to apply binary search on answer space
- [ ] I've implemented solutions for rotated arrays
- [ ] I've practiced at least 5 binary search problems

## **Mini Challenge**

**Problem:** Given a sorted array and a target, find the first position where it appears (or -1 if it doesn't exist).

**Solution**:
1. Use standard binary search with a variable to store the found position
2. Continue searching to the left even after finding the target
3. Return the leftmost position found

---

# **Depth-First Search & Backtracking: Exploring All Possibilities**

## **The Power of Recursive Exploration**

Depth-First Search (DFS) and Backtracking are techniques that allow us to **systematically explore all possibilities** in a search space. They are fundamental for:

- Exploring trees and graphs
- Finding all possible paths
- Solving permutation and combination problems
- Breaking complex problems into subproblems

The difference between them is subtle:
- **DFS** is the depth-first search technique
- **Backtracking** is DFS with the ability to "undo" choices and try new paths

## **Visualizing DFS and Backtracking**

```
                  Root
                /  |  \
               A   B   C
              / \     / \
             D   E   F   G
```

DFS Exploration: Root → A → D → E → B → C → F → G

Backtracking in [1,2,3] Permutation:
```
                []
              /  |  \
            [1]  [2]  [3]
           /  \    ...  ...
       [1,2] [1,3]
       /       \
  [1,2,3]     [1,3,2]
```

## **Base DFS Implementation**

### **1. Recursive DFS in Trees**

```python
def dfs(node):
    if not node:
        return
        
    # Process the current node
    process(node)
    
    # Explore left and right
    dfs(node.left)
    dfs(node.right)
```

### **2. Recursive DFS in Graphs**

```python
def dfs(graph, node, visited):
    if node in visited:
        return
        
    visited.add(node)
    
    # Process the current node
    process(node)
    
    # Explore neighbors
    for neighbor in graph[node]:
        dfs(graph, neighbor, visited)
```

### **3. Iterative DFS with Stack**

```python
def dfs_iterative(graph, start):
    visited = set()
    stack = [start]
    
    while stack:
        node = stack.pop()
        
        if node in visited:
            continue
            
        visited.add(node)
        process(node)
        
        # Add neighbors to stack
        for neighbor in graph[node]:
            if neighbor not in visited:
                stack.append(neighbor)
```

## **Backtracking Pattern**

```python
def backtrack(current_state, choices, result):
    # Base condition: final state reached
    if is_solution(current_state):
        result.append(current_state.copy())  # Add copy of solution
        return
        
    # Try each possible choice
    for choice in choices:
        if is_valid(current_state, choice):
            # Apply the choice
            make_choice(current_state, choice)
            
            # Explore with the choice made
            backtrack(current_state, choices, result)
            
            # Undo the choice (backtrack)
            undo_choice(current_state, choice)
```

## **Classic DFS Problems**

### **1. Traversing a Binary Tree**

```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right

def inorder_traversal(root):
    result = []
    
    def dfs(node):
        if not node:
            return
            
        dfs(node.left)  # Left
        result.append(node.val)  # Root
        dfs(node.right)  # Right
        
    dfs(root)
    return result
```

### **2. Number of Islands (LeetCode #200)**

```python
def numIslands(grid):
    if not grid or not grid[0]:
        return 0
        
    rows, cols = len(grid), len(grid[0])
    islands = 0
    
    def dfs(r, c):
        # Out of bounds or not land
        if r < 0 or r >= rows or c < 0 or c >= cols or grid[r][c] != '1':
            return
            
        # Mark as visited
        grid[r][c] = '0'
        
        # Explore the 4 directions
        dfs(r+1, c)
        dfs(r-1, c)
        dfs(r, c+1)
        dfs(r, c-1)
    
    for r in range(rows):
        for c in range(cols):
            if grid[r][c] == '1':
                islands += 1
                dfs(r, c)  # Mark the entire island as visited
                
    return islands
```

## **Classic Backtracking Problems**

### **1. Permutations (LeetCode #46)**

```python
def permute(nums):
    result = []
    
    def backtrack(current, remaining):
        if not remaining:
            result.append(current[:])
            return
            
        for i in range(len(remaining)):
            # Choice
            current.append(remaining[i])
            
            # Explore
            backtrack(current, remaining[:i] + remaining[i+1:])
            
            # Undo (backtrack)
            current.pop()
    
    backtrack([], nums)
    return result
```

### **2. Subsets (LeetCode #78)**

```python
def subsets(nums):
    result = []
    
    def backtrack(start, current):
        # Each intermediate state is a valid solution
        result.append(current[:])
        
        for i in range(start, len(nums)):
            # Include the element
            current.append(nums[i])
            
            # Explore with this element added
            backtrack(i + 1, current)
            
            # Remove the element
            current.pop()
    
    backtrack(0, [])
    return result
```

## **Optimizations in Backtracking**

### **1. Pruning**

Eliminate paths that you know won't lead to valid solutions.

```python
def combinationSum(candidates, target):
    result = []
    candidates.sort()  # Helps with pruning
    
    def backtrack(start, current, remaining):
        if remaining == 0:
            result.append(current[:])
            return
            
        for i in range(start, len(candidates)):
            # Pruning: if the current candidate is larger than what's left, no subsequent ones will work
            if candidates[i] > remaining:
                break
                
            # Avoid duplicate processing
            if i > start and candidates[i] == candidates[i-1]:
                continue
                
            current.append(candidates[i])
            backtrack(i, current, remaining - candidates[i])  # Can reuse the same element
            current.pop()
    
    backtrack(0, [], target)
    return result
```

### **2. Memoization**

Store results of already calculated subproblems.

```python
def word_break(s, wordDict):
    words = set(wordDict)
    memo = {}
    
    def can_break(start):
        if start == len(s):
            return True
            
        if start in memo:
            return memo[start]
            
        for end in range(start + 1, len(s) + 1):
            if s[start:end] in words and can_break(end):
                memo[start] = True
                return True
                
        memo[start] = False
        return False
        
    return can_break(0)
```

## **Popular Problems on LeetCode**

| **Name** | **ID** | **Technique** | **Difficulty** |
|----------|--------|-------------|-----------------|
| Number of Islands | #200 | DFS | Medium |
| Max Area of Island | #695 | DFS | Medium |
| Permutations | #46 | Backtracking | Medium |
| Subsets | #78 | Backtracking | Medium |
| Combination Sum | #39 | Backtracking | Medium |
| N-Queens | #51 | Backtracking | Hard |
| Word Search | #79 | DFS | Medium |
| Sudoku Solver | #37 | Backtracking | Hard |

## **Ninja Tips**

- Always mark nodes as visited to avoid cycles.
- In matrix problems, a common way to mark as visited is to modify the value itself.
- Try to use **pruning** to eliminate infeasible paths as early as possible.
- For subsets/combinations, pre-sorting often helps.
- Check if the problem requires all solutions or just one solution.
- Use memoization for DFS in problems that revisit the same states.

## **Thinking Out Loud: Word Search**

*Problem*: Given a matrix of characters and a word, check if the word exists in the matrix. The word can be constructed from adjacent letters in the matrix, where adjacent means horizontally or vertically neighboring. The same cell cannot be used more than once.

*Insights*:
1. For each cell in the matrix, try to start a DFS if the character matches the first one in the word
2. At each step of the DFS, check the 4 directions
3. Mark cells as visited to avoid reuse
4. Unmark when backtracking

```python
def exist(board, word):
    rows, cols = len(board), len(board[0])
    
    def dfs(r, c, index):
        # Found the complete word
        if index == len(word):
            return True
            
        # Out of bounds or character doesn't match
        if (r < 0 or r >= rows or c < 0 or c >= cols or 
            board[r][c] != word[index]):
            return False
            
        # Mark as temporarily visited
        temp = board[r][c]
        board[r][c] = '#'
        
        # Explore the 4 directions
        found = (dfs(r+1, c, index+1) or 
                 dfs(r-1, c, index+1) or 
                 dfs(r, c+1, index+1) or 
                 dfs(r, c-1, index+1))
        
        # Backtrack - restore the character
        board[r][c] = temp
        
        return found
    
    # Try to start DFS from each cell
    for r in range(rows):
        for c in range(cols):
            if board[r][c] == word[0] and dfs(r, c, 0):
                return True
                
    return False
```

## **Checklist DFS/Backtracking**

- [ ] I understand the difference between iterative and recursive DFS
- [ ] I know how to apply DFS in trees and graphs
- [ ] I understand the backtracking pattern (choice, exploration, undo)
- [ ] I know how to optimize backtracking with pruning
- [ ] I've implemented at least 5 problems using these techniques

## **Mini Challenge**

**Problem:** Generate all possible combinations of k numbers chosen from 1 to n.

**Example:** 
Input: n = 4, k = 2
Output: [[1,2], [1,3], [1,4], [2,3], [2,4], [3,4]]

**Solution**:
1. Use backtracking to generate the combinations
2. For each number from 1 to n, decide whether to include it in the current combination
3. When the combination has size k, add it to the result

---

# **Breadth-First Search & Graph Traversal: Shortest Path and Beyond**

## **When Width Beats Depth**

Breadth-First Search (BFS) is a traversal technique that explores all neighbors of a node before moving to the next level. It's essential for:

- Finding the **shortest path** in unweighted graphs
- Traversing a tree level by level
- Solving mazes and connectivity problems
- Detecting components in undirected graphs

The main difference from DFS:
- DFS goes as far as possible along one path before backtracking
- BFS explores in "waves" or levels, guaranteeing minimum paths

## **Visualizing BFS**

```
             A
           / | \
          B  C  D
         / \    |
        E   F   G
```

BFS Traversal: A → B → C → D → E → F → G (Level by level)

## **Classic BFS Implementation**

```python
from collections import deque

def bfs(graph, start):
    visited = set([start])
    queue = deque([start])
    
    while queue:
        node = queue.popleft()  # Remove the first (FIFO)
        process(node)
        
        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)
```

## **BFS for Finding Shortest Path**

```python
def shortest_path(graph, start, end):
    if start == end:
        return [start]
        
    visited = set([start])
    queue = deque([(start, [start])])  # (node, path_so_far)
    
    while queue:
        node, path = queue.popleft()
        
        for neighbor in graph[node]:
            if neighbor == end:
                return path + [neighbor]  # Path found!
                
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append((neighbor, path + [neighbor]))
                
    return None  # No path
```

## **Multi-Source BFS**

```python
def multi_source_bfs(grid, sources):
    rows, cols = len(grid), len(grid[0])
    queue = deque(sources)  # Start with multiple sources
    visited = set(sources)
    
    level = 0
    while queue:
        size = len(queue)
        
        for _ in range(size):
            r, c = queue.popleft()
            
            # Process current node
            process(r, c, level)
            
            # Directions: up, right, down, left
            for dr, dc in [(0, 1), (1, 0), (0, -1), (-1, 0)]:
                nr, nc = r + dr, c + dc
                
                if (0 <= nr < rows and 0 <= nc < cols and 
                    grid[nr][nc] == 0 and (nr, nc) not in visited):
                    visited.add((nr, nc))
                    queue.append((nr, nc))
                    
        level += 1  # Next level
```

## **Classic BFS Problems**

### **1. Binary Tree Level Order Traversal**

```python
def levelOrder(root):
    if not root:
        return []
        
    result = []
    queue = deque([root])
    
    while queue:
        level_size = len(queue)
        level = []
        
        for _ in range(level_size):
            node = queue.popleft()
            level.append(node.val)
            
            if node.left:
                queue.append(node.left)
                
            if node.right:
                queue.append(node.right)
                
        result.append(level)
        
    return result
```

### **2. Rotting Oranges (LeetCode #994)**

```python
def orangesRotting(grid):
    rows, cols = len(grid), len(grid[0])
    queue = deque()
    fresh_count = 0
    
    # Find all rotten oranges and count the fresh ones
    for r in range(rows):
        for c in range(cols):
            if grid[r][c] == 2:  # Rotten
                queue.append((r, c))
            elif grid[r][c] == 1:  # Fresh
                fresh_count += 1
    
    # No fresh oranges, we're done
    if fresh_count == 0:
        return 0
        
    # BFS from all rotten oranges
    minutes = 0
    while queue and fresh_count > 0:
        size = len(queue)
        
        for _ in range(size):
            r, c = queue.popleft()
            
            for dr, dc in [(0, 1), (1, 0), (0, -1), (-1, 0)]:
                nr, nc = r + dr, c + dc
                
                if (0 <= nr < rows and 0 <= nc < cols and grid[nr][nc] == 1):
                    grid[nr][nc] = 2  # Contaminate
                    fresh_count -= 1
                    queue.append((nr, nc))
                    
        minutes += 1
        
    return minutes if fresh_count == 0 else -1
```

## **BFS in Implicit Graphs**

Many problems involve graphs that are not explicitly provided but are implicit in the problem description:

```python
def word_ladder(beginWord, endWord, wordList):
    word_set = set(wordList)
    if endWord not in word_set:
        return 0
        
    queue = deque([(beginWord, 1)])  # (word, length_so_far)
    visited = set([beginWord])
    
    while queue:
        current_word, length = queue.popleft()
        
        if current_word == endWord:
            return length
            
        # Generate all one-letter transformations
        for i in range(len(current_word)):
            for c in 'abcdefghijklmnopqrstuvwxyz':
                next_word = current_word[:i] + c + current_word[i+1:]
                
                if next_word in word_set and next_word not in visited:
                    visited.add(next_word)
                    queue.append((next_word, length + 1))
                    
    return 0
```

## **Bi-directional BFS**

To improve efficiency in some problems, we can perform BFS from both the start and end simultaneously:

```python
def bidirectional_bfs(graph, start, end):
    if start == end:
        return 1
        
    forward_queue = deque([start])
    backward_queue = deque([end])
    
    forward_visited = {start: 1}  # node -> distance
    backward_visited = {end: 1}
    
    while forward_queue and backward_queue:
        # Expand the smaller front to optimize
        if len(forward_queue) <= len(backward_queue):
            distance = expand_front(graph, forward_queue, forward_visited, backward_visited)
        else:
            distance = expand_front(graph, backward_queue, backward_visited, forward_visited)
            
        if distance:
            return distance
            
    return -1  # No path

def expand_front(graph, queue, visited, other_visited):
    node = queue.popleft()
    distance = visited[node]
    
    for neighbor in graph[node]:
        if neighbor in other_visited:  # Found intersection
            return distance + other_visited[neighbor] - 1
            
        if neighbor not in visited:
            visited[neighbor] = distance + 1
            queue.append(neighbor)
            
    return None
```

## **Popular Problems on LeetCode**

| **Name** | **ID** | **Technique** | **Difficulty** |
|----------|--------|-------------|-----------------|
| Binary Tree Level Order Traversal | #102 | Simple BFS | Medium |
| Rotting Oranges | #994 | Multi-source BFS | Medium |
| Word Ladder | #127 | BFS in Implicit Graph | Hard |
| Shortest Bridge | #934 | Multi-source BFS | Medium |
| Course Schedule | #207 | BFS/Topological Sort | Medium |
| Walls and Gates | #286 | Multi-source BFS | Medium |
| 01 Matrix | #542 | Multi-source BFS | Medium |

## **Ninja Tips for Graphs**

- Use `collections.deque` for efficient BFS implementations (O(1) for popleft).
- For implicit graphs, clearly define what are the "nodes" and "edges".
- In matrix problems, use a directions array to simplify code.
- To detect cycles in directed graphs, combine BFS with in-degree counting.
- Maintain a distance map instead of just a visited set to track levels.
- Consider bidirectional BFS to improve efficiency in large graphs.

## **Thinking Out Loud: 01 Matrix**

*Problem*: Given a matrix with 0s and 1s, calculate the distance of the nearest 0 for each cell. The distance is the minimum number of steps to reach a 0.

*Insights*:
1. Multi-source BFS starting from all zeros simultaneously
2. As BFS progresses, the distance is the level in the BFS
3. This ensures each 1 cell gets the minimum distance to a 0

```python
def update_matrix(mat):
    rows, cols = len(mat), len(mat[0])
    queue = deque()
    
    # Start with all 0s as sources
    for r in range(rows):
        for c in range(cols):
            if mat[r][c] == 0:
                queue.append((r, c))
            else:
                mat[r][c] = float('inf')  # Mark 1s as infinity
    
    directions = [(0, 1), (1, 0), (0, -1), (-1, 0)]
    
    # Multi-source BFS
    while queue:
        r, c = queue.popleft()
        
        for dr, dc in directions:
            nr, nc = r + dr, c + dc
            
            # If the adjacent cell can be improved
            if (0 <= nr < rows and 0 <= nc < cols and 
                mat[nr][nc] > mat[r][c] + 1):
                mat[nr][nc] = mat[r][c] + 1
                queue.append((nr, nc))
                
    return mat
```

## **Checklist BFS & Graphs**

- [ ] I understand the basic implementation of BFS with queue
- [ ] I know how to find shortest paths with BFS
- [ ] I've implemented multi-source BFS in matrix problems
- [ ] I know how to apply BFS in implicit graphs
- [ ] I know techniques to optimize BFS in large graphs

## **Mini Challenge**

**Problem:** In a binary matrix with 1s (land) and 0s (water), find the island furthest from the coast (in terms of distance).

**Example:** 
```
[0, 0, 0, 0]
[0, 1, 1, 0]
[0, 1, 1, 0]
[0, 0, 0, 0]
```
The furthest island from the coast is 1 unit away.

**Solution**:
1. Use multi-source BFS starting from all water cells (0s)
2. As the BFS progresses, distances are calculated
3. The largest distance found is the answer

---

# **Dynamic Programming: Building Incremental Solutions**

## **The Art of Storing Subproblems**

Dynamic Programming (DP) is a powerful technique for optimizing problems that have:
- Optimal substructure (the optimal solution contains optimal solutions of subproblems)
- Overlapping subproblems (the same subproblems are solved multiple times)

DP transforms exponential problems into polynomial ones by **storing and reusing subproblem results**.

## **The Two Main Approaches**

### **1. Memoization (Top-down)**

```python
def fibonacci(n, memo={}):
    if n in memo:
        return memo[n]
        
    if n <= 1:
        return n
        
    memo[n] = fibonacci(n-1, memo) + fibonacci(n-2, memo)
    return memo[n]
```

### **2. Tabulation (Bottom-up)**

```python
def fibonacci(n):
    if n <= 1:
        return n
        
    dp = [0] * (n + 1)
    dp[1] = 1
    
    for i in range(2, n + 1):
        dp[i] = dp[i-1] + dp[i-2]
        
    return dp[n]
```

## **Framework for Solving DP Problems**

1. **Define the state**: What do the indices of the dp array mean?
2. **Define the base case**: What are the simplest cases?
3. **Formulate the recurrence**: How to solve for dp[i] using previous values?
4. **Computation ordering**: In what order to compute the values?
5. **Find the answer**: Which value in the dp array is the final solution?

## **DP Patterns and Examples**

### **1. Linear Sequences**

**Problem**: Longest Increasing Subsequence (LeetCode #300)

```python
def lengthOfLIS(nums):
    if not nums:
        return 0
        
    n = len(nums)
    dp = [1] * n  # Each element is a subsequence of size 1
    
    for i in range(n):
        for j in range(i):
            if nums[i] > nums[j]:  # If we can add nums[i] after nums[j]
                dp[i] = max(dp[i], dp[j] + 1)
                
    return max(dp)
```

### **2. DP on Strings**

**Problem**: Longest Common Subsequence (LCS)

```python
def longestCommonSubsequence(text1, text2):
    m, n = len(text1), len(text2)
    dp = [[0] * (n + 1) for _ in range(m + 1)]
    
    for i in range(1, m + 1):
        for j in range(1, n + 1):
            if text1[i-1] == text2[j-1]:
                dp[i][j] = dp[i-1][j-1] + 1
            else:
                dp[i][j] = max(dp[i-1][j], dp[i][j-1])
                
    return dp[m][n]
```

### **3. DP on Grid/Matrix**

**Problem**: Unique Paths (LeetCode #62)

```python
def uniquePaths(m, n):
    dp = [[1] * n for _ in range(m)]
    
    for i in range(1, m):
        for j in range(1, n):
            dp[i][j] = dp[i-1][j] + dp[i][j-1]
            
    return dp[m-1][n-1]
```

### **4. Knapsack Problem**

**Problem**: 0/1 Knapsack

```python
def knapsack(weights, values, capacity):
    n = len(weights)
    dp = [[0] * (capacity + 1) for _ in range(n + 1)]
    
    for i in range(1, n + 1):
        for w in range(capacity + 1):
            if weights[i-1] <= w:
                dp[i][w] = max(values[i-1] + dp[i-1][w-weights[i-1]], dp[i-1][w])
            else:
                dp[i][w] = dp[i-1][w]
                
    return dp[n][capacity]
```

### **5. DP with State Optimization**

**Problem**: House Robber (LeetCode #198)

```python
def rob(nums):
    if not nums:
        return 0
        
    if len(nums) == 1:
        return nums[0]
        
    # dp[i] = maximum that can be robbed up to house i
    dp = [0] * len(nums)
    dp[0] = nums[0]
    dp[1] = max(nums[0], nums[1])
    
    for i in range(2, len(nums)):
        dp[i] = max(dp[i-1], dp[i-2] + nums[i])
        
    return dp[-1]
```

## **Optimizing Space in DP**

Many DP problems can be optimized to use only O(1) or O(n) space:

```python
def rob_optimized(nums):
    if not nums:
        return 0
        
    if len(nums) == 1:
        return nums[0]
        
    # We only need two previous states
    prev1 = max(nums[0], nums[1])  # dp[1]
    prev2 = nums[0]  # dp[0]
    
    for i in range(2, len(nums)):
        current = max(prev1, prev2 + nums[i])
        prev2, prev1 = prev1, current
        
    return prev1
```

## **Popular Problems on LeetCode**

| **Name** | **ID** | **Pattern** | **Difficulty** |
|----------|--------|------------|-----------------|
| Climbing Stairs | #70 | Linear Sequence | Easy |
| House Robber | #198 | Linear Sequence | Medium |
| Longest Increasing Subsequence | #300 | Linear Sequence | Medium |
| Coin Change | #322 | Knapsack | Medium |
| Longest Common Subsequence | #1143 | DP on Strings | Medium |
| Regular Expression Matching | #10 | DP on Strings | Hard |
| Edit Distance | #72 | DP on Strings | Hard |
| Maximum Subarray | #53 | Kadane | Easy |

## **Ninja Tips for DP**

- Always start with the recursive approach (top-down) to understand the recurrence relation.
- Draw a recursion tree to identify overlapping subproblems.
- For space optimization, check if you only need the last few states.
- When working with arrays, consider sorting first if it simplifies the problem.
- In subsequence problems, try formulating the recurrence based on including or not including the current element.
- Be careful with base case initialization - usually it's the simplest case of the problem.
- For two-dimensional DP problems, draw the table and trace some examples manually.

## **Thinking Out Loud: Coin Change**

*Problem*: Given a list of coins of different denominations and a total amount, find the minimum number of coins needed to make that amount. If not possible, return -1.

*Insights*:
1. State: dp[i] = minimum number of coins to make i
2. Base: dp[0] = 0 (I need no coins to make 0)
3. Transition: dp[i] = min(dp[i], dp[i-coin] + 1) for each coin
4. Order: calculate from 1 to amount
5. Answer: dp[amount]

```python
def coinChange(coins, amount):
    # Initialize with impossible value
    dp = [float('inf')] * (amount + 1)
    dp[0] = 0  # Base: 0 coins to make 0
    
    for coin in coins:
        for i in range(coin, amount + 1):
            dp[i] = min(dp[i], dp[i - coin] + 1)
            
    return dp[amount] if dp[amount] != float('inf') else -1
```

This is more efficient than the intuitive way of iterating by amount and then by coins, because we avoid unnecessary recomputations.

## **Checklist Dynamic Programming**

- [ ] I understand the difference between top-down and bottom-up approaches
- [ ] I can identify overlapping subproblems
- [ ] I know how to formulate recurrence relations
- [ ] I can optimize space in DP solutions
- [ ] I've implemented at least 5 different DP solutions

## **Mini Challenge**

**Problem:** Given an m x n grid filled with non-negative numbers, find a path from top left to bottom right that minimizes the sum of all numbers along its path.

**Note**: You can only move down or right.

**Solution**:
1. Create a dp array where dp[i][j] is the minimum sum to reach position (i,j)
2. Use the recurrence: dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1])
3. Initialize the edges appropriately
4. The answer will be dp[m-1][n-1]

---

# **Greedy Algorithms: Optimizing Step by Step**

## **The Intuition Behind Greedy Algorithms**

Greedy Algorithms make locally optimal choices at each step, hoping to find a global optimum. They are efficient when:

- Local greedy choice leads to global optimal solution
- No need to look back or reconsider previous choices
- The problem has "optimal substructure" (like DP) but without overlap

The big advantage: they are generally simpler and more efficient than DP or Backtracking.

## **How to Recognize Greedy Problems**

Greedy problems typically involve:
- Maximizing or minimizing something
- Making incremental choices without reconsidering
- Sorting that establishes a clear priority
- Interval, scheduling, or selection problems

## **Proving Greedy Algorithms**

Unlike other techniques, greedy algorithms often require **mathematical proofs** to ensure they work:

1. **Proof by Induction**: Show that if the first k choices are optimal, then the k+1-th is too
2. **Proof by Contradiction**: Assume a better solution exists and derive a contradiction
3. **Exchange Proof**: Show that any non-greedy solution can be transformed into a greedy one without worsening it

## **Classic Examples**

### **1. Activity Selection**

**Problem**: Given a set of activities with start and end times, select the maximum number of non-overlapping activities.

```python
def activity_selection(start, finish):
    # Sort activities by end time
    activities = sorted(zip(start, finish), key=lambda x: x[1])
    selected = [activities[0]]  # Select the first activity
    
    for activity in activities[1:]:
        # If the current activity doesn't overlap the last selected
        if activity[0] >= selected[-1][1]:
            selected.append(activity)
            
    return selected
```

### **2. Fractional Knapsack**

**Problem**: Given a knapsack with capacity W and items with values and weights, maximize the total value in the knapsack. You can take fractions of items.

```python
def fractional_knapsack(values, weights, capacity):
    # Calculate value/weight ratio
    ratio = [(v/w, v, w) for v, w in zip(values, weights)]
    ratio.sort(reverse=True)  # Sort by value/weight ratio
    
    total_value = 0
    
    for r, v, w in ratio:
        if capacity >= w:  # Take the whole item
            total_value += v
            capacity -= w
        else:  # Take fraction of the item
            total_value += v * (capacity / w)
            break
            
    return total_value
```

### **3. Huffman Coding**

**Problem**: Create an optimal prefix code for data compression.

```python
import heapq
from collections import Counter

def huffman_encoding(text):
    # Frequency count
    freq = Counter(text)
    
    # Create min heap of nodes
    heap = [[weight, [char, ""]] for char, weight in freq.items()]
    heapq.heapify(heap)
    
    # Build Huffman tree
    while len(heap) > 1:
        lo = heapq.heappop(heap)
        hi = heapq.heappop(heap)
        
        for pair in lo[1:]:
            pair[1] = '0' + pair[1]
        for pair in hi[1:]:
            pair[1] = '1' + pair[1]
            
        heapq.heappush(heap, [lo[0] + hi[0]] + lo[1:] + hi[1:])
        
    # Extract codes
    huffman_codes = {char: code for char, code in heap[0][1:]}
    return huffman_codes
```

## **Applications in LeetCode Problems**

### **1. Jump Game (LeetCode #55)**

```python
def canJump(nums):
    max_reach = 0
    
    for i in range(len(nums)):
        # If we can't reach the current position
        if i > max_reach:
            return False
            
        # Update maximum reach
        max_reach = max(max_reach, i + nums[i])
        
        # If we can already reach the end
        if max_reach >= len(nums) - 1:
            return True
            
    return True
```

### **2. Gas Station (LeetCode #134)**

```python
def canCompleteCircuit(gas, cost):
    if sum(gas) < sum(cost):
        return -1  # Impossible to complete the circuit
        
    start = 0
    tank = 0
    
    for i in range(len(gas)):
        tank += gas[i] - cost[i]
        
        if tank < 0:  # Can't reach the next station
            start = i + 1  # Try starting from the next
            tank = 0
            
    return start
```

## **Common Pitfalls in Greedy**

- **Applying to problems where it doesn't work**: Not all problems that seem greedy have optimal greedy solutions
- **Not sorting correctly**: Wrong sorting can lead to suboptimal solutions
- **Ignoring edge cases**: Greedy algorithms can fail on certain edge cases
- **Not proving correctness**: Just because it works on examples doesn't mean it's optimal

## **Popular Problems on LeetCode**

| **Name** | **ID** | **Greedy Technique** | **Difficulty** |
|----------|--------|---------------------|-----------------|
| Jump Game | #55 | Maximum reach | Medium |
| Gas Station | #134 | Accumulated balance | Medium |
| Task Scheduler | #621 | Sorting+Priority | Medium |
| Non-overlapping Intervals | #435 | Sorting+Selection | Medium |
| Meeting Rooms II | #253 | Line Sweep | Medium |
| Partition Labels | #763 | Last index | Medium |
| Minimum Number of Arrows to Burst Balloons | #452 | Sorting+Selection | Medium |

## **Ninja Tips for Greedy**

- Try a greedy solution first on optimization problems - they're usually simpler.
- Verify if the greedy property actually applies - use examples to test your intuition.
- Sort the data when needed to establish clear priorities.
- In interval problems, it's often useful to sort by end time (as in Activity Selection).
- Maintain some sort of "global state" (like max_reach, current_tank) to track your progress.

## **Thinking Out Loud: Non-overlapping Intervals**

*Problem*: Given a collection of intervals, find the minimum number of intervals you need to remove to make the rest non-overlapping.

*Insights*:
1. We sort by end time to maximize the number of intervals that can remain
2. Always keep the current interval with the smallest end time
3. Remove any interval that overlaps

```python
def eraseOverlapIntervals(intervals):
    if not intervals:
        return 0
        
    # Sort by end time
    intervals.sort(key=lambda x: x[1])
    
    count = 0  # Number of intervals to remove
    end = intervals[0][1]  # End of first interval
    
    for i in range(1, len(intervals)):
        if intervals[i][0] < end:  # Overlap
            count += 1
        else:  # No overlap, update end
            end = intervals[i][1]
            
    return count
```

## **Checklist Greedy Algorithms**

- [ ] I understand when a problem may have a greedy solution
- [ ] I know how to apply sorting as pre-processing for greedy algorithms
- [ ] I can identify the correct greedy choice
- [ ] I've implemented at least 5 different greedy solutions
- [ ] I have a notion of how to prove that a greedy algorithm is correct

## **Mini Challenge**

**Problem:** Given a set of people with different skills (represented as numbers), form the maximum number of pairs such that each pair has at least one person with skill >= threshold.

**Example:** 
skills = [1, 3, 2, 5, 1, 3, 2], threshold = 3
Answer: 3 pairs

**Solution**:
1. Sort the skills array
2. Use two pointers at the extremes to form pairs
3. If skills[high] >= threshold, form a pair
4. Otherwise, try to form a pair with two lower elements

---

# **Advanced Data Structures: Trie, Union Find and Segment Trees**

## **Why Specialized Structures Make a Difference**

While arrays, lists, and hash maps are fundamental structures, complex problems often require specialized data structures. The three most important for interviews are:

- **Trie**: great for string problems, prefixes, and lexicographic searches
- **Union Find**: excellent for connectivity problems and disjoint sets
- **Segment Tree**: powerful for range queries and updates

These structures transform seemingly O(n²) or worse problems into O(n log n) or even O(n) solutions.

## **Trie (Prefix Tree)**

A Trie is a tree that stores strings hierarchically, where each node represents a character and paths from root to any node form a prefix:

```
      root
     / | \
    a  b  c
   / \    |
  p   t   a
 /     \  |
p       o t
```

### **Basic Implementation**

```python
class TrieNode:
    def __init__(self):
        self.children = {}
        self.is_end_of_word = False

class Trie:
    def __init__(self):
        self.root = TrieNode()
        
    def insert(self, word):
        node = self.root
        for char in word:
            if char not in node.children:
                node.children[char] = TrieNode()
            node = node.children[char]
        node.is_end_of_word = True
        
    def search(self, word):
        node = self.root
        for char in word:
            if char not in node.children:
                return False
            node = node.children[char]
        return node.is_end_of_word
        
    def starts_with(self, prefix):
        node = self.root
        for char in prefix:
            if char not in node.children:
                return False
            node = node.children[char]
        return True
```

### **Classic Applications**

- **Implementing autocomplete**
- **Prefix search**
- **Longest common prefix**
- **Word Dictionary with advanced operations**

### **Example: Implement Trie (LeetCode #208)**

The implementation above is basically the solution for this problem.

### **Example: Word Search II (LeetCode #212)**

Combining Trie with DFS to find all words in a character matrix:

```python
def findWords(board, words):
    # Build the trie with all words
    trie = {}
    for word in words:
        node = trie
        for c in word:
            node = node.setdefault(c, {})
        node['#'] = word  # Mark the end of word
        
    rows, cols = len(board), len(board[0])
    result = []
    
    def dfs(r, c, node):
        char = board[r][c]
        
        # Char is not in current trie
        if char not in node:
            return
            
        node = node[char]
        
        # Found a complete word
        if '#' in node:
            result.append(node['#'])
            del node['#']  # Avoid duplicates
            
        # Mark as visited
        board[r][c] = '*'
        
        # Explore in all directions
        for dr, dc in [(0, 1), (1, 0), (0, -1), (-1, 0)]:
            nr, nc = r + dr, c + dc
            if 0 <= nr < rows and 0 <= nc < cols and board[nr][nc] != '*':
                dfs(nr, nc, node)
                
        # Restore the character
        board[r][c] = char
        
        # Cleanup - remove nodes without children to save space
        if not node:
            del node[char]
    
    # Start DFS from each cell
    for r in range(rows):
        for c in range(cols):
            dfs(r, c, trie)
            
    return result
```

## **Union Find (Disjoint Set)**

Union Find is a specialized structure for tracking disjoint sets of elements. The main operations are:

- **Find**: Determines which set an element belongs to
- **Union**: Unites two sets

### **Efficient Implementation**

```python
class UnionFind:
    def __init__(self, n):
        self.parent = list(range(n))
        self.rank = [0] * n
        self.count = n  # Number of components
        
    def find(self, x):
        if self.parent[x] != x:
            self.parent[x] = self.find(self.parent[x])  # Path compression
        return self.parent[x]
        
    def union(self, x, y):
        root_x = self.find(x)
        root_y = self.find(y)
        
        if root_x == root_y:
            return
            
        # Union by rank
        if self.rank[root_x] < self.rank[root_y]:
            self.parent[root_x] = root_y
        elif self.rank[root_x] > self.rank[root_y]:
            self.parent[root_y] = root_x
        else:
            self.parent[root_y] = root_x
            self.rank[root_x] += 1
            
        self.count -= 1  # Decrement the component count
```

### **Classic Applications**

- **Detecting cycles in undirected graphs**
- **Finding connected components**
- **Kruskal's Algorithm for MST**
- **Dynamic connectivity problems**

### **Example: Number of Connected Components (LeetCode #323)**

```python
def countComponents(n, edges):
    uf = UnionFind(n)
    
    for x, y in edges:
        uf.union(x, y)
        
    return uf.count
```

### **Example: Redundant Connection (LeetCode #684)**

```python
def findRedundantConnection(edges):
    n = len(edges)
    uf = UnionFind(n + 1)  # Nodes are 1-indexed
    
    for u, v in edges:
        if uf.find(u) == uf.find(v):
            return [u, v]  # This edge forms a cycle
        uf.union(u, v)
        
    return []
```

## **Segment Tree**

Segment Tree is a tree structure used for efficient range queries (sum, minimum, maximum, etc.) and updates:

### **Implementation for Range Sum Query**

```python
class SegmentTree:
    def __init__(self, nums):
        self.n = len(nums)
        # The size of the tree is approximately 4 * n
        self.tree = [0] * (4 * self.n)
        if self.n > 0:
            self._build(nums, 0, 0, self.n - 1)
    
    def _build(self, nums, node, start, end):
        if start == end:
            self.tree[node] = nums[start]
        else:
            mid = (start + end) // 2
            left = 2 * node + 1
            right = 2 * node + 2
            
            self._build(nums, left, start, mid)
            self._build(nums, right, mid + 1, end)
            
            self.tree[node] = self.tree[left] + self.tree[right]
    
    def update(self, index, val):
        self._update(0, 0, self.n - 1, index, val)
    
    def _update(self, node, start, end, index, val):
        if start == end:
            self.tree[node] = val
        else:
            mid = (start + end) // 2
            left = 2 * node + 1
            right = 2 * node + 2
            
            if start <= index <= mid:
                self._update(left, start, mid, index, val)
            else:
                self._update(right, mid + 1, end, index, val)
                
            self.tree[node] = self.tree[left] + self.tree[right]
    
    def query(self, left, right):
        return self._query(0, 0, self.n - 1, left, right)
    
    def _query(self, node, start, end, left, right):
        if right < start or end < left:
            return 0  # Out of range
            
        if left <= start and end <= right:
            return self.tree[node]  # Completely within range
            
        # Partially overlapping interval
        mid = (start + end) // 2
        left_sum = self._query(2 * node + 1, start, mid, left, right)
        right_sum = self._query(2 * node + 2, mid + 1, end, left, right)
        
        return left_sum + right_sum
```

### **Classic Applications**

- **Range Sum Query**
- **Range Minimum/Maximum Query**
- **Finding the element at a specific position**
- **Range update and query problems**

### **Example: Range Sum Query - Mutable (LeetCode #307)**

The implementation above is essentially the solution for this problem.

## **Other Important Structures**

### **1. Binary Indexed Tree (Fenwick Tree)**

A simpler alternative to Segment Tree for prefix sums:

```python
class BIT:
    def __init__(self, n):
        self.n = n
        self.tree = [0] * (n + 1)
    
    def update(self, i, val):
        while i <= self.n:
            self.tree[i] += val
            i += i & -i  # Next index to update
    
    def query(self, i):
        sum = 0
        while i > 0:
            sum += self.tree[i]
            i -= i & -i  # Next index to query
        return sum
```

### **2. LRU Cache (Least Recently Used)**

Using HashMap + Doubly Linked List for O(1) operations:

```python
class LRUCache:
    class Node:
        def __init__(self, key=0, val=0):
            self.key = key
            self.val = val
            self.prev = None
            self.next = None
    
    def __init__(self, capacity):
        self.capacity = capacity
        self.cache = {}  # key -> Node
        
        # Dummy head and tail
        self.head = self.Node()
        self.tail = self.Node()
        self.head.next = self.tail
        self.tail.prev = self.head
    
    def get(self, key):
        if key not in self.cache:
            return -1
        
        # Move to front
        node = self.cache[key]
        self._remove(node)
        self._add(node)
        
        return node.val
    
    def put(self, key, value):
        # Remove existing node, if any
        if key in self.cache:
            self._remove(self.cache[key])
        
        # Create new node
        node = self.Node(key, value)
        self._add(node)
        self.cache[key] = node
        
        # Remove LRU if exceeding capacity
        if len(self.cache) > self.capacity:
            lru = self.tail.prev
            self._remove(lru)
            del self.cache[lru.key]
    
    def _add(self, node):
        # Add after head
        node.prev = self.head
        node.next = self.head.next
        self.head.next.prev = node
        self.head.next = node
    
    def _remove(self, node):
        # Remove a node from the list
        node.prev.next = node.next
        node.next.prev = node.prev
```

## **Popular Problems on LeetCode**

| **Name** | **ID** | **Structure** | **Difficulty** |
|----------|--------|---------------|-----------------|
| Implement Trie | #208 | Trie | Medium |
| Word Search II | #212 | Trie + DFS | Hard |
| Number of Islands II | #305 | Union Find | Hard |
| Redundant Connection | #684 | Union Find | Medium |
| Range Sum Query - Mutable | #307 | Segment Tree | Medium |
| LRU Cache | #146 | HashMap + DLL | Medium |
| Design Add and Search Words Data Structure | #211 | Trie | Medium |
| Accounts Merge | #721 | Union Find | Medium |

## **Ninja Tips for Advanced Structures**

- **Trie**: Use when the problem involves prefixes, strings, or word searches.
- **Union Find**: Ideal for problems of dynamic connectivity or components.
- **Segment Tree**: Perfect for range queries and updates.
- **Many "Design" problems** on LeetCode require advanced structures.
- Optimizing these structures (path compression in Union Find, lazy propagation in Segment Tree) can be crucial.

## **Thinking Out Loud: Design Add and Search Words**

*Problem*: Implement a data structure that supports adding words and searching with wildcards ('.' represents any letter).

*Insights*:
1. We'll use a Trie to efficiently store words
2. For search, when we encounter a '.', we need to explore all possibilities
3. We can use recursive DFS for wildcard search

```python
class WordDictionary:
    def __init__(self):
        self.trie = {}
        
    def addWord(self, word):
        node = self.trie
        for c in word:
            node = node.setdefault(c, {})
        node['] = True  # Mark end of word
        
    def search(self, word):
        def dfs(node, i):
            if i == len(word):
                return ' in node
                
            if word[i] == '.':
                return any(dfs(node[c], i+1) for c in node if c != ')
            
            if word[i] in node:
                return dfs(node[word[i]], i+1)
                
            return False
            
        return dfs(self.trie, 0)
```

## **Checklist Advanced Structures**

- [ ] I understand the basic implementation of Trie
- [ ] I know when to use Union Find and how to implement it efficiently
- [ ] I understand how Segment Tree works for range queries
- [ ] I've applied at least 2 of these structures in complex problems
- [ ] I know the optimizations for each structure

## **Mini Challenge**

**Problem:** Given a set of strings, group the anagrams.

**Example:** 
Input: ["eat", "tea", "tan", "ate", "nat", "bat"]
Output: [["eat","tea","ate"], ["tan","nat"], ["bat"]]

**Solution**:
1. Use a HashMap to group anagrams (key = sorted characters)
2. For optimization, consider using a Trie where each level stores characters in alphabetical order

---

# **12-Week Study Plan: From Foundation to Mastery**

This study plan is designed to take you from basic proficiency to complete mastery, using spaced repetition and progressive practice to maximize retention and skill transfer.

## **Week 1: Fundamentals and Arrays**

**Focus**: Arrays, Sliding Window, Two Pointers

**Day 1-2: Basic Arrays**
- Easy: Two Sum (#1), Best Time to Buy and Sell Stock (#121)
- Medium: Container With Most Water (#11)

**Day 3-4: Sliding Window**
- Easy: Maximum Subarray (#53)
- Medium: Longest Substring Without Repeating Characters (#3)

**Day 5-6: Two Pointers**
- Easy: Valid Palindrome (#125)
- Medium: 3Sum (#15)

**Day 7: Review + Challenge**
- Hard: Trapping Rain Water (#42)
- Review: Solve again the two problems you found most difficult

## **Week 2: Hash Maps and Prefix Sum**

**Focus**: Hash Maps, Prefix Sum, Difference Arrays

**Day 1-2: Basic Hash Maps**
- Easy: Contains Duplicate (#217), Valid Anagram (#242)
- Medium: Group Anagrams (#49)

**Day 3-4: Advanced Hash Maps**
- Medium: Subarray Sum Equals K (#560)
- Medium: Longest Consecutive Sequence (#128)

**Day 5-6: Prefix Sum**
- Easy: Range Sum Query - Immutable (#303)
- Medium: Product of Array Except Self (#238)

**Day 7: Review + Challenge**
- Hard: First Missing Positive (#41)
- Spaced Review: Difficult problems from week 1

## **Week 3: Binary Search**

**Focus**: Binary Search in Arrays and Answer Space

**Day 1-2: Basic Binary Search**
- Easy: Binary Search (#704), First Bad Version (#278)
- Medium: Search in Rotated Sorted Array (#33)

**Day 3-4: Binary Search on Answer**
- Medium: Koko Eating Bananas (#875)
- Medium: Split Array Largest Sum (#410)

**Day 5-6: Advanced Binary Search**
- Medium: Find First and Last Position (#34)
- Medium: Find Peak Element (#162)

**Day 7: Review + Challenge**
- Hard: Median of Two Sorted Arrays (#4)
- Spaced Review: Difficult problems from weeks 1-2

## **Week 4: DFS and Backtracking I**

**Focus**: Tree Traversal, Basic Backtracking

**Day 1-2: DFS in Trees**
- Easy: Maximum Depth of Binary Tree (#104)
- Medium: Binary Tree Inorder Traversal (#94)

**Day 3-4: DFS in Matrices**
- Medium: Number of Islands (#200)
- Medium: Word Search (#79)

**Day 5-6: Basic Backtracking**
- Medium: Permutations (#46)
- Medium: Subsets (#78)

**Day 7: Review + Challenge**
- Hard: Word Search II (#212)
- Spaced Review: Problems from weeks 1-3 according to plan

## **Week 5: BFS and Graphs**

**Focus**: BFS, Graphs, Shortest Path

**Day 1-2: BFS in Trees**
- Easy: Binary Tree Level Order Traversal (#102)
- Medium: Binary Tree Zigzag Level Order Traversal (#103)

**Day 3-4: BFS in Matrices**
- Medium: Rotting Oranges (#994)
- Medium: 01 Matrix (#542)

**Day 5-6: Graphs**
- Medium: Course Schedule (#207)
- Medium: Number of Connected Components in an Undirected Graph (#323)

**Day 7: Review + Challenge**
- Hard: Word Ladder (#127)
- Spaced Review: Difficult problems from weeks 1-4

## **Week 6: Dynamic Programming I**

**Focus**: DP on Sequences, Tabulation

**Day 1-2: Sequential DP**
- Easy: Climbing Stairs (#70)
- Medium: House Robber (#198)

**Day 3-4: 2D DP**
- Medium: Unique Paths (#62)
- Medium: Minimum Path Sum (#64)

**Day 5-6: DP on Strings**
- Medium: Longest Palindromic Substring (#5)
- Medium: Decode Ways (#91)

**Day 7: Review + Challenge**
- Hard: Regular Expression Matching (#10)
- Spaced Review: Most difficult problems from weeks 1-5

## **Week 7: Dynamic Programming II**

**Focus**: Advanced DP, Memoization

**Day 1-2: Knapsack Problems**
- Medium: Coin Change (#322)
- Medium: Partition Equal Subset Sum (#416)

**Day 3-4: DP on Strings**
- Medium: Longest Increasing Subsequence (#300)
- Medium: Longest Common Subsequence (#1143)

**Day 5-6: DP with Optimization**
- Hard: Edit Distance (#72)
- Medium: Jump Game (#55)

**Day 7: Review + Challenge**
- Hard: Burst Balloons (#312)
- Spaced Review: Most difficult problems from weeks 1-6

## **Week 8: Greedy Algorithms**

**Focus**: Greedy, Intervals, Sorting

**Day 1-2: Basic Greedy**
- Medium: Jump Game (#55)
- Medium: Task Scheduler (#621)

**Day 3-4: Intervals**
- Medium: Merge Intervals (#56)
- Medium: Non-overlapping Intervals (#435)

**Day 5-6: Advanced Greedy**
- Medium: Gas Station (#134)
- Medium: Partition Labels (#763)

**Day 7: Review + Challenge**
- Hard: Employee Free Time (#759)
- Mega Review: Reconstruct solutions for difficult problems from weeks 1-7

## **Week 9: Advanced Structures I**

**Focus**: Trie, Union Find

**Day 1-2: Basic Trie**
- Medium: Implement Trie (#208)
- Medium: Design Add and Search Words Data Structure (#211)

**Day 3-4: Advanced Trie**
- Hard: Word Search II (#212)
- Hard: Palindrome Pairs (#336)

**Day 5-6: Union Find**
- Medium: Redundant Connection (#684)
- Medium: Accounts Merge (#721)

**Day 7: Review + Challenge**
- Hard: Swim in Rising Water (#778)
- Spaced Review: Problems from weeks 5-8

## **Week 10: Advanced Structures II**

**Focus**: Segment Tree, Binary Indexed Tree, Design

**Day 1-2: Range Queries**
- Medium: Range Sum Query - Mutable (#307)
- Hard: Count of Smaller Numbers After Self (#315)

**Day 3-4: LRU/LFU**
- Medium: LRU Cache (#146)
- Hard: LFU Cache (#460)

**Day 5-6: Design Problems**
- Medium: Design Twitter (#355)
- Medium: Design Snake Game (#353)

**Day 7: Review + Challenge**
- Hard: Sliding Window Maximum (#239)
- Spaced Review: Problems from weeks 5-9

## **Week 11: Simulation and Interview Problems**

**Focus**: Mock Interviews, Implementation Problems

**Day 1-2: Interview Simulation 1**
- Diverse set: 1 Easy + 2 Medium

**Day 3-4: Interview Simulation 2**
- Diverse set: 1 Medium + 1 Hard

**Day 5-6: Interview Simulation 3**
- Focus on identified weak points

**Day 7: Review + Challenge**
- Hard: Merge k Sorted Lists (#23)
- Spaced Review: Repeat problems you still struggle with

## **Week 12: Consolidation and Final Strategy**

**Focus**: Pattern Review, Verbalization Practice

**Day 1-2: Meta Top-20**
- Medium/Hard: Review of most common patterns in Big Tech

**Day 3-4: Amazon Top-20**
- Medium/Hard: Emphasis on design problems and scalability

**Day 5-6: Google Top-20**
- Medium/Hard: Focus on complex algorithmic problems

**Day 7: Final Review**
- Review of key patterns and solutions
- Final mock interview
- Post-guide personalized plan

## **Study Methodology**

### **For Each New Problem:**

1. **Try to solve in 25-40 minutes** without looking at the solution
2. If stuck, review only the hints (not the complete solution)
3. Try 15 more minutes
4. If still unsuccessful, study the solution and understand completely
5. **Wait 24 hours and solve the problem from scratch**
6. **Add to your spaced repetition system**

### **Spaced Repetition:**

- 1st review: 24 hours later
- 2nd review: 3 days later
- 3rd review: 7 days later
- 4th review: 14 days later
- 5th review: 30 days later

Use a system like Anki or the tracking spreadsheet below to schedule your reviews.

### **Measuring Progress:**

1. **Time to recognize the pattern**: should decrease with practice
2. **Time to implement**: should stabilize around 20-25 minutes for medium problems
3. **First-try success rate**: should gradually increase

### **Tracking Spreadsheet:**

| ID | Problem | Pattern | Difficulty | Initial Date | Rev1 | Rev2 | Rev3 | Rev4 | Mastery |
|----|----------|--------|-------------|--------------|------|------|------|------|---------|
| 1  | Two Sum  | Hash   | Easy        | 01/05        | 02/05| 04/05| 08/05| 15/05| ⭐⭐⭐   |
|... |          |        |             |              |      |      |      |      |         |

---

# **150 Essential Problems: The Map to Mastery**

These 150 problems form a complete map for mastering algorithms and data structures, covering all important patterns with strategic repetition to reinforce learning.

## **Arrays and Strings (25 problems)**

### **Sliding Window**
1. Maximum Subarray (#53) - Easy
2. Best Time to Buy and Sell Stock (#121) - Easy
3. Longest Substring Without Repeating Characters (#3) - Medium
4. Minimum Size Subarray Sum (#209) - Medium
5. Longest Repeating Character Replacement (#424) - Medium
6. Sliding Window Maximum (#239) - Hard

### **Two Pointers**
7. Valid Palindrome (#125) - Easy
8. Two Sum II - Input array is sorted (#167) - Easy
9. Container With Most Water (#11) - Medium
10. 3Sum (#15) - Medium
11. 3Sum Closest (#16) - Medium
12. Trapping Rain Water (#42) - Hard

### **Basic Arrays**
13. Two Sum (#1) - Easy
14. Best Time to Buy and Sell Stock II (#122) - Easy
15. Product of Array Except Self (#238) - Medium
16. Find the Duplicate Number (#287) - Medium
17. First Missing Positive (#41) - Hard

### **Strings**
18. Valid Anagram (#242) - Easy
19. Valid Parentheses (#20) - Easy
20. Longest Palindromic Substring (#5) - Medium
21. Group Anagrams (#49) - Medium
22. Encode and Decode Strings (#271) - Medium
23. Minimum Window Substring (#76) - Hard
24. Basic Calculator (#224) - Hard
25. Palindrome Pairs (#336) - Hard

## **Hash Maps and Sets (15 problems)**

26. Contains Duplicate (#217) - Easy
27. Valid Anagram (#242) - Easy
28. Group Anagrams (#49) - Medium
29. Top K Frequent Elements (#347) - Medium
30. Subarray Sum Equals K (#560) - Medium
31. Longest Consecutive Sequence (#128) - Medium
32. LRU Cache (#146) - Medium
33. Insert Delete GetRandom O(1) (#380) - Medium
34. Copy List with Random Pointer (#138) - Medium
35. Longest Substring with At Most K Distinct Characters (#340) - Medium
36. Longest Substring with At Most Two Distinct Characters (#159) - Medium
37. Find All Anagrams in a String (#438) - Medium
38. Design Twitter (#355) - Medium
39. Random Pick with Weight (#528) - Medium
40. Sudoku Solver (#37) - Hard

## **Binary Search (15 problems)**

41. Binary Search (#704) - Easy
42. First Bad Version (#278) - Easy
43. Search Insert Position (#35) - Easy
44. Search in Rotated Sorted Array (#33) - Medium
45. Find First and Last Position of Element in Sorted Array (#34) - Medium
46. Find Peak Element (#162) - Medium
47. Search a 2D Matrix (#74) - Medium
48. Koko Eating Bananas (#875) - Medium
49. Find Minimum in Rotated Sorted Array (#153) - Medium
50. Search in Rotated Sorted Array II (#81) - Medium
51. Time Based Key-Value Store (#981) - Medium
52. Split Array Largest Sum (#410) - Hard
53. Find in Mountain Array (#1095) - Hard
54. Median of Two Sorted Arrays (#4) - Hard
55. Capacity To Ship Packages Within D Days (#1011) - Medium

## **Trees and Graphs (30 problems)**

### **Tree Traversal**
56. Maximum Depth of Binary Tree (#104) - Easy
57. Same Tree (#100) - Easy
58. Invert Binary Tree (#226) - Easy
59. Binary Tree Level Order Traversal (#102) - Medium
60. Binary Tree Zigzag Level Order Traversal (#103) - Medium
61. Construct Binary Tree from Preorder and Inorder Traversal (#105) - Medium
62. Validate Binary Search Tree (#98) - Medium
63. Kth Smallest Element in a BST (#230) - Medium
64. Lowest Common Ancestor of a Binary Tree (#236) - Medium
65. Binary Tree Maximum Path Sum (#124) - Hard

### **Graph Traversal**
66. Number of Islands (#200) - Medium
67. Clone Graph (#133) - Medium
68. Pacific Atlantic Water Flow (#417) - Medium
69. Course Schedule (#207) - Medium
70. Course Schedule II (#210) - Medium
71. Graph Valid Tree (#261) - Medium
72. Number of Connected Components in an Undirected Graph (#323) - Medium
73. Word Ladder (#127) - Hard
74. Alien Dictionary (#269) - Hard
75. Shortest Distance from All Buildings (#317) - Hard

### **Matrix DFS/BFS**
76. Flood Fill (#733) - Easy
77. Word Search (#79) - Medium
78. Rotting Oranges (#994) - Medium
79. Walls and Gates (#286) - Medium
80. 01 Matrix (#542) - Medium
81. Shortest Bridge (#934) - Medium
82. Word Search II (#212) - Hard
83. Making A Large Island (#827) - Hard
84. Serialize and Deserialize Binary Tree (#297) - Hard
85. Swim in Rising Water (#778) - Hard

## **Backtracking (15 problems)**

86. Letter Combinations of a Phone Number (#17) - Medium
87. Permutations (#46) - Medium
88. Permutations II (#47) - Medium
89. Subsets (#78) - Medium
90. Subsets II (#90) - Medium
91. Combination Sum (#39) - Medium
92. Combination Sum II (#40) - Medium
93. Combination Sum III (#216) - Medium
94. Generate Parentheses (#22) - Medium
95. Palindrome Partitioning (#131) - Medium
96. Word Break (#139) - Medium
97. Restore IP Addresses (#93) - Medium
98. N-Queens (#51) - Hard
99. Sudoku Solver (#37) - Hard
100. Word Break II (#140) - Hard

## **Dynamic Programming (25 problems)**

### **1D Dynamic Programming**
101. Climbing Stairs (#70) - Easy
102. House Robber (#198) - Medium
103. House Robber II (#213) - Medium
104. Longest Increasing Subsequence (#300) - Medium
105. Decode Ways (#91) - Medium
106. Coin Change (#322) - Medium
107. Maximum Product Subarray (#152) - Medium
108. Word Break (#139) - Medium
109. Jump Game (#55) - Medium
110. Palindromic Substrings (#647) - Medium

### **2D Dynamic Programming**
111. Unique Paths (#62) - Medium
112. Unique Paths II (#63) - Medium
113. Minimum Path Sum (#64) - Medium
114. Longest Common Subsequence (#1143) - Medium
115. Longest Palindromic Subsequence (#516) - Medium
116. Interleaving String (#97) - Medium
117. Edit Distance (#72) - Hard
118. Regular Expression Matching (#10) - Hard
119. Maximal Rectangle (#85) - Hard
120. Burst Balloons (#312) - Hard

### **Advanced DP**
121. Best Time to Buy and Sell Stock with Cooldown (#309) - Medium
122. Partition Equal Subset Sum (#416) - Medium
123. Target Sum (#494) - Medium
124. Ones and Zeroes (#474) - Medium
125. Frog Jump (#403) - Hard

## **Greedy Algorithms (10 problems)**

126. Jump Game (#55) - Medium
127. Jump Game II (#45) - Medium
128. Gas Station (#134) - Medium
129. Task Scheduler (#621) - Medium
130. Meeting Rooms II (#253) - Medium
131. Non-overlapping Intervals (#435) - Medium
132. Merge Intervals (#56) - Medium
133. Insert Interval (#57) - Medium
134. Partition Labels (#763) - Medium
135. Queue Reconstruction by Height (#406) - Medium

## **Advanced Structures (15 problems)**

### **Trie**
136. Implement Trie (Prefix Tree) (#208) - Medium
137. Design Add and Search Words Data Structure (#211) - Medium
138. Word Search II (#212) - Hard
139. Palindrome Pairs (#336) - Hard
140. Design Search Autocomplete System (#642) - Hard

### **Union Find**
141. Number of Islands (#200) - Medium
142. Graph Valid Tree (#261) - Medium
143. Redundant Connection (#684) - Medium
144. Accounts Merge (#721) - Medium
145. Smallest String With Swaps (#1202) - Medium

### **Segment Tree / Binary Indexed Tree**
146. Range Sum Query - Mutable (#307) - Medium
147. Count of Smaller Numbers After Self (#315) - Hard
148. Sliding Window Maximum (#239) - Hard
149. The Skyline Problem (#218) - Hard
150. Count of Range Sum (#327) - Hard

---

# **Problem-Solving Framework: From Reading to Optimized Solution**

## **The 7-Step Process for Any Problem**

Below is a detailed framework for systematically and efficiently solving any algorithmic problem:

### **1. Problem Understanding (2 minutes)**

✅ **Read the statement carefully**
- Identify inputs and expected outputs
- Note constraints and special cases
- Examine the provided examples

✅ **Ask clarifying questions**
- What happens with empty inputs?
- Are there assumptions about the input format?
- What behavior is expected in edge cases?

✅ **Restate the problem**
- Reformulate the problem in your own words
- Verify your understanding is correct

### **2. Example Analysis (1 minute)**

✅ **Work through the provided examples**
- Trace the process manually
- Identify patterns or insights

✅ **Create your own examples**
- Add edge cases
- Try to identify cases that violate your assumptions

✅ **Find counter-examples**
- If you have an approach in mind, try to break it

### **3. Pattern Identification (2 minutes)**

✅ **Categorize the problem**
- What category does this problem fall into?
- What techniques are commonly used for this type of problem?

✅ **Ask yourself:**
- Does this problem involve searching, sorting, or counting?
- Is there a natural data structure for this?
- Is there optimal substructure (DP) or greedy choices?

✅ **Use the Technique Decision Tree**
- If it's overlapping subproblems → Dynamic Programming
- If it's contiguous subsequence → Sliding Window
- If it's sorted array → Binary Search or Two Pointers
- If it's counting/frequency → Hash Map
- If it's graph/matrix → DFS/BFS

### **4. Approach Brainstorming (3 minutes)**

✅ **Start with Brute Force**
- Always have a basic solution, even if inefficient
- Analyze the complexity of brute force

✅ **Refine with Specific Techniques**
- Apply the pattern identified in step 3
- Think of incremental optimizations

✅ **Compare Multiple Solutions**
- List pros and cons of each approach
- Complexity analysis (time and space)

### **5. Solution Planning (2 minutes)**

✅ **Define the Main Steps**
- Outline the algorithm at a high level
- Identify helper functions or subroutines

✅ **Identify Variables and Structures**
- What data structures will you need?
- What variables will track the state?

✅ **Plan in Pseudocode**
- Write pseudocode before implementing

### **6. Implementation (15 minutes)**

✅ **Code Methodically**
- Follow your pseudocode
- Keep comments for complex sections

✅ **Attention to Details**
- Watch for index issues (off-by-one errors)
- Initialize correctly
- Check array bounds

✅ **Readable Code**
- Use meaningful variable names
- Break into functions when appropriate

### **7. Verification and Optimization (5 minutes)**

✅ **Test with Examples**
- Follow the code with initial examples
- Check edge cases

✅ **Find Bugs**
- Look for common errors: off-by-one, null checks, infinite loops

✅ **Final Optimizations**
- Are there space optimizations?
- Refactor for clarity
- Discuss trade-offs

## **Technique Decision Tree**

Use this flowchart to quickly identify the most suitable technique for a problem:

```
Algorithmic problem
├── Is it about contiguous subsets of array/string?
│   └── Yes → Sliding Window
├── Is array sorted or almost sorted?
│   └── Yes → Binary Search or Two Pointers
├── Does it involve counting or frequency of elements?
│   └── Yes → Hash Map
├── Need to process ranges or intervals?
│   └── Yes → Prefix Sum or Difference Array
├── Has multiple overlapping subproblems?
│   └── Yes → Dynamic Programming
├── Is it about exploring all possible combinations?
│   └── Yes → Backtracking
├── Involves graphs or a 2D matrix?
│   └── Yes
│       ├── Need shortest path? → BFS
│       ├── Need to explore everything? → DFS
│       ├── Detect cycles? → Topological Sort
├── Need to select incrementally? 
│   └── Yes → Greedy
├── About strings and prefixes?
│   └── Yes → Trie
├── About connected components?
│   └── Yes → Union Find
└── About queries and updates in ranges?
    └── Yes → Segment Tree
```

## **Communication Tips During Problem Solving**

During an interview, communicating your thinking is as important as solving the problem:

### **1. Thinking Out Loud**

- **Verbalize your reasoning**: "I see that this problem involves substrings, so sliding window might be useful..."
- **Share intuitions**: "Pre-sorting would allow us to use binary search..."
- **Explain trade-offs**: "The hash map solution uses more memory but is O(n) vs. O(n²)..."

### **2. Communicating Complexity**

- **Be precise**: "The time complexity is O(n log n) due to the initial sorting..."
- **Explain bottlenecks**: "The bottleneck is in the nested loop, which gives us O(n²)..."
- **Mention optimizations**: "We can reduce to O(n) using a single pass with a hash map..."

### **3. Communicating Design Decisions**

- **Justify choices**: "I chose HashMap because we need O(1) lookups..."
- **Explain alternatives**: "We could use DFS, but BFS is more appropriate for finding the shortest path..."
- **Acknowledge limitations**: "This solution works well for small inputs, but for large datasets..."

## **Final Verification Checklist**

Before considering your solution finalized, check:

- [ ] Does your solution work for all provided examples?
- [ ] Have you tested edge cases (empty, single, extremes)?
- [ ] Is the time and space complexity optimal?
- [ ] Is your code free of common bugs (off-by-one, nulls, overflow)?
- [ ] Could you explain your solution to a non-technical person?

## **Example Problem Analysis**

### **Example 1: Maximum Subarray (Kadane's Algorithm)**

**Problem:** Find the contiguous subarray with the largest sum.

**7-step thought process:**

1. **Understanding:** We need the sum of consecutive elements in an array with maximum value.
2. **Examples:** [-2,1,-3,4,-1,2,1,-5,4] → Output: 6 (subarray [4,-1,2,1])
3. **Patterns:** It's a contiguous subsequence problem → Kadane's Algorithm (DP variation)
4. **Approaches:**
   - Brute force: Check all subarrays O(n²)
   - Kadane's: Keep current and maximum sum O(n)
5. **Planning:**
   - Initialize current_sum and max_sum with first element
   - For each element, decide whether to start new subarray or continue
6. **Implementation:**
   ```python
   def maxSubArray(nums):
       current_sum = max_sum = nums[0]
       for num in nums[1:]:
           current_sum = max(num, current_sum + num)
           max_sum = max(max_sum, current_sum)
       return max_sum
   ```
7. **Verification:** 
   - Time complexity: O(n)
   - Space complexity: O(1)
   - Tested with examples and edge cases

### **Example 2: 3Sum**

**Problem:** Find all unique triplets that sum to zero.

**7-step thought process:**

1. **Understanding:** We need to find all combinations i,j,k where nums[i] + nums[j] + nums[k] = 0.
2. **Examples:** [-1,0,1,2,-1,-4] → Output: [[-1,-1,2],[-1,0,1]]
3. **Patterns:** Sum problem in array → Two Pointers after sorting
4. **Approaches:**
   - Brute force: Three nested loops O(n³)
   - Two pointers: Fix one element and use two pointers on the rest O(n²)
5. **Planning:**
   - Sort array
   - For each element, use two pointers on remaining elements
   - Skip duplicates to avoid repeat results
6. **Implementation:**
   ```python
   def threeSum(nums):
       nums.sort()
       result = []
       
       for i in range(len(nums)-2):
           if i > 0 and nums[i] == nums[i-1]:
               continue
               
           left, right = i+1, len(nums)-1
           
           while left < right:
               s = nums[i] + nums[left] + nums[right]
               
               if s < 0:
                   left += 1
               elif s > 0:
                   right -= 1
               else:
                   result.append([nums[i], nums[left], nums[right]])
                   
                   while left < right and nums[left] == nums[left+1]:
                       left += 1
                   while left < right and nums[right] == nums[right-1]:
                       right -= 1
                       
                   left += 1
                   right -= 1
                   
       return result
   ```
7. **Verification:**
   - Time complexity: O(n²)
   - Space complexity: O(1) excluding output
   - Careful with duplicates
   - Test with arrays of different sizes

---

# **Interview Preparation: Simulation, Communication, and Performance**

## **Beyond Algorithms: Mastering the Interview**

Solving algorithmic problems is just part of the equation. To succeed in technical interviews, you need to:

1. **Communicate your thinking clearly**
2. **Manage time efficiently**
3. **Handle pressure and hints**
4. **Demonstrate collaboration and receptiveness**

## **Communication Script for Problems**

Use this script to communicate your problem-solving process clearly and structurally:

### **1. Repeat and Clarify (30 seconds)**

"So, the problem asks to find [objective]. The inputs are [input] and the expected output is [output]. Some edge cases to consider would be [empty/extreme cases]. Is that correct?"

### **2. Brute Force Approach (30 seconds)**

"Let's start with a brute force approach. We could [describe brute force] which would have time complexity O(X) and space O(Y). Let's see if we can improve this."

### **3. Optimization and Insights (1 minute)**

"I notice that [insight about the problem]. This suggests we can use [technique/data structure]. The main idea is [explain the key idea]."

### **4. Solution Planning (1 minute)**

"I'll approach this as follows:
1. First, I'll [first step]
2. Then, [second step]
3. Finally, [final step]

The time complexity would be O(X) and space O(Y)."

### **5. During Implementation**

"I'm implementing [specific part]. Here I need to be careful with [edge case/important detail]."

"I'll use [data structure] because [reason]."

### **6. Testing and Debugging**

"Let's test with the example: [trace the example]"

"Hmm, I found an issue in [X]. I'll fix this [explanation of the fix]."

### **7. Final Analysis**

"The solution has time complexity O(X) due to [reason] and space O(Y) because [explanation]. One trade-off is [mention some trade-off]."

## **45-Minute Interview Simulation**

| Time | Activity | Tips |
|-------|-----------|-------|
| 0-5 min | Problem clarification | Ask questions, note constraints |
| 5-10 min | Brainstorming and approach | Discuss multiple ideas, analyze complexity |
| 10-25 min | Implementation | Think aloud, structure your code |
| 25-35 min | Testing and debugging | Test meticulously, start with simple examples |
| 35-40 min | Optimization and discussion | Discuss possible improvements |
| 40-45 min | Questions and follow-ups | Ask about extensions to the problem |

## **Strategies for Handling Blocks**

When you get stuck during an interview, use these techniques:

### **1. Go Back to Basics**

"Let's review the requirements again and ensure I understood correctly."

### **2. Examine Examples Again**

"Let me work with a simple example to see if I can identify any pattern."

### **3. Think Aloud**

"I'm considering using [technique], but I'm concerned about [potential problem]."

### **4. Systematic Approach**

"Let's try to categorize this problem. It seems like a [category] problem, which typically can be solved with [technique]."

### **5. Ask for Hints Intelligently**

"I'm thinking of two directions: [option A] or [option B]. Do you have any suggestion about which might be more promising?"

## **Reading Feedback During the Interview**

### **Positive Signals:**
- The interviewer asks about optimizations
- Asks you to implement a more efficient solution
- Asks related follow-up questions
- Asks you to explain the complexity

### **Warning Signals:**
- Questions directed toward a specific technique
- Repeated suggestions about the same thing
- Questions if you know a specific data structure
- Hints about how to simplify the problem

## **Simulating Real Interviews**

To maximize your preparation:

1. **Use mock interview platforms**:
   - Pramp, interviewing.io, LeetCode Mock
   - Ask friends to interview you

2. **Record your practice sessions**:
   - Review your behavior and communication
   - Identify problem patterns

3. **Simulate pressure environments**:
   - Practice with timer
   - Switch between different problem types

4. **Structured feedback**:
   - Ask for specific feedback on communication
   - Evaluate both the solution and the process

## **Pre-Interview Checklist**

- [ ] Reviewed the main patterns (Sliding Window, DP, Graphs, etc.)
- [ ] Practiced problems from the target company
- [ ] Did at least 5 mock interviews
- [ ] Have prepared answers for common blocks
- [ ] Tested my environment (if remote interview)
- [ ] Have paper/whiteboard for diagrams (if needed)
- [ ] Reviewed my own code for difficult problems
- [ ] Prepared 2-3 questions for the interviewer

## **Company-Specific Preparation**

### **Google**
- Focus: Pure algorithms, code efficiency
- Particularities: Original problems, multiple solutions
- Tip: Practice edge cases exhaustively

### **Meta (Facebook)**
- Focus: Arrays, strings, graphs
- Particularities: Practical problems, scalability
- Tip: Communicate clearly, value optimizations

### **Amazon**
- Focus: Object-oriented design, practical problems
- Particularities: Questions based on their leadership principles
- Tip: Relate problems to real-world scenarios

### **Microsoft**
- Focus: Arrays, trees, design
- Particularities: Incremental problems, collaborative discussion
- Tip: Demonstrate thought process and collaboration

## **Final Words**

Remember that the goal of technical interviews isn't just to verify if you know algorithms, but also:

1. **How you think** and approach problems
2. **How you communicate** and collaborate
3. **How you handle feedback** and pressure
4. **If you would be a good team** member

Consistent practice with this guide's framework will develop not only your technical skills but also your confidence and ability to showcase your best during interviews.

**Good luck on your LeetCode mastery journey!**