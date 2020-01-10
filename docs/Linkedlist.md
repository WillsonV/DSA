# Linked List

Linked list is linear DS that stores elemenst in a non- contiugious  mannner.

## L2

 problems with array w.r.t Linked list:
 1.  Either size is Fixed and pre-allocated (in both local and dynamic array) OR  Worst case insertion at end is thetha(n).
 2. Inserion at middle(or begining ) is costly.
 3. Deletion at middle(or begining ) is costly.
 4. Implimentation of other DS like queue,dequeue is complex if we impliment them with array.
 
 ####  Problems with arrays
 
 1. 1)How to impliment robin round scheduling using array DS??
 > In RR scheduling every process is given a quantam of time ,if  a process still have it's execution time left then it's moved to the end of queue ,if process is completed it;s execution them it' s removed from queue.
         
 2.         
 



## L7

### Detect loop in a linked list

What is Loop in LL: when next pointer of a the node in linked list points to the already existing node of the linked list.

## Approach to detect loop in linked list:

1. Naive approach (Hashing technique)
   - Traverse the linked list .
   - while traversing ,for every node keep checking if next of that node contains the address of some already existing node of linked          list.
  >> T.C=O(n^2)

