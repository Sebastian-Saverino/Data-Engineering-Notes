What is Big O and what does it help explain about algorithms?
It is the equation to understand the time and space complexity of algorithm going through an input so data


What are the three key concepts for understanding time complexity in Big O notation?
Growth in respects to input
Drop constants 
Assume worst measure for algo


How can you quickly determine the Big O complexity of an algorithm?
Look for the loop that iterate over the input, so like the number and the nature of the loops


What are some common time complexity classifications in Big O notation?
O(1) constant time
O(n) linear time
O(logn) logarithmic time
O()

We're not looking for the number at the end we care about the time complexity so the efficiency.


What is the fundamental definition of an array in terms of computer memory?

A contiguous memory block that contains 0 or more pieces of memory that is understood as a single type in a row, its all binary at the end of the day, and we can access this memory by calculating the memory offset and based on type sizez and index


What is the time complexity for accessing an element in a an array by its index?

It is constant time, it goes from one step to another like a straight line, but to be specific you don't have to iterate through the entire array.

What limitation exists when inserting elements into a traditional array?
You can't "grow" the array so you have to overwrite a value as you have already been allocated the memory so you can't add to it as it might fall onto the next memory chunk.

How does an array handle deletion of an element?

Deletion is handled through using zero value, we don't lose the memory space though it will become a sentinel value

What determines how memory is interpreted in an array?
We can understand through 8-bit integer view vs 16-bit integer view, as this can also change the way the numbers are interpreted within the memory.

What characteristic defines a traditional array's size?
The memory buffer, so for example rust on initialization is set to 5. The size is fixed and must be determined when the array is created.
What happens when you want to increase the size of a traditional array?
You must reallocate a new array, create a new larger array, and copy the contents of the old array into the new one. We can just grow it we must create an entire new one
What are the key components needed when defining an array in older languages?
We need to pass the type of data, the pointer so where the data starts in memory and then the length of the array.
What considerations are important when determining the initial size of an array's memory buffer?
How much poping and methods would be used against this array? I was kinda right but you have to balance between having enough space to avoid frequent reallocation and not wasting excessive memory by creating an overly large buffer.
What are the different types of array size specification in programming languages?
Arrays can have variable sizes so what we set at runtime or compile-time fixed sizes where the size is decided before the program execution.


What is the time complexity of a linear search algorithm?

It is O(n), as the input grows so does the search time making it constant

What are the key steps in implementing a basic linear search algorithm? Having a loop that loops through the data for a selected value

So to be more specific have the array from index 0 loop through length -1 so the entire data set then compare the val to each number in the array. If the value is not in the data set then return false.

What is the basic signature for a learn search function?
The loop but more specifically, having an array so our data with a target value to find then return a boolean saying whether or not a value is there

What is the worst-case scenario for a linear search?
The value not being in the dataset. Therefor you have to search through each element in the array.

How does a linear search compare an array's elements to find a specific value?
As the loop goes through the array the element is compared to the value.


What is the key characteristic of an algorithm that can take advantage of an ordered data set?

mathematical operations, by this we can optimize the search by making strategic jumps instead of checking everything.

What is the primary problem with jumping a fixed percentage (like 10%) through an array when searching?

You're still going in O(n) speed so constant time. Think worst case scenario, you would still be looping through the last section one by one when looking for the last one.

How does binary search reduce the search space with each iteration?
It cuts the search in half.

What is the runtime complexity of binary search?
O(logN) the number of steps grows logarithmically with the size of the input array.

What does the equation N/2^k = 1 represent in binary search? this is equal to O(logN)


What are the three main conditions in binary search?
A low, hi, val

if the needle our check is equal to the value return true, when the value is greater than the needle increase high side when value is is less then the needle search on the high side

left + ((left + right) / 2) 

How does binary search modify the search range when the current value is less than the needle. 
Reduce the high side

What are the initial values for lo and hi in binary search?

lo = 0 hi = len(data) + 1


What is the primary loop condition in binary search?
when lo <= hi


Give two crystal balls that will break if dropped form high enough distance, determine the exact spot in which ti will break in the most optimize way.

I first thought the best way to do this was to do a binary search and start at q1 and q3 but the best way is actually using the square root of n then doing a linear search after that last jump which is very interesting.

