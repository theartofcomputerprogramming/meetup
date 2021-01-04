# TAOCP #15 - Batcher Sort (Chapter 5, Sorting: Section 5.2.2)

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
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

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

## Chat Copy

**Zartaj Majeed** 2:09 PM\
reading till 2:14

**Arthur O'Dwyer** 2:14 PM\
IIUC, the horizontal lines in Fig 14 don't actually numerically correspond to the values of "t" in Algorithm B.

**Zartaj Majeed** 2:18 PM\
reading till 2:22

**Arthur O'Dwyer** 2:19 PM\
Ah, I see: The horizontal line ("water level") in the Nth column [where the leftmost column is the 0th column] goes in between the last two elements to have been actually swapped in Pass N.

**Zartaj Majeed** 2:22 PM\
yes - t is the temporary tracking that level\
and BOUND gets updated to t at the end of loop

**Zartaj Majeed** 2:34 PM\
reading till 2:37

**Zartaj Majeed** 2:47 PM\
reading till 2:50

**Arthur O'Dwyer** 2:48 PM\
Is the final `POP 0,0` instruction basically just a no-op that he put there so that there'd be somewhere to hang label 9H? Or is it significant to the operation of the program?

**Arthur O'Dwyer** 2:52 PM\
"Another idea is to eliminate most of the exchanges; since most elements simply shift left one step during an exchange, we could achieve the same effect by viewing the array differently, shifting the origin of indexing"\
I don't follow this part.

**Zartaj Majeed** 3:02 PM\
reading till 3:05

**Arthur O'Dwyer** 3:03 PM\
Historical note: Ken Iverson's "A Programming Language" is also known as "APL". :)

**Arthur O'Dwyer** 3:05 PM\
5.1.1 exercise 5 sketches an O(n lg n) algorithm for computing a permutation from its inversion table.

**Zartaj Majeed** 3:05 PM\
break till 3:15

**Zartaj Majeed** 3:16 PM\
we're back

**Zartaj Majeed** 3:27 PM\
reading till 3:34

**Arthur O'Dwyer** 3:59 PM\
16 16 0 16\
8 16 0 8\
8 8 8 8

**Arthur O'Dwyer** 4:03 PM\
https://en.wikipedia.org/wiki/Hybrid_algorithm\
https://en.wikipedia.org/wiki/Introsort

**Zartaj Majeed** 4:07 PM\
MMIX stepthru of Bubble sort - https://github.com/theartofcomputerprogramming/mmixsamples/blob/master/program_b_bubble_sort.mms

**Arthur O'Dwyer** 4:19 PM\
I just wrote up this C++ "bubblesort vs. shaker sort" demo: https://godbolt.org/z/avEcjT\
Now I'm trying to write up the "shift up by 1, shift down by 1" variation of shaker sort...

**Zartaj Majeed** 4:31 PM\
break for 5 minutes

**Zartaj Majeed** 4:35 PM\
we're back

**Zartaj Majeed** 5:27 PM\
array in memory corresponds to array in Table 1 after pass 1 on row 1\
i.e. this is row 2 of Table 1

**Zartaj Majeed** 5:30 PM\
this is now row 4 of Table 1\
this is row 6 of Table 1

