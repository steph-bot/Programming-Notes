# Sorting Algorithms

| Algorithm            | Exact $\theta(n)$ | Worst Case $O(n)$ | Best Case $\Omega(n)$ | Avg Case |
| -----------          | -----------       | -----------       | -----------           | ----------- |
| Selection Sort       | $\theta(n^2)$     | $O(n^2)$          | $\Omega(n^2)$         | |
| Bubble Sort          | $\theta(n^2)$     | $O(n^2)$          | $\Omega(n^2)$         | |
| Insertion Sort       |                   | $O(n^2)$          | $\Omega(n)$           | |
| Merge Sort           | $\theta(nlog(n))$ | $O(nlog(n))$      | $\Omega(nlog(n))$     | |
| Quick Sort           |                   | $O(n^2)$          | $\Omega(nlog(n))$     | $\theta(nlog(n))$ |
| Heap Sort            |                   | $O(nlog(n))$      |                       | |
| Binary Heap Actions**|                   | $O(log(n))$       |                       | |
| Build Heap           |                   | $O(n)$            |                       | |

**insert/extract/change priority/search a binary heap

## Brute Force
- Selection Sort: Scan to find minimum element, swap it with first position, continue till sorted
- Bubble Sort

## Decrease and Conquer
- Upfront work to reduce problem from n to n-1
    * Selection Sort
    * Bubble Sort
- Work at end to extend problem from n-1 to n
    * Insertion Sort:
- Reduce problem by size of partition
    * Quick Select (Randomized)

## Divide and Conquer
- Merge Sort
    * Backend work: Solve each half and merge results together
- Quick sort (Randomized)
    * Upfront work: Select arbitrary pivot value, solve each half, and merge results together
    * Lomuto Partitioning
    * Hoare’s Partitioning

## Transform and Conquer
- Heap Sort


