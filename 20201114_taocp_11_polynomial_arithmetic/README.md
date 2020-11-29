# TAOCP #11 - Polynomial Arithmetic and Circular Lists (Chapter 2, Information Structures: Section 2.2.4) 

Circular lists!

Linking the last node of a list to the first has advantages that we explore in this meetup. We see how insertion and deletion is affected. And consider how to properly handle an empty circular list.

The problem for this section is of arithmetic on polynomials. We present algorithms for adding and multiplying polynomials in three variables, x, y and z. For example

(x<sup>4</sup> + 2x³y + 3x²y² + 4xy³ + 5y<sup>4</sup>) * (x² - 2xy + y²) = x<sup>6</sup> - 6xy<sup>5</sup> + 5y<sup>6</sup>

We see why circular lists are good data structures to use for this problem.

We'll work on some exercises too.

After the main meetup session, we'll continue to record a walkthrough in the MMIX Visual Debugger of Program A for polynomial addition from The MMIX Supplement. Attendees will be welcome to stay on for as long as they like. This bonus segment will run for as long as it takes to complete the walkthrough including any discussion with attendees who remain present.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

**Date:** Saturday, 14 November 2020\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.2 Linear Lists* (pp.273-278)

  - *2.2.4 Circular Lists* (pp.273-275)
  - *Arithmetic on polynomials* (pp.275-276), MMIX Supplement (pp.25-26)
  - *Algorithm A (Addition of polynomials)* (p.276)
  - *Algorithm M (Multiplication of polynomials)* (p.277)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.278-280), MMIX Supplement (p.27)
- Shoot the breeze

**Bonus Segment**

Stepthru in MMIX Visual Debugger

- *Program A (Addition of polynomials)* from MMIX Supplement (p.26)

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Chat Copy


**Zartaj Majeed** 2:04 PM\
IRC channel on freenode ##taocp

**Zartaj Majeed** 2:06 PM\
https://webchat.freenode.net/##taocp

**Michael Zalewski** 2:20 PM\
count the predecessors, maintain a list of successors

**Zartaj Majeed** 2:24 PM\
reading till 2:28

**Arthur O'Dwyer** 2:28 PM\
"For example, it is very convenient to "erase" a list, that is, to put an entire circular list onto the AVAIL stack at once."\
This is an interesting difference between Knuth's very-low-level approach and usual industry practice. Normally in practice we wouldn't get to assume that our linked list and our "free store" data structure shared _exactly_ the same representation, and so freeing a whole list is normally just as expensive as walking over the whole list.

**Michael Zalewski** 2:40 PM\
Deleted nodes go into AVAIL, but when you want a new node and AVAIL is empty, you make a new node from BOTTOM of sequential free memory\
or TOP... FRONT... BACK... whatever free sequential memory pronouns are in effect

**Michael Zalewski** 2:42 PM\
MATLAB solves these problems pretty good

**Zartaj Majeed** 2:42 PM\
1 minute on problem description then your approaches to solving

**Zartaj Majeed** 2:51 PM\
reading till 2:58

**Arthur O'Dwyer** 2:51 PM\
For example, the first polynomial on page 275 would be represented as the 5-element vector {((4,0),1),  ((3,1),2), ((2,2),3), ((1,3),4), ((0,4),5)}

**Zartaj Majeed** 2:52 PM\
there's a little piece in the MMIX Supplement too

**Arthur O'Dwyer** 2:52 PM\
and the second as the 3-element vector {((2,0),1), ((1,1),-2), ((0,2),1)}

**Zartaj Majeed** 3:07 PM\
break till 3:16

**Zartaj Majeed** 3:17 PM\
we're  back
reading till 3:23

**Michael Zalewski** 3:30 PM\
Why not replace polynomial P with P * M like algorithm A did? Ans: it's a lot harder to maintain P with sorted exponents.

**Arthur O'Dwyer** 3:34 PM\
Remember "ABC(K)" means the exponents of polynomial term K. Unless ABC(K)== -1, which means we're at the end of the list.

**Jolene Dunne** 3:34 PM\
got to drop off, thanks and see you all next time!

**Arthur O'Dwyer** 3:38 PM\
"such as (1)" -- on page 273

**Miguel Angel Iglesias** 3:43 PM\
what exercise are we looking at?

**Zartaj Majeed** 3:43 PM\
this was ex 9
ex 9 for multiplication

**Miguel Angel Iglesias** 3:45 PM\
A would work for P=Q right?

**Arthur O'Dwyer** 3:45 PM\
I think yes, Algorithm A works if P=Q.\
I think Algorithm M works if P=M, but *not* if Q=P nor if Q=M.

**Arthur O'Dwyer** 3:46 PM\
Certainly multiplication is commutative, so we know that "the algorithm works if Q=P" must have the same truth-value as "the algorithm works if Q=M".

**Zartaj Majeed** 3:48 PM\
(x + y) + (xy) * (xy + y)\
example: (x + y) + (xy) * (xy + y)

**Zartaj Majeed** 3:49 PM\
Q = x + y, M = xy, P = xy + y

**Zartaj Majeed** 3:50 PM\
Q = x+y, M=xy, P=xy\
Q= x+y, M=xy, P=x+y

**Miguel Angel Iglesias** 3:52 PM\
P + P * M

**Zartaj Majeed** 3:54 PM\
ex 17\
what's the benefit of a circular list over straight linked list?\
Michael - ex 17

**Zartaj Majeed** 3:57 PM\
last one - ex 18

**Arthur O'Dwyer** 3:57 PM\
Spoiler alert: https://en.wikipedia.org/wiki/XOR_linked_list

**Arthur O'Dwyer** 4:03 PM\
You want to be able to combine LINK(x_i) with (x\_{i-1}) to produce the value (x\_{i+1}); and you want to be able to combine LINK(x_i) with (x\_{i+1}) to produce the value (x\_{i-1}).

**Arthur O'Dwyer** 4:05 PM\
Right. You want to make LINK(x_i) == (x\_{i-1}) XOR (x\_{i+1}).\
Combining LINK(x_i) with (x\_{i-1}) gives you (x\_{i+1}).\
Combining LINK(x_i) with (x\_{i+1}) gives you (x\_{i-1}).

**Arthur O'Dwyer** 4:08 PM\
I won't be here next week (the 21st), but I could do Thanksgiving weekend probably.

**Zartaj Majeed** 4:10 PM\
https://github.com/theartofcomputerprogramming/mmixsamples/blob/master/program_a_addition_of_polynomials.mms

**Arthur O'Dwyer** 4:16 PM\
Kind of weird that the syntax highlighting treats ';' as '//'.

**Arthur O'Dwyer** 4:23 PM\
I'll have to drop off ~4:30, myself.

**Zartaj Majeed** 4:25 PM\
P: 5xy + 7x + 7yz + 20\
Q: 3xy - 7yz + 3y - 20


