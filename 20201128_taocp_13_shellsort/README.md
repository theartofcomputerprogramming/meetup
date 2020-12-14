# TAOCP #13 - Shellsort (Chapter 5, Sorting: Section 5.2.1)

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
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

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

## Chat Copy

**Zartaj Majeed** 2:10 PM\
reading till 2:13

**Zartaj Majeed** 2:16 PM\
reading till 2:21

**Zartaj Majeed** 2:36 PM\
reading till 2:43

**Arthur O'Dwyer** 2:37 PM\
I just googled up this manual on the LARC Scientific Compiler, since I didn't really understand that anecdote as well as I'd like to. http://archive.computerhistory.org/resources/text/Knuth_Don_X4100/PDF_index/k-9-pdf/k-9-u2226-LARC-scientific-compiler.pdf<br>
I confirm that the note on the first page is written in Knuth's handwriting. :)

**Arthur O'Dwyer** 2:40 PM\
On the difference between "insertion sort" and "bubble sort", I found this extremely enlightening (although I'll forget it again in a minute): https://stackoverflow.com/a/17271911/1424877

**Zartaj Majeed** 2:43 PM\
thanks Arthur - this will certainly help make more sense of Knuth's description of LARC

**Arthur O'Dwyer** 2:48 PM\
It looks to me like the colon in Table 1 is the "sorted up to here" point, and the caret underneath is the "here's the insertion point" point.

**Zartaj Majeed** 2:51 PM\
reading till 2:58

**Arthur O'Dwyer** 2:57 PM\
On page 82, do we implicitly assume that "A" and "B" are independent of each other? Is their independence mathematically obvious? And/or is there some deep mathematical reason that they don't need to be independent?

**Arthur O'Dwyer** 3:07 PM\
H_N

**Zartaj Majeed** 3:09 PM\
break till 3:20

**Michael Zalewski** 3:16 PM\
I guess Hn is the Harmonic Number. H1 = 1, H2 = 1 + 1/2, H3 = 1 + 1/2 + 1/3. Defined on page 101

**Zartaj Majeed** 3:17 PM\
yes - Volume 1, 1.2.7 Harmonic Numbers

**Zartaj Majeed** 3:20 PM\
we're back

**Zartaj Majeed** 3:21 PM\
reading till 3:24

**Arthur O'Dwyer** 3:24 PM\
I failed to google any information on the IBM 705 "tumble" instruction. But I did learn that some IBM printers use the term "tumble duplex" to describe double-sided printing where the binding goes at the top edge instead of the side. :P

**Zartaj Majeed** 3:25 PM\
reading till 3:30

**Zartaj Majeed** 3:32 PM\
referring to Table 3

**Zartaj Majeed** 3:41 PM\
reading till 3:48

**Zartaj Majeed** 3:50 PM\
exercise 1

**Arthur O'Dwyer** 3:59 PM\
Hmm.
a[0]=3, a[1]=0, a[3]=1, a[4]=1, a[7]=4, a[10]=2, ...\
appears to be 7-ordered, but 3-sorting it produces a[1]=0, a[4]=1, a[7]=2, a[10]=4, ...

**Zartaj Majeed** 4:05 PM\
MMIX source for Algorithm S (Straight insertion sort): https://github.com/theartofcomputerprogramming/mmixsamples/blob/master/program_s_straight_insertion_sort.mms

**Jolene D** 4:09 PM\
also dropping off now, thanks all and see you next time!

**Michael Zalewski** 4:29 PM\
Thanks Zartaj

