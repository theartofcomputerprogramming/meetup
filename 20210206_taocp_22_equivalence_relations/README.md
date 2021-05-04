# TAOCP #22 - Equivalence Relations (Chapter 2, Information Structures: Section 2.3.3)

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
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Chat Copy

**Zartaj Majeed** 2:14 PM\
reading till 2:19

**Zartaj Majeed** 2:17 PM\
the orthogonal binary tree diagram in (2) on p.349 is what Knuth calls the natural correspondence of ""general" trees/forests and binary trees

**Arthur O'Dwyer** 2:18 PM\
Fig 20(b) is on page 312.

**Zartaj Majeed** 2:18 PM\
defined on p.334 in 2.3.2

**Zartaj Majeed** 2:21 PM\
2 minutes more till 2:22

**Zartaj Majeed** 2:29 PM\
reading till 2:35

**Arthur O'Dwyer** 2:30 PM\
Btw, "Λ" is how Knuth spells "the null pointer"

**Zartaj Majeed** 2:34 PM\
exercise 2.4.12 given as an application of SCOPEd representation has to do with symbol table lookups from what I gather

**Zartaj Majeed** 2:45 PM\
reading till 2:50

**Arthur O'Dwyer** 2:49 PM\
Page 350: What is a "family" again?

**Zartaj Majeed** 2:50 PM\
I think it's the family tree\
p.311

**Zartaj Majeed** 2:59 PM\
fig 8 is level order

**Zartaj Majeed** 3:01 PM\
reading till 3:05

**Zartaj Majeed** 3:09 PM\
break till 3:19

**Zartaj Majeed** 3:19 PM\
we're back
reading till 3:25

**Arthur O'Dwyer** 3:23 PM\
Bottom of page 352 also uses "family" in the sense of "set of siblings." So I guess that's pretty well established as Knuth's intended meaning.

**Zartaj Majeed** 3:33 PM\
reading till 3:38

**Zartaj Majeed** 3:46 PM\
reading till 3:51

**Zartaj Majeed** 3:58 PM\
exercise 2.3.3.1

**Zartaj Majeed** 4:06 PM\
exercise 2.3.3.6

