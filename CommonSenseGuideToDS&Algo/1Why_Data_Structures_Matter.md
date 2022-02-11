# Why Data Structures Matter

- _Data Structures_ refer to how data is _organized._
- Depending on the Data Structure you choose, It can impact how fast your code runs.

## Arrays: The Foundational Data Structure

- The size of an array is how many data elements the array holds.

**Data Structure Operations**

- Operations used on data structures, Arrays in this case. → read, search, insert, delete.
  - **Read**: looking up a _value_ at an index.
  - **Search**: looking to see if a _value_ exists
  - **Insert**: adding new _values_
  - **Delete**: removing a value

**Measuring Speed**

- When measuring how fast an operation takes, we do not refer to pure time, but instead in how many steps(iterations) it takes
- Measuring the speed of an operation in terms of time is undependable since the time will always change depending on the hardware it is run on.
- Measuring the speed of an operation is also known as measuring its time complexity. (Big O)

### Analyzing Array data structure efficiency

When an array is created, the computer allocates cells in memory to accommodate the array. Every cell in memory has a specific address that is represented with a number and in sequential order.

**Reading**

- Takes one step to read from the array. O(1)
- Actually takes 2 steps. The computer jumps to beginning of where the array is allocated in memory and adds index to memory cell address.

**Searching**

- Goes through each element until it finds the index associated with the value.
- linear search, O(n)

**Insertion**

- **Insert end**: many programming languages allocate additional memory cells to arrays, so in case of adding new elements at the end would only take one step O(1)
- **Insert middle**: shift elements to make space for the incoming element. O(n)
- **Insert beginning**: This is the worst-case scenario as all elements need to shift which would take n + 1 steps. 0(n)

**Deletion**

- Deleting takes one step.
- For an array of five elements, we’d spend one step deleting the first element, and four steps shifting the four remaining elements.
- The worst-case or maximum steps would be O(n)

## Sets: How a Single Rule Can Affect Efficiency (Array Based)

A set is a data Structure that does not allow duplicate values to be contained within, and therefore useful when you need to ensure that you don’t have duplicated data.

Array based sets and arrays have same efficiency in reading, searching, and deletion. But not insertion.

The computer needs to determine that value being inserted is not already in the set. The computer would search the whole array before inserting. O(n+1)

Inserting at the beginning is the worst case because the computer needs to search(O(n)), shift elements to the right(0(n)), and insert(O(1)). (2n + 1)

The difference between an array and array based set is insertion. Array insertion is more efficient than sets. Sets should be used when you need to ensure no duplicate data.

## Exercises

1. For an array containing 100 elements, provide the number of steps the following operations would take:
   1. Reading → 1 step
   2. Searching for a value not contained within the array → N steps
   3. Insertion at the beginning of the array → N + 1
   4. Insertion at the end of the array → 1
   5. Deletion at the beginning of the array → N
   6. Deletion at the end of the array → 1
2. For an array-based set containing 100 elements, provide the number of steps the following operations would take:
   1. Reading → 1 step
   2. Searching → N
   3. Insert beginning → 2n + 1
   4. Insert end → N + 1
   5. Delete beginning → N
   6. Delete end → 1
3. count all instance of value (searching) → N times
