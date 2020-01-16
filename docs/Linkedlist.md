# Linked List

Linked list is linear DS that stores elemenst in a non- contiugious  mannner.

## L2

 problems with array w.r.t Linked list:
 1.  Either size is Fixed and pre-allocated (in both local and dynamic array) OR  Worst case insertion at end is thetha(n).
 2. Inserion at middle(or begining ) is costly.
 3. Deletion at middle(or begining ) is costly.
 4. Implimentation of other DS like queue,dequeue is complex if we impliment them with array.
 
 #### Problems with arrays
 
 1. 1)How to impliment robin round scheduling using array DS??
 > In RR scheduling every process is given a quantam of time ,if  a process still have it's execution time left then it's moved to the end of queue ,if process is completed it;s execution them it' s removed from queue.
         
 2.         
 



## L7

### Detect loop in a linked list

What is Loop in LL: The next of last node instead of being null points to some earlier node of linked list.  In general -> when next pointer of a the node in linked list points to the already existing node of the linked list.


### Approach to detect loop in linked list:

1. Naive approach (H̶a̶s̶h̶i̶n̶g̶ ̶t̶e̶c̶h̶n̶i̶q̶u̶e̶) O(n^2)
   - Traverse the linked list .
   - while traversing ,for every node keep checking if next of that node contains the address of some already existing node of linked          list.
  > T.C=O(n^2)
     Implimentaion: - Traverse LL. 
                     - store next of current node in temp var
                    - Again Traverse LL till current node.
                     * ``` - if(temp==any of previous node till curr)
                              loop exists.
                       else
                        No loop
                        ```
                    
     
     
2.  #### By modidfying  Node Structure[Use visited Flag ]  O(N)
       


3. ####  By Mdoifying Linked List pointers [Dummy node Approach]  O(N)

4. ####  Use Hashing  O(N)
