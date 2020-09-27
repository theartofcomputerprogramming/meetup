# TAOCP #4 - Basic MMIX Instructions (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 26 September 2020\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*)

- *1.2.4 Integer Functions and Elementary Number Theory* (pp.39-40 of *TAOCP Chapter 1*, not *Fascicle 1, MMIX*)
- *1.3.1' Description of MMIX* (pp.8-12)

  - *Arithmetic operators* (pp.8-9)
  - *Conditional instructions* (p.10)
  - *Bitwise operations* (pp.10-11)
  - *Bytewise operations* (pp.11-12)

**3:00 - 3:10** Break\
**3:10 - 4:00**
  - Hands-on MMIX Visual Debugger
  - *Exercises* (pp.24-28)
  - Shoot the breeze

We continue to learn more about **MMIX** - the TAOCP computer!

We cover more of the instruction set architecture of **MMIX** from *Fascicle 1, MMIX*. We'll also need to consult *TAOCP, Chapter 1* for a little section on the mathematical basis for the `DIV` instruction.

We'll start with instructions for simple arithmetic. We'll learn how to compare values. We'll see instructions for working with the bits and bytes in registers.

After the break, we'll use the free and open source MMIX Visual Debugger https://mmix.cs.hm.edu/mmixvd introduced in TAOCP Meetup #3 for hands-on practice with the instructions we have learnt so far. We'll work on some exercises too.

## Chat Copy

**Zartaj Majeed** 2:00PM\
What's your favorite bit hack?

**Arthur O'Dwyer** 2:02 PM\
(x & (x-1)) to remove the low-order set bit :)

**Jason Vigil** 2:02 PM\
to square a number, shift left

**Jason Vigil** 2:04 PM\
I guess I
'm wrong about that one. maybe it's just multiply by 2

