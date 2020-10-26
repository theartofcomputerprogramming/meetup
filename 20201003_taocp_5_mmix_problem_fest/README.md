# TAOCP #5 - MMIX Problem Fest

**Date:** Saturday, 3 October 2020\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** *Exercises* (pp.24-28) for topics from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*)

- *1.3.1' Description of MMIX* (pp.8-12)

  - *Bits and bytes* (pp.2-4)
  - *Memory and registers* (pp.4-5)
  - *Instructions* (pp.5-6)
  - *Loading and storing* (pp.6-8)
  - *Arithmetic operators* (pp.8-9)
  - *Conditional instructions* (p.10)
  - *Bitwise operations* (pp.10-11)
  - *Bytewise operations* (pp.11-12)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- Continue *Exercises* (pp.24-28)
- Shoot the breeze

MMIX exercises galore!

We've covered the bulk of instructions for the **MMIX** computer. We've tried out some examples in the MMIX Visual Debugger. But nothing like working on a lot of problems to truly strengthen our grasp of the material. This event is an opportunity to deepen our understanding of **MMIX**. Equally we want to share our work with the group and help others with any questions.  It's also a chance for anyone who missed a session on **MMIX** to catch up.

We're dedicating the full two hours to solving exercises from *Fascicle 1, MMIX*. The format is rather free-form. A restricted Google Doc with many exercises is now available on request for members to work in and collaborate with the group. We'll work collectively and individually in parallel to attempt as many exercises as possible. And share solutions or partial work with everyone. Afterwards all our work will be posted to the meetup's Github repos for notes and exercises.

It's better to not look at the answers to exercises. Instead members are encouraged to ask questions and enter any comments into the shared doc or in the chat panel. Every note that reflects genuine individual thought could be useful to people who come across the notes in the future.

## Chat Copy
 
**Zartaj Majeed** 2:04 PM\
Question: What website do you like for problem solving?

**Arthur O'Dwyer** 2:05 PM\
I'd suggest Google's yearly "Advent of Code", and StackExchange (puzzling.SE, plus regular StackOverflow).

**Miguel Iglesias** 2:09 PM\
https://www.chegg.com/

**Arthur O'Dwyer** 2:13 PM\
I haven't watched this video yet, but for those interested in recent Knuth interviews, https://www.youtube.com/watch?v=O5g4Zl8ppQA just happened on Sept 21.

**Deepa Annamalai** 2:14 PM\
question is not visible
yes

**Deepa Annamalai** 2:24 PM\
take them like 4 as a set and convert?

**Miguel Iglesias** 2:24 PM\
+1

**Arthur O'Dwyer** 2:25 PM\
So that number is (0)111'1101'1001 in sets of four

**Zartaj Majeed** 2:26 PM\
0xfd9

**Deepa Annamalai** 2:26 PM\
FD9
it is not F

**Arthur O'Dwyer** 2:27 PM\
0x1000 would be 2^12, which is 4096

**Deepa Annamalai** 2:27 PM\
there are three 1's\
111-1101-1001

**Zartaj Majeed** 2:28 PM\
0x7d9

**Arthur O'Dwyer** 2:28 PM\
Just like in decimal: 000123 is the same number as 123.

**Deepa Annamalai** 2:29 PM\
hex because it is 8 bit is one byte ?

**Arthur O'Dwyer** 2:30 PM\
https://en.wikipedia.org/wiki/Hexadecimal#History_of_written_representations

**Deepa Annamalai** 2:33 PM\
11 - A in hexa and 65 in ASCII

**Deepa Annamalai** 2:34 PM\
they are consecutive from 65 onwards and 97 is lower case a

**Deepa Annamalai** 2:36 PM\
sorry i did not get it ...why there are 6 empty  90 to 97...i know this is not relevant

**Arthur O'Dwyer** 2:37 PM\
To lowercase "A", just bitwise-OR it with 32 (0x20).\
To uppercase 'a', just bitwise-XOR it with 32 (0x20).

**Deepa Annamalai** 2:37 PM\
oh ok.

**Arthur O'Dwyer** 2:38 PM\
So, in order to  get a displacement of exactly 32 (0x20) between 'A' and 'a', we must have six other characters filling in the gap between 'Z' and 'a'.

**Arthur O'Dwyer** 2:40 PM\
Note: TEtRA, PEnTA, hEXA.

**Arthur O'Dwyer** 2:42 PM\
After those three the system starts getting a bit strained: zetta, yotta. And then it seems to stop (for now).

