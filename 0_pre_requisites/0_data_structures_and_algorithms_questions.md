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
