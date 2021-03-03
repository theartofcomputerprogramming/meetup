# TAOCP #23 - Polynomials As Trees (Chapter 2, Information Structures: Sections 2.3.3, 2.3.4.5)

Trees above! Trees to the left! Trees to the right! Trees below????

We examine more complex representations of trees. A particular doubly linked ring structure is applied to the problem of arithmetic on polynomials.

We have previously seen algorithms for polynomial addition and multiplication using circular lists. Those however were limited to polynomials in three or four variables.

We close out section 2.3.3 Other Representations of Trees with Algorithm A (Addition of polynomials) that works for polynomials in any number of variables. The algorithm illustrates traversal, insertion, and deletion in a four-way-linked tree.

Then we jump to section 2.3.4.5 Path length. We look at extended binary trees that insure every node of the original tree has two children. This is used to establish some results on path lengths in binary trees that are generalized to ternary, quaternary and higher-order trees.

Finally we consider associating weights with the nodes of a tree and look at Huffman's method for finding a tree with minimum weighted path length.

We'll do some exercises

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 13 February 2021\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3.3 Other Representations of Trees* (pp.355-359)
  - Ring structures (pp.355-357)
  - *Algorithm A (Addition of polynomials)* (pp.357-359), MMIX Supplement (pp.43-44)

- *2.3.4.5 Path length* (pp.399-404)
  - Extended binary tree (pp.399-400)
  - Internal and external path lengths (p.400)
  - Complete binary trees and higher-order trees (pp.401-402)
  - Huffman's method for weighted path lengths (pp.402-404)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.359-362, 404-406)
- Shoot the breeze

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Chat Copy

**Zartaj Majeed** 2:19 PM\
reading till 2:26

**Arthur O'Dwyer** 2:20 PM\
This is your weekly reminder that Knuth uses "Λ" to mean "null pointer" :)

**Miguel Angel Iglesias** 2:21 PM\
this Λ means "null" btw

**Zartaj Majeed** 2:22 PM\
don't worry about thread versus unthreaded trees here\
but later you can find threaded trees defined on p.322

**Shreevatsa R** 2:31 PM\
I think "CV" may stand for "either a Constant or the Variable name"

**Arthur O'Dwyer** 2:35 PM\
In a sense, Miguel, our DOWN and RIGHT here are playing the role of LLINK and RLINK in the "corresponding binary tree" stuff.\
DOWN points to my eldest child; RIGHT points to my next-youngest sibling.

**Arthur O'Dwyer** 2:41 PM\
(And I said "LLINK and RLINK," but we even saw one place last week where Knuth calls them "LCHILD and RLINK". Here he's calling them "DOWN and RIGHT".)

**Shreevatsa R** 2:42 PM\
If I understand correctly, the idea is that the given polynomial\
3 + x^2 + xyz + z^3 - 3xz^3\
can be written out as a polyomial in z, namely\
z^0(3 + x^2) + z^1(xy) + z^3(1 - 3x)\
and these 3 polynomials (namely 3+x^2, xy, and 1-3x) are the 3 "children" of the root node, themselves represented (recursively) using the same representation.

**Arthur O'Dwyer** 2:42 PM\
:+1:

**Zartaj Majeed** 2:44 PM\
reading till 2:50\
That's great Shreevatsa! These comments are immensely useful for viewers of the recordings!

**Zartaj Majeed** 2:49 PM\
AVAIL is the free memory allocator\
R <= AVAIL means allocate a node and assign to R

**Arthur O'Dwyer** 2:50 PM\
"Before and after diagrams" are explained a bit on page 260.

**Zartaj Majeed** 2:50 PM\
AVAIL <= R means free the node or return node to memory pool\
read another couple minutes

**Zartaj Majeed** 2:54 PM\
can we try adding the examples he gives?

**Zartaj Majeed** 2:55 PM\
3 + x^2 + x * y * z + z^3 − 3 * x * z^3

**Zartaj Majeed** 2:56 PM\
(x * y) − (x^2) − (x * y * z) − (z^3) + (3 * x * z^3)

**Zartaj Majeed** 3:00 PM\
z^0 * (( x * y) - (x^2)) + z^1 * ( (-1) * (x * y) ) + z^3 * ( (-1) + (3 * x))

**Zartaj Majeed** 3:10 PM\
break till 3:20

**Shreevatsa R** 3:14 PM\
https://imgur.com/SLdjLnE

**Arthur O'Dwyer** 3:18 PM\
Here's mine. Let's see if they match! https://i.imgur.com/VUONGNm.jpg

**Arthur O'Dwyer** 3:19 PM\
Three places near the bottom left: My understanding is that EXP(DOWN(x)) must invariably be zero (when DOWN(x) is not Λ).\
Other than that, we match.

**Shreevatsa R** 3:20 PM\
yeah, looks like the difference is I left out the (0, 0) nodes... I think I'm missing why are they needed

**Zartaj Majeed** 3:21 PM\
we're back

**Michael Zalewski** 3:21 PM\
You need the 0,0 nodes to define the part of the polynomial that does not include the parent's variable

**Shreevatsa R** 3:22 PM\
ah yes, makes sense, thanks

**Miguel Angel Iglesias** 3:53 PM\
I fear we used up too much time in this algorithm, I fail to see its significance, other than as an example of what can be done with a circular Tree, the next section we were going to talk about, Path Length seems way more relevant

**Zartaj Majeed** 3:54 PM\
true Miguel - we will be sure to continue with path length next Saturday

**Shreevatsa R** 3:58 PM\
The page does say "Our main interest in Algorithm A is the way it typifies manipulations on trees with many links." ... so it's indeed intended as an example mainly I think

**Zartaj Majeed** 3:59 PM\
it looks liike P + Q = 3 + x y

**Shreevatsa R** 4:13 PM\
Funnily the page also says "In Chapter 8 we will consider another format for polynomial representation [...] with significant advantages of conceptual simplicity..." and Chapter 8 (yet to be published) is Recursion, so this probably refers to a more straightforward recursive representation way we might think of implementing (multi-variable) polynomial addition today

**Arthur O'Dwyer** 4:13 PM\
3 + xx + xyz + zzz + 3xzzz\
\+ xy - xx - xyz - zzz + 3xzzz\
should have produced "3 + xy + 6xzzz", I guess

