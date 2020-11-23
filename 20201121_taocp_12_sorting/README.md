# TAOCP #12 - Sorting (Chapter 5, Sorting: Section 5.2)

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
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

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

## Chat Copy

**Zartaj Majeed** 2:15 PM\
reading till 2:22

**Sensea Sensea** 2:24 PM\
exchange

**Sensea Sensea** 2:27 PM\
bubble sort most popular likely

**Zartaj Majeed** 2:31 PM\
reading till 2:37

**Zartaj Majeed** 2:39 PM\
K: 5, -2, -3, 6\
COUNT: ?

**Miguel Angel Iglesias** 2:40 PM\
0,0,0,0

**Miguel Angel Iglesias** 2:42 PM\
0,0,0,3
 

**James Curran** 2:42 PM\
1,1,0,3

**James Curran** 2:44 PM\
2,1,0,3

**James Curran** 2:49 PM\
final [0] = data[address[0]  ]\
final[count[0]] = data[0]

**Miguel Angel Iglesias** 2:53 PM\
brb

**Sensea Sensea** 2:54 PM\
5  | -2 | -3 | 6\
2 | 1 | 0 | 3

**Michael Zalewski** 2:57 PM\
DATA = 4 3 1 2\
COUNT = 3 2 0 1\
DATA[ COUNT[ 0] ] = 2, which is not the min

**Zartaj Majeed** 3:00 PM\
thanks Michael!

**Zartaj Majeed** 3:03 PM\
break till 3:14

**Zartaj Majeed** 3:15 PM\
we're back

**Zartaj Majeed** 3:19 PM\
reading till 3:26

**Zartaj Majeed** 3:26 PM\
ex 6:\
K: 5, 0, 5, 0, 9, 1, 8, 2, 6, 4, 1, 5, 6, 6, 7, 7\
N = 16

**Zartaj Majeed** 3:29 PM\
initialize: COUNT[0..9]
COUNT: 0, 0, 0, 0, 0, 0, 0, 0, 0, 0

**James Curran** 3:31 PM\
after D3: count = [2,2,1,0,1,3,3,2,1,1]\
after D4, count = [2,4,5,5,6,9,12,14,15,16]

**James Curran** 3:38 PM\
final[0..2] = 0\
final[3..4] = 1|\
final[5..5] = 2|\
final[-] = 3|\
final[6..6] = 4

**Miguel Angel Iglesias** 3:49 PM\
I got to drop off, see you next time!

**Sensea Sensea** 3:54 PM\
need to run, catch up in the replay

**Zartaj Majeed** 3:55 PM\
thanks Paul!


