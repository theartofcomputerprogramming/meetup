# TAOCP #21 - Derivatives (Chapter 2, Information Structures: Section 2.3.2)

Calculus with trees!

It turns out any tree may be represented as a binary tree. We learn this correspondence in Section 2.3.2 Binary Tree Representation of Trees and use it to compute the derivative of an algebraic expression. For example the derivative of 
y = 3 * ln(x + 1) − a / x² is 
D(y) = 3 * (1 / (x + 1)) − (-(a * (2 * x)) / (x²)²)

Knuth provides the bulk of the algorithm and MMIX code for differentiation. Some parts are left to exercises. We'll try to go over the complete program.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 30 January 2021\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.3.2. Binary Tree Representation of Trees* (pp.334-346)
  - Natural correspondence of forests and binary trees (p.334-337)
  - Tree of an algebraic formula (pp.337-338), MMIX Supplement (p.39)
  - Finding the derivative (pp.338-340)
  - *Algorithm D (Differentiation)* (p.340)
  - Routines for various operators (pp.340-342)
  - *Program D (Differentiation)* (pp.342-346), MMIX Supplement (pp.39-43)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.346-348), MMIX Supplement (p.43)
- Shoot the breeze

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Chat Copy

**Zartaj Majeed** 2:14 PM\
reading till 3:21 ny

**Zartaj Majeed** 2:17 PM\
section 2.3.2 Binary Tree Representation of Trees\
sorry - reading till 2:21 ny

**Zartaj Majeed** 2:42 PM\
inorder traversal of binary tree in (3) should be postorder traversal of forest of trees in (1)

**Adam Zippor** 2:44 PM\
BKCAHEJFGD?

**Zartaj Majeed** 2:50 PM\
reading till 2:55 ny

**Zartaj Majeed** 2:53 PM\
threaded trees are defined on pp.321-323 of vol 1 3rd ed.\
the point of threaded trees is to make traversals more efficient

**Zartaj Majeed** 2:56 PM\
note memory representation of node structure is different for MMIX - shown in the MMIX supplement p.39

**Zartaj Majeed** 3:08 PM\
break till 3:18 ny

**Zartaj Majeed** 3:18 PM\
we're back
reading till 3:24 ny

**Zartaj Majeed** 3:31 PM\
reading till 3:36 ny

**Zartaj Majeed** 3:32 PM\
the Y$ notation is defined on p.321 of vol 1 3rd ed

**Zartaj Majeed** 3:34 PM\
Λ (big lambda) is a NULL link/pointer

**Zartaj Majeed** 3:37 PM\
RTAG is a flag that tells you if the right link points to an actual child (RTAG=0) or is a thread that points to the inorder successor of the node (RTAG=1)

**Zartaj Majeed** 3:52 PM\
reading till 3:59 ny

**Michael Zalewski** 4:00 PM\
3 x 1 + ln x a x 2 ^ / -

**Michael Zalewski** 4:04 PM\
D(3) 3 x 1 ...

**Michael Zalewski** 4:05 PM\
0 3 x$ 1 + ln ...\
0 3 1 x 1$ + ln ...

**Michael Zalewski** 4:06 PM\
0 3 1 x 0 1 +$ ln ...

**Michael Zalewski** 4:08 PM\
((0 3) ((1 x) (0 1)))

**Michael Zalewski** 4:15 PM\
2^n > n^3    when n > 10

**Zartaj Majeed** 4:15 PM\
p.11 of vol 1 3rd ed\
section 1.2.1 Mathematical Induction

**Michael Zalewski** 4:15 PM\
2^(n + 1) > (n + 1)^3\
2^n + 2^n > n^ 3 n^3

**Michael Zalewski** 4:17 PM\
2^n + 2^n > n^3 + 7 * n^2\
2^n + 2^n > n^3 + 3* n^2 + 3*n + 1

**Michael Zalewski** 4:18 PM\
2^(n+1) > (n+1)^3

