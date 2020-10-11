# TAOCP #6 - MMIX Branching

**Date:** Saturday, 10 October 2020\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

#### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*)

- *1.3.1' Description of MMIX* (pp.13-24)

  - *Immediate constants* (pp.13-14)
  - *Jumps and branches* (pp.15-16)
  - *The complete instruction set* (pp.19-21)
  - *Timing* (pp.21-23)
  - *MMIX versus reality* (p.23)
  - *Summary* (p.24)
  
**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.24-28)
- Shoot the breeze

We wrap up the **MMIX** instruction set!

We learn that many instructions can take constants instead of registers as operands. This is often a nice convenience that allows small values to be used for arithmetic or for relative addressing. It also allows a register to be set to any value without loading data from memory.

Then we learn instructions to branch and jump. These are the basis of essential programming control constructs like **if-else** conditions and **while** loops. This will allow us to finally study and write complete programs for an **MMIX** computer.

We'll go over the costs of the entire **MMIX** instruction set. This lets us estimate the performance of a program and compare the speed of two programs.

After the break, we'll work on exercises on the new instructions and those from previous meetups on **MMIX**.

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Chat Copy

**Zartaj Majeed** 2:20 PM\
Question: Do you like problem-solving in the large, or in the small?

**Zartaj Majeed** 2:32 PM\
ADD $1,$2,$3

**Zartaj Majeed** 2:34 PM\
ADD $1,$2,25

**Zartaj Majeed** 2:35 PM\
SETH $1,$2,$3

**Zartaj Majeed** 2:38 PM\
SETH $0,#0123

**Deepa Annamalai** 2:39 PM\
$0 <=== #0123 #hexa

**Zartaj Majeed** 2:39 PM\
INCMH $0,#4567

**Deepa Annamalai** 2:40 PM\
0123 + 4567 # hex addition

**Zartaj Majeed** 2:41 PM\
$0 = #0123 00 00 00 00 00 00

**Deepa Annamalai** 2:45 PM\
INCMH <=== 0123 4567 00 00 00 00

**Zartaj Majeed** 2:46 PM\
INCML $0,#89ab

**Deepa Annamalai** 2:47 PM\
$0 <==== 0123 4567  89ab 00 00

**Zartaj Majeed** 2:48 PM\
INCL $0,#cdef

**Deepa Annamalai** 2:48 PM\
$0 <====0123 4567 89ab cdef

**Zartaj Majeed** 3:01 PM\
symbolic form #f0 00 00 02\
operand is @+4 * 2

**Zartaj Majeed** 3:03 PM\
XYZ = 2\
@=#1000

**Zartaj Majeed** 3:05 PM\
next address will be #1000 + 4 * 2\
= #1008

**Zartaj Majeed** 3:15 PM\
$1 = #1000\
GO $1,$1,0

**Zartaj Majeed** 3:17 PM\
$1 = ?\
$1 = #1004

**Zartaj Majeed** 3:19 PM\
@=#1000\
$1 = #1234

**Zartaj Majeed** 3:20 PM\
GO $1,$1,0\
@=#1234

**Zartaj Majeed** 3:21 PM\
$1=?

**Deepa Annamalai** 3:22 PM\
$1 = #1234

**Deepa Annamalai** 3:24 PM\
$1 = #1004  # this gets saved before

**Zartaj Majeed** 3:34 PM\
break till 3:42

**Deepa Annamalai** 3:42 PM\
i am ready

**Deepa Annamalai** 3:51 PM\
btw, this is a fixed link for every week?

**Deepa Annamalai** 4:02 PM\
Sorry, i need to leave now. i will watch the recording for this last part.
