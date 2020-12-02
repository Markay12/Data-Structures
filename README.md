# Data Structures
---

# Table of Contents

1. Whats wrong with linked lists?
2. Binary Trees
3. Binary Search Trees

---
---


# Whats wrong with Linked Lists?

<a href="url"><img src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.cs.usfca.edu%2F~srollins%2Fcourses%2Fcs112-f07%2Fweb%2Fnotes%2Flinkedlists%2Fll2.gif&f=1&nofb=1" align="center" height="175" width="340" ></a>

* Arrays 
	-  (+) Indexed
	- (+) Exploitable memory pattern
	- (-) Fixed Size
	- (-) Waste of Time and Space

* Linked Lists
	- (+) Exactly the size we need them to be
	- (+) Fully dynamic
	- (-) No exploitable memory
	- (-) Slow
	
Linked lists can't be searched quickly  
Even with modifications


# Binary Trees

*  Gives us two links per node
	-  Similar to a Doubly Linked list node, with a major difference
	-  *structured top-down*
	

This is  opposite of the linear progression of a linked list

## Properties

Unique path must exist from the root to every other part of the tree  
The tree is also organized into subtrees

* This is the left and right sides of the tree respectively
	- Can keep being broken down until we reach the final node
	

## Organization

Nodes are organized into levels and depth

Depth

* Number of edges from root to the node
* starts at index 0

Level

* Depth + 1

Some sources may have these terms changed, level may mean depth to someone else  
This is the definition that we chose to use

Height

* Moves backwards
	- Number of edges in the longest path starts at one
	
Height == MAX Depth

* Max level - 1

The maximum number of nodes any level can have is the power of two  
Each level can have  2^(depth) number of nodes  

* 2^(level - 1) is also acceptable

The max possible nodes in the tree is the sum of the max number of nodes that is equal to its height

Full Tree: Every node has *two children* AND all leaves are on the same level

Complete Tree: A binary tree where every level, except the last, is full and the nodes are as far left as possible

* A complete tree is not necessarily a full tree
* A full tree is always complete
* A tree can be both **complete and full**

If we know that a tree is full and we know how many nodes, we can know the height of the tree  
2^(height + 1) - 1 = N  
2^(height + 1) = N + 1


## Run Time
Our tree height dictates run time  
O(log(n)) is fast

* Binary search fast


## Searching Binary Trees

![Binary Search Trees](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.basicsbehind.com%2Fwp-content%2Fuploads%2F2014%2F12%2FBinary-search-tree.png&f=1&nofb=1)

Brute force algorithm

1. Is this the node we are looking for? STOP
2. If not, put children of that node in a Queue
3. Pop the front of the queue and return to Step #1

1. Start at the root
2. Search level by level, until you find the element you are searching for or we reach a leaf


### Binary Search Tree Property

* If the value stored at the node is **greater** than the value stored in its left Child and stored at the node less that its right child

