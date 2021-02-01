# TAOCP #17 - Mergesort (Chapter 5, Sorting: Sections 5.2.3, 5.2.4)

New Year! New sorting methods!

We've studied algorithms that use the techniques of sorting by insertion and sorting by exchanging. We now look at two other approaches.

Sorting by selection involves repeatedly selecting and separating the smallest key. We'll introduce the technique with Algorithm S (Straight selection sort) and discuss its refinements. Section 5.2.3 has other algorithms that we'll skip for now and return to after we have studied tree data structures in Volume 1.

The next section 5.2.4 presents sorting by merging. We'll go over couple mergesort algorithms in this meetup and cover the rest in the next meetup. Mergesort is particularly useful for external sorting when it is infeasible to sort large amounts of data all in memory. It is the technique used by the GNU sort program.

We'll do some exercises.

The bonus segment will include a debugger stepthru of Program S (Straight selection sort) from The MMIX Supplement.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 2 January 2021\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.2.3 Sorting by Selection* (pp.138-141)
  - *Algorithm S (Straight selection sort)* (p.139)
  - *Program S (Straight selection sort)*, MMIX Supplement (p.87)
  - *Refinements of straight selection* (pp.140-141)
  
- *5.2.4 Sorting by Merging* (pp.158-163)
  - *Algorithm M (Two-way merge)* (pp.158-159)
  - Mergesort (pp.159-160)
  - *Algorithm N (Natural two-way merge sort)* (pp.160-161)
  - Analysis of Algorithm N (pp.161-162), MMIX Supplement (p.89)
  - *Algorithm S (Straight two-way merge sort)* (pp.162-163)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.166-168), MMIX Supplement (p.92)
- Shoot the breeze

**Bonus Segment**

Stepthru in MMIX Visual Debugger

- *Program S (Straight selection sort)*, MMIX Supplement (p.87)

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Chat Copy

**Arthur O'Dwyer** 2:06 PM\
https://news.ycombinator.com/item?id=25589619
"I’m a grad student in my second year of grad school. I had been working part-time writing compilers and people knew that I was fairly good at writing compilers. So a guy came to me from the publishing house Addison-Wesley and said that his editor had recommended that they ask me to write a book on how to write compilers."\
"Anyway, I went home from that lunch and I wrote down on a piece of yellow paper a list of twelve chapters that I thought ought to be in a book on how to write compilers. Chapter 12 was actually “Compilers.” The first eleven chapters were techniques that you wanted to know in general that would be of help."

**Arthur O'Dwyer** 2:09 PM\
LR parsers: https://web.archive.org/web/20120315152151/http://www.cs.dartmouth.edu/~mckeeman/cs48/mxcom/doc/knuth65.pdf\
Interview: https://news.ycombinator.com/item?id=25589619

**Zartaj Majeed** 2:15 PM\
reading till 2:20

**Zartaj Majeed** 2:28 PM\
reading till 2:30

**Zartaj Majeed** 2:34 PM\
reading till 2:39

**Zartaj Majeed** 2:38 PM\
repasting Arthur's earlier comments in case you missed them

**Arthur O'Dwyer** 2:38 PM\
"8. [24] Show that if the search for max (K_1, ..., K_j) in step S2 is carried out by examining keys in left-to-right order K_1, K_2, ..., K_j, instead of going from right to left as in Program S, it is often possible to reduce the number of comparisons needed on the next iteration of step S2."

**Zartaj Majeed** 2:38 PM\

**Arthur O'Dwyer** 2:06 PM\
https://news.ycombinator.com/item?id=25589619
"I’m a grad student in my second year of grad school. I had been working part-time writing
compilers and people knew that I was fairly good at writing compilers. So a guy came to me
from the publishing house Addison-Wesley and said that his editor had recommended that they
ask me to write a book on how to write compilers."
"Anyway, I went home from that lunch and I wrote down on a piece of yellow paper a list of
twelve chapters

