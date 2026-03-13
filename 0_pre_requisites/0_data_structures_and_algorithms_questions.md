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