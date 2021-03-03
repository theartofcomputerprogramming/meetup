# TAOCP #20 - Binary Trees (Chapter 2, Information Structures: Section 2.3.1)

Binary trees and proof by induction!

We wrap up the introduction to binary trees and threaded trees with two algorithms. Algorithm I (Insertion into a threaded binary tree) shows how to construct a threaded tree. Algorithm C (Copy a binary tree) may be used to copy binary trees that are threaded or unthreaded, or have threads only on one side.

Section 2.3.1 has a number of exercises that flesh out many aspects of the material. We'll attempt a few.

But first we'll go over section 1.2.1 Mathematical Induction that is part of section 1.2 Mathematical Preliminaries. We've already seen the use of induction in a proof of Algorithm T (Traverse binary tree in inorder). And it's bound to be used often to prove properties of recursive data structures like trees and of algorithms on them. Knuth's presentation of induction is quite interesting and different from that typically given in purely mathematical texts.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 23 January 2021\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 1, Basic Concepts* and *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *1.2.1 Mathematical Induction* (pp.11-18)
  - Algorithmic proof procedure (pp.11-13)
  - *Algorithm I (Construct a proof)* (pp.11-12)
  - *Algorithm E (Extended Euclid’s algorithm)* (pp.13-16)
  - Inductive assertions (pp.16-18)

- *2.3.1 Traversing Binary Trees* (pp.327-330)
  - *Algorithm I (Insertion into a threaded binary tree)* (p.327)
  - Similar trees and equivalent trees (pp.327-329)
  - *Algorithm C (Copy a binary tree)* (pp.329-330)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.18-21, 330-334), MMIX Supplement (p.39)
- Shoot the breeze

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Chat Copy

**Zartaj Majeed** 2:09 PM\
reading till 2:14

**Zartaj Majeed** 2:16 PM\
if n >= 10, then 2^n > n^3

**Zartaj Majeed** 2:19 PM\
(n + 1)^3 = n^3 + 3n^2 + 3n + 1

**James Curran** 2:20 PM\
p(n+1) = n^2  + 5n + 4 is even\
p(n) = n\* (N+3) is even

(n+1) * (n+4) is even

n^2 +4n+n + 4

**Zartaj Majeed** 2:23 PM\
n times (n + 3) is an even number

**Zartaj Majeed** 2:28 PM\
n^2 + 3n + 2n + 4
n(n + 3) + 2n + 4

**Zartaj Majeed** 2:29 PM\
induction hypothesis says n(n + 3) is even\
so that plus 2n + 4 is even\
reading till 2:35

**Zartaj Majeed** 2:39 PM\
reading till 2:46

**Arthur O'Dwyer** 2:51 PM\
Searching "dijkstra discipline of programming pdf" turns up a (presumably pirate) PDF pretty easily.

**James Curran** 2:54 PM\
P(1) = (1-a)^1 >= 1-a\
P(N+1) = (1-a)^(n+1) >= 1-A(N+1)

**Zartaj Majeed** 2:57 PM\
rhs = 1 - n - a

**James Curran** 2:57 PM\
P(n) = (1-a)^n >= 1-na

**Michael Zalewski** 2:58 PM\
P(N) =>  (1-a)^n > 1 - na

**Arthur O'Dwyer** 2:58 PM\
So we're multiplying the LHS by (1-a), which is to say we're subtracting LHS\*a from the LHS. But on the right we're subtracting a, which is to say 1\*a. And 1 >= LHS, so 1\*a >= LHS\*a, so the amount we're subtracting from the RHS is *no less than* the amount we're subtracting from the LHS.

**Michael Zalewski** 2:58 PM\
(1-a)^n(1-a) > (1 - na)( 1 - a)\
(1-a)^(n+1) > (1 - na)(1 - a)\
(10a)^(n+1) > (1 - (n+1) + na^2

**Michael Zalewski** 2:59 PM\
(10a)^(n+1) > (1 - (n+1)a + na^2\
(1-a)^(n+1) > (1 - (n+1)a + na^2

**Michael Zalewski** 3:01 PM\
(1-a)^(n+1) > (1 - (n+1)a + na^2 > 1 - (n+1)a

**Arthur O'Dwyer** 3:01 PM\
Completely off-topic, but the diagram for Exercise 8 reminds me of https://mathworld.wolfram.com/McGregorMap.html :)

**Zartaj Majeed** 3:03 PM\
reading till 3:07

**Zartaj Majeed** 3:05 PM\
threaded trees were introduced pp.322-323

**Zartaj Majeed** 3:18 PM\
break till 3:28

**Zartaj Majeed** 3:29 PM\
we're back

**Zartaj Majeed** 3:32 PM\
exercise 17 on p.332
how to find the the preorder successor of P

**Zartaj Majeed** 3:33 PM\
preorder is node - left child - right child

**Arthur O'Dwyer** 3:36 PM\
- If P has a left child, that's P\*.
- Else if P has a right child, that's P\*.
- Else let Q = P's right thread; then if Q has a right child, that's P\*.
- Else let Q = Q's right thread; then if Q has a right child, that's P\*.
- Else repeat that very last step.
(I think.)

**Zartaj Majeed** 3:39 PM\
reading till 3:46

**James Curran** 3:57 PM\
I have another thing at 4PM, so I'm going to have to bow out now.  See you next week.

**Zartaj Majeed** 3:59 PM\
reading till 4:04

**Arthur O'Dwyer** 4:00 PM\
p. 569, answer to exercise 24

**Arthur O'Dwyer** 4:01 PM\
(A,B,(C,D,E)) and ((A,B,C),D,E) would both come out as 00,11,00,11,00 in in-order traversal\
but in preorder they'd be 11,00,11,00,00 and 11,11,00,00,00 respectively

