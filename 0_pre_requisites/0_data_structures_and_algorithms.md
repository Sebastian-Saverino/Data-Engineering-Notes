What are data structures and algorithms?
We are going to use a actual course for this because why not, we are commited to doing software engineering and data engineering so might as well do a course for this

I want to preface this section can either be super complicated but understand that we use data structures and algoritms all the time, databases have b trees an other things, simply put data structures and algoritms are the big brain ideas behind why a print fuctions works or why we can hold data in a list in python, the logic behind this had to be coded in a way the computer can understand which can be a whole lot, being aware of data structures and algorithms is important and knowing when to use them is just as important like tools in a toolbox. This is how you gain "aura" in the world of computers. This is the idea of how we use data structures and algorithms to be EFFICIENT!

First what is the definition of a data structure? Data structure is a data storage forma that enables efficient access and modification

What is an algorithm?

An unambigous, finite, sequence of intrcutions to solve a problem

reference: DSA

What is Big O notation?

Big O is a way to categorize your algorithms time or memory requirements based on input. This is meant to generalize the growth of an algorithm, I see it as an equation to figure what is the best way to figure what is the best algorithm to use based on your needs.

Hint: Look for loops this can tell us what time complexity we're using

constants are always dropped say you have two algoritims that loop through so see each value

The cost of processing one element is constant, and we repeat that constant operation n times, which results in O(n).

Constants are in theory not in important as they don't change the time complexity.

The big question we're asking is, how does the algo grow? So we're not as understanding of.

In interview questions they do a problem where the list stops at the end of the list to effect O(n) but remember we care about the algo not the constants

When we talk about space and time complexity Growth is with respect to the input constants are dropped worst case is usually the way we measure

Big O Chart

O(1) O(n2) O(n3)

O(logn) Binary search tress

O(n) O(nlogn) Quicksort

O(n^2)

O(2^n)

o(n!)

O(sqrt(n))

## Array Data Structure
What is an array?

It is a unbreaking memory space with a certain amount bytes.

What you said:

"a[0] is just asking to view those bytes in memory through the array"

That is basically correct, but more precisely:

a[0] means "go to the memory location that represents the first element of the array and interpret those bytes as an integer."

So the array acts like a structured way to access raw memory.