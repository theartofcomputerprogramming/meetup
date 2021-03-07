# TAOCP #24 - Huffman Trees (Chapter 2, Information Structures: Sections 2.3.4.5)

We look at the concept of path length in trees in section 2.3.4.5 that Knuth considers "of great importance in the analysis of algorithms, since this quantity is often directly related to the execution time".

We look at extended binary trees that insure every node of the original tree has two children. This is used to establish some short results on path lengths in binary trees that are generalized to ternary, quaternary and higher-order trees.

Finally we consider associating weights with the nodes of a tree and look at Huffman's method for finding a tree with minimum weighted path length.

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 20 February 2021\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

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

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Chat Copy

**Zartaj Majeed** 2:17 PM\
reading till 2:22

**Zartaj Majeed** 2:19 PM\
the result about the number of edges of a free tree is on pp.363-364

**Zartaj Majeed** 2:21 PM\
specifically Theorem A a) G is a free tree with n > 0 vertices implies d) G contains no cycles and has n − 1 edges

**Arthur O'Dwyer** 2:22 PM\
"To prove formula (3), consider deleting..." seems to be presented backwards; I think it'd be (a) more technically correct logical induction and (b) clearer if he'd said "Consider replacing an external node at distance k with an internal node."\
Then all that remains to prove is that every binary tree is constructible by iterating this "add a node" step starting from the empty tree.

**Zartaj Majeed** 2:24 PM\
reading till 2:29

**Zartaj Majeed** 2:42 PM\
reading till 2:47

**Zartaj Majeed** 2:56 PM\
reading till 3:01

**Arthur O'Dwyer** 2:57 PM\
= (n+1)(lg n + O(1)) - 2^(lg n + O(1)) + 2\
= (n lg n) + lg n + O(n) + O(1) - (2^O(1)) * n + 2\
= (n lg n) + lg n + O(n) + O(1) - O(n) + 2\
= (n lg n) + O(n)

**Zartaj Majeed** 3:02 PM\
break till 3:12

**Zartaj Majeed** 3:12 PM\
we're back\
reading till 3:18

**Arthur O'Dwyer** 3:32 PM\
Divide our 20 possibilities into:\
(2 3 4), (11)\
Then recursively divide the left-hand 9 possibilities into:\
(4), (2 3)\
and so on

**Zartaj Majeed** 3:36 PM\
reading till 3:41

**Arthur O'Dwyer** 3:38 PM\
"we can apply it to the merging of sorted sequences" — ah, I see (I think). He means if we have a bunch of small sorted sequences but we're allowed to merge only 2 at a time. It takes (n+m) time to merge a sequence of length n with a sequence of length m. So we want to merge the smaller sequences first and save the longer sequences for later (higher up in our "tree" of merges).

**Zartaj Majeed** 3:50 PM\
reading till 3:54

**Arthur O'Dwyer** 3:51 PM\
Re my extended "20 Questions" problem: I'm fairly confident that if you have a fixed list of "questions" you're allowed to ask (e.g. suppose I know a question that distinguishes A,B,C from D,E,F, but I don't know any single question that distinguishes A,B,E from C,D,F), then the top-down "20 Questions" algorithm is the only optimal solution. Huffman's bottom-up solution stops working.\
Because perhaps E and F are the least likely answers, so I want to keep them together in the lowest subtree; but in fact all the questions I know *distinguish* between E and F. So I physically can't keep them together in the same subtree.

**Arthur O'Dwyer** 3:54 PM\
(or rather, Huffman would greedily keep them together in the lowest subtree, thus producing a subtree that would not be physically possible to place into the larger tree)

**Michael Zalewski** 3:54 PM\
You need something stronger than a "fixed list of question". A fixed list might not be sufficient to arrive at an answer.

**Arthur O'Dwyer** 4:18 PM\
"Convex function" is what we called "concave up" in high school.

