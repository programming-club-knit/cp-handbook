<a name="br1"></a> 

**Module on Queue Data Structure**

Introduction to Queues:

A queue is a linear data structure that follows the FIFO (First In

First Out) principle. This means that the element which is inserted

ﬁrst will be the one to be removed ﬁrst. Think of it like a queue of

people waiting for a bus to go to a particular destination, where

the person who arrived ﬁrst gets on the bus ﬁrst and the person

who enters at last will exit ﬁrst.

Properties of Queue:

->FIFO (First In First Out): The element that is added ﬁrst is the

one that gets removed ﬁrst.

->Linear Data Structure: Queue elements are arranged in a linear

sequence.

->Two Ends: A queue has two ends, namely the front and the rear.

Elements are added to the rear end and removed from the front

end.

->Dynamic Size: Queues can be of ﬁxed size or dynamic size,

depending on the implementation.

Types of Queues:

1\. Simple Queue: A basic queue where elements are inserted at

the rear end and removed from the front end.

Circular Queue: A queue where the rear end is connected to the

front end, forming a circle. This allows for eﬃcient space

utilization in a ﬁxed-size queue.



<a name="br2"></a> 

2\. Priority Queue: A queue where elements have associated

priorities, and the element with the highest priority is dequeued

ﬁrst.

3\. Double Ended Queue (Deque): A queue that supports insertion

and deletion at both ends.

Applications of Queue:

1\. Job Scheduling: Queues are used in job scheduling algorithms

like First-Come-First-Serve (FCFS) scheduling.

2\. Breadth-First Search (BFS): Queues are utilized in graph

traversal algorithms like BFS to explore nodes level by level.

Buffer Management: Queues are used in managing buffers in

operating systems and networking.

3\. Printing Queues: Queues are used to manage print jobs in

printers.

4\. CPU Scheduling: Queues are used in CPU scheduling

algorithms to manage processes waiting to be executed.

Implementation:

5\. Queues can be implemented using arrays, linked lists, or other

data structures. The choice of implementation depends on the

requirements such as dynamic size, eﬃciency, etc.

Array Implementation:

->Uses an array to store queue elements.

->Requires additional logic to handle wrap-around in circular

queues.

->Can have ﬁxed or dynamic size.

Linked List Implementation:

->Uses a linked list to store queue elements.



<a name="br3"></a> 

Allows for dynamic size without worrying about resizing.

Eﬃcient for frequent insertions and deletions.

Complexity Analysis:

Time Complexity:

->Enqueue: O(1)

->Dequeue: O(1)

->Front: O(1)

->Rear: O(1)

Space Complexity: O(n)

Operations on Queue:

1\. Enqueue (Insertion): Adds an element to the rear of the queue.

2\. Dequeue (Deletion): Removes an element from the front of the

queue.

3\. Front: Returns the element at the front of the queue without

removing it.

4\. Rear: Returns the element at the rear of the queue without

removing it.

5\. isEmpty: Checks if the queue is empty.

6\. isFull: Checks if the queue is full (applicable in a ﬁxed-size array

implementation).



<a name="br4"></a> 

**Queue Implementation using STL:**



<a name="br5"></a> 

**Queue Implementation:**

**In software terms, the queue can be viewed as a set or collection of**

**elements as shown below. The elements are arranged linearly.**

**We have two ends i.e. “front” and “rear” of the queue. When the**

**queue is empty, then both the pointers are set to -1.**

**The “rear” end pointer is the place from where the elements are**

**inserted in the queue. The operation of adding /inserting elements in**

**the queue is called “enqueue”.**

**The “front” end pointer is the place from where the elements are**

**removed from the queue. The operation to remove/delete elements**

**from the queue is called “dequeue”.**

**When the rear pointer value is size-1, then we say that the queue is**

**full. When the front is null, then the queue is empty.**

**Enqueue**

**In this process, the following steps are performed:**



<a name="br6"></a> 

**● Check if the queue is full.**

**● If full, produce overflow error and exit.**

**● Else, increment ‘rear’.**

**● Add an element to the location pointed by ‘rear’.**

**● Return success.**

**Dequeue**

**Dequeue operation consists of the following steps:**

**● Check if the queue is empty.**

**● If empty, display an underflow error and exit.**

**● Else, the access element is pointed out by ‘front’.**

**● Increment the ‘front’ to point to the next accessible data.**

**● Return success.**

**Next, we will see a detailed illustration of insertion and deletion**

**operations in queue.**

**Illustration**

**This is an empty queue and thus we have rear and empty set to -1.**

**Next, we add 1 to the queue and as a result, the rear pointer moves**

**ahead by one location.**



<a name="br7"></a> 

**In the next figure, we add element 2 to the queue by moving the rear**

**pointer ahead by another increment.**

**In the following figure, we add element 3 and move the rear pointer by**

**1.**

**At this point, the rear pointer has value 2 while the front pointer is at**

**the 0th location.**

**Next, we delete the element pointed by the front pointer. As the front**

**pointer is at 0, the element that is deleted is 1.**



<a name="br8"></a> 

**Thus the first element entered in the queue i.e. 1 happens to be the**

**first element removed from the queue. As a result, after the first**

**dequeue, the front pointer now will be moved ahead t0 the next**

**location which is 1.**

**Array Implementation For Queue:**

->Uses an array to store queue elements.

->Requires additional logic to handle wrap-around in circular

queues.

->Can have ﬁxed or dynamic size.

Using array Queues can be implemented as given below:



<a name="br9"></a> 



<a name="br10"></a> 



<a name="br11"></a> 



<a name="br12"></a> 

**Additional resources:**

**1. [Queue**](https://leetcode.com/tag/queue/)[** ](https://leetcode.com/tag/queue/)[-**](https://leetcode.com/tag/queue/)[** ](https://leetcode.com/tag/queue/)[LeetCode**](https://leetcode.com/tag/queue/)**

**2.[Queue**](https://www.geeksforgeeks.org/queue-data-structure/)[** ](https://www.geeksforgeeks.org/queue-data-structure/)[Data**](https://www.geeksforgeeks.org/queue-data-structure/)[** ](https://www.geeksforgeeks.org/queue-data-structure/)[Structure**](https://www.geeksforgeeks.org/queue-data-structure/)[** ](https://www.geeksforgeeks.org/queue-data-structure/)[-**](https://www.geeksforgeeks.org/queue-data-structure/)[** ](https://www.geeksforgeeks.org/queue-data-structure/)[GeeksforGeeks**](https://www.geeksforgeeks.org/queue-data-structure/)**

**3.[Queue**](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[** ](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[Data**](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[** ](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[Structure**](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[** ](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[-**](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[** ](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[Tutorialspoint**](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)**

**4.[Queues**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[-**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[Solve**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[Data**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[Structures**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[|**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[HackerRank**](https://www.hackerrank.com/domains/data-structures/queues)**

**Practice problems as much as possible in order to**

**get a good command on queue from above**

**mentioned resources….**

**Happy coding…**

