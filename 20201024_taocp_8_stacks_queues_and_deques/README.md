# TAOCP #8 - Stacks, Queues and Deques

**Date:** Saturday, 24 October 2020\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

**A recording of this event is at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

## Agenda

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

## Chat Copy

**Arthur O'Dwyer** 2:05 PM\
http://mmix.cs.hm.edu/supplement/index.html\
http://mmix.cs.hm.edu/supplement/1.3.2/ex14opt.mms

**Arthur O'Dwyer** 2:09 PM\
Not a first-timer, but I'm in Yonkers :)

**Arvind Sharma** 2:12 PM\
Love to be a part of this regularly

**Arthur O'Dwyer** 2:14 PM\
In my paper copy, this is pages i-xxi.

**Arthur O'Dwyer** 2:18 PM\
Re ".mms files", I wonder where the ".s" suffix for assembly source files first came from. Does it stand for "source"? I should ask StackExchange.\
Here's all I've found so far: https://stackoverflow.com/questions/10285410/what-are-s-files

**Arthur O'Dwyer** 2:22 PM\
also "gcc -S", yep

**James Curran** 2:25 PM\
-S\
Stop after the stage of compilation proper; do not assemble. The output is in the form of an assembler code file for each non-assembler input file specified.\
\
By default, the assembler file name for a source file is made by replacing the suffix ‘.c’, ‘.i’, etc., with ‘.s’.

**Arthur O'Dwyer** 2:30 PM\
In my paper copy of the MMIX supplement, this is pp. 15-16.

**Arthur O'Dwyer** 2:32 PM\
"Using the most significant bit has [the] advantage [that] it can be tested directly" -- but MMIX _also_ lets us test the _least_ significant bit directly, via "if odd" and "if even"! So, color me skeptical.

**Arthur O'Dwyer** 2:42 PM\
a) LDA t,TOP; LDB t,t,SUIT\
b) LDA t,TOP+SUIT; LDB t,t,0\
c) LDOU t,TOP; LDB t,t,SUIT

**Miguel Iglesias** 2:42 PM\
I also didn't realize we were using the supplement, so I don't have it, and cannot find it on the web o_O

**Arthur O'Dwyer** 2:43 PM\
"bring the quantity TOP(SUIT) into t"\
SUIT(TOP)

**Arthur O'Dwyer** 2:44 PM\
The official place to buy the supplement is https://www.oreilly.com/library/view/the-mmix-supplement/9780133992892/ , fwiw

**Miguel Iglesias** 2:44 PM\
ah too bad, already bought it from Amazon :(

**Miguel Iglesias** 2:49 PM\
I'm going to drop off, will catch up offline

**Arthur O'Dwyer** 2:50 PM\
p237 in the third edition

**James Curran** 2:51 PM\
SO ,I'm guessing\
LD1   0\
LdA TOP

**Arthur O'Dwyer** 2:52 PM\
I think MMIX calls that "SET x, 0"?\
er, "SET n, 0"

**Michael Zalewski** 2:53 PM\
LDA t,TOP\
And we will walk t through the list\
O right\
LDOU t,TOP

**Arthur O'Dwyer** 2:56 PM\
What I ended up with for the entire Exercise 8 was:\
LDOU x, TOP\
SET n, 0\
JMP Step2\
Step3: ADD n, n, 1\
LDOU x, x, NEXT\
Step2: BNZ x, Step3

**Arthur O'Dwyer** 2:59 PM\
We could replace "ADD n, n, 1" with "INCL n, 1".

**Zartaj Majeed** 3:03 PM\
Step2: PBNZ   x,Step3

**Arvind Sharma** 3:03 PM\
Thanks for sharing that Arthur

**Zartaj Majeed** 3:04 PM\
Break till 3:13 NY

**Zartaj Majeed** 3:12 PM\
I wonder if S in .s or -S stands for symbolic\
we're back

**Zartaj Majeed** 3:14 PM\
reading till 3:21 NY

**Arthur O'Dwyer** 3:15 PM\
Asked: https://retrocomputing.stackexchange.com/questions/16656/where-and-when-did-the-s-suffix-for-assembly-language-source-files-originate

**Zartaj Majeed** 3:26 PM\
Exercise 2.2.1.1 [06] An input-restricted deque is a linear list in which items may be inserted at one end but removed from either end; clearly an input-restricted deque can operate either as a stack or as a queue, if we consistently remove all items from one of the two ends. Can an output-restricted deque also be operated either as a stack or as a queue?

**Arthur O'Dwyer** 3:31 PM\
In Exercise 3, suppose we replace 'S' by '(' and replace 'X' by ')'...

**Zartaj Majeed** 3:32 PM\
2. [15 ] Imagine four railroad cars positioned on the input side of the track in Fig. 1, numbered 1, 2, 3, and 4, from left to right. Suppose we perform the following sequence of operations (which is compatible with the direction of the arrows in the diagram and does not require cars to “jump over” other cars):\
(i) move car 1 into the stack;\
(ii) move car 2 into the stack;\
(iii) move car 2 into the output;\
(iv) move car 3 into the stack;\
(v) move car 4 into the stack;\
(vi) move car 4 into the output;\
(vii) move car 3 into the output;\
(viii) move car 1 into the output.\
As a result of these operations the original order of the cars, 1234, has been changed into 2431. It is the purpose of this exercise and the following exercises to examine what permutations are obtainable in such a manner from stacks, queues, or deques.\
If there are six railroad cars numbered 123456, can they be permuted into the order 325641? Can they be permuted into the order 154623? (In case it is possible, show how to do it.)

**Arthur O'Dwyer** 3:35 PM\
((())) 321\
(()()) 231\
()()() 123\
[but not any of the other 3 permutations of three cars]

**Arthur O'Dwyer** 3:41 PM\
Exercise 5 [M28]: Show that it is possible to obtain a permutation p1p2p3...pn from 123...n using a stack, if and only if there are no indices i < j < k such that pj < pk < pi.

**Arthur O'Dwyer** 3:46 PM\
Google says these parens-strings are "Dyck words" and the number of Dyck words of length 2n (n opening and n closing braces) is the nth Catalan number.

**Arthur O'Dwyer** 3:51 PM\
What I was saying is that we can get to the possible permutations of 1,2,3 by looking at the number of _partitions_ of 3:\
(123) -> 321\
(12)(3) -> 213\
(1)(23) -> 132\
(1)(2)(3) -> 123\
...which means I missed one possibility earlier! :D\
()(()) 132\
(())() 213\
Well, I'm confusing myself...

**Arthur O'Dwyer** 3:54 PM\
Ah, we have more possibilities than *just* the partitions of n. The permutation 231 does not correspond to any partition of 3 — we push 1 on the stack and LEAVE it there while we push/pop 2 and push/pop 3, THEN pop 1. So our number of possible permutations / possible Dyck words of length 2n is GREATER than the number of partitions of n.

**Arvind Sharma** 3:56 PM\
so Arthur this affects the understanding for the second number in exercise 2 (154623)

**Arthur O'Dwyer** 3:58 PM\
https://oeis.org/A000108\
https://math.mit.edu/~apost/courses/18.204-2016/18.204_Gabriella_Baracchini_final_paper.pdf

