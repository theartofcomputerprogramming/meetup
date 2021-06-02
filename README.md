# TAOCP - The Art Of Computer Programming Reading Group Meetup

https://www.meetup.com/theartofcomputerprogramming

## Next TAOCP Meetup

[TAOCP #37 - Binary Merge](#taocp-37---binary-merge-chapter-5-sorting-section-532)\
Saturday, 5 Jun 2021, 2-4pm America/New_York

## Next Papers Meetup

[Papers #1 - Binomial Heaps, Jean Vuillemin, 1978](#papers-1---binomial-heaps-jean-vuillemin-1978)\
Wednesday, 26 May 2021, 7-9pm America/New_York

## Description

We are devoted to reading, understanding and working through The Art Of Computer Programming by Donald Knuth (TAOCP). We go through a portion of TAOCP at each meetup. Text is read out and discussed. We work on some simple and medium exercises.

The world is fortunate that over 50 years ago a person like Donald Knuth undertook an epic quest of bringing "readers to the frontiers of knowledge in every [computer science] subject that was treated". Later realizing that "the rapid rise of computer science made such a dream impossible", he decided to "concentrate on classic techniques that are likely to remain important for many more decades, and to describe them as well as [he could]".

We strongly believe Knuth has gathered timeless concepts and explained them with great flair. The material is detailed and rigorous and leavened with humor.

If you feel the same way or would like to know why the ACM Turing Award cited Knuth's TAOCP as having "served as a focal point for developing curricula and as an organizing influence on computer science", please join us in our endeavor to study and learn from TAOCP in a systematic and regular manner.

Anyone may join from anywhere. No programming knowledge is required.

## Note on MMIX and MIX

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Scheduled and Past Meetups

All scheduled meetups in reverse chronological order

## TAOCP #37 - Binary Merge (Chapter 5, Sorting: Section 5.3.2)

Caution Short Merge Ahead!

We're looking at optimum sorting. After analyzing what it means to minimize comparisons for sorting, Knuth turns to the related question of how to most efficiently merge two sorted sets in *5.3.2 Minimum-Comparison Merging*. This is an optional starred section so expect a bit more math than usual.

We go over couple theorems on the minimum number of comparisons needed for merging from Graham/Karp, Hwang/Lim and Stockmeyer/Yao

We learn the proof technique of an adversary to establish these results

The constrained adversaries approach leads to *Algorithm H (Binary merge)* also from Hwang and Lim that takes its name from an application of binary search

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 5 Jun 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.3.2 Minimum-Comparison Merging* (197-204)
  - What is the best way to merge two ordered sets? (197)
  - *Theorem M* (198)
  - *Constructing lower bounds*, constrained adversaries (198-199)
  - An adversary for merging, Strategy A (199)
  - All strategies (199)
  - Constraints on the strategies (200)
  - Lower bounds on merging from the adversary, *Table 1* (200-202)
  - *Theorem K* (202)
  - *Upper bounds on merging* (202-203)
  - *Algorithm H (Binary merging)*, *Table 2* (203)
  - Analysis of Algorithm H (204)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises*
  - Volume 3 (205-207)
- Shoot the breeze

## TAOCP #36 - Merge Insertion Sort (Chapter 5, Sorting: Section 5.3.1)

It's The Best Sort, Don - The Best!

Knuth - "Of course there is no best possible way to sort"

What Knuth offers instead are three sections on minimizing the number of comparisons while sorting, merging or selecting

We look at the first section under 5.3 Optimum Sorting in this meetup - 5.3.1 Minimum-Comparison Sorting

We introduce comparison trees to establish a theoretical framework for analyzing comparison-based sorting techniques

Then we consider two problems - finding comparison trees that minimize the maximum number of comparisons made - similarly those that minimize the average number of comparisons

More concretely we learn merge insertion sort that came about as a generalization of a solution to the question - "What is the best way to sort five elements? Can five elements be sorted using only seven comparisons?"

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 29 May 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.3. Optimum Sorting*/*5.3.1 Minimum-Comparison Sorting* (pp.180-187, 192-193)
  - Binary comparison tree (pp.180-182)
  - *The best worst case* (pp.182-184)
  - *Merge insertion* (pp.184-185)
  - Analysis of merge insertion sort (pp.185-187)
  - *The average number of comparisons* (pp.192-193)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises*
  - Volume 3 (pp.193-197)
  - MMIX Supplement (p.94)
- Shoot the breeze

## Papers #1 - Binomial Heaps, Jean Vuillemin, 1978

**Title:** A Data Structure for Manipulating Priority Queues\
**Authors:** Jean Vuillemin\
**Year:** 1978\
**Length:** 6 pages\
**Citation:** Communications of the ACM, April 1978, 309-315\
**Paper:** https://dl.acm.org/doi/abs/10.1145/359460.359478

Welcome to our first TAOCP Papers meetup!

TAOCP Papers is an irregular series of meetups on papers on algorithms and data structures related to *TAOCP*

These could be papers mentioned in *TAOCP* - like today's selection - or papers that expand on a topic Knuth has covered in *TAOCP*

The Papers meetup will typically be scheduled on weekdays at 7p New York time - the format is much the same as the main TAOCP meetup - we'll read a bit and discuss - and repeat

It's expected the portions we discuss at a time will be much smaller than couple pages since papers tend to be more dense than a text like *TAOCP* - it's quite possible some papers may need more than one session

Our regular Saturday afternoon TAOCP meetup continues with no change

Today's paper on binomial heaps - called binomial queues in the paper - is one of the "new ways to represent priority queues" that Knuth mentions in *5.2.3 Sorting by Selection*

Along with Fibonacci heaps they are implemented in Knuth's Stanford GraphBase library for graph algorithms development

Supplementary Resources:

- Binomial heaps are based on binomial trees which are covered in *7.2.1.3 Generating all combinations, TAOCP Volume 4A, Combinatorial Algorithms, Part 1*

- Binomial heaps are the subject of a lecture on 15 Apr 2021 in CS166, Data Structures, Spring 2021 at Stanford - accompanied by an excellent set of slides at https://web.stanford.edu/class/cs166

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Wednesday, 26 May 2021\
**Time:** 7-9pm America/New_York

### Agenda

**7:00 - 7:10** Meet and greet\
**7:10 - 8:00** Read and discuss a bit at a time

- A Data Structure for Manipulating Priority Queues (pp.309-314)
  - *1 Introduction* (p.309)
  - INSERT, DELETE, MIN, UPDATE, UNION operations (pp.309-310)
  - *2 Binomial Trees and Forests*, *Fig 1, 2, 3* (pp.310-311)
  - *3 Binomial Queues* (p.311)
  - UNION algorithm, *Fig 4, 5* (p.311)
  - INSERT algorithm (pp.311-312)
  - DELETE algorithm, *Fig 6, 7* (p.312)

**8:00 - 8:10** Break\
**8:10 - 9:00** Continue reading and discussing
- UPDATE algorithm (pp.312-313)
- *4 Implementation of Binomial Forests as Binary Trees*, *Fig 8* (p.313)
- UNION pseudocode (pp.313-314)
- DELETE/EXTRACTMIN pseudocode (p.314)

## TAOCP #35 - Priority Queues (Chapter 5, Sorting: Section 5.2.3)

Top Of The Heap!

We saw in TAOCP #34 how a heap - a tree with of keys *K_1, ..., K_N* with the heap condition

--------------------- *K_⌊j/2⌋ >= K_j for 1 <= ⌊j/2⌋ < j <= N* -------------------

may be used to sort the keys in a guaranteed worst case time of O(N * log(N))

This time we look at priority queues - another application where heaps shine

Priority queues are convenient data structures for whenever data arrives in an unpredictable way but has to be processed in a known priority order. Priority may be time or distance or some measure of the importance of the key. This implies data once stored must be retrieved in order of its priority.

A heap may be used as the base data structure for a priority queue - thus providing insertion and deletion in *O(log n)* time

We look at leftist trees as another representation for priority queues - these offer constant time insertion and deletion at the cost of increased memory

Knuth compares these two choices and a balanced tree representation - and lists a bunch of alternatives found up through the 1990s

He concludes by saying

-------------- "Many new ways to represent priority queues have been discovered since ... Programmers now have a large menu of options to ponder, besides simple lists, heaps, leftist or balanced trees ... Not all of these methods will survive the test of time" --------------

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 22 May 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.2.3 Sorting by Selection* (pp.148-152)
  - *Largest in, first out* (pp.148-149)
  - *A linked representation for priority queues* (pp.149-150)
  - *Comparison of priority queue techniques*, *Fig 27* (pp.150-152)

- *5.2.3 Exercises* - *Sorting by Selection* (pp.155-158)
  - *Exercise 15* - Prime numbers table without division (p.156)
  - *Exercise 16* - Add a key to a heap (p.156)
  - *Exercise 29* - Polynomial multiplication (p.157)
  - *Exercise 31* - Priority deque (p.157)
  - *Exercise 33* - Merge leftist tree priority queues (p.157)
  - *Exercise 36* - LRU page replacement (p.158)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises*
  - Volume 3 (pp.155-158)
  - MMIX Supplement (p.89)
- Shoot the breeze
- 
## TAOCP #34 - Heapsort (Chapter 5, Sorting: Section 5.2.3)

Winner winner chicken dinner!

We begin to see the broad applicability of tree data structures to solving large categories of problems in our return to *Volume 3, Sorting and Searching*

We develop heapsort as an example of selection by sorting in section 5.2.3. Tree selection is a popular elimination scheme for sports tournaments. Normally tournaments are only concerned with the single ultimate winner - the person that rises to the root of the selection tree. But the principle may be repeated with tweaks to obtain an efficient way to rank all participants exploiting information retained in the tree structure from every comparison.

We look at Algorithm H (Heapsort) and its **MMIX** implementation

Time permitting we'll go over the mathematical analysis of a portion of heapsort - though Knuth marks it as optional

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 15 May 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.2.3 Sorting by Selection* (pp.141-148, 152-155)
  - *Tree selection* (pp.141-142)
  - *Exercise 5.2.3.10* (p.156)
  - Top-down tree selection, Fig 23, 24, 25 (pp.142-144)
  - *Heapsort* (pp.144-145)
  - *Algorithm H (Heapsort)*, *Fig 26* (pp.145-146)
  - *Program H (Heapsort)*, *Table 2* (pp.146-147), MMIX Supplement (pp.87-88)
  - Timing Program H (pp.147-148), MMIX Supplement (pp.88-89)
  - *Analysis of heapsort*, *Theorem H* (pp.152-155)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises*
  - Volume 3 (pp.155-158)
  - MMIX Supplement (p.89)
- Shoot the breeze

## TAOCP #33 - The Matrix (Chapter 2, Information Structures: Section 2.2.6)

AKA Two-dimensional Array!

Wow - we are nearly done with *Volume 1* of TAOCP!

True - we didn't read it cover to cover or do all exercises. Yet we read almost all non-optional sections - exceptions being some of the mathematical preliminaries. We covered all **MMIX** instructions needed for application programming. We wrote C and C++ programs for many algorithms. We did a few exercises.

Soon we'll pick off the sections from *Volume 3* on internal sorting that were deferred till we had covered trees

Afterwards we'll continue with external sorting in *Volume 3*

So here's the final section from *Volume 1* - on two-dimensional arrays or matrices

We see techniques for representing a matrix using sequential and linked allocation

Knuth gives an algorithm for pivoting a matrix around an element as an example of how a linked representation may be used for efficient transformations of sparse matrices

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 8 May 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.2.6 Arrays and Orthogonal Lists* (pp.298-305)
  - *Sequential Allocation* (pp.298-300)
  - Triangular matrices (pp.300-301)
  - *Linked Allocation*, sparse matrices (pp.301-302), MMIX Supplement (p.36)
  - Pivot step operation (pp.302-303)
  - *Algorithm S (Pivot step in a sparse matrix)* (pp.304-305), MMIX Supplement (p.36)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises*
  - Volume 1 (pp.305-307)
  - MMIX Supplement (p.37)
- Shoot the breeze

## TAOCP #32 - Coroutines For Elevator Simulation (Chapter 2, Information Structures: Section 2.2.5)

The Sims - Elevator Edition!

We continue with the elevator simulation problem in section 2.2.5 on doubly linked lists

We go over the coroutines that simulate the elevator and passengers. We see how doubly linked lists are used for efficient queues. And how everything is tied together through a controller/scheduler routine.

Finally we cover **MMIX** code for the elevator simulation program from the MMIX Supplement

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 1 May 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.2.5. Doubly Linked Lists* (pp.283-296)
  - *Coroutine U (Users)* (pp.283-284)
  - *Coroutine E (Elevator)* (pp.284-285)
  - *Subroutine D (DECISION subroutine)*, *Table 1* (pp.286-287)
  - WAIT, ELEVATOR, QUEUE doubly linked lists, *Fig 12* (pp.287-288), MMIX Supplement (p.28)
  - Elevator simulation program (pp.288-296), MMIX Supplement (pp.28-35)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises*
  - Volume 1 (pp.297-298)
  - MMIX Supplement (p.36)
- Shoot the breeze

## TAOCP #31 - Knuth Elevator Problem (Fascicle 1, MMIX: Sections 1.3.1', 1.4.2') (Chapter 2, Information Structures: Section 2.2.5)

Going up!

We continue with the introduction to coroutines in **MMIX** after the detailed review of subroutines in **TAOCP #30**

We learn how to use **MMIX** instructions to achieve coroutine linkage in section 1.4.2' from *Fascicle 1, MMIX*. A problem of decoding a string serves as a concrete yet simple application of coroutines using the **GO** instruction.

Also we cover the **TRIP** and **RESUME** instructions that allow Unix-like signal-handling - they may be used for a kind of dynamic dispatch that can be useful with coroutines

We then return to *Volume 1, Fundamental Algorithms* where we find the Knuth elevator simulation problem in section 2.2.5 on doubly linked lists

We've come across this data structure in past meetups on later sections of *Volume 1*. Here they're used in one of the longest programs in TAOCP - a simulation of the elevator in the Math building at Caltech.

While the program is meant to be "the simplest set of rules that explain all the phenomena observed during several hours of experimentation by the author", Knuth has some doubts about its utility since "it may be simpler just to try using the elevator several times instead of writing a computer program"

It is however a great application of doubly-linked lists used to implement multiple queues. It also demonstrates concurrency using coroutines to simulate the independent behavior of the elevator and passengers.

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 24 April 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*) and *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *1.4.2' Coroutines* (pp.66-72)
  - Coroutine linkage, a decoding problem for coroutines (pp.66-68)
  - MMIX coroutines program (pp.68-70)
  - *Multipass algorithms* (pp.70-72)

- *1.3.1' Description of MMIX* (pp.18-19)
  - *Interrupts* (pp.18-19)

- *2.2.5. Doubly Linked Lists* (pp.280-288)
  - Doubly Linked Lists (pp.280-281)
  - Elevator simulation (pp.282-283), MMIX Supplement (pp.27-28)
  - *Coroutine U (Users)* (pp.283-284)
  - *Coroutine E (Elevator)* (pp.284-285)
  - *Subroutine D (DECISION subroutine)*, *Table 1* (pp.286-287)
  - WAIT, ELEVATOR, QUEUE doubly linked lists, *Fig 12* (pp.287-288), MMIX Supplement (p.28)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises*
  - Fascicle 1 (pp.72-73)
  - Volume 1 (pp.297-298)
  - MMIX Supplement (p.36)
- Shoot the breeze

## TAOCP #30 - MMIX Coroutines (Fascicle 1, MMIX: Sections 1.4.1', 1.4.2')

Coroutines!

We cover some advanced features of Knuth's **MMIX** computer that are needed for the last couple sections on lists that we had skipped earlier.

The main feature covered in this meetup is coroutines

Knuth describes the difference between subroutines and coroutines as

"Subroutines are special cases of more general program components, called coroutines. In contrast to the unsymmetric relationship between a main routine and a subroutine, there is complete symmetry between coroutines, which call on each other."

We have seen plenty of examples of subroutines in the meetups on **MMIX** programming but it's worthwhile to go over them in a bit more detail as covered in section 1.4.1' from *Fascicle 1*. Most of this material will be review.

Section 1.4.1' ends with Knuth's early thoughts on writing longer complex programs. He describes a hybrid process that mixes a top-down and bottom-up approach that lets a programmer iteratively refine and expand the program.

We go on to coroutines in section 1.4.2' where we learn how to use **MMIX** instructions to achieve coroutine linkage. We consider a simple problem of decoding a string. We'll go over the **MMIX** code that uses coroutines to solve the problem.

This should prepare us for the elevator simulation problem that Knuth uses as an application of doubly-linked lists and solves with coroutines in section 2.2.5 of *Volume 1*

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 17 April 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*)

- *1.4.1' Subroutines* (pp.52-65)
  - Subroutines and linkage (pp.52-53)
  - Parameters and calling sequences (pp.53-56)
  - Multiple entrances and exits (pp.56-57)
  - *Using a memory stack* (pp.57-58)
  - *Using the register stack* (p.58-61)
  - *Strategic considerations* (pp.62-65)

- 1.4.2' Coroutines (pp.66-72)
  - Coroutine linkage, a decoding problem for coroutines (pp.66-68)
  - MMIX coroutines program (pp.68-70)
  - *Multipass algorithms* (pp.70-72)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises*
  - Fascicle 1 (pp.65-66, 72-73)
- Shoot the breeze

## TAOCP #29 - The Buddy System (Chapter 2, Information Structures: Sections 2.5, 2.6)

You know where to find me, buddy!

We continue to look at methods for allocating variable-size blocks of memory in section 2.5 *Dynamic Storage Allocation*

The main remaining technique is the buddy system that improves the process of coalescing freed blocks of memory

Knuth spends considerable time to explain and analyze the expected behavior of the various algorithms in this section. This includes programs to simulate an application requesting and releasing memory. The results of the simulations are discussed leading Knuth to recommend certain methods over others.

Finally we wrap up *Chapter 2* with section 2.6 *History and Bibliography*. It has extensive references that places the topics on trees, lists and memory allocation that we covered in historical context and offers threads for future investigation and discussion

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 27 March 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.5 Dynamic Storage Allocation* (pp.442-452)
  - *C. The "buddy system"* (pp.442-443)
  - *Algorithm R (Buddy system reservation)* (p.443)
  - *Algorithm S (Buddy system liberation)* (pp.443-444)
  - *D. Comparison of the methods* (p.444-445)
  - Monte Carlo simulation program (pp.445-446)
  - Almost-last-in-first-out simulation (pp.446-448)
  - Results and recommendations (pp.449-450), MMIX Supplement (p.46)
  - *E. Distributed fit* (pp.450-451)
  - *F. Overflow*, *G. For further reading* (pp.451-452)

- *2.6 History and Bibliography* (pp.457-465)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises*
  - Volume 1 (pp.452-456)
- Shoot the breeze

## TAOCP #28 - Memory Allocation (Chapter 2, Information Structures: Section 2.5)

Heap memory!

We look at how to allocate variable-size blocks of memory in section 2.5 Dynamic Storage Allocation

Knuth covers two aspects of managing a pool of memory, or a heap - reservation and liberation

Reservation covers algorithms for selecting a block of memory to fulfill a requested size. Liberation refers to returning blocks of memory that are no longer in use to the pool

We'll go over algorithms for reservation that include first-fit, best-fit - and next-fit which is an exercise

Two liberation algorithms are covered - *Algorithm B (Liberation with sorted list)* and the more efficient *Algorithm C (Liberation with boundary tags)* that avoids the cost of searching the heap

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 20 March 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- 2.5 Dynamic Storage Allocation (pp.435-442)
  - *Reservation* (pp.435-437)
  - *Algorithm A (First-fit method)* (pp.437-438)
  - *Liberation* (pp.438-439)
  - *Algorithm B (Liberation with sorted list)* (p.440)
  - Avoid searching the heap (pp.440-441)
  - *Algorithm C (Liberation with boundary tags)* (pp.441-442)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises*
  - Volume 1 (pp.452-456)
- Shoot the breeze

## TAOCP #27 - COBOL?!? (Chapter 2, Information Structures: Section 2.4)

Compiling COBOL!

It shouldn't be much of a surprise that Knuth finds applications of complex multilinked structures in compilers for COBOL - a language designed for processing structured data in files.

We learn how hierarchical data is supported in COBOL internally and in external files.

A COBOL variable has an associated level number that allows elementary items to be grouped like **DAY OF DATE OF SALES**.

A tree-like data structure with parent, sibling and child links plus couple more links is used to represent the various relationships

We look at algorithms to support statements like **MOVE CORRESPONDING DATE OF SALES TO DATE OF PURCHASES**.

Specifically three algorithms are covered for use in a COBOL compiler to solve the following problems:

1. Generate data tables from a hierarchical description of names and level numbers
2. Look up data items corresponding to valid qualified references
3. Find all corresponding pairs of items for a **CORRESPONDING** statement

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 13 March 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.4 Multilinked Structures* (pp.424-433)
  - COBOL variables, records and levels (pp.424-425)
  - Operations on and data structures for COBOL records (pp.426-427)
  - *Algorithm A (Build Data Table)* (pp.427-429)
  - *Algorithm B (Check a qualified reference)* (pp.429-430)
  - *Algorithm C (Find CORRESPONDING pairs)* (pp.430-431)
  - Analysis of the algorithms and data structures (pp.432-433)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.433-434)
- Shoot the breeze

## TAOCP #26 - Stackless Garbage Collection (Chapter 2, Information Structures: Section 2.3.5)

No stacks of trash here!

We close section 2.3.5 Lists and Garbage Collection with Algorithm E (Marking) credited to Schorr and Waite, also to Deutsch.

We'll actually begin with an exercise from an earlier section on binary tree traversal. Exercise 2.3.1.21 asks for an algorithm to traverse an unthreaded binary tree in inorder but not use a stack. A solution is provided by Knuth. The key idea used to solve this problem is also used in the Schorr-Waite algorithm.

We continue our discussion of garbage collection with Algorithm C (Marking). It combines ideas from the first two algorithms seen in our last meetup. It uses a fixed stack size to avoid the problem of running out of stack space during garbage collection.

Next we cover Algorithm D (Marking). It uses links in List header nodes to maintain a stack.

Finally we cover Algorithm E (Marking) that manages to avoid a stack altogether. It is often called the Schorr-Waite algorithm.

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 6 March 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3.1 Traversing Binary Trees*
  - *Exercise 2.3.1.21* Inorder traversal of an unthreaded binary tree without a stack (p.332)
  - *Answer 2.3.1.21* (p.567)

- *2.3.5 Lists and Garbage Collection* (pp.416-421)
  - *Algorithm C (Marking)* (pp.416-417)
  - *Algorithm D (Marking)* (p.417)
  - *Algorithm E (Marking)* (pp.418-419)
  - Analysis of garbage collection algorithms (pp.420-421)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.422-423)
- Shoot the breeze

## TAOCP #25 - Garbage Collection (Chapter 2, Information Structures: Section 2.3.5)

So you think you know lists?

We've now covered nearly all sections on trees in Chapter 2 - the remaining sections have important mathematical results on free trees and oriented trees but are marked optional by Knuth. We'll postpone studying these in detail till we actually need the material - possibly in Volume 3 for searching, certainly for many of the combinatorial algorithms in Volume 4.

So we shift from trees to a specialized data structure with a deceptively ordinary name - List.

A List in Knuth's parlance is related to both trees and linked lists. It is a recursive data structure that can contain itself. Different lists may overlap each other.

We'll see what Lists are good for and how to represent them in memory.

Then we consider the problem of managing memory for List objects. Approaches such as reference counting and garbage collection are discussed.

We look at two algorithms for garbage collection.

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 27 February 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- Review *2.3 Trees* (pp.315-316)
  - Lists (pp.315-316)

- *2.3.5 Lists and Garbage Collection* (pp.408-416)
  - Data structures for Lists (pp.408-411)
  - Operations on Lists (pp.411-413), MMIX Supplement (pp.44-45)
  - Garbage collection (pp.413-415)
  - *Algorithm A (Marking)* (p.415)
  - *Algorithm B (Marking)* (pp.415-416)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.422-423)
- Shoot the breeze

## TAOCP #24 - Huffman Trees (Chapter 2, Information Structures: Section 2.3.4.5)

We look at the concept of path length in trees in section 2.3.4.5 that Knuth considers "of great importance in the analysis of algorithms, since this quantity is often directly related to the execution time".

We look at extended binary trees that insure every node of the original tree has two children. This is used to establish some short results on path lengths in binary trees that are generalized to ternary, quaternary and higher-order trees.

Finally we consider associating weights with the nodes of a tree and look at Huffman's method for finding a tree with minimum weighted path length.

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 20 February 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3.4.5 Path length* (pp.399-404)
  - Extended binary tree (pp.399-400)
  - Internal and external path lengths (p.400)
  - Complete binary trees and higher-order trees (pp.401-402)
  - Huffman's method for weighted path lengths (pp.402-404)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.404-406)
- Shoot the breeze

## TAOCP #23 - Polynomials As Trees (Chapter 2, Information Structures: Sections 2.3.3, 2.3.4.5)

Trees above! Trees to the left! Trees to the right! Trees below????

We examine more complex representations of trees. A particular doubly linked ring structure is applied to the problem of arithmetic on polynomials.

We have previously seen algorithms for polynomial addition and multiplication using circular lists. Those however were limited to polynomials in three or four variables.

We close out section 2.3.3 Other Representations of Trees with Algorithm A (Addition of polynomials) that works for polynomials in any number of variables. The algorithm illustrates traversal, insertion, and deletion in a four-way-linked tree.

Then we jump to section 2.3.4.5 Path length. We look at extended binary trees that insure every node of the original tree has two children. This is used to establish some results on path lengths in binary trees that are generalized to ternary, quaternary and higher-order trees.

Finally we consider associating weights with the nodes of a tree and look at Huffman's method for finding a tree with minimum weighted path length.

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 13 February 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3.3 Other Representations of Trees* (pp.355-359)
  - Ring structures (pp.355-357)
  - *Algorithm A (Addition of polynomials)* (pp.357-359), MMIX Supplement (pp.43-44)

- *2.3.4.5 Path length* (pp.399-404)
  - Extended binary tree (pp.399-400)
  - Internal and external path lengths (p.400)
  - Complete binary trees and higher-order trees (pp.401-402)
  - Huffman's method for weighted path lengths (pp.402-404)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.359-362, 404-406)
- Shoot the breeze

## TAOCP #22 - Equivalence Relations (Chapter 2, Information Structures: Section 2.3.3)

Trees in memory!

We look at ways to represent a binary tree in memory in section 2.3.3 Other Representations of Trees.

Knuth's fascinating coverage begins with the pros and cons of a few sequential representation techniques. We see one of these - postorder with degrees - applied to the bottom-up evaluation of functions in Algorithm F (Evaluate a locally defined function in a tree).

Then we discuss linked representations. An application based on oriented trees is shown in Algorithm E (Process equivalence relations)

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 6 February 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3.3 Other Representations of Trees* (pp.348-355)
  - Preorder sequential representation (pp.348-349)
  - Reusing empty right-link fields (pp.349-350)
  - Family order and level order (pp.350-351)
  - *Algorithm F (Evaluate a locally defined function in a tree)* (p.351)
  - Linked representations (pp.352-353)
  - Equivalence relations (pp.353-354)
  - *Algorithm E (Process equivalence relations)* (pp.354-355)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.359-362)
- Shoot the breeze

## TAOCP #21 - Derivatives (Chapter 2, Information Structures: Section 2.3.2)

Calculus with trees!

It turns out any tree may be represented as a binary tree. We learn this correspondence in Section 2.3.2 Binary Tree Representation of Trees and use it to compute the derivative of an algebraic expression. For example the derivative of 
y = 3 * ln(x + 1) − a / x² is 
D(y) = 3 * (1 / (x + 1)) − (-(a * (2 * x)) / (x²)²)

Knuth provides the bulk of the algorithm and MMIX code for differentiation. Some parts are left to exercises. We'll try to go over the complete program.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 30 January 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3.2. Binary Tree Representation of Trees* (pp.334-346)
  - Natural correspondence of forests and binary trees (p.334-337)
  - Tree of an algebraic formula (pp.337-338), MMIX Supplement (p.39)
  - Finding the derivative (pp.338-340)
  - *Algorithm D (Differentiation)* (p.340)
  - Routines for various operators (pp.340-342)
  - *Program D (Differentiation)* (pp.342-346), MMIX Supplement (pp.39-43)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.346-348), MMIX Supplement (p.43)
- Shoot the breeze

## TAOCP #20 - Binary Trees (Chapter 2, Information Structures: Section 2.3.1)

Binary trees and proof by induction!

We wrap up the introduction to binary trees and threaded trees with two algorithms. Algorithm I (Insertion into a threaded binary tree) shows how to construct a threaded tree. Algorithm C (Copy a binary tree) may be used to copy binary trees that are threaded or unthreaded, or have threads only on one side.

Section 2.3.1 has a number of exercises that flesh out many aspects of the material. We'll attempt a few.

But first we'll go over section 1.2.1 Mathematical Induction that is part of section 1.2 Mathematical Preliminaries. We've already seen the use of induction in a proof of Algorithm T (Traverse binary tree in inorder). And it's bound to be used often to prove properties of recursive data structures like trees and of algorithms on them. Knuth's presentation of induction is quite interesting and different from that typically given in purely mathematical texts.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 23 January 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 1, Basic Concepts* and *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *1.2.1 Mathematical Induction* (pp.11-18)
  - Algorithmic proof procedure (pp.11-13)
  - *Algorithm I (Construct a proof)* (pp.11-12)
  - *Algorithm E (Extended Euclid’s algorithm)* (pp.13-16)
  - Inductive assertions (pp.16-18)

- *2.3.1 Traversing Binary Trees* (pp.327-330)
  - *Algorithm I (Insertion into a threaded binary tree)* (p.327)
  - Similar trees and equivalent trees (pp.327-329)
  - *Algorithm C (Copy a binary tree)* (pp.329-330)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.18-21, 330-334), MMIX Supplement (p.39)
- Shoot the breeze

## TAOCP #19 - Trees (Chapter 2, Information Structures: Section 2.3)

Return to the forest!

We're back in Volume 1 of TAOCP, Fundamental Algorithms. We'll try to cover most of what remains on data structures in Volume 1 before continuing with sorting and searching in Volume 3

We begin with section 2.3 Trees that introduces the concept of trees. There's much terminology and examples of different kinds of trees.

The next section 2.3.1 Traversing Binary Trees looks at the highly important category of binary trees. We consider the different ways to visit the nodes of a binary tree - inorder, preorder and postorder. We'll go over Algorithm T for inorder traversal of a binary tree. Then we look at Algorithm S that improves on Algorithm T by adding special links called threads to a basic binary tree turning it into a threaded binary tree.

Knuth has published extensively on trees - and still does. Here's a preprint from just last year https://www-cs-faculty.stanford.edu/~knuth/papers/fibonacci-matchings.pdf - Trees have been a favorite topic for his annual Christmas Lectures.

By the way, his most recent preprint was on New Year's Day just a few days ago! https://www-cs-faculty.stanford.edu/~knuth/papers/amazing.pdf

I'm very excited to follow his development of the foundations of this fundamental data structure.

We'll do some exercises.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 16 January 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3 Trees* (pp.308-316)
  - Trees and forests (pp.308-311)
  - Binary trees and Lists (pp.312-316)

- *2.3.1 Traversing Binary Trees* (pp.318-326)
  - Preorder, inorder and postorder traversal (pp.318-320)
  - *Algorithm T (Traverse binary tree in inorder)* (pp.320-321)
  - Threaded tree representation (pp.322-323)
  - *Algorithm S (Symmetric (inorder) successor in a threaded binary tree)* (pp.323-324), MMIX Supplement (p.37)
  - *Program T (Traverse binary tree in inorder)*, MMIX Supplement (pp.37-38)
  - *Program S (Symmetric (inorder) successor in a threaded binary tree)*, MMIX Supplement (p.38)
  - Analysis of Programs T and S (p.326)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.316-318, 330-334), MMIX Supplement (p.39)
- Shoot the breeze

## TAOCP #18 - Radix Sort (Chapter 5, Sorting: Section 5.2.5)

Sorting is sorted out! (for now...)

We'll take a break from sorting after this meetup. We wrap up sorting by merging by questioning the need for twice the amount of memory as required for the array of keys. This motivates a variant of mergesort using link fields called Algorithm L (List merge sort). There is an interesting use of links serving dual purposes that is somewhat specific to the old MIX machine. As such we also need to look at the MMIX version of Algorithm L (List merge sort) in The MMIX Supplement. It, on the other hand, relies on the MMIX feature of an address being implicitly aligned to the word type of the instruction, e.g. `LDTU` ignores the low 2 bits of the address when loading a tetrabyte (4 bytes).

The final section is on sorting by distribution. This technique expands on the basic sorting by counting method we covered in section 5.2. There is quite a bit of discussion of this approach and its applicability to various types of data. We go over Algorithm R (Radix list sort), its MMIX implementation and analysis.

This meetup marks the end of our first pass through Volume 3 of TAOCP. The next few meetups will be on data structures from Volume 1. There is a lot to still learn about lists, arrays and trees from TAOCP. It will all stand us in good stead when we return to Volume 3 for more sorting (and searching) ...

We'll do some exercises.

The bonus segment will include a debugger stepthru of Program L (List merge sort) from The MMIX Supplement.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 9 January 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.2.4 Sorting by Merging* (pp.163-166)
  - List merge sort (pp.163-164)
  - *Algorithm L (List merge sort)* (pp.164-165), MMIX Supplement (pp.89-90)
  - *Program L (List merge sort)*, MMIX Supplement (pp.90-92)
  - Analysis of Program L, MMIX Supplement (p.92)
  
- *5.2.5 Sorting by Distribution* (pp.168-177)
  - Sorting by Distribution (pp.168-171)
  - *Algorithm R (Radix list sort)* (pp.171-172)
  - *Algorithm H (Hooking-up of queues)* (pp.172-173)
  - *Program R (Radix list sort)*, MMIX Supplement (pp.93-94)
  - Analysis of Algorithm R (pp.174-177), MMIX Supplement (pp.93-94)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.166-168, 177-179), MMIX Supplement (pp.92, 94)
- Shoot the breeze

**Bonus Segment**

Stepthru in MMIX Visual Debugger

- *Program L (List merge sort)*, MMIX Supplement (pp.90-92)

## TAOCP #17 - Mergesort (Chapter 5, Sorting: Sections 5.2.3, 5.2.4)

New Year! New sorting methods!

We've studied algorithms that use the techniques of sorting by insertion and sorting by exchanging. We now look at two other approaches.

Sorting by selection involves repeatedly selecting and separating the smallest key. We'll introduce the technique with Algorithm S (Straight selection sort) and discuss its refinements. Section 5.2.3 has other algorithms that we'll skip for now and return to after we have studied tree data structures in Volume 1.

The next section 5.2.4 presents sorting by merging. We'll go over couple mergesort algorithms in this meetup and cover the rest in the next meetup. Mergesort is particularly useful for external sorting when it is infeasible to sort large amounts of data all in memory. It is the technique used by the GNU sort program.

We'll do some exercises.

The bonus segment will include a debugger stepthru of Program S (Straight selection sort) from The MMIX Supplement.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 2 January 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.2.3 Sorting by Selection* (pp.138-141)
  - *Algorithm S (Straight selection sort)* (p.139)
  - *Program S (Straight selection sort)*, MMIX Supplement (p.87)
  - *Refinements of straight selection* (pp.140-141)
  
- *5.2.4 Sorting by Merging* (pp.158-163)
  - *Algorithm M (Two-way merge)* (pp.158-159)
  - Mergesort (pp.159-160)
  - *Algorithm N (Natural two-way merge sort)* (pp.160-161)
  - Analysis of Algorithm N (pp.161-162), MMIX Supplement (p.89)
  - *Algorithm S (Straight two-way merge sort)* (pp.162-163)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.166-168), MMIX Supplement (p.92)
- Shoot the breeze

**Bonus Segment**

Stepthru in MMIX Visual Debugger

- *Program S (Straight selection sort)*, MMIX Supplement (p.87)

## TAOCP #16 - Quicksort (Chapter 5, Sorting: Section 5.2.2)

Quicksort!

We close out the section on Sorting by Exchanging with two fast algorithms.

First we look at the famous quicksort algorithm invented by Tony Hoare. Quicksort works by partitioning the array around a pivot key. Keys smaller than the pivot are placed in one partition and larger keys in the other. This process is repeated with smaller and smaller partitions resulting in a completely sorted array.

Quicksort naturally lends itself to a recursive formulation. And we'll see this in the MMIX implementation of Program Q (Quicksort).

The second algorithm is Algorithm R (Radix exchange sort). It is similar to quicksort in separating keys into two groups. But the criteria is different. Keys are separated into two groups based on the most significant bit in the binary representation of a key. The process is repeated with the next most significant bit and so on. The MMIX code for Program R (Radix exchange sort) is also recursive.

We'll work on some exercises.

The bonus segment will demo a debugger stepthru of Program Q (Quicksort) from The MMIX Supplement.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 19 December 2020\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.2.2 Sorting by Exchanging* (pp.113-128)
  - *Quicksort* (pp.113-115)
  - *Algorithm Q (Quicksort)* (pp.115-117)
  - *Program Q (Quicksort)*, MMIX Supplement (pp.82-84)
  - *Analysis of quicksort* (pp.118-122), MMIX Supplement (pp.84-85)
  - *Radix exchange* (pp.122-123)
  - *Algorithm R (Radix exchange sort)* (pp.123-125)
  - *Program R (Radix exchange sort)*, MMIX Supplement (pp.85-86)
  - Analysis of radix exchange sort (pp.126-128), MMIX Supplement (p.86)
    
**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.134-138), MMIX Supplement (p.86)
- Shoot the breeze

**Bonus Segment**

Stepthru in MMIX Visual Debugger

- *Program Q (Quicksort)*, MMIX Supplement (pp.82-84)

## TAOCP #15 - Batcher Sort (Chapter 5, Sorting: Section 5.2.2)

Bubble sorting!

We've explored two techniques for sorting - counting smaller values to figure out the final position of a key - and insertion of a new key in its correct position in an already sorted sequence.

We look at the category of sorting by exchanging in our fourth meetup on sorting.

The first algorithm is bubblesort - it makes multiple passes through an array making bigger keys bubble up as high as possible.

We'll discuss deficiencies of Algorithm B (Bubble sort) and how it may be improved.

Then we look at Algorithm M (Merge exchange) due to Batcher that too falls under the approach of sorting by exchanging. It has particular appeal because it may be parallelized making it one of the fastest known general sorting methods. Also its method of comparisons make it an example of data-oblivious algorithms as well as constant-time algorithms that are of interest to cryptography. Constant-time algorithms take the same amount of time for a given input size independent of the actual data values.

We'll work on some exercises.

The bonus segment will demo a debugger stepthru of an MMIX program for Algorithm M (Merge exchange) from The MMIX Supplement.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 12 December 2020\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.2.2 Sorting by Exchanging* (pp.105-113)
  - *The bubble sort* (pp.105-107)
  - *Algorithm B (Bubble sort)* (p.107)
  - *Program B (Bubble sort)*, MMIX Supplement (p.81)
  - *Analysis of the bubble sort* (pp.108-109), MMIX Supplement (p.82)
  - *Refinements of the bubble sort* (pp.109-110)
  - *Batcher's parallel method* (pp.110-111)
  - *Algorithm M (Merge exchange)* (pp.111-113)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.134-138), MMIX Supplement (p.86)
- Shoot the breeze

**Bonus Segment**

Stepthru in MMIX Visual Debugger

- *Exercise 5.2.2.12* implements Algorithm M (Merge exchange), MMIX Supplement (p.169)

## TAOCP #14 - Link Order (Chapter 5, Sorting: Section 5.2.1)

Sorting with links!

We continue to look at the technique of sorting by insertion - by making a change to the data structure.

We begin with a bit of theory about sorting. We discuss permutations and inversions because their combinatorial properties are useful for analyzing sorting algorithms

We finish off section 5.2.1 Sorting by Insertion with couple algorithms that make use of an extra link field to impose a sort order on records.

First is Algorithm L (List insertion) that is very similar to Algorithm S (Straight insertion sort) covered in TAOCP #13. We discuss its relative merits and how it may be enhanced.

Finally we look at an enhancement that sorts keys into multiple lists corresponding to ranges of keys

We'll work on some exercises.

The bonus segment will demo debugger stepthrus of MMIX code for Program L (List insertion) and Program M (Multiple list insertion) from The MMIX Supplement.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 5 December 2020\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.1 Combinatorial Properties of Permutations* (pp.11-17)
  - *5.1.1 Inversions* (pp.11-17)

- *5.2.1 Sorting by Insertion* (pp.95-102)
  - *List insertion* (pp.95-96)
  - *Algorithm L (List insertion)* (pp.96-97)
  - *Program L (List insertion)*, MMIX Supplement (pp.78-79)
  - Enhancements to insertion sort (pp.97-98)
  - *Address calculation sorting* (p.99)
  - *Program M (Multiple list insertion)*, MMIX Supplement (pp.79-80)
  - Analysis of Program M (Multiple list insertion) (pp.100-102)
  
**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.102-105), MMIX Supplement (pp.80-81)
- Shoot the breeze

**Bonus Segment**

Stepthru in MMIX Visual Debugger

- *Program L (List insertion)*, MMIX Supplement (pp.78-79)
- *Program M (Multiple list insertion)*, MMIX Supplement (pp.79-80)

## TAOCP #13 - Shellsort (Chapter 5, Sorting: Section 5.2.1)

Sorting by insertion!

We'll begin with a quick introduction to the field of sorting and a mathematical definition of sorting using permutations that we missed covering in the previous meetup.

Then we continue with another simple approach to sorting often used by card players when arranging a hand being dealt to them. It's also a natural choice when items arrive one by one and need to be kept in order. The technique presumes the list is already sorted and the new item can simply be inserted into its correct position. We look at couple algorithms to do this.

First is Algorithm S (Straight insertion sort). It compares the new item successively with each item in the list moving the list till the correct position for the new item is found. We'll go over the MMIX Program S that implements this algorithm.

The main cost in straight insertion sort is from possibly repeated movements of items in a sequential list (array). We discuss some ways to reduce this cost using binary insertion and two-way insertion.

Shellsort is a kind of insertion sort that makes interesting choices for selecting the items of the list to compare. We'll study Algorithm D (Shellsort) and briefly discuss its performance. Knuth provides extensive analysis of Shellsort for interested readers.

We'll work on some exercises.

The bonus segment will have a demo of Program D (Shellsort) from The MMIX Supplement in the MMIX Visual Debugger.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 28 November 2020\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *Preface* (pp.v-vii)

- *5 Sorting* (pp.1-5)

- *5.2.1 Sorting by Insertion* (pp.80-85)

  - *Straight insertion* (p.80)
  - *Algorithm S (Straight insertion sort)* (pp.80-81)
  - *Program S (Straight insertion sort)*, MMIX Supplement (p.xi, p.76)
  - *Binary insertion and two-way insertion* (pp.82-83)
  - *Shell's method* (pp.83-84)
  - *Algorithm D (Shellsort)* (pp.84-85)
    
**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.102-105), MMIX Supplement (pp.80-81)
- Shoot the breeze

**Bonus Segment**

Stepthru in MMIX Visual Debugger

- *Program S (Straight insertion sort)*, MMIX Supplement (p.76)
- *Program D (Shellsort)*, MMIX Supplement (pp.77-78)

## TAOCP #12 - Sorting (Chapter 5, Sorting: Section 5.2)

TAOCP Volume 3!

We dip our toes in Volume 3 with an introduction to sorting. We consider broad categories of approaches to solving the problem of sorting items. TAOCP covers many sorting techniques in great depth. Fortunately some of the initial algorithms don't need data structures any more complex than an array or singly linked list.

We should be able to spend about a dozen meetups on these first sorting algorithms. Afterwards we'll return to data structures in Volume 1 to learn more on lists and trees.

Our initial focus will be on sorting quantities of data that entirely fit in memory. This is what TAOCP calls internal sorting.

We look at two methods of sorting by counting in this meetup - comparison counting and distribution counting. An MMIX program for comparison counting will be demoed in the bonus segment.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 21 November 2020\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.2 Internal Sorting* (pp.73-79)

  - *5.2 Internal Sorting* (pp.73-75)
  - *Sorting by counting* (pp.75-76)
  - *Algorithm C (Comparison counting)* (p.76)
  - *Program C (Comparison counting)* (pp.76-78), MMIX Supplement (pp.74-75)
  - *Algorithm D (Distribution counting)* (pp.78-79)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.79-80), MMIX Supplement (p.75)
- Shoot the breeze

**Bonus Segment**

Stepthru in MMIX Visual Debugger

- *Program C (Comparison counting)*, MMIX Supplement (pp.74-75)

## TAOCP #11 - Polynomial Arithmetic and Circular Lists (Chapter 2, Information Structures: Section 2.2.4) 

Circular lists!

Linking the last node of a list to the first has advantages that we explore in this meetup. We see how insertion and deletion is affected. And consider how to properly handle an empty circular list.

The problem for this section is of arithmetic on polynomials. We present algorithms for adding and multiplying polynomials in three variables, x, y and z. For example

(x⁴ + 2x³y + 3x²y² + 4xy³ + 5y⁴) * (x² − 2xy + y²) = x⁶ - 6xy⁵ + 5y⁶

We see why circular lists are good data structures to use for this problem.

We'll work on some exercises too.

After the main meetup session, we'll continue to record a walkthrough in the MMIX Visual Debugger of Program A for polynomial addition from The MMIX Supplement. Attendees will be welcome to stay on for as long as they like. This bonus segment will run for as long as it takes to complete the walkthrough including any discussion with attendees who remain present.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

**Date:** Saturday, 14 November 2020\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.2 Linear Lists* (pp.273-278)

  - *2.2.4 Circular Lists* (pp.273-275)
  - *Arithmetic on polynomials* (pp.275-276), MMIX Supplement (pp.25-26)
  - *Algorithm A (Addition of polynomials)* (p.276)
  - *Algorithm M (Multiplication of polynomials)* (p.277)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.278-280), MMIX Supplement (p.27)
- Shoot the breeze

**Bonus Segment**

Stepthru in MMIX Visual Debugger

- *Program A (Addition of polynomials)* from MMIX Supplement (p.26)

## TAOCP #10 - Topological Sort and Linked Lists (Chapter 2, Information Structures: Section 2.2.3)

Linked lists!

We look at adding links to nodes in a list to allow more flexible memory allocation schemes. We discuss what would need to be done for insertions and deletions. We go over tradeoffs between linked allocation and sequential allocation.

Then we use linked lists in an algorithm for topological sorting to create a linear order on a set of items that only has a partial order. We'll work on some exercises as well.

After the main meetup session, we'll continue to record a demo and walkthrough of Program T for topological sorting in the MMIX Visual Debugger. Attendees will be welcome to stay on if they desire.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

**Date:** Saturday, 7 November 2020\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.2 Linear Lists* (pp.254-268)

  - *2.2.3 Linked Allocation* (pp.254-256), MMIX Supplement (p.18)
  - *2.2.3 Linked Allocation* (pp.256-258), MMIX Supplement (pp.18-19)
  - *2.2.3 Linked Allocation* (pp.259-260), MMIX Supplement (p.19)
  - *Topological sorting* (pp.261-263), MMIX Supplement (p.19)
  - *Topological sorting* (pp.263-264), MMIX Supplement (p.19)
  - *Algorithm T (Topological sort)* (pp.265-266), MMIX Supplement (p.20)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.268-273), MMIX Supplement (pp.22-25)
- Shoot the breeze

**Bonus Segment**

- *Program T (Topological sort)* (pp.266-268), MMIX Supplement (pp.20-22)
  - Stepthru in MMIX Visual Debugger

## TAOCP #9 - Sequential Allocation (Chapter 2, Information Structures: Section 2.2.2)

Memory allocation schemes!

We've begun to look at lists of records that may grow and shrink. Now we consider how to manage these lists in memory. We'll look at a few algorithms for sequential allocation and work on some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

**Date:** Saturday, 31 October 2020\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.2 Linear Lists* (pp.244-251)

  - *2.2.2 Sequential Allocation* (pp.244-245)
  - *2.2.2 Sequential Allocation* (pp.245-246)
  - *2.2.2 Sequential Allocation* (pp.247-248)
  - *Algorithms G, R* (pp.248-250)
  - *2.2.2 Sequential Allocation* (pp.250-251)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.251-254)
- Shoot the breeze

## TAOCP #8 - Stacks, Queues and Deques (Chapter 2, Information Structures: Section 2.1-2.2)

**Date:** Saturday, 24 October 2020\
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- Skim *MMIX Supplement* (pp.7-25)

  - *Foreword* (pp.7-8)
  - *Preface* (pp.9-11)
  - *Style Guide* (pp.12-25)
  
- *2.1 Introduction* (pp.232-236) (with *MMIX Supplement*, pp.49-51)
- *2.2 Linear Lists* (pp.238-242)

  - *2.2.1 Stacks, Queues, and Deques* (pp.238-242)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.236-237, pp.242-243)
- Shoot the breeze

Data structures - Yay!

We begin to look at representing and manipulating tabular arrangements of data in programs. A table that is laid out in a linear manner is known as a list or array. Three simple and pervasive data structures - stacks, queues and deques - are introduced. We'll examine their structural differences and how it affects their application to different problems.

We'll also introduce *The MMIX Supplement*. We'll be using it as a companion text to TAOCP Volumes 1-3 for all future meetups. It has **MMIX** variants of code in TAOCP.

After the break, we'll do some exercises.

## TAOCP #7 - MMIX Programming (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 17 October 2020\
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*)

- *1.2.10 Analysis of an algorithm* (p.96 of *TAOCP Vol.1*, not *Fascicle 1, MMIX*)

  - *Algorithm M (Find the maximum)* (p.96 of *TAOCP Vol.1*, not *Fascicle 1, MMIX*)
  
- *1.3.2' The MMIX Assembly Language* (pp.28-43)

  - *Program M (Find the maximum)* (pp.28-30)
  - Stepthru *Program M* in MMIX Visual Debugger
  - *Program H (Hail the world)* (pp.30-32)
  - Stepthru *Program H* in MMIX Visual Debugger
  - *Algorithm P (Print table of 500 primes)* (p.32)
  - *Program P (Print table of 500 primes)* (pp.32-37)
  - Stepthru *Program P* in MMIX Visual Debugger
  - *Language summary* (pp.37-40)
  - *Primitive input and output* (pp.40-43)
  
**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.24-28, pp.43-51)
- MMIX Simulator and Assembler
- Shoot the breeze

We begin to program the **MMIX** computer!

Programs for **MMIX** are written in assembly language. An assembly language program is made up of a sequence of **MMIX** instructions plus directives for the assembly language processing program called the assembler. The output of the assembler is an object file that can actually run on the **MMIX**.

The first program we'll study finds the maximum of some numbers. Its code is in *Fascicle 1, MMIX* but the algorithm is in *TAOCP Volume 1, Fundamental Algorithms*.

Two programs that print output follow, completing our introduction to **MMIX**. This lets us tackle basic algorithms and data structures from Chapters 2 and 5 right away. We'll swing back at some point to cover the few remaining **MMIX** features like subroutines, coroutines and interrupts as needed.

First is the requisite "Hello World" program. It's short and sweet.

Then there's a program to compute small primes and print them in a table. It introduces some interesting features of **MMIX** assembly like local symbols and symbolic expressions.

We'll step through each program in the MMIX Visual Debugger to see it in action.

After the break, we'll do some exercises.

Exercises are posted at https://github.com/theartofcomputerprogramming/exercises/tree/master/fasc_1_mmix_chap_1_basic_concepts/sec_1.3.2_the_mmix_assembly_language - anyone may contribute solutions or partial work to the repo at any time.

## TAOCP #6 - MMIX Branching (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 10 October 2020\
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*)

- *1.3.1' Description of MMIX* (pp.13-24)

  - *Immediate constants* (pp.13-14)
  - *Jumps and branches* (pp.15-16)
  - *The complete instruction set* (pp.19-21)
  - *Timing* (pp.21-23)
  - *MMIX versus reality* (p.23)
  - *Summary* (p.24)
  
**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.24-28)
- Shoot the breeze

We wrap up the **MMIX** instruction set!

We learn that many instructions can take constants instead of registers as operands. This is often a nice convenience that allows small values to be used for arithmetic or for relative addressing. It also allows a register to be set to any value without loading data from memory.

Then we learn instructions to branch and jump. These are the basis of essential programming control constructs like **if-else** conditions and **while** loops. This will allow us to finally study and write complete programs for an **MMIX** computer.

We'll go over the costs of the entire **MMIX** instruction set. This lets us estimate the performance of a program and compare the speed of two programs.

After the break, we'll work on exercises on the new instructions and those from previous meetups on **MMIX**.

Exercises are posted at https://github.com/theartofcomputerprogramming/exercises/tree/master/fasc_1_mmix_chap_1_basic_concepts/sec_1.3.1_description_of_mmix - anyone may contribute solutions or partial work to the repo at any time.

## TAOCP #5 - MMIX Problem Fest (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 3 October 2020\
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Work on *Exercises* (pp.24-28) for topics from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*)

- *1.3.1' Description of MMIX* (pp.8-12)

  - *Bits and bytes* (pp.2-4)
  - *Memory and registers* (pp.4-5)
  - *Instructions* (pp.5-6)
  - *Loading and storing* (pp.6-8)
  - *Arithmetic operators* (pp.8-9)
  - *Conditional instructions* (p.10)
  - *Bitwise operations* (pp.10-11)
  - *Bytewise operations* (pp.11-12)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- Continue *Exercises* (pp.24-28)
- Shoot the breeze

MMIX exercises galore!

We've covered the bulk of instructions for the **MMIX** computer. We've tried out examples in the MMIX Visual Debugger. But nothing like working on a lot of problems to truly strengthen our grasp of the material. This event is an opportunity to deepen our understanding of **MMIX**. Equally we want to share our work with the group and help others with any questions.  It's also a chance for anyone who missed a session on **MMIX** to catch up.

We're dedicating the full two hours to solving exercises from *Fascicle 1, MMIX*. The format is rather free-form. A restricted Google Doc https://docs.google.com/document/d/1BUjM3CUOlHYBdgC7QOUENwP3IAk07tYx0GiFzO5cleo/edit?usp=sharing with many exercises is now available on request for members to work in and collaborate with the group. We'll work collectively and individually in parallel to attempt as many exercises as possible. And share solutions or partial work with everyone. Afterwards all our work will be posted to the meetup's Github repos for notes and exercises.

It's better not to look at the answers to exercises. Instead members are encouraged to ask questions and enter comments into the shared doc or the chat panel. Every note that reflects genuine individual thought could be useful to people who come across it in the future.

## TAOCP #4 - Basic MMIX Instructions (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 26 September 2020\
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*)

- *1.2.4 Integer Functions and Elementary Number Theory* (pp.39-40 of *TAOCP Chapter 1*, not *Fascicle 1, MMIX*)
- *1.3.1' Description of MMIX* (pp.8-12)

  - *Arithmetic operators* (pp.8-9)
  - *Conditional instructions* (p.10)
  - *Bitwise operations* (pp.10-11)
  - *Bytewise operations* (pp.11-12)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- Hands-on MMIX Visual Debugger
- *Exercises* (pp.24-28)
- Shoot the breeze

We continue to learn more about **MMIX** - the TAOCP computer!

We cover more of the instruction set architecture of **MMIX** from *Fascicle 1, MMIX*. We'll also need to consult *TAOCP, Chapter 1* for a little section on the mathematical basis for the `DIV` instruction.

We'll start with instructions for simple arithmetic. We'll learn how to compare values. We'll see instructions for working with the bits and bytes in registers.

After the break, we'll use the free and open source MMIX Visual Debugger https://mmix.cs.hm.edu/mmixvd introduced in TAOCP Meetup #3 for hands-on practice with the instructions we have learnt so far. We'll work on some exercises too.

## TAOCP #3 - Introduction to MMIX (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 19 September 2020<br>
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

### Agenda

**2:00 - 2:10** Meet and greet<br>
**2:10 - 3:00** Read and discuss couple pages at a time from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*)

- *Preface* (pp.iii-v)
- *1.3' MMIX* (p.2)
- *1.3.1' Description of MMIX* (pp.2-8)

  - *Bits and bytes* (pp.2-4)
  - *Memory and registers* (pp.4-5)
  - *Instructions* (pp.5-6)
  - *Loading and storing* (pp.6-8)

**3:00 - 3:10** Break<br>
**3:10 - 4:00** MMIX Visual Debugger, shoot the breeze<br>

We introduce the MMIX computer used throughout TAOCP!

Algorithms in TAOCP are described in pseudocode and implemented as programs written in assembly language for the MMIX computer. But an MMIX computer has never been manufactured. It can only be used in simulator programs. Outside of TAOCP, there are almost no code examples, guides, tutorials or videos. This can be a dealbreaker for many people used to an abundance of information for other programming languages readily available at popular websites.

The next few TAOCP meetups will cover enough of MMIX to attain a working knowledge sufficient to read and write simple programs. Side by side we will learn to use tools to run and debug our programs. Hopefully by the time we're done, our meetup notes, discussions and videos will lower the barrier to learning and working with MMIX.

In this first meetup on MMIX, we learn how data is represented and stored in MMIX memory. Data is operated upon using instructions from the MMIX instruction set. We'll start with instructions for moving data between memory and registers where data may be manipulated. We'll continue with more instructions in the following meetups.

We'll begin to use some invaluable tools for working with MMIX in the second half of the meetup. We'll see how to use the MMIX Visual Debugger GUI https://mmix.cs.hm.edu/mmixvd to edit, run and step through MMIX assembly language programs. The MMIX simulator and assembler https://mmix.cs.hm.edu/src are commandline tools that will be demoed in upcoming meetups. All these tools are free and open source.

## TAOCP #2 - Algorithms (Chapter 1, Basic Concepts: Section 1.1)

**Date:** Saturday, 12 September 2020<br>
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

### Agenda

**2:00 - 2:10** Meet and greet<br>
**2:10 - 3:00** Read and discuss couple pages at a time from *Volume 1, Fundamental Algorithms*: *Chapter 1, Basic Concepts*

-  *1.1 Algorithms* (pp.1-9)
-  Skim *Appendix A*, *B*, and *C* (pp.619-629)

**3:00 - 3:10** Break<br>
**3:10 - 4:00** *Exercises* (p.9), shoot the breeze<br>

Well - We begin reading TAOCP in earnest today!

As its title suggests, TAOCP is about three things - "Art", "Computers" and "Programming". Knuth spoke at length on "Art" in his Turing Award lecture https://dl.acm.org/doi/pdf/10.1145/1283920.1283929. Today we look at the foundation of "Programming" that is built upon the concept of an algorithm. And we'll spend time on "Computers" in the coming sessions.

## TAOCP #1 - Inaugural Meeting

**Date:** Saturday, 5 September 2020<br>
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

### Agenda

**2:00 - 2:10** Meet and greet<br>
**2:10 - 3:00** Read and discuss couple pages at a time of *Volume 1, Fundamental Algorithms*

-  *Preface* (pp.v-xi)
-  *Procedure for Reading* (pp.xii-xiv)
-  *Notes on Exercises* (pp.xv-xvii)

**3:00 - 3:10** Break<br>
**3:10 - 4:00** Meetup structure and schedule, shoot the breeze<br>

All - Welcome to the inaugural organizational meeting!

We'll start with reading the prefatory sections to *Volume 1, Fundamental Algorithms*. We'll go over logistics and the regular schedule.

A tentative schedule is available at https://github.com/theartofcomputerprogramming/meetup.

Each meeting will be two hours long with a 10-minute break after the first hour. We'll aim to read just a few pages of the book in the first half. Typically we'll have around 5-10 minutes to read 1-2 pages and everyone will be encouraged to enter comments, questions and thoughts in the Meet chat. Then we'll go over chat comments and discuss the text we just read for 5-10 minutes. Then we'll move on to the next couple pages.

The goal is to read with understanding, counting on the support of the entire group but not to get stuck on anything. The material can be very dense and difficult to absorb right away. If something does not click despite the discussion, there will be time in the second half for clarification when we attempt some exercises. Yet sometimes it could take a day or two for things to sink in after revisiting the material.

The second half of the meeting will be reserved for exercises and more free-form discussion of current or previous topics. Knuth has a difficulty rating for every exercise. The rating also includes a mathematical level indicator. We will attempt a few of the exercises rated *Simple* or *Medium*. We may try some of the mathematical exercises from time to time especially if the topic demands it. Here too we'd like to work out some problems as a group but not obsess over any single exercise or solution.

A shared Google Doc will be available during and for some time after the meeting for every attendee to add their own notes. Later, the doc with everybody's notes will be posted to the meetup github repo and may be edited via pull requests.

A separate repo for member solutions to exercises is available at https://github.com/theartofcomputerprogramming/exercises

It is my hope to build a permanent resource of our meeting recordings, notes and exercise solutions to help anyone who'd like to study TAOCP. More immediately it's meant to aid members who miss a meeting to catch up on their own.

## Future Meetups (Tentative)

A very rough plan for future meetups. This is constantly changing. Descriptions and agenda are just placeholders for now.

## TAOCP #38 - Alice at Wimbledon? (Chapter 5, Sorting: Section 5.3.3)

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 1 TBD 2021\
**Time:** 2-4pm America/New_York

### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.3.3 Minimum-Comparison Selection* (pp.207-216)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises*
  - Volume 3 (pp.155-158)
  - MMIX Supplement (p.89)
- Shoot the breeze

