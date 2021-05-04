# TAOCP #18 - Radix Sort (Chapter 5, Sorting: Section 5.2.5)

Sorting is sorted out! (for now...)

We'll take a break from sorting after this meetup. We wrap up sorting by merging by questioning the need for twice the amount of memory as required for the array of keys. This motivates a variant of mergesort using link fields called Algorithm L (List merge sort). There is an interesting use of links serving dual purposes that is somewhat specific to the old MIX machine. As such we also need to look at the MMIX version of Algorithm L (List merge sort) in The MMIX Supplement. It, on the other hand, relies on the MMIX feature of an address being implicitly aligned to the word type of the instruction, e.g. `LDTU` ignores the low 2 bits of the address when loading a tetrabyte (4 bytes).

The final section is on sorting by distribution. This technique expands on the basic sorting by counting method we covered in section 5.2. There is quite a bit of discussion of this approach and its applicability to various types of data. We go over Algorithm R (Radix list sort), its MMIX implementation and analysis.

This meetup marks the end of our first pass through Volume 3 of TAOCP. The next few meetups will be on data structures from Volume 1. There is a lot to still learn about lists, arrays and trees from TAOCP. It will all stand us in good stead when we return to Volume 3 for more sorting (and searching) ...

We'll do some exercises.

The bonus segment will include a debugger stepthru of Program L (List merge sort) from The MMIX Supplement.

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

Keep the conversation going!

Facebook: https://www.facebook.com/groups/678335496099220<br>
IRC ##taocp: https://webchat.freenode.net/##taocp

**Date:** Saturday, 9 January 2021\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 5, Sorting* (along with *MMIX Supplement*)

- *5.2.4 Sorting by Merging* (pp.163-166)
  - List merge sort (pp.163-164)
  - *Algorithm L (List merge sort)* (pp.164-165), MMIX Supplement (pp.89-90)
  - *Program L (List merge sort)*, MMIX Supplement (pp.90-92)
  - Analysis of Program L, MMIX Supplement (p.92)
  
- *5.2.5 Sorting by Distribution* (pp.168-177)
  - Sorting by Distribution (pp.168-171)
  - *Algorithm R (Radix list sort)* (pp.171-172)
  - *Algorithm H (Hooking-up of queues)* (pp.172-173)
  - *Program R (Radix list sort)*, MMIX Supplement (pp.93-94)
  - Analysis of Algorithm R (pp.174-177), MMIX Supplement (pp.93-94)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.166-168, 177-179), MMIX Supplement (pp.92, 94)
- Shoot the breeze

**Bonus Segment**

Stepthru in MMIX Visual Debugger

- *Program L (List merge sort)*, MMIX Supplement (pp.90-92)

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Chat Copy

**Arthur O'Dwyer** 2:09 PM\
I may end up nerdsniped by this: https://www-cs-faculty.stanford.edu/~knuth/pi_hamilton_maze.png

**Zartaj Majeed** 2:12 PM\
reading till 2:19

**Zartaj Majeed** 2:53 PM\
reading till 2:58

**Arthur O'Dwyer** 2:57 PM\
Btw, my internet seems to be really bad today (Hangouts keeps blacking out your video feeds due to lack of bandwidth), but I hope my own speech is still coming through okay.

**Zartaj Majeed** 2:58 PM\
audio has been fine Arthur

**Zartaj Majeed** 3:04 PM\
reading till 3:07

**Zartaj Majeed** 3:07 PM\
break till 3:17

**Arthur O'Dwyer** 3:09 PM\
Btw, in the "execution counts" column, I notice that C = C'+C'', and B=B'+B''. In case that helps anyone's intuition.

**Zartaj Majeed** 3:18 PM\
we're back
GNU sort has this note in its TODO file about trying out Algorithm L (List merge sort): https://github.com/coreutils/coreutils/blob/master/TODO#:~:text=sort:%20Investigate%20better%20sorting%20algorithms%3b%20see%20Knuth%20vol.%203

**Arthur O'Dwyer** 3:19 PM\
https://github.com/coreutils/coreutils/commit/93f9ffc6141ad028223a33e5ab0614aebbd4aa2e

**Zartaj Majeed** 3:20 PM\
reading till 3:27

**Arthur O'Dwyer** 3:23 PM\
"Turn the deck face down and deal again, this time into four piles for the four suits. (Again you turn the cards face up as you deal them.)"\
For someone so concerned with constant factors, I'm surprised at Knuth here. ;) Surely it would be faster to leave the deck face-up during the whole process (and stack the 13 piles in the opposite order).

**Arthur O'Dwyer** 3:24 PM\
Speaking of algorithmic card tricks, here's one I just recently learned of. Totally off-topic of course. https://www.vanishingincmagic.com/blog/the-gilbreath-principle

**Arthur O'Dwyer** 3:29 PM\
"The desired sum of products is easily seen to be..." — Knuth doesn't say so, but the point of this rigmarole is to minimize the number of integer multiplications that we have to do: from number-of-cards number of multiplications (maybe hundreds or thousands) down to like 30 multiplications.

**Zartaj Majeed** 3:36 PM\
reading till 3:43

**Arthur O'Dwyer** 3:43 PM\
The [square brackets] in the MIX version of Program R indicate self-modifying code. Good times.

**Zartaj Majeed** 3:48 PM\
reading till 3:51

**Zartaj Majeed** 3:53 PM\
reading till 4:00

**Zartaj Majeed** 4:02 PM\
nice table summarizing performance of sorting algorithms on p.382 (MMIX Supplement p.96)

**Zartaj Majeed** 4:03 PM\
exercise 5.2.5.4

**Miguel Angel Iglesias** 4:08 PM\
I'm dropping off, I am so sleepy I can barely think

**Zartaj Majeed** 4:09 PM\
exercise 5.2.5.8

