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