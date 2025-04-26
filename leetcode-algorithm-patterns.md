# **Algorithm Patterns: The Key to LeetCode Mastery**

## **Introduction**

The difference between solving LeetCode problems randomly versus strategically understanding patterns is like the difference between memorizing phrases in a foreign language versus learning its grammar and structure. One approach leads to short-term success with specific problems, while the other builds a foundation for solving entire classes of problems.

This guide breaks down the most important algorithmic patterns that appear in coding interviews. For each pattern, we'll:

1. Explain why the naive approach is intuitive but inefficient
2. Demonstrate how the optimized approach works step-by-step
3. Provide clean, reusable code implementations in Kotlin
4. Visualize the algorithm in action
5. Compare performance between naive and optimized approaches

By the end of this guide, you'll be able to recognize these patterns instantly and apply them to solve a wide range of problems.

## **Table of Contents**

1. [Sliding Window](#sliding-window)
2. [Two Pointers](#two-pointers)
3. [Hash Maps](#hash-maps)
4. [Binary Search](#binary-search)
5. [Prefix Sum](#prefix-sum)
6. [Depth-First Search (DFS)](#depth-first-search-dfs)
7. [Breadth-First Search (BFS)](#breadth-first-search-bfs)
8. [Dynamic Programming](#dynamic-programming)
9. [Greedy Algorithms](#greedy-algorithms)

---

# **Sliding Window**

## **Why It's Important**

Sliding Window is one of the most elegant techniques in algorithm design, turning O(n²) nested loop solutions into O(n) linear time solutions. It's used for problems involving:

- Contiguous subarrays or substrings
- Finding maximum/minimum within a window
- Maintaining a window that satisfies certain conditions

## **The Problem With Naive Approaches**

Consider finding the maximum sum of a subarray of size k:

```kotlin
// Naive: O(n*k) time complexity
fun maxSumNaive(nums: IntArray, k: Int): Int {
    if (k > nums.size) return 0
    
    var maxSum = Int.MIN_VALUE
    
    // Try every possible window of size k
    for (i in 0..nums.size - k) {
        var windowSum = 0
        
        // Calculate sum of current window
        for (j in i until i + k) {
            windowSum += nums[j]
        }
        
        maxSum = maxOf(maxSum, windowSum)
    }
    
    return maxSum
}
```

The problem? For every window, we're recalculating the entire sum, leading to many redundant calculations.

## **The Sliding Window Insight**

When we slide the window one position to the right:
- We remove the leftmost element (the one leaving the window)
- We add the rightmost element (the one entering the window)

This means we can calculate each new window sum in O(1) time instead of O(k) time!

## **Optimized Solution**

```kotlin
// Optimized: O(n) time complexity
fun maxSumOptimized(nums: IntArray, k: Int): Int {
    if (k > nums.size) return 0
    
    // Calculate sum of first window
    var windowSum = 0
    for (i in 0 until k) {
        windowSum += nums[i]
    }
    
    var maxSum = windowSum
    
    // Slide window and update
    for (i in k until nums.size) {
        windowSum += nums[i] - nums[i - k]  // Add new, remove old
        maxSum = maxOf(maxSum, windowSum)
    }
    
    return maxSum
}
```

## **How It Works: Step by Step**

Given array: `[2, 5, 1, 8, 2, 3]` and k = 3

1. Calculate initial window sum: [2, 5, 1] = 8
2. Slide window:
   - Remove 2, add 8: [5, 1, 8] = 5 + 1 + 8 = 14
   - Remove 5, add 2: [1, 8, 2] = 14 - 5 + 2 = 11
   - Remove 1, add 3: [8, 2, 3] = 11 - 1 + 3 = 13
3. Maximum sum is 14

## **Fixed vs Variable Size Window**

The above example uses a fixed-size window. For variable-size windows (where the window expands and contracts based on conditions), we use a slightly different approach:

```kotlin
// Variable size window to find smallest subarray with sum >= target
fun minSubArrayLen(target: Int, nums: IntArray): Int {
    var left = 0
    var sum = 0
    var minLength = Int.MAX_VALUE
    
    for (right in nums.indices) {
        sum += nums[right]  // Expand window
        
        // Contract window as much as possible while maintaining the condition
        while (sum >= target) {
            minLength = minOf(minLength, right - left + 1)
            sum -= nums[left]
            left++
        }
    }
    
    return if (minLength == Int.MAX_VALUE) 0 else minLength
}
```

## **Problems to Practice**

1. **Fixed Window Problems:**
   - Maximum Sum Subarray of Size K
   - First Negative Number in Every Window of Size K
   - Count Occurrences of Anagrams

2. **Variable Window Problems:**
   - Longest Substring Without Repeating Characters (LeetCode #3)
   - Minimum Size Subarray Sum (LeetCode #209)
   - Longest Repeating Character Replacement (LeetCode #424)

## **When to Recognize It**

Look for keywords like:
- "Contiguous sequence of elements"
- "Subarray", "Substring"
- "Maximum/minimum sum/length"
- "At most K distinct elements"

---

# **Two Pointers**

## **Why It's Important**

Two Pointers is a technique that uses two references to traverse an array or string, helping solve problems that would otherwise require nested loops (O(n²)) in linear time (O(n)).

It's especially powerful for:
- Searching for pairs
- Removing duplicates
- Finding subarrays with specific properties
- Palindrome problems

## **The Problem With Naive Approaches**

Consider finding a pair of elements in a sorted array that sum to a target:

```kotlin
// Naive: O(n²) time complexity
fun twoSumNaive(nums: IntArray, target: Int): IntArray {
    for (i in nums.indices) {
        for (j in i + 1 until nums.size) {
            if (nums[i] + nums[j] == target) {
                return intArrayOf(i, j)
            }
        }
    }
    return intArrayOf(-1, -1)
}
```

This checks every possible pair with nested loops, leading to O(n²) complexity.

## **The Two Pointers Insight**

When the array is sorted, we can use two pointers:
- One starting from the beginning (left)
- One starting from the end (right)

We move these pointers based on whether their sum is greater or less than the target, eliminating many unnecessary comparisons.

## **Optimized Solution**

```kotlin
// Optimized: O(n) time complexity
fun twoSumSorted(nums: IntArray, target: Int): IntArray {
    var left = 0
    var right = nums.size - 1
    
    while (left < right) {
        val sum = nums[left] + nums[right]
        
        when {
            sum == target -> return intArrayOf(left, right)
            sum < target -> left++
            else -> right--
        }
    }
    
    return intArrayOf(-1, -1)
}
```

## **How It Works: Step by Step**

Given sorted array: `[1, 3, 4, 5, 7, 10, 11]` and target = 9

1. Initialize left = 0, right = 6
2. Calculate sum = nums[left] + nums[right] = 1 + 11 = 12
3. 12 > 9, so decrement right: right = 5
4. New sum = 1 + 10 = 11, still > 9, so right = 4
5. New sum = 1 + 7 = 8, now < 9, so increment left: left = 1
6. New sum = 3 + 7 = 10, still > 9, so right = 3
7. New sum = 3 + 5 = 8, now < 9, so left = 2
8. New sum = 4 + 5 = 9, which equals target, return [2, 3]

## **Common Two Pointer Patterns**

### **1. Opposite Ends (like the example above)**

```kotlin
var left = 0
var right = array.size - 1

while (left < right) {
    // Process elements and move pointers
}
```

### **2. Fast and Slow Pointers**

```kotlin
// Remove duplicates from sorted array
fun removeDuplicates(nums: IntArray): Int {
    if (nums.isEmpty()) return 0
    
    var slow = 0 // Position to place next unique element
    
    for (fast in 1 until nums.size) {
        if (nums[fast] != nums[slow]) {
            slow++
            nums[slow] = nums[fast]
        }
    }
    
    return slow + 1 // Number of unique elements
}
```

### **3. Multiple Arrays**

```kotlin
// Merge two sorted arrays
fun merge(nums1: IntArray, m: Int, nums2: IntArray, n: Int) {
    var p1 = m - 1 // Pointer for nums1
    var p2 = n - 1 // Pointer for nums2
    var p = m + n - 1 // Pointer for result
    
    while (p1 >= 0 && p2 >= 0) {
        if (nums1[p1] > nums2[p2]) {
            nums1[p] = nums1[p1]
            p1--
        } else {
            nums1[p] = nums2[p2]
            p2--
        }
        p--
    }
    
    // Copy remaining elements from nums2
    while (p2 >= 0) {
        nums1[p] = nums2[p2]
        p2--
        p--
    }
}
```

## **Problems to Practice**

1. **Two Pointers from Opposite Ends:**
   - Container With Most Water (LeetCode #11)
   - Valid Palindrome (LeetCode #125)
   - Trapping Rain Water (LeetCode #42)

2. **Fast and Slow Pointers:**
   - Remove Duplicates from Sorted Array (LeetCode #26)
   - Middle of the Linked List (LeetCode #876)
   - Linked List Cycle (LeetCode #141)

3. **Multiple Arrays:**
   - Merge Sorted Array (LeetCode #88)
   - Intersection of Two Arrays II (LeetCode #350)

## **When to Recognize It**

Look for keywords like:
- "Sorted array"
- "Find a pair"
- "Palindrome"
- "Two elements that satisfy a condition"
- "Merge two sorted arrays"

---

# **Hash Maps**

## **Why It's Important**

Hash Maps (or dictionaries) provide O(1) lookup time, transforming problems that would require O(n) linear search or O(n²) nested loops into efficient O(n) solutions.

They're essential for:
- Finding unique elements
- Counting frequencies
- Finding pairs/complements
- Caching results for quick lookup

## **The Problem With Naive Approaches**

Consider finding two numbers in an array that sum to a target:

```kotlin
// Naive: O(n²) time complexity
fun twoSumNaive(nums: IntArray, target: Int): IntArray {
    for (i in nums.indices) {
        for (j in i + 1 until nums.size) {
            if (nums[i] + nums[j] == target) {
                return intArrayOf(i, j)
            }
        }
    }
    return intArrayOf(-1, -1)
}
```

This approach checks every possible pair, leading to O(n²) complexity.

## **The Hash Map Insight**

Instead of searching for a complement, we can store elements we've seen in a hash map for instant lookup:
- For each element, calculate its complement (target - current)
- Check if that complement exists in our hash map
- If it does, we've found our pair
- If not, add the current element to the hash map and continue

## **Optimized Solution**

```kotlin
// Optimized: O(n) time complexity
fun twoSum(nums: IntArray, target: Int): IntArray {
    val map = HashMap<Int, Int>() // value -> index
    
    for (i in nums.indices) {
        val complement = target - nums[i]
        
        if (map.containsKey(complement)) {
            return intArrayOf(map[complement]!!, i)
        }
        
        map[nums[i]] = i
    }
    
    return intArrayOf(-1, -1)
}
```

## **How It Works: Step by Step**

Given array: `[7, 2, 11, 15]` and target = 9

1. Process nums[0] = 7:
   - Complement = 9 - 7 = 2
   - 2 is not in map
   - Add 7 -> 0 to map
   - Map: {7 -> 0}

2. Process nums[1] = 2:
   - Complement = 9 - 2 = 7
   - 7 IS in map!
   - Return [map[7], 1] = [0, 1]

## **Common Hash Map Applications**

### **1. Frequency Counting**

```kotlin
fun findMostFrequent(nums: IntArray): Int {
    val frequencyMap = mutableMapOf<Int, Int>()
    var maxFreq = 0
    var result = 0
    
    for (num in nums) {
        val freq = frequencyMap.getOrDefault(num, 0) + 1
        frequencyMap[num] = freq
        
        if (freq > maxFreq) {
            maxFreq = freq
            result = num
        }
    }
    
    return result
}
```

### **2. Checking for Anagrams**

```kotlin
fun isAnagram(s: String, t: String): Boolean {
    if (s.length != t.length) return false
    
    val charCount = mutableMapOf<Char, Int>()
    
    // Count characters in s
    for (c in s) {
        charCount[c] = charCount.getOrDefault(c, 0) + 1
    }
    
    // Check against t
    for (c in t) {
        val count = charCount.getOrDefault(c, 0)
        if (count == 0) return false
        charCount[c] = count - 1
    }
    
    return true
}
```

### **3. Subarrays with Sum K**

```kotlin
fun subarraySum(nums: IntArray, k: Int): Int {
    val prefixSumCount = mutableMapOf<Int, Int>()
    prefixSumCount[0] = 1  // Empty subarray
    
    var prefixSum = 0
    var count = 0
    
    for (num in nums) {
        prefixSum += num
        
        // If prefixSum - k exists, we found subarrays with sum k
        count += prefixSumCount.getOrDefault(prefixSum - k, 0)
        
        // Update map
        prefixSumCount[prefixSum] = prefixSumCount.getOrDefault(prefixSum, 0) + 1
    }
    
    return count
}
```

## **Problems to Practice**

1. **Lookup Problems:**
   - Two Sum (LeetCode #1)
   - Longest Substring Without Repeating Characters (LeetCode #3)
   - Contains Duplicate (LeetCode #217)

2. **Frequency Problems:**
   - Valid Anagram (LeetCode #242)
   - First Unique Character in a String (LeetCode #387)
   - Group Anagrams (LeetCode #49)

3. **Prefix Sum Problems:**
   - Subarray Sum Equals K (LeetCode #560)
   - Continuous Subarray Sum (LeetCode #523)

## **When to Recognize It**

Look for keywords like:
- "Find if an element exists"
- "Count occurrences"
- "Find pairs/complements"
- "Check if two strings are anagrams"
- "Track frequency of elements"

---

# **Binary Search**

## **Why It's Important**

Binary Search is a divide-and-conquer technique that reduces the search space by half at each step, resulting in a logarithmic O(log n) time complexity instead of linear O(n).

It's crucial for:
- Searching in sorted arrays
- Finding insertion points
- Optimizing answers in a monotonic search space
- Finding bounds or ranges

## **The Problem With Naive Approaches**

Consider finding a target value in a sorted array:

```kotlin
// Naive: O(n) time complexity
fun linearSearch(nums: IntArray, target: Int): Int {
    for (i in nums.indices) {
        if (nums[i] == target) {
            return i
        }
    }
    return -1
}
```

This checks every element sequentially, missing the advantage of the array being sorted.

## **The Binary Search Insight**

Since the array is sorted, we can:
- Check the middle element first
- If it's our target, we're done
- If target is smaller, search the left half
- If target is larger, search the right half
- Repeat until we find the target or exhaust the array

This cuts the search space in half with each comparison.

## **Optimized Solution**

```kotlin
// Optimized: O(log n) time complexity
fun binarySearch(nums: IntArray, target: Int): Int {
    var left = 0
    var right = nums.size - 1
    
    while (left <= right) {
        val mid = left + (right - left) / 2  // Avoid overflow
        
        when {
            nums[mid] == target -> return mid
            nums[mid] < target -> left = mid + 1
            else -> right = mid - 1
        }
    }
    
    return -1
}
```

## **How It Works: Step by Step**

Given sorted array: `[2, 5, 8, 12, 16, 23, 38, 56, 72, 91]` and target = 23

1. Initialize left = 0, right = 9
2. Calculate mid = (0 + 9) / 2 = 4, nums[mid] = 16
3. 16 < 23, so search right half: left = mid + 1 = 5, right = 9
4. New mid = (5 + 9) / 2 = 7, nums[mid] = 56
5. 56 > 23, so search left half: left = 5, right = mid - 1 = 6
6. New mid = (5 + 6) / 2 = 5, nums[mid] = 23
7. 23 == 23, found at index 5!

## **Common Binary Search Patterns**

### **1. Standard Binary Search**

```kotlin
var left = 0
var right = array.size - 1

while (left <= right) {
    val mid = left + (right - left) / 2
    
    when {
        array[mid] == target -> return mid
        array[mid] < target -> left = mid + 1
        else -> right = mid - 1
    }
}
```

### **2. Find Lower Bound (First Position ≥ Target)**

```kotlin
fun lowerBound(nums: IntArray, target: Int): Int {
    var left = 0
    var right = nums.size
    
    while (left < right) {
        val mid = left + (right - left) / 2
        
        if (nums[mid] < target) {
            left = mid + 1
        } else {
            right = mid
        }
    }
    
    return left
}
```

### **3. Binary Search on Answer Space**

```kotlin
// Koko Eating Bananas (LeetCode #875)
fun minEatingSpeed(piles: IntArray, h: Int): Int {
    var left = 1
    var right = piles.maxOrNull() ?: 1
    
    while (left < right) {
        val mid = left + (right - left) / 2
        
        if (canEatAll(piles, h, mid)) {
            right = mid
        } else {
            left = mid + 1
        }
    }
    
    return left
}

private fun canEatAll(piles: IntArray, h: Int, k: Int): Boolean {
    var hours = 0
    for (pile in piles) {
        // Ceiling division: (pile + k - 1) / k
        hours += (pile + k - 1) / k
    }
    return hours <= h
}
```

## **Problems to Practice**

1. **Basic Binary Search:**
   - Binary Search (LeetCode #704)
   - Search Insert Position (LeetCode #35)
   - First Bad Version (LeetCode #278)

2. **Finding Bounds:**
   - Find First and Last Position of Element (LeetCode #34)
   - Search in Rotated Sorted Array (LeetCode #33)
   - Find Minimum in Rotated Sorted Array (LeetCode #153)

3. **Binary Search on Answer Space:**
   - Koko Eating Bananas (LeetCode #875)
   - Split Array Largest Sum (LeetCode #410)
   - Capacity To Ship Packages Within D Days (LeetCode #1011)

## **When to Recognize It**

Look for keywords like:
- "Sorted array"
- "Find efficiently"
- "Minimize maximum" or "Maximize minimum"
- "First occurrence" or "Last occurrence"
- "Find smallest/largest value that satisfies a condition"

---

# **Prefix Sum**

## **Why It's Important**

Prefix Sum is a simple yet powerful technique for efficiently calculating cumulative sums in arrays, transforming range sum queries from O(n) to O(1) time complexity after O(n) preprocessing.

It's essential for:
- Multiple range sum queries
- Finding subarrays with specific sum properties
- Calculating running statistics

## **The Problem With Naive Approaches**

Consider calculating the sum of elements in various ranges:

```kotlin
// Naive: O(n) per query
fun rangeSum(nums: IntArray, left: Int, right: Int): Int {
    var sum = 0
    for (i in left..right) {
        sum += nums[i]
    }
    return sum
}
```

This recalculates the entire sum for each query, which is inefficient for multiple queries.

## **The Prefix Sum Insight**

Instead of calculating each range sum from scratch:
- Precompute a prefix sum array where prefix[i] = sum of elements from 0 to i-1
- Calculate any range sum using: sum(left, right) = prefix[right+1] - prefix[left]

This allows O(1) time for each range sum query after O(n) preprocessing.

## **Optimized Solution**

```kotlin
class RangeSumQuery(nums: IntArray) {
    private val prefix: IntArray
    
    init {
        prefix = IntArray(nums.size + 1)
        for (i in nums.indices) {
            prefix[i + 1] = prefix[i] + nums[i]
        }
    }
    
    fun sumRange(left: Int, right: Int): Int {
        return prefix[right + 1] - prefix[left]
    }
}
```

## **How It Works: Step by Step**

Given array: `[4, 2, 7, 1, 8, 3]`

1. Calculate prefix sums:
   - prefix[0] = 0 (empty prefix)
   - prefix[1] = 0 + 4 = 4
   - prefix[2] = 4 + 2 = 6
   - prefix[3] = 6 + 7 = 13
   - prefix[4] = 13 + 1 = 14
   - prefix[5] = 14 + 8 = 22
   - prefix[6] = 22 + 3 = 25

2. To find sum of range [1, 3] (elements at indices 1, 2, 3):
   - sumRange(1, 3) = prefix[4] - prefix[1] = 14 - 4 = 10
   - Which is 2 + 7 + 1 = 10

## **Advanced Applications**

### **1. 2D Prefix Sum for Matrix Queries**

```kotlin
class Matrix2DSum(matrix: Array<IntArray>) {
    private val prefix: Array<IntArray>
    
    init {
        val rows = matrix.size
        val cols = if (rows > 0) matrix[0].size else 0
        
        prefix = Array(rows + 1) { IntArray(cols + 1) }
        
        // Build prefix sum matrix
        for (r in 0 until rows) {
            for (c in 0 until cols) {
                prefix[r + 1][c + 1] = prefix[r + 1][c] + 
                                       prefix[r][c + 1] - 
                                       prefix[r][c] + 
                                       matrix[r][c]
            }
        }
    }
    
    fun sumRegion(row1: Int, col1: Int, row2: Int, col2: Int): Int {
        return prefix[row2 + 1][col2 + 1] - 
               prefix[row2 + 1][col1] - 
               prefix[row1][col2 + 1] + 
               prefix[row1][col1]
    }
}
```

### **2. Finding Subarrays with Given Sum**

```kotlin
fun subarraySum(nums: IntArray, k: Int): Int {
    val prefixSumCount = mutableMapOf<Int, Int>()
    prefixSumCount[0] = 1  // Empty subarray
    
    var prefixSum = 0
    var count = 0
    
    for (num in nums) {
        prefixSum += num
        
        // If prefixSum - k exists, we found subarrays with sum k
        count += prefixSumCount.getOrDefault(prefixSum - k, 0)
        
        // Update map
        prefixSumCount[prefixSum] = prefixSumCount.getOrDefault(prefixSum, 0) + 1
    }
    
    return count
}
```

## **Problems to Practice**

1. **Range Sum Queries:**
   - Range Sum Query - Immutable (LeetCode #303)
   - Range Sum Query 2D - Immutable (LeetCode #304)

2. **Subarray Sum Problems:**
   - Subarray Sum Equals K (LeetCode #560)
   - Maximum Size Subarray Sum Equals k (LeetCode #325)
   - Continuous Subarray Sum (LeetCode #523)

3. **Advanced Applications:**
   - Product of Array Except Self (LeetCode #238)
   - Corporate Flight Bookings (LeetCode #1109)

## **When to Recognize It**

Look for keywords like:
- "Range queries"
- "Sum of subarray"
- "Multiple queries on the same array"
- "Find subarrays with sum equal to k"
- "Cumulative statistics"

---

# **Depth-First Search (DFS)**

## **Why It's Important**

Depth-First Search is a fundamental graph traversal algorithm that explores as far as possible along each branch before backtracking.

It's crucial for:
- Exploring all possible paths in a graph or tree
- Finding connected components
- Detecting cycles
- Solving maze-like problems
- Implementing backtracking algorithms

## **The Problem With Naive Approaches**

Consider traversing a graph without keeping track of visited nodes:

```kotlin
// Naive: May cause infinite loops in cyclic graphs
fun exploreGraph(graph: Map<Int, List<Int>>, node: Int) {
    println("Visiting node: $node")
    
    val neighbors = graph[node] ?: return
    for (neighbor in neighbors) {
        exploreGraph(graph, neighbor)
    }
}
```

This may cause infinite loops in cyclic graphs and redundant explorations.

## **The DFS Insight**

To systematically explore a graph:
- Start at a source node
- Recursively explore each unvisited neighbor
- Mark nodes as visited to avoid cycles
- Backtrack when you reach a dead end or a node with all neighbors visited

## **Optimized Solution**

```kotlin
// Recursive DFS with visited tracking
fun dfs(graph: Map<Int, List<Int>>, node: Int, visited: MutableSet<Int>) {
    if (node in visited) return
    
    visited.add(node)
    println("Visiting node: $node")
    
    val neighbors = graph[node] ?: return
    for (neighbor in neighbors) {
        dfs(graph, neighbor, visited)
    }
}

// Usage
fun exploreGraph(graph: Map<Int, List<Int>>, start: Int) {
    val visited = mutableSetOf<Int>()
    dfs(graph, start, visited)
}
```

## **How It Works: Step by Step**

Given this simple graph:
```
1 --- 2 --- 4
|     |
3 --- 5
```

DFS traversal starting from node 1:

1. Mark 1 as visited
2. Explore neighbor 2
   - Mark 2 as visited
   - Explore neighbor 4
     - Mark 4 as visited
     - No unvisited neighbors, backtrack to 2
   - Explore neighbor 5
     - Mark 5 as visited
     - Explore neighbor 3
       - Mark 3 as visited
       - Explore neighbor 1 (already visited, skip)
       - No more unvisited neighbors, backtrack to 5
     - No more unvisited neighbors, backtrack to 2
   - No more unvisited neighbors, backtrack to 1
3. Explore neighbor 3 (already visited, skip)
4. No more unvisited neighbors, traversal complete

## **Common DFS Patterns**

### **1. Recursive DFS**

```kotlin
fun dfs(graph: Map<Int, List<Int>>, node: Int, visited: MutableSet<Int>) {
    if (node in visited) return
    
    visited.add(node)
    process(node)
    
    for (neighbor in graph[node] ?: emptyList()) {
        dfs(graph, neighbor, visited)
    }
}
```

### **2. Iterative DFS with Stack**

```kotlin
fun dfsIterative(graph: Map<Int, List<Int>>, start: Int) {
    val visited = mutableSetOf<Int>()
    val stack = Stack<Int>()
    
    stack.push(start)
    
    while (stack.isNotEmpty()) {
        val node = stack.pop()
        
        if (node in visited) continue
        
        visited.add(node)
        process(node)
        
        // Add neighbors in reverse order for same traversal as recursive
        for (neighbor in (graph[node] ?: emptyList()).reversed()) {
            if (neighbor !in visited) {
                stack.push(neighbor)
            }
        }
    }
}
```

### **3. DFS in a Grid/Matrix**

```kotlin
fun numIslands(grid: Array<CharArray>): Int {
    if (grid.isEmpty()) return 0
    
    val rows = grid.size
    val cols = grid[0].size
    var count = 0
    
    for (r in 0 until rows) {
        for (c in 0 until cols) {
            if (grid[r][c] == '1') {
                count++
                dfs(grid, r, c)  // Mark connected land as visited
            }
        }
    }
    
    return count
}

private fun dfs(grid: Array<CharArray>, r: Int, c: Int) {
    val rows = grid.size
    val cols = grid[0].size
    
    // Check bounds and if it's land
    if (r < 0 || r >= rows || c < 0 || c >= cols || grid[r][c] != '1') {
        return
    }
    
    // Mark as visited
    grid[r][c] = '0'
    
    // Explore 4 directions
    dfs(grid, r + 1, c)
    dfs(grid, r - 1, c)
    dfs(grid, r, c + 1)
    dfs(grid, r, c - 1)
}
```

## **Problems to Practice**

1. **Graph DFS:**
   - Number of Islands (LeetCode #200)
   - Clone Graph (LeetCode #133)
   - Course Schedule (LeetCode #207)

2. **Tree DFS:**
   - Binary Tree Inorder Traversal (LeetCode #94)
   - Path Sum (LeetCode #112)
   - Maximum Depth of Binary Tree (LeetCode #104)

3. **Backtracking with DFS:**
   - Word Search (LeetCode #79)
   - Permutations (LeetCode #46)
   - N-Queens (LeetCode #51)

## **When to Recognize It**

Look for keywords like:
- "Find all paths"
- "Explore all possibilities"
- "Connected components"
- "Depth" or "deep" exploration
- "Maze solving"
- "Tree traversal"

---

# **Breadth-First Search (BFS)**

## **Why It's Important**

Breadth-First Search is a traversal algorithm that explores all neighbors at the current depth before moving to nodes at the next depth level.

It's essential for:
- Finding shortest paths in unweighted graphs
- Level-order traversal of trees
- Finding nodes at a specific distance
- Connected components

## **The Problem With Naive Approaches**

Consider using DFS to find shortest paths:

```kotlin
// Naive: DFS doesn't guarantee shortest path
fun findPathDFS(graph: Map<Int, List<Int>>, start: Int, end: Int): List<Int> {
    val visited = mutableSetOf<Int>()
    val path = mutableListOf<Int>()
    
    fun dfs(node: Int): Boolean {
        visited.add(node)
        path.add(node)
        
        if (node == end) return true
        
        for (neighbor in graph[node] ?: emptyList()) {
            if (neighbor !in visited) {
                if (dfs(neighbor)) return true
            }
        }
        
        // Backtrack if no path found
        path.removeAt(path.size - 1)
        return false
    }
    
    dfs(start)
    return path
}
```

This DFS approach finds a path, but not necessarily the shortest one.

## **The BFS Insight**

To find the shortest path:
- Start from the source node
- Explore all neighbors at the current distance
- Then move to neighbors at the next distance
- Use a queue to process nodes in order of their distance from source
- The first time you reach the destination is guaranteed to be the shortest path

## **Optimized Solution**

```kotlin
// BFS guarantees shortest path in unweighted graphs
fun shortestPath(graph: Map<Int, List<Int>>, start: Int, end: Int): List<Int> {
    val visited = mutableSetOf<Int>()
    val queue = LinkedList<Int>()
    val parent = mutableMapOf<Int, Int>() // To reconstruct path
    
    queue.add(start)
    visited.add(start)
    
    while (queue.isNotEmpty()) {
        val node = queue.poll()
        
        if (node == end) {
            // Path found, reconstruct it
            return reconstructPath(parent, start, end)
        }
        
        for (neighbor in graph[node] ?: emptyList()) {
            if (neighbor !in visited) {
                queue.add(neighbor)
                visited.add(neighbor)
                parent[neighbor] = node
            }
        }
    }
    
    return emptyList() // No path found
}

private fun reconstructPath(parent: Map<Int, Int>, start: Int, end: Int): List<Int> {
    val path = mutableListOf<Int>()
    var current = end
    
    // Traverse from end to start
    while (current != start) {
        path.add(0, current)
        current = parent[current] ?: break
    }
    
    path.add(0, start)
    return path
}
```

## **How It Works: Step by Step**

Given this simple graph:
```
1 --- 2 --- 5
|     |
3 --- 4
```

BFS traversal starting from node 1 to find path to node 5:

1. Initialize: queue = [1], visited = {1}
2. Dequeue 1, explore neighbors 2 and 3
   - queue = [2, 3], visited = {1, 2, 3}, parent = {2:1, 3:1}
3. Dequeue 2, explore neighbors 4 and 5
   - queue = [3, 4, 5], visited = {1, 2, 3, 4, 5}, parent = {2:1, 3:1, 4:2, 5:2}
4. Node 5 is our target!
5. Reconstruct path: Start from 5, parent[5] = 2, parent[2] = 1
   - Path: 1 → 2 → 5

## **Common BFS Patterns**

### **1. Level Order Traversal**

```kotlin
fun levelOrder(root: TreeNode?): List<List<Int>> {
    val result = mutableListOf<List<Int>>()
    if (root == null) return result
    
    val queue = LinkedList<TreeNode>()
    queue.add(root)
    
    while (queue.isNotEmpty()) {
        val levelSize = queue.size
        val currentLevel = mutableListOf<Int>()
        
        for (i in 0 until levelSize) {
            val node = queue.poll()
            currentLevel.add(node.`val`)
            
            node.left?.let { queue.add(it) }
            node.right?.let { queue.add(it) }
        }
        
        result.add(currentLevel)
    }
    
    return result
}
```

### **2. Find Shortest Path in Grid**

```kotlin
fun shortestPathBinaryMatrix(grid: Array<IntArray>): Int {
    val n = grid.size
    if (grid[0][0] == 1 || grid[n-1][n-1] == 1) return -1
    
    val directions = arrayOf(
        intArrayOf(-1, -1), intArrayOf(-1, 0), intArrayOf(-1, 1),
        intArrayOf(0, -1),                     intArrayOf(0, 1),
        intArrayOf(1, -1),  intArrayOf(1, 0),  intArrayOf(1, 1)
    )
    
    val queue = LinkedList<IntArray>()
    queue.add(intArrayOf(0, 0))
    grid[0][0] = 1  // Mark as visited
    
    var length = 1
    
    while (queue.isNotEmpty()) {
        val size = queue.size
        
        for (i in 0 until size) {
            val cell = queue.poll()
            val row = cell[0]
            val col = cell[1]
            
            if (row == n - 1 && col == n - 1) {
                return length
            }
            
            for (dir in directions) {
                val newRow = row + dir[0]
                val newCol = col + dir[1]
                
                if (newRow >= 0 && newRow < n && 
                    newCol >= 0 && newCol < n && 
                    grid[newRow][newCol] == 0) {
                    
                    queue.add(intArrayOf(newRow, newCol))
                    grid[newRow][newCol] = 1  // Mark as visited
                }
            }
        }
        
        length++
    }
    
    return -1  // No path found
}
```

## **Problems to Practice**

1. **Shortest Path:**
   - Word Ladder (LeetCode #127)
   - Shortest Path in Binary Matrix (LeetCode #1091)
   - Rotting Oranges (LeetCode #994)

2. **Level Order:**
   - Binary Tree Level Order Traversal (LeetCode #102)
   - Binary Tree Zigzag Level Order Traversal (LeetCode #103)
   - Average of Levels in Binary Tree (LeetCode #637)

3. **Other BFS Applications:**
   - 01 Matrix (LeetCode #542)
   - Walls and Gates (LeetCode #286)
   - Pacific Atlantic Water Flow (LeetCode #417)

## **When to Recognize It**

Look for keywords like:
- "Shortest path"
- "Minimum steps"
- "Level order"
- "Breadth" or "width" exploration
- "Nearest" or "closest"
- "Distance from source"

---

# **Dynamic Programming**

## **Why It's Important**

Dynamic Programming is a powerful technique for solving optimization problems by breaking them down into overlapping subproblems and solving each subproblem only once.

It's crucial for:
- Optimization problems (maximum/minimum)
- Counting problems
- Decision-making sequences
- Problems with optimal substructure

## **The Problem With Naive Approaches**

Consider calculating the nth Fibonacci number:

```kotlin
// Naive recursion: O(2^n) time complexity
fun fibNaive(n: Int): Int {
    if (n <= 1) return n
    return fibNaive(n - 1) + fibNaive(n - 2)
}
```

This approach recalculates the same values multiple times, leading to exponential time complexity.

## **The Dynamic Programming Insight**

To optimize overlapping subproblems:
- Identify the recurring subproblems
- Use memoization (top-down) or tabulation (bottom-up) to store results
- Build complex solutions from previously computed simpler ones
- Avoid redundant calculations

## **Optimized Solution**

### **Top-Down (Memoization)**

```kotlin
// Top-down DP: O(n) time and space
fun fibonacci(n: Int): Int {
    val memo = IntArray(n + 1) { -1 }
    
    fun fib(n: Int): Int {
        if (n <= 1) return n
        
        if (memo[n] != -1) return memo[n]
        
        memo[n] = fib(n - 1) + fib(n - 2)
        return memo[n]
    }
    
    return fib(n)
}
```

### **Bottom-Up (Tabulation)**

```kotlin
// Bottom-up DP: O(n) time and space
fun fibonacci(n: Int): Int {
    if (n <= 1) return n
    
    val dp = IntArray(n + 1)
    dp[0] = 0
    dp[1] = 1
    
    for (i in 2..n) {
        dp[i] = dp[i - 1] + dp[i - 2]
    }
    
    return dp[n]
}
```

## **How It Works: Step by Step**

For Fibonacci(5):

### **Naive Recursion (with redundant calculations)**
```
                    fib(5)
                /           \
            fib(4)           fib(3)
          /      \          /     \
      fib(3)     fib(2)   fib(2)  fib(1)
     /     \     /    \    /    \
fib(2)  fib(1) fib(1) fib(0) fib(1) fib(0)
/    \
fib(1) fib(0)
```

### **DP with Memoization (each subproblem solved once)**
```
                    fib(5)
                /           \
            fib(4)           fib(3) [cached]
          /      \         
      fib(3)     fib(2) [cached]   
     /     \
fib(2)  fib(1) [cached]
/    \
fib(1) fib(0) [cached]
```

### **DP with Tabulation**
```
dp[0] = 0
dp[1] = 1
dp[2] = dp[1] + dp[0] = 1
dp[3] = dp[2] + dp[1] = 2
dp[4] = dp[3] + dp[2] = 3
dp[5] = dp[4] + dp[3] = 5
```

## **Common DP Patterns**

### **1. 1D Dynamic Programming**

```kotlin
// Climbing Stairs: How many ways to climb n stairs (1 or 2 steps at a time)
fun climbStairs(n: Int): Int {
    if (n <= 2) return n
    
    val dp = IntArray(n + 1)
    dp[1] = 1
    dp[2] = 2
    
    for (i in 3..n) {
        dp[i] = dp[i - 1] + dp[i - 2]
    }
    
    return dp[n]
}
```

### **2. 2D Dynamic Programming**

```kotlin
// Unique Paths: How many ways to reach bottom-right from top-left in a grid
fun uniquePaths(m: Int, n: Int): Int {
    val dp = Array(m) { IntArray(n) { 1 } }
    
    for (i in 1 until m) {
        for (j in 1 until n) {
            dp[i][j] = dp[i-1][j] + dp[i][j-1]
        }
    }
    
    return dp[m-1][n-1]
}
```

### **3. State Transition**

```kotlin
// House Robber: Maximum amount that can be robbed without taking adjacent houses
fun rob(nums: IntArray): Int {
    if (nums.isEmpty()) return 0
    if (nums.size == 1) return nums[0]
    
    val dp = IntArray(nums.size)
    dp[0] = nums[0]
    dp[1] = maxOf(nums[0], nums[1])
    
    for (i in 2 until nums.size) {
        dp[i] = maxOf(dp[i-1], dp[i-2] + nums[i])
    }
    
    return dp[nums.size - 1]
}
```

## **Problems to Practice**

1. **1D Dynamic Programming:**
   - Climbing Stairs (LeetCode #70)
   - House Robber (LeetCode #198)
   - Maximum Subarray (LeetCode #53)

2. **2D Dynamic Programming:**
   - Unique Paths (LeetCode #62)
   - Minimum Path Sum (LeetCode #64)
   - Longest Common Subsequence (LeetCode #1143)

3. **Advanced DP Problems:**
   - Edit Distance (LeetCode #72)
   - Coin Change (LeetCode #322)
   - Longest Increasing Subsequence (LeetCode #300)

## **When to Recognize It**

Look for keywords like:
- "Maximum" or "Minimum" value
- "Count the number of ways"
- "What is the optimal strategy"
- "Can you construct ____"
- "How many distinct ways"

---

# **Greedy Algorithms**

## **Why It's Important**

Greedy Algorithms make locally optimal choices at each step, hoping that these local optimizations will lead to a global optimum.

They're valuable for:
- Optimization problems
- Scheduling problems
- Interval selection
- Huffman coding
- Simple and efficient solutions when applicable

## **The Problem With Naive Approaches**

Consider the Activity Selection problem (maximum number of non-overlapping activities):

```kotlin
// Naive: Try all possible combinations, O(2^n) time complexity
fun maxActivitiesBruteForce(activities: List<Activity>): Int {
    fun backtrack(index: Int, currentActivities: List<Activity>): Int {
        if (index >= activities.size) return currentActivities.size
        
        // Try including this activity if it doesn't overlap
        val canInclude = currentActivities.all { activity ->
            activity.end <= activities[index].start || activity.start >= activities[index].end
        }
        
        val includeThis = if (canInclude) {
            backtrack(index + 1, currentActivities + activities[index])
        } else {
            0
        }
        
        // Try skipping this activity
        val skipThis = backtrack(index + 1, currentActivities)
        
        return maxOf(includeThis, skipThis)
    }
    
    return backtrack(0, emptyList())
}
```

This tries all possible combinations, leading to exponential time complexity.

## **The Greedy Insight**

For many problems, a simple greedy strategy works:
- Sort activities by ending time
- Always pick the activity with the earliest ending time
- Skip activities that overlap with the last selected activity

This leads to the optimal solution in O(n log n) time.

## **Optimized Solution**

```kotlin
data class Activity(val start: Int, val end: Int)

fun maxActivitiesGreedy(activities: List<Activity>): List<Activity> {
    // Sort by end time
    val sortedActivities = activities.sortedBy { it.end }
    
    val result = mutableListOf<Activity>()
    if (sortedActivities.isEmpty()) return result
    
    // Select first activity
    result.add(sortedActivities[0])
    var lastEnd = sortedActivities[0].end
    
    // Greedily select non-overlapping activities
    for (i in 1 until sortedActivities.size) {
        val current = sortedActivities[i]
        if (current.start >= lastEnd) {
            result.add(current)
            lastEnd = current.end
        }
    }
    
    return result
}
```

## **How It Works: Step by Step**

Given activities: `[(1,4), (2,6), (3,5), (5,7), (8,9)]` (start, end times):

1. Sort by end time: `[(1,4), (3,5), (2,6), (5,7), (8,9)]`
2. Select first activity: `(1,4)`, lastEnd = 4
3. Check if `(3,5)` can be selected: 3 < 4, can't select (overlaps)
4. Check if `(2,6)` can be selected: 2 < 4, can't select (overlaps)
5. Check if `(5,7)` can be selected: 5 >= 4, select it, lastEnd = 7
6. Check if `(8,9)` can be selected: 8 >= 7, select it, lastEnd = 9
7. Result: `[(1,4), (5,7), (8,9)]` (3 activities)

## **Common Greedy Patterns**

### **1. Interval Scheduling**

```kotlin
// Merge Intervals
fun mergeIntervals(intervals: Array<IntArray>): Array<IntArray> {
    if (intervals.isEmpty()) return emptyArray()
    
    // Sort by start time
    val sorted = intervals.sortedBy { it[0] }
    
    val result = mutableListOf<IntArray>()
    var current = sorted[0]
    
    for (i in 1 until sorted.size) {
        if (sorted[i][0] <= current[1]) {
            // Overlapping intervals, merge them
            current[1] = maxOf(current[1], sorted[i][1])
        } else {
            // Non-overlapping interval, add current to result
            result.add(current)
            current = sorted[i]
        }
    }
    
    // Add the last interval
    result.add(current)
    
    return result.toTypedArray()
}
```

### **2. Fractional Knapsack**

```kotlin
data class Item(val weight: Int, val value: Int) {
    val valuePerWeight: Double
        get() = value.toDouble() / weight
}

fun fractionalKnapsack(items: List<Item>, capacity: Int): Double {
    // Sort by value per weight in descending order
    val sortedItems = items.sortedByDescending { it.valuePerWeight }
    
    var remainingCapacity = capacity
    var totalValue = 0.0
    
    for (item in sortedItems) {
        if (remainingCapacity >= item.weight) {
            // Take the whole item
            totalValue += item.value
            remainingCapacity -= item.weight
        } else {
            // Take a fraction of the item
            totalValue += item.valuePerWeight * remainingCapacity
            break
        }
    }
    
    return totalValue
}
```

## **Problems to Practice**

1. **Interval Problems:**
   - Merge Intervals (LeetCode #56)
   - Non-overlapping Intervals (LeetCode #435)
   - Meeting Rooms II (LeetCode #253)

2. **Other Greedy Problems:**
   - Jump Game (LeetCode #55)
   - Gas Station (LeetCode #134)
   - Task Scheduler (LeetCode #621)
   - Partition Labels (LeetCode #763)

## **When to Recognize It**

Look for keywords like:
- "Maximum number of activities"
- "Minimum number of intervals"
- "Optimal scheduling"
- "Most efficient way"
- "Largest possible value with constraints"

## **Warning: When Greedy Fails**

Greedy doesn't work for all optimization problems. It fails when:
- The locally optimal choice doesn't lead to a global optimum
- Future decisions depend on past choices in complex ways

Examples where greedy fails:
- 0/1 Knapsack (use Dynamic Programming instead)
- Longest Path in a Graph (use Bellman-Ford or Floyd-Warshall)
- Traveling Salesman Problem (use DP or approximation algorithms)

---

# **Conclusion and Further Learning**

## **Pattern Recognition is Key**

The ability to recognize which algorithm pattern fits a given problem is crucial. Here's a quick reference:

- **Sliding Window**: For problems about contiguous subarrays/substrings
- **Two Pointers**: For problems about pairs or reducing space
- **Hash Maps**: For frequency counting, lookups, and tracking
- **Binary Search**: For efficient search in sorted arrays or answer spaces
- **Prefix Sum**: For range queries and cumulative statistics
- **DFS**: For exploring all paths, tree traversal, or backtracking
- **BFS**: For shortest paths or level-order traversal
- **Dynamic Programming**: For optimization with overlapping subproblems
- **Greedy**: For locally optimal choices leading to global optimum

## **Hybrid Approaches**

Many complex problems require combining multiple patterns:
- **Sliding Window + Hash Map**: For problems about unique elements in a window
- **BFS + DP**: For shortest path with weights
- **Binary Search + Greedy**: For optimization problems
- **Prefix Sum + Hash Map**: For subarray sum problems

## **Practice Recommendations**

1. **Master One Pattern at a Time**:
   - Solve 5-10 problems of each pattern
   - Start with easier problems and gradually increase difficulty
   - Ensure you understand why the pattern works

2. **Implement Templates**:
   - Create template code for each pattern
   - Practice applying these templates to new problems

3. **Spaced Repetition**:
   - Revisit problems after 1 day, 3 days, 7 days
   - Focus on understanding the approach, not memorizing solutions

## **Advanced Topics**

Once you're comfortable with these patterns, explore:
- Graph Algorithms (Dijkstra's, Bellman-Ford, Floyd-Warshall)
- Advanced Data Structures (Segment Trees, Tries, Disjoint Sets)
- Mathematical Algorithms (Modular Arithmetic, Combinatorics)
- Bit Manipulation Techniques
- String Algorithms (KMP, Rabin-Karp, Suffix Arrays)

## **Final Thoughts**

Remember that algorithmic problem-solving is a skill that improves with deliberate practice. Focus on understanding patterns rather than memorizing solutions, and you'll develop a solid foundation for tackling even the most complex problems.

Happy coding!