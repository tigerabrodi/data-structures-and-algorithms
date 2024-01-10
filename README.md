# Introduction

Data Structures and Algorithms focuses on problem solving.

Foundations of programming are required.

# What are Data Structures?

Coding is just manipulating data in a way so that you can accomplish a task.

There are values and relationships between them.

We can remove, insert, and manipulate data.

Data Structures have different kinds of relationships and different ways of storing data.

Data structures are a particular way of organizing data in a computer so that it can be accessed and modified efficiently.

Data structures are categorized into two main types: primitive and non-primitive. Primitive data structures include basic types like integers, floats, and characters, while non-primitive structures, which are more complex, include arrays, lists, trees, and graphs.

# Complexity Analysis

The process of determining how efficient an algorithm is. It is a measure of how much time and space an algorithm requires to run.

These are called time complexity and space complexity.

# Memory

Memory can be visualized as a canvas. Memory canvas is bounded. We have a finite amount of memory. Your program will store your variables in memory slots or a row of memory slots for related data e.g. arrays.

In a computer, memory is organized as a large number of bytes. Each byte is used to store value and has a unique address. The computer can perform read or write operations to these addresses.

Each byte has 8 bits. Each bit can be either 0 or 1. A bit is the smallest unit of memory. A byte is the smallest addressable unit of memory.

A memory block is a section of computer memory where each byte is right next to its neighbor, without any gaps or interruptions This arrangement makes it easier for the computer to read and write multiple pieces of related data.

You often use memory blocks for storing groups of data that belong together, such as the elements in an array or the characters in a string. By keeping them arranged like that, the computer can access and manage the data more efficiently.

Different computer architectures have different memory block sizes. For example, a 32-bit computer has a memory block size of 32 bits, or 4 bytes. A 64-bit computer has a memory block size of 64 bits, or 8 bytes. This means that e.g. numbers on a 32-bit computer are stored in 4 bytes, while numbers on a 64-bit computer are stored in 8 bytes. So the computer needs to find 4 bytes of free memory to store a number on a 32-bit computer, but 8 bytes of free memory to store a number on a 64-bit computer.

ASCII is a character encoding standard that assigns each character a number between 0 and 127. For example, the ASCII number for the character A is 65, and the ASCII number for the character B is 66. The ASCII number for the character 0 is 48, and the ASCII number for the character 9 is 57.

## Pointers

Pointers are variables that store the memory address of another variable. They are used to store the addresses of other variables. So in memory, a pointer would be stored in a memory slot, and it would point to another memory slot.

## Computer accessing memory

Computer is able to access memory given a memory address very fast.

# Big O Notation

Big O notation is a way of describing how fast the runtime grows relative to the input as the input gets arbitrarily large.

Different algorithms can have different runtimes for the same input. And they would grow at different rates as the input gets arbitrarily large.

Different O notations:

- O(1) - **Constant Time:** The runtime is the same regardless of the input size e.g. accessing an array element by index.
- O(log n) - **Logarithmic Time:** The runtime grows logarithmically in proportion to the input size. This means that as the input gets arbitrarily large, the runtime grows very slowly e.g. if problem is divided in half each time.
- O(n log n) - **Linearithmic Time:** The runtime grows in proportion to N log N of the input size. This means that as the input gets arbitrarily large, the runtime grows faster than linear time but slower than quadratic time e.g. sorting algorithms
- O(n) - **Linear Time:** The runtime grows directly in proportion to the input size. This means that as the input gets arbitrarily large, the runtime grows at the same rate e.g. iterating through an array.
- O(N^2) - **Quadratic Time:** The runtime grows quadratically in proportion to the input size. This means that as the input gets arbitrarily large, the runtime grows very fast e.g. nested loops.
- O(2^n) - **Exponential Time:** The runtime grows exponentially in proportion to the input size. This means that as the input gets arbitrarily large, the runtime grows even faster than quadratic time e.g. recursive algorithms that solve a problem of size N by recursively solving two smaller problems of size N-1.

## Mathematical term

Asymptotic analysis is a method of describing limiting behavior. It is used in many branches of mathematics, but especially in mathematical analysis of algorithms. It looks like this:

```
f(n) = O(g(n))
```

As N grows towards infinity, how does the runtime of the algorithm grow?

## What is N?

Abstract concept of input size. It is the number of elements in the input.

## Accessing in memory