**Arthur O'Dwyer** 2:09 PM\
LR parsers: https://web.archive.org/web/20120315152151/http://www.cs.dartmouth.edu/~mckeeman/cs48/mxcom/doc/knuth65.pdf\
Interview: https://news.ycombinator.com/item?id=25589619

**Zartaj Majeed** 2:47 PM\
reading till 2:52

**Arthur O'Dwyer** 2:51 PM\
Algorithm M, steps M4 and M6, seem like unnecessary frills, but actually reflect physically relevant details of how the algorithm is done in practice. I happen to have been messing with libc++'s `std::merge` code very recently and can confirm that it delegates to `std::copy` at the end: https://github.com/llvm-mirror/libcxx/blob/master/include/algorithm#L4352\
And this ends up mattering physically because `std::copy` in trivial cases can just do a byte-copying thing instead of element-by-element.

**Zartaj Majeed** 2:56 PM\
reading till 3:01

**Zartaj Majeed** 3:08 PM\
break till 3:18

**Zartaj Majeed** 3:18 PM\
we're back

**Zartaj Majeed** 3:19 PM\
reading till 3:26

**Zartaj Majeed** 3:31 PM\
can we go back to Table 1 on p.160?

**Arthur O'Dwyer** 3:35 PM\
1 2 3 4 2 4 6 8\
m(1 2 3 4, 8)\
m(2 4 6, )

**Arthur O'Dwyer** 3:36 PM\
produces 1 2 3 4 8 2 4 6

**Arthur O'Dwyer** 3:37 PM\
1 2 3 4 6 8 2 4\
1 2 3 4 4 6 8 2\
1 2 2 3 4 4 6 8

**Arthur O'Dwyer** 3:38 PM\
Knuth: 1 2 3 4 8 4 6 2\
1 2 2 3 4 6 8 4\
1 2 2 3 4 4 6 8

**Zartaj Majeed** 3:40 PM\
reading till 3:43

**Zartaj Majeed** 3:45 PM\
reading till 3:52

**Arthur O'Dwyer** 3:47 PM\
"Therefore it is possible to predict the location of the sorted output in advance, and copying will usually be unnecessary." — IIUC, Knuth means that copying will be unnecessary because the caller can just deal with it. Sorting 15 elements? then the output will show up in location FOO. Sorting 17 elements? then the output will show up in location BAR. Caller's problem, not mine.

**Zartaj Majeed** 3:50 PM\
I take it to mean two possibilities\
callee can say which area has output\
or callee can modify start of algorithm to insure output is in original area

**Zartaj Majeed** 4:01 PM\
exercise 1

**Zartaj Majeed** 4:02 PM\
exercise 5

**Arthur O'Dwyer** 4:05 PM\
If I have a sorted (increasing) run from the left, and a backwards sorted (decreasing) run from the right, they meet in a local maximum which is the end of both runs simultaneously.

**Zartaj Majeed** 4:05 PM\
exercise 8

**Zartaj Majeed** 4:10 PM\
exercise 10

**Arthur O'Dwyer** 4:13 PM\
What I'm trying to say, in code, is:\
(0,0,0,0,2,4,6,8,1,3,5,7)\
I can std::merge [a+4,a+8) and [a+8,a+12) together into [a+0,a+8) without physical undefined behavior. Because by the time I've begun to overwrite \*(a+4), I must have already moved its old value out (or else I'm just doing a self-move).\
Knuth says merely: "With care we can exploit this idea so that N + 2⌊lg N⌋−1 locations are required for an entire sort. But the program seems to be rather complicated..."

**Zartaj Majeed** 4:20 PM\
MMIX Debugger stepthru of Algorithm S (Straight selection sort)

**Zartaj Majeed** 4:21 PM\
MMIX program will be in the mmixsamples github repo\
https://github.com/theartofcomputerprogramming/mmixsamples

**Zartaj Majeed** 4:34 PM\
going to demo Table 1 on p.139 of TAOCP\
section 5.2.3

**Zartaj Majeed** 4:50 PM\
we've now got row 2 of Table 1 showing in the debugger memory panel below

**Zartaj Majeed** 4:54 PM\
now we're seeing row 3 of Table 1