What is the mathematical definition of a sorted array?

Any element x[i] is less than or equal to x[i + 1] throughout the entire array.

How does the basic bubble sort algorithm work?

It compares adjacent elements and swaps them if they are in the wrong order, moving the largest element to the end of the array in each iteration.

What is the time complexity of bubble sort?
O(n**2)

What unique property occurs in each iterations of bubble sort?
The largest unsorted element is moved to the end of the unsorted portion of the array.

How does the number of comparisons change in each iterations of bubble sort?
The number of comparisons decreases with each pass, as the last element becomes sorted and is no longer compared.

What are the runtime characteristics of Bubble Sort?

O(n**2)

What are the key steps in implementing the Bubble Sort algorithm?
having an unsorted array
Use nested loops with outer loop running n times
Inner loop compares adjacent elements
Swap elements if they are in the wrong order
Reduce inner loop iterations with each pass
Largest unsorted element 'bubbles up' to the end in each pass


How does the inner loop range change in Bubble Sort?
The inner loop range progressively decreases by subtracting the current outer loop iteration (i), so it goes from n-1 to n-1-i, ensuring already sorted elements at the end are not re-examined.

What is the basic swap operation in Bubble Sort?



        if array[j] > array[j + 1]:
            array[j], array[j + 1] = array[j + 1], array[j]

print(array)


What happens to the array after each complete pass in Bubble Sort?

After each complete pass, the largest unsorted element 'bubbles up' to its correct final position at the end of the array, reducing the range of unsorted elements.


What is a linked list, and how does it fundamentally differ from an array?
It cannot be indexed like an array instead it uses nodes for each value.

A linked list is a node-based data structure where each node contains a value and a reference (pointer) to the next node. Unlike arrays, linked lists allow dynamic insertion and deletion with constant time complexity, and do not require shifting indices when modifying the list.


What are the key characteristics of a singly linked list?
The value can only see next and not previous
In a singly linked list, each node points only forward to the next node, which means you can only traverse the list in one direction. If you lose the reference to a previous node, you cannot access it again.

What distinguishes a doubly linked list from a singly linked list?
you can move forward and backwards in the linked list.

How does insertion work in a linked list, and what is its time complexity?
Say we want to insert in front of the second value in the list, you would move each value to the right in a single linked list and it is in O(n)

Insertion in a linked list involves adjusting pointers. The pointer manipulation itself is O(1), but finding the insertion position may require O(n) traversal. Overall complexity is O(1) for insertion at the head or with a known reference, and O(n) when searching for a specific position.

What are the memory allocation characteristics of a linked list?
Linked lists use heap-allocated objects, which means nodes are stored in memory locations that are typically more expensive than stack memory. Each node is a separate object containing a value and references to other nodes.

What is the time complexity of accessing the head or tail of a linked list?
constant
Accessing the head or tail of a linked list is a constant time operation (O(1)) because the linked list maintains direct references to these nodes

What are the time complexities of deletion in a linked list?
0(N) can still be a computational heavy as you have to traverse the input
Deletion at the head or tail is a constant time operation (O(1)), while deletion in the middle requires traversal, making it more costly with a time complexity of O(n)


Why can prepending and appending to a linked list be fast?
Prepending and appending are constant time operations because you can simply break and rearrange links at the head or tail without traversing the entire list


What is a key weakness of linked lists compared to other data structures?
Linked lists are not contiguous in memory, which means traversal can be costly and they lack the memory optimization benefits of contiguous data structures


How can a linked list be conceptually viewed in relation to other data structures?
Every linked list can be considered a graph and technically a tree, making it a foundational data structure for understanding more complex data structures


What is the primary characteristic of a queue data structure?
First in first out just need to use single linked list

What are the two main operations when inserting an element into a queue?

make the prev head in the head next then make the original header null 
make the tail equal to next

What are the performance characteristics of queue operations?
Both pushing and popping elements from a queue are constant time (O(1)) operations, as they only involve updating pointers and do not require traversing the entire list


What are the performance characteristics of queue operations?

Both pushing and popping elements from a queue are constant time (O(1)) operations, as they only involve updating pointers and do not require traversing the entire list.

A singly linked list is used, which does not require the additional computation time or storage requirements of a doubly linked list.