Accessing memory is O(1) constant time. If we had to access a number in a 32 bit computer, we would need to access 4 bytes of memory. If we had to access a number in a 64 bit computer, we would need to access 8 bytes of memory. It is constant time because it doesn't matter how big the number is, we still access it via the address.

## Simplify Big O

We focus on how the runtime grows towards infinity. We drop the constants and coefficients. In Big O notation, you only keep the term that grows the fastest as the input size increases. This term is known as the dominant term.

When we have more complex big O expressions, we drop the less significant terms. Because as N grows towards infinity, the less significant terms become insignificant.

If you've different inputs, you can use different variables to represent them. For example, if you have two arrays of different sizes, you can use N and M to represent their sizes. But do not drop any of the variables.

**Drop Lower Order Terms:** In O(n^2 + n), the n term is much smaller than n^2 for large n, so it's dropped, simplifying to O(n^2).

**Ignore Coefficients:** Big O ignores constants because it's about growth rates. For example, O(2n) simplifies to O(n), and O(5n^2) simplifies to O(n^2).

# Logarithm

A logarithm is essentially another way of expressing exponentiation, which is the process of multiplying a number by itself a certain number of times. For instance, \(2^3 = 2 \times 2 \times 2 = 8\). The logarithm asks the question: "To what power do we raise a base number (like 2 in this example) to get another number?"

So, in our example, the logarithm of 8 with base 2 is 3 (written as \( \log_2 8 = 3 \)) because 2 raised to the power of 3 is 8.

Parts of a logarithm:

1. **Base:** This is the number that is being raised to a power. In \( \log_2 8 \), 2 is the base.
2. **Argument:** This is the number you want to find the logarithm of. In \( \log_2 8 \), 8 is the argument.
3. **Exponent:** This is the answer to the logarithm, the power to which the base must be raised to get the argument. In \( \log_2 8 = 3 \), 3 is the exponent.

## Explaination

Log of 2 to N = Y iiF (only if) 2^Y = N

Example: log of 2 to 8 = 3 because 2^3 = 8

2^4 = 16

If we double right side of equation, we add 1 to left side of equation.

This means: 2^5 = 32

## Input in O notation

Log of N, this means when N doubles, the runtime only increases by 1. This is good. This is better than linear time because linear time would increase by 2.

2^20 = 1,048,576
2^30 = 1,073,741,824

It's so powerful because as N grows, the runtime grows very slowly.

## Logarithm in Big O

Usually algorithms that involve dividing problems in half have logarithmic time complexity.

# Arrays

Let's say we have [1, 2, 3]. The program has to store this in memory. Imagine we have a 64 bit computer. Each number is 8 bytes. So we need 24 bytes of memory to store this array. The computer needs to find 24 bytes of free memory to store this array.

For recap: A byte consists of 8 bits. A bit is the smallest unit of memory. A byte is the smallest addressable unit of memory.

We have two types of arrays: static and dynamic.

## Static Arrays

Static arrays have fixed size. You have to specify the size of the array when you declare it. You can't add or remove elements from a static array. You can only update existing elements.

### Big O Notation

#### Get

Getting an element by index is O(1) constant time. This is because the computer can access the memory address of the element directly. It knows where the first element is stored. From there, it can calculate the memory address of the targetted element.

#### Set

Setting an element by index is O(1) constant time. It is simply swapping binary values.

#### Initialize

Initializing an array is O(n) linear time. This is because the computer has to initialize each element in the array.

#### Traverse

Traversing an array is O(n) linear time. This is because the computer has to traverse each element in the array.

#### Copy

Copying an array is O(n) linear time. The computer first has to traverse each element in the array. Then it has to copy each element to the new array. In memory, the computer has to find a new block of memory to store the new array.

People will do this mistake during coding interview by thinking that copying an array is O(1) constant time. This is because they think that the computer can just copy the memory address of the array. But this is not true. The computer has to copy each element to the new array. In memory, the computer has to find a new block of memory to store the new array. You don't just simply copy.

#### Insert

Let's say we want to insert at place X. For the rest of the bytes in memory, we have to shift them to the right. However, the problem is that there may not be any space to the right. We would have the same problem if we want to insert at the beginning or end of array.

When you insert to the array, no matter what position, the computer has to copy the entire array and find a new block of memory to store the new array.

Inserting an element is O(n) linear time.

#### Pop

Pop means removing the last element of the array. This is O(1) constant time. This is because the computer can just remove the last element. It doesn't have to copy the entire array.

## Dynamic Arrays

