# readme.md
Comparison of Linear Search and Binary Search algorithms with performance analysis, edge case testing, and real-world applications.

## Unit 5 Discussion: Search Algorithms
## Overview
This assignment compares linear search and binary search.

## Learning Objectives
Implement linear search
Implement binary search
Compare performance
Analyze algorithm efficiency
## Requirements
Test both algorithms on a small dataset.
Test both algorithms on a large dataset.
Demonstrate edge cases.
Analyze performance.
Create a real-world search scenario.
## Discussion Board Reflection
After completing the programming assignment, add this reflection to your initial discussion post in LEO.

Your reflection should be approximately 150–200 words and address the following questions:

What concepts or skills did you learn while completing this assignment?
What challenges did you encounter, and how did you overcome them?
Explain when to use linear versus binary search, including tradeoffs in real-world scenarios.

## Unit 5 Discussion: Search Algorithms
## Overview
This assignment compares linear search and binary search in Java across different dataset sizes, boundary conditions, and a real-world scenario to evaluate their efficiency and practical tradeoffs.
## Learning Objectives
Implement linear search and binary search from scratch.
Compare algorithmic performance using comparison counts and execution time (O(n) vs. O(\log n)).
Validate edge cases and boundary conditions.
Apply search algorithms to a realistic software scenario.
## Implementation Linear Search
Scans a collection sequentially from index 0 until a match is found or the array ends.
Time Complexity: O(n) 
Works on both unsorted and sorted arrays.
## Binary Search
Repeatedly divides a sorted search interval in half by comparing the target to the middle element.
Time Complexity: O(\log n) 
Requires sorted data.
## Testing and Results
Small Dataset (8 Elements: [12, 24, 36, 48, 60, 72, 84, 96])
Searching for 72 returned index 5 (6 comparisons for linear; 2 for binary).
Searching for a missing value (50) returned -1 for both.
## Large Dataset (500,000 Sorted Integers)
Searching near the end (999,996) required 499,999 comparisons in linear search versus just 19 comparisons in binary search.
## Edge Case Testing 
Empty Array ([]): Both returned -1.
Single-Element Array ([42]): Both returned index 0 for a match and -1 for a miss.
First & Last Elements: Both correctly resolved boundary indices.
Duplicate Values ([10, 20, 20, 30]): Linear search returned the first occurrence (1), while standard binary search returned the midpoint hit (2).
## Real-World Application
Simulating a retail SKU lookup: linear search was ideal for checking incoming, unsorted shipment manifests without sorting overhead, while binary search powered the pre-sorted main catalog for fast, repeated queries.
## Conclusion
Linear search is simple and works on raw data, whereas binary search requires sorted input but scales vastly more efficiently for large datasets.
## Discussion Board Reflection
Completing this assignment highlighted how theoretical Big-O notation translates into real performance differences as data scales. Writing both algorithms in Java and tracking exact comparison counts alongside System.nanoTime() made the gap between O(n) linear scanning and O(log n) interval halving clear. I also strengthened my testing habits by covering boundary conditions like empty arrays and duplicate values.My main challenge while coding binary search was preventing infinite loops and handling midpoint calculations safely. I resolved this by using low + (high - low) / 2 and strictly updating low = mid + 1 and high = mid - 1 inside a while (low <= high) loop.In practice, linear search fits small collections or incoming unsorted logs where sorting first costs more time than scanning, while binary search excels in large, heavily queried datasets where sorting once pays off.