What additional operation is commonly included with queue implementations?
A peek operation, which allows viewing the first element (at the head) without removing it from the queue, typically accessed via head.value.


What are the primary methods typically implemented in a queue data structure?
The primary methods are enqueue (adding an item to the queue), dequeue (removing an item from the queue), and peek (viewing the first item without removing it)


What is the purpose of having a next property as optional in a queue node?
An optional next property allows flexibility in the data structure, preventing infinite memory creation and accommodating varying numbers of elements in the queue

What are the two key references maintained in a queue implementation?
The two key references are head and tail, which point to the first and last nodes in the queue respectively

What bookkeeping operation is crucial when implementing a queue's dequeue method?
Decrementing the length property is crucial to keep track of the number of items in the queue when removing an item

When adding the first element to an empty queue, what special handling is required?
When the queue is empty, the first element becomes both the head and tail of the queue, and the length is incremented



What is a stack in data structures? 

A stack is a singly linked list where elements are added and removed only from the head, following a Last-In-First-Out (LIFO) principle, similar to a stack of plates where the last item added is the first one removed.

How does the push operation work in a stack?
To push an element in a stack, you point the new element's 'next' pointer to the current head, and then update the head to point to the new element.


How does the pop operation work in a stack?
In a pop operation, you first save the current head, then update the head to point to the next element, effectively removing the top element from the stack.


What makes stack operations efficient?
Stack operations are efficient because they involve constant time pointer manipulations, which do not depend on the number of items in the list or the size of the values.


How are function calls related to a stack?
Function calls are conceptually similar to a stack, with each function call being 'pushed' onto the call stack and 'popped' off when the function completes. The memory used for these calls is literally called the 'stack'.


What is the key difference in node definition when implementing a Stack compared to a traditional linked list?
Instead of using 'next', the instructor uses 'previous' to point to the previous node, which helps with visualization and understanding the stack's structure


What are the two key operations when implementing a Stack data structure?
Push (adding an element to the top of the stack) and Pop (removing the top element from the stack)

How does the pop method handle length to prevent negative values?
By using Math.max(0, this.length - 1) to ensure the length never goes below zero



What are the three main steps when implementing the pop method in a Stack?
Save a pointer to the current head, 2. Update head to point to the previous node, 3. Return the value of the popped node


What are the performance characteristics of accessing elements in an array?
Array access is O(1), meaning it's fast and constant time. You can directly access elements by their index with immediate retrieval.


What is a key limitation when inserting or deleting elements in an array?
Inserting or deleting elements in an array requires manually shifting all other elements, which typically involves writing for loops to move elements and create space for the new value.

How does memory allocation differ between arrays and linked lists?
Arrays allocate all memory upfront, meaning if you want space for 1000 items, you reserve all that memory immediately. Linked lists, in contrast, allocate memory dynamically, creating nodes only when elements are inserted.

What is the primary search mechanism for a linked list?
Linked lists can only perform linear search, which means traversing each element sequentially until the desired item is found. There is no possibility of binary search or direct random access.


What is an example use case where a linked list might be preferred over an array?
A linked list is ideal for scenarios like an async request queue, where you need to efficiently push and pop elements from the head or tail without the performance overhead of shifting array indices.


What are the two primary operations performed in an ArrayList?
push and a pop at constant time

How does an ArrayList handle capacity when adding elements beyond its initial size?
It creates a new array with a larger capacity (often doubled), then copies existing elements to the new array, allowing for dynamic growth


What are the performance characteristics of inserting or deleting elements from the front or middle of an ArrayList?
Inserting or deleting from the front or middle requires shifting all subsequent elements, resulting in an O(N) time complexity


What is the primary difference between an ArrayList's push/pop operations versus enqueue/dequeue operations?
Push and pop at the end are O(1) operations, while enqueue and dequeue from the front require shifting all elements, making them O(N) operations


An ArrayList provides constant-time random access by index and efficient push/pop operations at the end, whereas a Linked List provides efficient insertion and deletion at any point
What are the key advantages of an ArrayList compared to a Linked List?

Click to reveal answer
An ArrayList provides constant-time random access by index and efficient push/pop operations at the end, whereas a Linked List provides efficient insertion and deletion at any point

