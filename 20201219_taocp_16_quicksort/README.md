# TAOCP #16 - Quicksort (Chapter 5, Sorting: Section 5.2.2)

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
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

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

## Chat Copy

**Zartaj Majeed** 2:15 PM\
reading till 2:21

**Zartaj Majeed** 2:35 PM\
reading till 3:41\
putting up a slide that breaks out step Q7

**Zartaj Majeed** 2:41 PM\
meant 2:41, anyway ...

**Miguel Angel Iglesias** 3:01 PM\
https://stackify.com/premature-optimization-evil/
 

**Zartaj Majeed** 3:04 PM\
reading till 3:09

**Zartaj Majeed** 3:10 PM\
break till 3:19

**Zartaj Majeed** 3:19 PM\
we're back

**Zartaj Majeed** 3:22 PM\
reading till 3:29

**Zartaj Majeed** 3:40 PM\
reading till 3:45

**Zartaj Majeed** 3:55 PM\
reading till 4:01

