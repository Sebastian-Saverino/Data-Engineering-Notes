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


How to index an array.

It takes the width then multiples by the offset then goes and get it at the memory address


address = base + (offset × width)

Example:

base = 1000
offset = 2
width = 4

1000 + (2 × 4) = 1008

Arrays don't insert, they overwrite go the a value

When it comes to deletion, it is a little more simple as its will make the value 0 so a null value.

Arrays are constant time, no matter the change nothing changes. THis made sense!! Felt a little smart.


You cannot grow an array as it is continiguous memory chunks it will fall over to the next memory chunk which could remove data.

So each element occupies 4 bytes worth of addresses (1000, 1001, 1002, 1003 all belong to arr[0]), but you only need to remember that each "step" is 4 addresses wide.
Everything else you said is spot on — index × width + base address, and you land exactly on the right chunk of memory.



Our first search, 

so how do we search on an array

# Linear search:

a[v1,v2,v3,v9]

search(a,v8)

We look for the worst case 
We are asking to look through the array and find v8, this goes through each value in a the array making it O(n)
Since it is constant


# Binary Search

When we look at our data, we ask, is it ordered?


### Simple Explanation of Binary Search

**Binary search** is a way to find something in a **sorted list** by repeatedly checking the **middle element** and eliminating half of the remaining items.

Instead of looking at every item one by one, binary search **cuts the search space in half each time**.

---

### Example

Sorted list:

```
[1, 3, 5, 7, 9, 11, 13, 15]
```

We want to find:

```
13
```

---

### Step 1 — Look at the Middle

```
[1, 3, 5, 7, 9, 11, 13, 15]
             ↑
```

Middle value = **9**

Since **13 > 9**, the number cannot be on the left side.

So we **throw away half the list**.

---

### Step 2 — Search the Remaining Half

```
[11, 13, 15]
      ↑
```

Middle value = **13**

We found it.

---

### Why It’s Fast

Each step removes **half of the remaining elements**.

Example with 1,000,000 items:

| Step | Items Remaining |
| ---- | --------------- |
| 1    | 1,000,000       |
| 2    | 500,000         |
| 3    | 250,000         |
| 4    | 125,000         |
| ...  | ...             |
| ~20  | 1               |

So even with **1 million items**, it only takes about **20 checks**.


---

### One Sentence Summary

**Binary search works by repeatedly checking the middle of a sorted list and eliminating half of the remaining elements until the target is found.**


If the input halves at each step it is either O(LogN) or O(NlogN)





