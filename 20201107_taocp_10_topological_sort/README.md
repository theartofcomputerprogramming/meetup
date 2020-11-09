# TAOCP #10 - Topological Sort and Linked Lists (Chapter 2, Information Structures: Section 2.2.3)

Linked lists!

We look at adding links to nodes in a list to allow more flexible memory allocation schemes. We discuss what would need to be done for insertions and deletions. We go over tradeoffs between linked allocation and sequential allocation.

Then we use linked lists in an algorithm for topological sorting to create a linear order on a set of items that only has a partial order. We'll work on some exercises as well.

After the main meetup session, we'll continue to record a demo and walkthrough of Program T for topological sorting in the MMIX Visual Debugger. Attendees will be welcome to stay on if they desire.

**A recording of this event is at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

**Date:** Saturday, 7 November 2020\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

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

## Chat Copy

**Michael Zalewski** 2:28 PM\
He kind of glosses over the 'extra memory' problem. He assumes that we can fit both LINK and INFO into a single OCTA

**Miguel Angel Iglesias** 2:37 PM\
brb

**Zartaj Majeed** 2:52 PM\
T for TOP of stack

**Michael Zalewski** 2:59 PM\
On p 256, he says a node has one word and that it is broken into the two fields INFO and LINK. But in the MMIX Supplement, INFO and LINK are consecutive words

**Zartaj Majeed** 3:03 PM\
break till 3:13

**Zartaj Majeed** 3:14 PM\
we're back

**Zartaj Majeed** 3:30 PM\
pick 9 then 2 then 5\
5 cannot be removed right now\
remove 1\
so we have 9, 2, 1\
then remove 3\
then 7

**Zartaj Majeed** 3:31 PM\
so we have 9, 2, 1, 3, 7, ...

**Jolene Dunne** 3:37 PM\
I need to drop off now unfortunately, thanks everyone and see you next week!

**Zartaj Majeed** 3:39 PM\
thanks Jolene

**Zartaj Majeed** 3:41 PM\
reading till 3:46

**Michael Zalewski** 3:43 PM\
The input to the problem can be thought of a a list of the 'arrows' from the network diagram in Fig. 6. But I think we are more likely to receive input as a list of the 'nodes'. (And each node would require its own list of outgoing arrows)

**Zartaj Majeed** 3:55 PM\
reading till 4:02

**Miguel Angel Iglesias** 4:40 PM\
got to drop off, see you next week!

**Zartaj Majeed** 5:58 PM\
Michael - your webcam is still on!


