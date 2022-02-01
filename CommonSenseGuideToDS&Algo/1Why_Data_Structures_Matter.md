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

**Reading**

- Takes one step to read from the array.

**Searching**

- Goes through each element until it finds the index associated with the value.
- linear search, O(n)

**Insertion**

- **Insert end**: many programming languages allocate additional memory cells to arrays, so in case of adding new elements at the end would only take one step O(1)
- **Insert middle**: shift elements to make space for the incoming element. O(n)
- **Insert beginning**: This is the worst-case scenario as all elements need to shift which would take n + 1 steps.

**Deletion**

- Deleting takes one step.
- For an array of five elements, we’d spend one step deleting the first element, and four steps shifting the four remaining elements.
- The worst-case or maximum steps would be O(n)
