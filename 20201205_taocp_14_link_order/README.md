# TAOCP #14 - Link Order (Chapter 5, Sorting: Section 5.2.1)

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
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

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

## Chat Copy


**Zartaj Majeed** 2:00 PM\
can you hear me?

**Michael Zalewski** 2:00 PM\
I guess not

**Zartaj Majeed** 2:00 PM\
I heard you for a bit
now I hear scratching

**Michael Zalewski** 2:08 PM\
That's 2 more programs in MMIX! and 2 more in C! Maybe 2 more in Rust!

**Zartaj Majeed** 2:10 PM\
reading till 2:17

**Zartaj Majeed** 2:13 PM\
btw Generating functions are section 1.2.9 in Volume 1 if you're interested in more detail later\
they're actually introduced toward the end of the previous section 1.2.8 on Fibonacci numbers

**Miguel Angel Iglesias** 2:14 PM\
oh I found H?

**Arthur O'Dwyer** 2:15 PM\
"The answer must be the number of possible inversion tables, and they are easily enumerated..." There's no accounting for taste, I guess. :) It's not at all obvious to me that the b's are independent here.

**Zartaj Majeed** 2:22 PM\
reading till 2:25

**Zartaj Majeed** 2:28 PM\
reading till 2:34

**Arthur O'Dwyer** 2:31 PM\
"if p(1). . . p(N) is the stable permutation that makes..." Here Knuth seems to be using "stable" in the sense of "stable sorting," i.e. let's assume that some of the Ks are equivalent-to-each-other for sorting purposes, then a "stable" permutation is one that doesn't invert any pairs of equivalent elements.

**Arthur O'Dwyer** 2:32 PM\
There exist many stable permutations, but only one of those stable permutations will actually satisfy  K\_{p(1)} = · · · = K\_{p(N)}.

**Michael Zalewski** 2:34 PM\
A stable permutation is one that preserves the order of equal keys. If you talk about the permutations that make K ordered, there are many such, but only one of them is stable

**Arthur O'Dwyer** 2:35 PM\
:+1:

**Zartaj Majeed** 2:44 PM\
reading till 2:49

**Arthur O'Dwyer** 2:45 PM\
"We assume..." Am I reading this right, that he's interleaving the arrays K and L in memory?\
Or, looked at another way, he's just got an array of `struct R { K key; L nextidx; }` records.

**Zartaj Majeed** 2:46 PM\
so there's no separate array\
just one array of records with a LINK field\
the sorted list is interlaced in the array

**Arthur O'Dwyer** 2:49 PM\
But he's sticking with an *array* of records; he hasn't jumped all the way to an actual linked list (where L would hold addresses of records, and would be initialized to non-garbage values on entry into this function).

**Zartaj Majeed** 2:57 PM\
reading till 3:00

**Arthur O'Dwyer** 3:00 PM\
"In other words, it is generally a good idea to "batch" operations that require
long searches, so that multiple operations can be done together. If we carry this idea to its natural conclusion, we rediscover [Mergesort]"

**Zartaj Majeed** 3:03 PM\
break till 3:13

**Zartaj Majeed** 3:13 PM\
we're back\
reading till 3:19

**Arthur O'Dwyer** 3:22 PM\
The very top of page 102 indicates that (I claim) I was right, last week, about the general strategy for the "O(N)" sorting algorithm Knuth promised us at the beginning of this chapter. The strategy is to divide the _range_ of possible element values into O(N) buckets, so that there's only O(1) elements per bucket on average.

**Zartaj Majeed** 3:24 PM\
reading till 3:28

**Zartaj Majeed** 3:35 PM\
reading till 3:39

**Zartaj Majeed** 3:45 PM\
exercise 35

**Zartaj Majeed** 3:50 PM\
exercise 26

**Zartaj Majeed** 4:03 PM\
first stepthru - Algorithm L (List insertion)\
https://github.com/theartofcomputerprogramming/mmixsamples/blob/master/program_l_list_insertion.mms

**Michael Zalewski** 4:34 PM\
I have to leave for 5:00 appointment

**Zartaj Majeed** 4:36 PM\
second stepthru - Algorithm M (Multiple list insertion)\
https://github.com/theartofcomputerprogramming/mmixsamples/blob/master/program_m_multiple_list_insertion.mms

**Miguel Angel Iglesias** 4:54 PM\
see you next week!

**Zartaj Majeed** 5:16 PM\
memory references M_2, M_4, M_8\
M_8[x]\
M_8[1000]\
M_8[1001]

**Zartaj Majeed** 5:37 PM\
c programs for these two algorithms: https://github.com/theartofcomputerprogramming/programs/tree/main/vol_3_sorting_and_searching_chap_5_sorting/sec_5.2.1_sorting_by_insertion

**Zartaj Majeed** 5:43 PM\
freenode irc: ##taocp