**Miguel Angel Iglesias** 2:05 PM\
I came here to _learn_ what shift left means, I read it in the book, but did not get it :(

**Michael Zalewski** 2:05 PM\
Swap two bytes using XOR instead of temp variable

**Arthur O'Dwyer** 2:06 PM\
Sometimes seen as a ^= b ^= a ^= b, IIRC

**Michael Zalewski** 2:11 PM\
Each instruction executes in a single clock cycle
(That is a goal)

**Miguel Angel Iglesias** 2:16 PM\
oh you mean that it is actually _hard_ to have a single instruction per cycle?

**Arthur O'Dwyer** 2:21 PM\
If you know something about hardware architecture and want your mind blown repeatedly, I recommend Ivan Godard's series of video talks on the "Mill" CPU architecture.

**Uri Segal** 2:37 PM\
shift left by one is multiply by 2
shift right by one is divide by 2
extremely cheap in hardware to do

**Miguel Angel Iglesias** 2:41 PM\
ah, so that is why if you want to shift left by n, you multiply by 2^n

**Zartaj T Majeed** 2:42 PM\
yes - thats right Miguel

**Arthur O'Dwyer** 2:45 PM\
On closer reading, the case-wise behavior(s) of the DIVU instruction seem very weird. If the dividend is greater than 2^64 times the divisor, we just put dividend-over-2^64 into the quotient register? That's not mathematically valid, right? Is it mechanically useful/convenient?

**Uri Segal** 2:52 PM\
-2

**Arthur O'Dwyer** 2:52 PM\
From my programmer's point of view, I wish Knuth had just said "For integer division, I always round the quotient //down//; I don't round it toward zero." So for example -2 divided by 3 is -1 in Knuth's model, not 0.

**Miguel Angel Iglesias** 2:55 PM\
are these comparisons built in terms of CMP and CMPU? or use some underlying trickery?

**Arthur O'Dwyer** 2:55 PM\
"A register is negative if and only if its leading
(leftmost) bit is 1. A register is odd if and only if its trailing (rightmost) bit is 1."
I like this symmetrical way of looking at it. OTOH, I don't like that the mnemonics for "CS if odd" and "CS if not odd" are "CSOD" and "CSEV" respectively.

**Uri Segal** 2:56 PM\
miguel seems like mostly bit comparisons. either the msb or the lsb. or all of them to know if it's zero

**Miguel Angel Iglesias** 2:56 PM\
right

**Arthur O'Dwyer** 2:57 PM\
@Miguel: you're talking about the CSP/CSZ/CSN operations, are they built in terms of CMP/CMPU?  If so: No, these are primitive operations in their own right. So they aren't "built in terms of" any other operations; they're on equal footing with the other primitive instructions.

**Miguel Angel Iglesias** 2:57 PM\
got it!

**Arthur O'Dwyer** 3:09 PM\
https://pharr.org/matt/blog/2018/04/30/ispc-all.html
"In general, the Intel hardware architects knew remarkably little about programming (that Forsyth fellow notwithstanding), and I’m sure those that thought that way really believed it. [... They] grew tired of the graphics people trying to tell them how they might improve their vector programming model and that their current one was insufficient for the kinds of programs we wanted to write."

**Zartaj T Majeed** 3:16 PM\
we're back

**Arthur O'Dwyer** 3:19 PM\
Using ?(x) $\nu(x)$ for what a programmer would call "popcount" is noteworthy to me.

**Uri Segal** 3:24 PM\
the ANDN and ORN seem non RISC like
because of the embedded inverse

**Arthur O'Dwyer** 3:25 PM\
I notice that "SADD $X, $Y hardcoded-zero-register" is equivalent to "X <- popcount(Y)".

**Arthur O'Dwyer** 3:28 PM\
In the discussion of matrix operations, Knuth uses "×" but it would have been equally correct to use "&": 0×0=0, 0×1=0, 1×1=1; 0&0=0, 0&1=0, 1&1=1.

**Arthur O'Dwyer** 3:30 PM\
Why "dot minus" but no "dot plus" or "dot times"?

**Uri Segal** 3:32 PM\
for each bit, if y==1 and z==0, then x=1. that seems like the input to SADD

**Michael Zalewski** 3:32 PM\
What would "dot plus" or "dot times" do?

**Arthur O'Dwyer** 3:33 PM\
@Michael: "Dot plus" (saturating add) is actually common in hardware, I think. It would add but clamp to 255/65535/whatever, instead of overflowing around.

**Arthur O'Dwyer** 3:34 PM\
For "dot times", I suppose there's not much sensible you could do with it with just integer arithmetic.

**Michael Zalewski** 3:35 PM\
"dotMinus" reminds me of ReLU, used in neural networks

**Uri Segal** 3:38 PM\
transistors weren't small enough before that

**Arthur O'Dwyer** 3:38 PM\
Based on exercise 37, I *think* MXOR is similar to https://en.wikipedia.org/wiki/CLMUL_instruction_set

**Uri Segal** 3:39 PM\
did the original MIX not have this instruction?

**Arthur O'Dwyer** 3:39 PM\
The original MIX didn't have 64-bit registers. Its registers were MUCH weirder.

**Arthur O'Dwyer** 3:46 PM\
https://en.wikipedia.org/wiki/36-bit_computing
In a 36-bit word you can store 6 6-bit characters; but the PDP convention was "five 7-bit characters and 1 unused bit", which explains why in the classic text adventure "Colossal Cave" the parser looks at only the first 5 letters of each word.

**Zartaj Majeed** 3:48 PM\
https://github.com/theartofcomputerprogramming/mmixsamples/blob/master/arithmetic.mms

**Uri Segal** 3:50 PM\
@Arthur, interesting that Lattice FPGAs include hardware that can do 36-bit multiplies

**Arthur O'Dwyer** 3:51 PM\
Looks like I was wrong about MXOR being similar to CLMUL. https://math.stackexchange.com/questions/1107839/how-is-d-knuth-mmix-instruction-mxor-useful-for-finite-field-multiplication

**Uri Segal** 3:56 PM\
vim keyboard bindings?

**Uri Segal** 4:00 PM\
alignment

**Uri Segal** 4:05 PM\
for the debuger?
\*debugger

**Uri Segal** 4:14 PM\
does mmix store & process doubles using ieee 754 format?

**Arthur O'Dwyer** 4:14 PM\
Yes, I believe so.
Beware that (AFAICT) Knuth uses the word "float" for what a C programmer would call IEEE double, and "short float" for what a C programmer would call IEEE float.

**Arthur O'Dwyer** 4:24 PM\
Would it make sense to devote one meeting to exercises?

**Miguel Angel Iglesias** 4:24 PM\
+1

**Jason Vigil** 4:26 PM\
Thanks!

**Uri Segal** 4:26 PM\
thanks all!!

**Miguel Angel Iglesias** 4:26 PM\
thanks! this was great!

**Deepa Annamalai** 4:26 PM\
Thank you

**Marc Vreuls** 4:26 PM\
Thanks!

## Zartaj

Zartaj's notes

## Your Name
Your notes