**Arthur O'Dwyer** 2:45 PM\
Knuth is surprisingly non-rigorous here. This is all he seems to have to say about what he means by s(x) throughout this whole section: "Here s(x) denotes the signed integer corresponding to the bit pattern x, according to the conventions of two's complement notation."

**Deepa Annamalai** 2:46 PM\
this is a maths exercise ...so prove it with maths way

**Miguel Iglesias** 2:52 PM\
have you tried the Whiteboard?\
perhaps we should try it?

**Zartaj Majeed** 2:52 PM\
s(alpha) = alpha if high bit is 0\
s(alpha) = alpha - 2^n if high bit is 1\
u(alpha) = alpha

**Arthur O'Dwyer** 2:56 PM\
Re Miguel's question, the intuition here is that 111 in binary is 7 = (2^3 - 1); 1111 in binary is 15 = 2^4 - 1; 11111 in binary is 31 = 2^5 - 1; and so on. The number 2^n is always one greater than the maximum possible value of an n-bit binary number.

**Zartaj Majeed** 2:58 PM\
0111 => s(0111) = 7\
u(0111) = 7\
1001 => u(1001) = 9\
s(1001) = ?

**Zartaj Majeed** 2:59 PM\
9 - 2^4 = 9 - 16
-7

**Zartaj Majeed** 3:01 PM\
x - u(alpha) is divisible by 2^n

**Zartaj Majeed** 3:02 PM\
any takers for #6?

**Deepa Annamalai** 3:04 PM\
ex.: 7 --> 0111 

negation -> 1000

add 1\
\_---------\
1001

 
compliment not negation

**Arthur O'Dwyer** 3:04 PM\
Sorry for my disappearance. I'll be back at... well, 3:14. :)

**Zartaj Majeed** 3:04 PM\
yes - 3:14

**Arthur O'Dwyer** 3:14 PM\
For problem 7, here's the actual definition of the LDHT and STHT instructions:\
LDHT $X, $Y, $Z (load high tetra): u($X) ← u(M4[A]) × 2^32\
STHT $X,$Y,$Z (store high tetra): u(M4[A]) ← ⌊u($X)/2^32⌋.

**Zartaj Majeed** 3:15 PM\
we're back

**Miguel Iglesias** 3:18 PM\
brb

**Arthur O'Dwyer** 3:24 PM\
If we use f($Y) to denote the real number between 0 and 1, we have basically s($Y) = 2^64 * f($Y).\
If we're multiplying s($Z) * f($Y), the result is going to be something between 0 and 2^64. So that means the radix point must be 64 bits from the left (which is also 64 bits from the right).

**Miguel Iglesias** 3:25 PM\
remind me what a "radix point is"?

**Arthur O'Dwyer** 3:25 PM\
Decimal point. But in a base that's not decimal.

**Arthur O'Dwyer** 3:36 PM\
(-2^63) divided by (-1) mathematically comes out to (2^63), but that overflows -- we get (0) as the answer, and signal overflow.

**Deepa Annamalai** 3:37 PM\
btw where are the answers

**Arthur O'Dwyer** 3:37 PM\
I have answers in my ebook, near the end.

**Deepa Annamalai** 3:38 PM\
oh ok thank yoh
you

**Arthur O'Dwyer** 3:42 PM\
s($X) * s($Y) is (u($X) maybe minus 2^64) * (u($Y) maybe minus 2^64)\
which should always be congruent to u($X) * u($Y) modulo 2^64

**Arthur O'Dwyer** 3:44 PM\
$Y / 0xFFFFFFFFFFFFFFFFF != $Y / (-1)

**Miguel Iglesias** 3:45 PM\
I need to sign off, thanks guy!

**Arthur O'Dwyer** 3:46 PM\
I happen to know that "there is a carry" if and only if "the sum is smaller than (either) one of the inputs."

**Arthur O'Dwyer** 3:58 PM\
I notice that 25 = 16 + 8 + 1.

**Arthur O'Dwyer** 4:01 PM\
2ADDU $0, $Y, $Y  // 2y+y\
8ADDU $X, $0, $Y  // 8(2y+y)+y

**Deepa Annamalai** 4:03 PM\
Thank you. I need to sign off

**Arthur O'Dwyer** 4:03 PM\
When I said "load effective address," I was thinking of "LDA", btw, which turns out to be just a synonym for "ADDU".