What is a ring buffer, and what makes its operations unique?
A ring buffer is a data structure where operations like pushing, popping, shifting, and unshifting are O(1), using modulo arithmetic to wrap around an array. It maintains order by using head and tail indices that can move circularly within a fixed-size array.

How does the modulo operator work in the context of a ring buffer?
The modulo operator helps calculate the actual index within the array by taking the remainder when an index exceeds the array's length. For example, if the array size is 10 and the tail is 12, 12 modulo 10 would be 2, wrapping the index back to the beginning of the array.


What happens when a ring buffer needs to resize?
When a ring buffer needs to resize, it creates a new larger buffer, starting at the head and copying elements in order. The head will be set to 0, and the tail will be set to the current length, allowing for additional capacity and continued circular operations.


What is a practical use case for a ring buffer?

A ring buffer can be used in log batching scenarios, where logs need to maintain order while being written. It allows for efficient logging by periodically flushing a batch of logs without blocking the main service, and without requiring complex mutex synchronization.


What is an object pool, and how is it related to ring buffers?
An object pool is a technique for reusing objects instead of creating new ones repeatedly, which can improve performance and memory usage. While ring buffers can be used for object pooling, a simple ArrayList is often sufficient if the order of object creation is not important.  


What are the three components that are used when a function is called?
Return address (where the function was called from), 2) Return value (the value to be returned), and 3) Arguments (the input parameters)


What are the three steps of recursion when breaking down the recursive process?
Pre-operation (something done before recursion), 2) Recursion (actual function call), and 3) Post-operation (something done after recursion)

What is the most critical aspect of creating a recursive function?
Establishing a clear and correct base case. Without a proper base case, recursion becomes extremely difficult to implement and can lead to infinite loops.

How does a recursive function typically terminate its recursive calls?
By reaching a base case, where the function no longer calls itself and instead returns a specific value or performs a final operation

What happens to the function call stack during a recursive process?
The stack grows downward as recursive calls are made, then unwinds upward as each function returns its calculated value, with each function adding its own computation to the final result

What are the four directions that can be explored when solving a maze recursively?
up down right left

What are the four base cases to consider when implementing a recursive maze?
Out of bounds, hit a wall, are we at the end point, and have we seen it

Why is it important to track previously visited titles in a recursive maze solver?
We can find ourselves in a loop forever

What data structures can be used to track visited tiles in a recursive maze solving algorithm?
A 2D boolean array, where false indicates an unvisited tile and true indicates a tile that has been previously explored

What happens if a recursive maze solving algorithm does not prevent revisiting tiles?
It can lead to an infinite loop that eventually causes a stack overflow, as the function keeps calling itself repeatedly on the same tiles

What are the three steps in recursion?
Find base case (Pre), find recursive case(recurse), your conclusion (post) 

What is the purpose of using direction arrays in recursive maze solving?
o systematically explore different directions (left, right, up, down) when navigating through a maze

When is recursion typically recommended over using a for loop?

When there is no defined end point, or when there is a significant branching factor that makes linear iteration difficult

What must be tracked when using recursion for pathfinding?
Maintaining a path array, marking visited locations, and tracking the current position

What is an important consideration when implementing a recursive function?
Clearly defining the base case to determine when to stop recursing, which helps reduce complexity and improve readability\

What is the core principle of the Divide and Conquer algorithm strategy?
Divide and Conquer involves splitting input into smaller chunks, solving those subsets progressively, and repeatedly splitting until reaching a fundamental unit that can be easily solved.

In QuickSort, what is a 'pivot' and how is it used in the sorting process?
This is the middle point in which we do our compartmentalizing from.

A pivot is an element used to partition the array, with elements less than or equal to the pivot placed on one side, and elements greater than the pivot placed on the other side.

What are the potential time complexity ranges for the QuickSort algorithm?
nlogn for good scenarios 
n2 for bad scenarios

What makes QuickSort perform poorly in its worst-case scenario?

When sorting a reverse sorted array, QuickSort can degrade to O(n squared) time complexity because each pivot selection results in an unbalanced partition.

How does QuickSort handle sorting an array recursively?
QuickSort recursively divides the array by selecting a pivot, partitioning elements around the pivot, and then applying the same process to the subarrays until the entire array is sorted.