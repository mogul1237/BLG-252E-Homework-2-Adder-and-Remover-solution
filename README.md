# BLG-252E-Homework-2-Adder-and-Remover-solution

Download Here: [BLG 252E Homework #2 (Adder and Remover) solution](https://jarviscodinghub.com/assignment/blg-252e-homework-2-adder-and-remover-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

1 Introduction
In this assignment, you will implement an adder remover in which the program will implement the primary operations for the diﬀerent container classes to handle the storage and processing of data.
2 Container (Data Storage) Classes
A container (collection) is a way that organizes storage of data in memory. The primary operations for the container classes which you are asked to implement are: • add: The function for adding element to the appropriate place of the list. • remove: The function for removing element from the appropriate place of the list. • removeAll: The function for deleting all elements in the list. • display: The function for printing AdderRemover list elements from ﬁrst element to last element to the screen. • setTraverser: The function for setting/initializing traverser property to desired traverser strategy. • traverse: The function for printing AdderRemover list elements using traverser.
3 The Problem Statement
You are going to implement diﬀerent container classes to store data of integer. You will use doubly linked list representation to store elements. You are not allowed to use any STL containers in this homework. You should create your own classes. First of all, deﬁne AdderRemover base class depicted in Figure 1 to extend classes and write polymorphic functions. Its add, remove and setTraverser methods are pure virtual since there are diﬀerent strategies to add, remove and traverse elements from its internal list. This internal data structure is a doubly linked list of integer elements. However, derived classes will directly use inherited display, removeAll and traverse methods.
AdderRemover # head: Node * # tail: Node * # name: string # nodeCount: int # traverser: ARTraverser * + add(..) + remove() + setTraverser() + display() + removeAll() + traverse()
ARTraverser # current: Node* + hasNode() + next()
has 1
Figure 1: Structure of the AdderRemover and ARTraverser Classses.
Some of the strategies (classes) for adding and removing elements from their internal lists are the following :
1. First Add First Remove (FAFR): When a new elements to be added, it adds to the beginning of the list, an element to be removed it removes from the beginning of list.
1
2
2. First Add Last Remove(FALR): When a new elements to be added, it adds to the beginning of the list, an element to be removed it removes from the end of list.
3. Last Add First Remove (LAFR): When a new elements to be added, it adds to the end of the list, an element to be removed it removes from the beginning of list.
4. Last Add Last Remove (LALR): When a new elements to be added, it adds to the end of the list, an element to be removed it removes from the end of list.
Secondly, deﬁne ARTraverser abstract class. It oﬀer a way of getting sequential access to all elements of a container class. It will be used to “read” data from a container. Its two methods: • hasNode: Returns true if the list has element. • next: Returns the current element in the list and advances the current position. are pure virtual since they should be implemented appropriately for each type of strategies. Two strategies will be deﬁned:
1. First AdderRemoverTraverser (ARTF): It is used to traverse through a container from the beginning element to the end element. FAFR and FALR classes are going to use this strategy as its traverser.
2. Last AdderRemoverTraverser (ARTL): It is used to traverse through a container from the end element to the beginning element. LAFR and LALR classes are going to use this strategy as its traverser.
4 Main Program
In main program, declare an array of pointers for base class AdderRemover. The pointer array will be a polymorphic array which will store memory addresses of four diﬀerent types of AdderRemover objects (FAFR, FALR, LAFR, LALR). Figure 2 shows an example of the objects involved. You would add/remove elements to polymorphic array FAFR, FALR, LAFR, LALR instances in order to test whether the functions work well or not. Your program should print the name, nodeCount and the elements of internal list as separate groups (Figure 3).
Figure 2: Pointer array of AdderRemover base class
5 Implementation Notes • Consider OOP approach in your design with well-chosen variable, method, and class names and comments where necessary. You would get 0 from implementation that do not contain inheritance and polymorphism. • Your program should compile and run on Linux environment using g++ (version 4.8.5 or later). You can test your program on ITUs Linux Server using SSH protocol. • Your homework assignments SHOULD NOT include any copy-paste material (from the Internet or from someone elses paper/thesis/project). Check the Academic honesty section in the syllabus. • For any questions about the assignment, contact Hasan Kivrak directly (oﬃce no: Research Lab3) or via mail (kivrakh@itu.edu.tr)
3
6 Test Code
Your program will be tested using below test code and expected to have desired output.
Figure 3: Example Test Code and Output
