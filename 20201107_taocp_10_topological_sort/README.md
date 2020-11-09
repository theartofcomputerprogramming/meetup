# TAOCP #11 - Polynomial Arithmetic and Circular Lists (Chapter 2, Information Structures: Section 2.2.4) 

Circular lists!

Linking the last node of a list to the first has advantages that we explore in this meetup. We see how insertion and deletion is affected. And consider how to properly handle an empty circular list.

The problem for this section is of arithmetic on polynomials. We present algorithms for adding and multiplying polynomials in three variables, x, y and z. For example

(x<sup>4</sup> + 2x³y + 3x²y² + 4xy³ + 5y<sup>4</sup>) * (x² - 2xy + y²) = x<sup>6</sup> - 6xy<sup>5</sup> + 5y<sup>6</sup>

We see why circular lists are good data structures to use for this problem.

We'll work on some exercises too.

After the main meetup session, we'll continue to record a walkthrough in the MMIX Visual Debugger of Program A for polynomial addition from The MMIX Supplement. Attendees will be welcome to stay on for as long as they like. This bonus segment will run for as long as it takes to complete the walkthrough including any discussion with attendees who remain present.

**Date:** Saturday, 14 November 2020\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

**A recording of this event is at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

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

- *Program A (Addition of polynomials)* from MMIX Supplement (p.26)
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


