# TAOCP #19 - Trees (Chapter 2, Information Structures: Section 2.3)

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
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

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
  - *Program T (Traverse binary tree in inorder)*, MMIX Supplement (pp.37-38)
  - *Program S (Symmetric (inorder) successor in a threaded binary tree)*, MMIX Supplement (p.38)
  - Analysis of Programs T and S (p.326)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.316-318, 330-334), MMIX Supplement (p.39)
- Shoot the breeze

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Chat Copy


**Zartaj Majeed** 2:18 PM\
reading till 2:23

**Arthur O'Dwyer** 2:21 PM\
"plane trees" har har

**Zartaj Majeed** 2:32 PM\
reading till 2:37

**Arthur O'Dwyer** 2:34 PM\
Page 312: I don't really get the significance of "...Figure 20(a) essentially represents Figure 19 as an _oriented_ tree..." — is it "oriented" in the sense that we can now talk about D being "to the left of" F? But in what sense did Figure 19 lack that kind of orientedness?

**Zartaj Majeed** 2:36 PM\
oriented means ordering is unimportant

**Zartaj Majeed** 2:38 PM\
Fig 19 displays an ordering of the subtrees -  to me that means it is not oriented

**Arthur O'Dwyer** 2:41 PM\
Ah, I infer from page 396 that "oriented tree" means a depiction of the tree with its root *labeled*; as opposed to an unoriented tree which would be like a matchstick figure laid out in the middle of a circular table with the root unmarked.

**Zartaj Majeed** 3:01 PM\
reading till 3:06

**Zartaj Majeed** 3:15 PM\
break till 3:16

**Zartaj Majeed** 3:17 PM\
we're back

**Zartaj Majeed** 3:24 PM\
reading till 3:31

**Arthur O'Dwyer** 3:35 PM\
The reference to "coroutines" made me wonder whether there would be some neat way to combine Algorithm T with C++20 `co_await`. I think not, though. Here's a plain old C++ version though. https://godbolt.org/z/hfej5q

**Zartaj Majeed** 3:40 PM\
Welcome Michael Lane!

**Michael Lane** 3:40 PM\
Internet is working ;D

**Zartaj Majeed** 3:42 PM\
glad to hear - chime in whenever you like

**Zartaj Majeed** 3:54 PM\
reading till 3:59

**Miguel Angel Iglesias** 3:54 PM\
I got to drop off, too early, see you next week

**Arthur O'Dwyer** 3:57 PM\
The page numbers on your slide must be wrong — reading up to Algorithm S, I'm assuming?

**Zartaj Majeed** 3:58 PM\
yes Arthur

**Zartaj Majeed** 3:59 PM\
pp.320-323 because of Fig 24

**Michael Lane** 4:03 PM\
Is it dumb to think the author is introducing some chirality to these trees?   In terms of whether LLink(x) and RLink(x) in are successor precessor.

**Zartaj Majeed** 4:07 PM\
let's discuss a little earlier - say at 4:10

**Arthur O'Dwyer** 4:08 PM\
Algorithm S ("find successor in order") isn't really a counterpart to Algorithm T ("traverse all nodes in order"); it's a counterpart to *one small piece of* Algorithm T.\
There is an "Algorithm S-prime" for use with non-threaded trees:
- Is RLINK(P) non-null? If so, set Q to RLINK(P), and then as long as LLINK(Q) is non-null, set Q to LLINK(Q).
- Otherwise, you're out of luck, give up.

**Arthur O'Dwyer** 4:13 PM\
I've got to drop off. Welcome @Michael Lane btw!

**Zartaj Majeed** 4:13 PM\
Thanks Arthur

**Zartaj Majeed** 4:15 PM\
LOC(T) is the address in memory of T\
location of T

**Michael Lane** 4:21 PM\
What edition are you guys doing? :D\
3rd :D

**Michael Lane** 4:23 PM\
This one: https://gatech.bncollege.com/shop/gatech/textbook/algorithms

