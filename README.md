# TAOCP - The Art Of Computer Programming Reading Group Meetup

https://www.meetup.com/theartofcomputerprogramming/

## Description

We are devoted to reading, understanding and working through The Art Of Computer Programming by Donald Knuth (TAOCP). We go through a portion of TAOCP at each meetup. Text is read out and discussed. We work on some simple and medium exercises.

The world is fortunate that over 50 years ago a person like Donald Knuth undertook an epic quest of bringing "readers to the frontiers of knowledge in every [computer science] subject that was treated". Later realizing that "the rapid rise of computer science made such a dream impossible", he decided to "concentrate on classic techniques that are likely to remain important for many more decades, and to describe them as well as [he could]".

We strongly believe Knuth has gathered timeless concepts and explained them with great flair. The material is detailed and rigorous and leavened with humor.

If you feel the same way or would like to know why the ACM Turing Award cited Knuth's TAOCP as having "served as a focal point for developing curricula and as an organizing influence on computer science", please join us in our endeavor to study and learn from TAOCP in a systematic and regular manner.

Anyone may join from anywhere. No programming knowledge is required.

## Next Meetup

[TAOCP #19 - Trees](#taocp-19---trees-chapter-2-information-structures-section-23)\
Saturday, 16 January 2021, 2-4pm America/New_York

## Scheduled and Past Meetups

All scheduled meetups in reverse chronological order

### TAOCP #19 - Trees (Chapter 2, Information Structures: Section 2.3)

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

#### Agenda

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
  - *Program T (Traverse binary tree in inorder)* (pp.320-321), MMIX Supplement (pp.37-38)
  - *Program S (Symmetric (inorder) successor in a threaded binary tree)* (pp.323-324), MMIX Supplement (p.38)
  - Analysis of Programs T and S (p.326)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.316-318, 330-334), MMIX Supplement (p.39)
- Shoot the breeze

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.


### TAOCP #18 - Radix Sort (Chapter 5, Sorting: Section 5.2.5)

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

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

### TAOCP #17 - Mergesort (Chapter 5, Sorting: Sections 5.2.3, 5.2.4)

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

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #16 - Quicksort (Chapter 5, Sorting: Section 5.2.2)

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

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #15 - Batcher Sort (Chapter 5, Sorting: Section 5.2.2)

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

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #14 - Link Order (Chapter 5, Sorting: Section 5.2.1)

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

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #13 - Shellsort (Chapter 5, Sorting: Section 5.2.1)

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

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #12 - Sorting (Chapter 5, Sorting: Section 5.2)

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

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #11 - Polynomial Arithmetic and Circular Lists (Chapter 2, Information Structures: Section 2.2.4) 

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

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #10 - Topological Sort and Linked Lists (Chapter 2, Information Structures: Section 2.2.3)

Linked lists!

We look at adding links to nodes in a list to allow more flexible memory allocation schemes. We discuss what would need to be done for insertions and deletions. We go over tradeoffs between linked allocation and sequential allocation.

Then we use linked lists in an algorithm for topological sorting to create a linear order on a set of items that only has a partial order. We'll work on some exercises as well.

After the main meetup session, we'll continue to record a demo and walkthrough of Program T for topological sorting in the MMIX Visual Debugger. Attendees will be welcome to stay on if they desire.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

**Date:** Saturday, 7 November 2020\
**Time:** 2-4pm America/New_York

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.


### TAOCP #9 - Sequential Allocation (Chapter 2, Information Structures: Section 2.2.2)

Memory allocation schemes!

We've begun to look at lists of records that may grow and shrink. Now we consider how to manage these lists in memory. We'll look at a few algorithms for sequential allocation and work on some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

**Date:** Saturday, 31 October 2020\
**Time:** 2-4pm America/New_York

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #8 - Stacks, Queues and Deques (Chapter 2, Information Structures: Section 2.1-2.2)

**Date:** Saturday, 24 October 2020\
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #7 - MMIX Programming (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 17 October 2020\
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #6 - MMIX Branching (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 10 October 2020\
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #5 - MMIX Problem Fest (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 3 October 2020\
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #4 - Basic MMIX Instructions (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 26 September 2020\
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #3 - Introduction to MMIX (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 19 September 2020<br>
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

#### Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #2 - Algorithms (Chapter 1, Basic Concepts: Section 1.1)

**Date:** Saturday, 12 September 2020<br>
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

#### Agenda

**2:00 - 2:10** Meet and greet<br>
**2:10 - 3:00** Read and discuss couple pages at a time from *Volume 1, Fundamental Algorithms*: *Chapter 1, Basic Concepts*

-  *1.1 Algorithms* (pp.1-9)
-  Skim *Appendix A*, *B*, and *C* (pp.619-629)

**3:00 - 3:10** Break<br>
**3:10 - 4:00** *Exercises* (p.9), shoot the breeze<br>

Well - We begin reading TAOCP in earnest today!

As its title suggests, TAOCP is about three things - "Art", "Computers" and "Programming". Knuth spoke at length on "Art" in his Turing Award lecture https://dl.acm.org/doi/pdf/10.1145/1283920.1283929. Today we look at the foundation of "Programming" that is built upon the concept of an algorithm. And we'll spend time on "Computers" in the coming sessions.

### TAOCP #1 - Inaugural Meeting

**Date:** Saturday, 5 September 2020<br>
**Time:** 2-4pm America/New_York

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Google Meet link will be updated here and sent to attendees before the meeting.

#### Agenda

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

### TAOCP #19 - Doubly Linked Lists (Chapter 2, Information Structures: Section 2.2.5)

Linked lists!

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 1 TBD 2021\
**Time:** 2-4pm America/New_York

#### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.2 Linear Lists* (pp.280-296)
  - *2.2.5 Doubly Linked Lists* (pp.280-296)

**3:00 - 3:10** Break\
**3:10 - 4:00** *Exercises* (pp.297-298), shoot the breeze

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #20 - Multidimensional Arrays (Chapter 2, Information Structures: Section 2.2.6) 

Matrices!

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 1 TBD 2021\
**Time:** 2-4pm America/New_York

#### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.2 Linear Lists* (pp.298-305)
  - *2.2.6 Arrays and Orthogonal Lists* (pp.298-305)

**3:00 - 3:10** Break\
**3:10 - 4:00** *Exercises* (pp.305-307), shoot the breeze

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #22 - Binary Trees (Chapter 2, Information Structures: Section 2.3.1)

Binary Trees!

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 1 TBD 2021\
**Time:** 2-4pm America/New_York

#### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3 Trees* (pp.308-330)
  - *2.3.1 Traversing Binary Trees* (pp.318-330)

**3:00 - 3:10** Break\
**3:10 - 4:00** *Exercises* (pp.330-334), shoot the breeze

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #23 - Binary Tree Representation Of Trees (Chapter 2, Information Structures: Section 2.3.2)

Binary Trees!

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 1 TBD 2021\
**Time:** 2-4pm America/New_York

#### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3 Trees* (pp.334-346)
  - *2.3.2 Binary Tree Representation of Trees* (pp.334-346)

**3:00 - 3:10** Break\
**3:10 - 4:00** *Exercises* (pp.346-348), shoot the breeze

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #24 - Other Representations Of Trees (Chapter 2, Information Structures: Section 2.3.3) 

Binary Trees!

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 1 TBD 2021\
**Time:** 2-4pm America/New_York

#### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3 Trees* (pp.348-359)
  - *2.3.3 Other Representations of Trees* (pp.348-359)

**3:00 - 3:10** Break<br>
**3:10 - 4:00** *Exercises* (pp.359-362), shoot the breeze

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

### TAOCP #25 - Path Length In Trees (Chapter 2, Information Structures: Section 2.3.4.5)

Binary Trees!

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 1 TBD 2021\
**Time:** 2-4pm America/New_York

#### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3 Trees* (pp.399-404)
  - *2.3.4.5 Path Length* (pp.399-404)

**3:00 - 3:10** Break\
**3:10 - 4:00** *Exercises* (pp.404-406), shoot the breeze


**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.