Dynamic arrays is an array that can grow and shrink in size. It is implemented by using a static array under the hood. When the array is full, we create a new array with double the size. Then we copy the elements from the old array to the new array. Then we delete the old array.

### Big O Notation

#### Insert

Inserting an element is typically O(1) constant time for Dynamic Arrays. Because Dynamic Arrays allocate extra space. So when we insert an element, we don't have to create a new array and copy the elements over. We can just insert the element into the extra space.

However, we have to check if the array is full. If it is full, we have to create a new array with double the size. Then we copy the elements from the old array to the new array. Then we delete the old array. This is O(n) linear time. But we don't do this every time we insert. We only do this when the array is full.

Because the worst case is O(n) linear time, we say that inserting an element is O(n) linear time.

## Interview

When doing interviews and using JS, you can use the built in array e.g. treating it as a queue. Explain to the interviewer you understand the big O of the built in array appears efficient in one way but in reality it is different.

But you do not wanna have to go through the trouble of importing a queue data structure. So you can use the built in array as a queue.

# Amortized Analysis

Amortized analysis averages the time required to perform a sequence of data structure operations over all the operations performed. Unlike average-case analysis, which considers probabilities of different inputs, amortized analysis guarantees the average performance of each operation in the worst case.

It provides a more realistic expectation of the algorithm's performance, especially when the algorithm has occasional costly operations.

# Linked Lists

Linked List is stored differently in memory.

**Singly Linked List:** Each element is a node. Each node has a value and a pointer to the next node.

**Doubly Linked List:** Each element is a node. Each node has a value and a pointer to the next node and a pointer to the previous node.

**Circular Linked List:** Each element is a node. Each node has a value and a pointer to the next node. The last node points to the first node.

In memory, arrays are stored in a block of memory.

Nodes of Linked Lists are dynamically allocated in the heap as the list grows. They don't occupy contiguous memory locations. Instead, each node can be anywhere in memory. The pointers in each node are used to "link" these scattered pieces together logically.

## Big O Notation

### Get

Get an element by index is O(n) linear time. This is because the computer has to traverse each node in the linked list.

### Set

Set an element by index is O(n) linear time. This is because the computer has to traverse each node in the linked list.

### Init

### Copy

Copy is O(n) linear time.

### Traverse

Copy is O(n) linear time.

### Insert

Insert is O(n) linear time. This is because the computer has to traverse each node in the linked list. Find the node and then change the pointers.

### Delete

Copy is O(n) linear time.

## Array in memory

Imagine a row of boxes, each representing an array element, placed side by side. The address of each element is predictable based on the array's base address and the size of each element.

```
| Element 0 | Element 1 | Element 2 | Element 3 | ... | Element N |
|-----------|-----------|-----------|-----------|-----|-----------|
 0x00A      0x00B       0x00C       0x00D      ...   0x00Z
```

## Linked List in memory

Think of each node as a separate entity, potentially scattered in memory. Each node contains its data and a pointer, which acts like an arrow pointing to the next node. The actual memory addresses of these nodes are not sequential.

```
[Node 0: Data | Ptr] --> [Node 1: Data | Ptr] --> [Node 2: Data | Ptr] --> ...
   0x100          |        0x1A2          |        0x03F          |
                  -------------------------        ----------------
```

Depending on the system, 32 or 64 bit, Linked List would take up e.g. in 64 bit system, 16 bytes of memory. 8 bytes for data and 8 bytes for pointer.

How it may look like for a 32 bit system:

```
[ Node 0 ]     [ Node 1 ]     [ Node 2 ]
| 4 bytes | 4  | 4 bytes | 4  | 4 bytes | 4
| Integer | Ptr| Integer | Ptr| Integer | Ptr
 0x100     0x104 0x108   0x10C 0x110   0x114
```

## Advantages over array

- **Dynamic Size:** Capable of growing and shrinking as needed during runtime.
- **Efficient Insertions/Deletions:** Especially at the beginning or in the middle, without the need to shift elements as in arrays.
- **Memory Utilization:** More efficient memory usage since it allocates memory as needed.

## Disadvantages over array

- **Memory Overhead:** Each node requires extra memory for a pointer, which can be significant, especially in systems with limited memory.
- **No Random Access:** Accessing elements is not as straightforward as in arrays, as it requires sequential access from the beginning of the list.
- **Increased Complexity:** Implementing and managing linked lists can be more complex than arrays, with additional considerations for pointer manipulation and potential issues like memory leaks.
