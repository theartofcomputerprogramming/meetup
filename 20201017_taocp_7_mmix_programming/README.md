# TAOCP #7 - MMIX Programming

**Date:** Saturday, 17 October 2020\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

**This event will be recorded and posted to YouTube as a public video at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

#### Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*)

- *1.2.10 Analysis of an algorithm* (p.96 of *TAOCP Vol.1*, not *Fascicle 1, MMIX*)

  - *Algorithm M (Find the maximum)* (p.96 of *TAOCP Vol.1*, not *Fascicle 1, MMIX*)
  
- *1.3.2' The MMIX Assembly Language* (pp.28-43)

  - *Program M (Find the maximum)* (pp.28-30)
  - *Program H (Hail the world)* (pp.30-32)
  - *Algorithm P (Print table of 500 primes)* (p.32)
  - *Program P (Print table of 500 primes)* (pp.32-37)
  - *Language summary* (pp.37-40)
  - *Primitive input and output* (pp.40-43)
  
**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.24-28, pp.43-51)
- MMIX Simulator and Assembler
- Shoot the breeze

We begin to program the **MMIX** computer!

Programs for **MMIX** are written in assembly language. An assembly language program is made up of a sequence of **MMIX** instructions plus directives for the assembly language processing program called the assembler. The output of the assembler is an object file that can actually run on the **MMIX**.

The first program we'll study finds the maximum of some numbers. Its code is in *Fascicle 1, MMIX* but the algorithm is in *TAOCP Volume 1, Fundamental Algorithms*.

Two programs that print output will follow, completing our introduction to **MMIX**. This lets us tackle basic algorithms and data structures from Chapters 2 and 5 right away. We'll swing back at some point to cover the few remaining **MMIX** features like subroutines, coroutines and interrupts as needed.

The first program with output is the requisite "Hello World" program. It's short and sweet.

Then there's a program to compute small primes and print them in a table. It introduces some interesting features of **MMIX** assembly like local symbols and symbolic expressions.

After the break, we'll do some exercises.

If there's time, we'll see a demo of the commandline **MMIX** simulator `mmix` and **MMIX** assembler `mmixal` tools (https://mmix.cs.hm.edu/src) that are very useful for practicing **MMIX** programming. Both tools are free and open source like the MMIX Visual Debugger seen in previous meetups.

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.

## Chat Copy

**Arthur O'Dwyer** 2:12 PM\
I actually watched last week's video immediately before joining. One thing I feel like is adding friction to people's understanding is how Knuth code-switches between talking about "assembly-language mnemonics" and "machine-code opcodes" and "hex numbers" as if those are all the same thing.

**Arthur O'Dwyer** 2:19 PM\
Here's a quote from 1.3.1' about the weirdness of mnemonics:
> Table 1 actually says ‘ADD[I]’, not ‘ADD’, because the symbol ADD really stands for two opcodes. [...]\
When a distinction is necessary, we say that opcode #20 is ADD and opcode #21 is ADDI (“add immediate”); similarly, #F0 is JMP and #F1 is JMPB ("jump backward"). This gives every opcode a unique name. However, the extra I and B are generally dropped for convenience when we write MMIX programs.

**Arthur O'Dwyer** 2:26 PM\
One thing I forgot to bring up way back when we talked about nybbles/bytes/wydes is that "wyde" is a pun on "word". Intel 8086 had a 16-bit "word" size, and Intel/Windows-land still uses "BYTE, WORD, DWORD, QWORD..." to refer to 8, 16, 32, 64...-byte quantities.\
Also in x86(-64) assembly language, you have e.g. "movb, movw, movl, movq", where "w" is the suffix for a 16-bit word.

**Zartaj Majeed** 2:29 PM\
register: 0 1 2 3 4 5 6 7 - 8 bytes\
actually better to index from the left

**Zartaj Majeed** 2:30 PM\
register: 7 6 5 4 3 2 1 0 bytes

**Zartaj Majeed** 2:32 PM\
SETH: set bytes 7 and 6

**Arthur O'Dwyer** 2:32 PM\
At least so far, Knuth has avoided having to pick an "endianness" for numbering the bytes of an octa. Instead, he just says that an octa consists of four wydes, and those wydes are called "H, MH, ML, and L" in that order from left to right. The SETH $X, YZ instruction sets wyde "H" of register X.

**Zartaj Majeed** 2:32 PM\
SETMH: sets bytes 5 and 4

**Arthur O'Dwyer** 2:34 PM\
Oh, and LDHT/STHT ("load high tetra, store high tetra") use a similar notation. For any given octa, its "H tetra" comprises its "H wyde" and its "MH wyde".

**Arthur O'Dwyer** 2:38 PM
> "We might in fact write ‘JMP #1008’; but then the value of XYZ would depend on the location jumped from."\
This is another example of Knuth mixing up opcodes and mnemonics in a confusing way. He's saying that the _assembler_ won't always convert the mnemonic "JMP #1008" into the same four-byte machine code. The assembly-language mnemonic "JMP #..." produces a machine code that is dependent on _where that line appears_ in our assembly-language program.

**Arthur O'Dwyer** 2:43 PM
> "The range of destination addresses RA is more limited than it was with JMP, because only two bytes are available..."\
Knuth doesn't actually say this anywhere, but the implication ("obvious" to his target audience) is that for these branch instructions RA is computed as @+(4 * YZ).

**Arthur O'Dwyer** 2:48 PM\
Yet another code-switching: In the opcode encoding of "JMP #1008", we encode a number of _instructions_ to jump ahead. Each instruction takes up 4 bytes. So we're jumping 4 * XYZ bytes. And each byte takes up 8 bits. So we're jumping 32 * XYZ bits (for whatever that's worth). Sometimes it's hard to keep track of what "multiplier" we're interested in at the moment.\
The address "#1008" is measured in _bytes_, not instructions.

**Arthur O'Dwyer** 2:51 PM\
Speaking of the limitations of relative jumps, yesterday I learned about https://en.wikipedia.org/wiki/Conway%27s_Soldiers :)

**Zartaj Majeed** 2:55 PM\
We'll switch to TAOCP Vol 1 for little bit to look at Algorithm M (Find the maximum) - it's on p.96 in section 1.2.10 Analysis of an Algorithm

**Arthur O'Dwyer** 3:00 PM\
Perhaps disconcerting to a modern programmer: the description of what Algorithm M should do, implicitly requires that n >= 1. And indeed, if n < 1, Algorithm M does bad stuff.

**Zartaj Majeed** 3:06 PM\
back at 3:14

**Zartaj Majeed** 3:15 PM\
we're back

**Miguel Iglesias** 3:17 PM\
you reading already? I'm in toddler business

**Arthur O'Dwyer** 3:17 PM\
Yep, reading.
And getting phone calls, apparently :)

**Zartaj Majeed** 3:18 PM\
too bad it's virtual - I wouldn't mind some ramen right now

**Arthur O'Dwyer** 3:25 PM\
Perhaps surprising to someone not versed in assembly-language programming: "JMP DecrK". In Algorithm M, step M2 does the test and says "stop when we're done"; step M5 says unconditionally go back to M2. In the MMIXAL program, step M2 appears at the very bottom of the loop and says "if we're NOT done, jump back to the top," and there is no equivalent to the unconditional jump in step M5.

**Arthur O'Dwyer** 3:27 PM\
MMIX really suffers from the lack of a "LDO m, x0+8 * k" instruction. We have "ADD8[U][I]", but not "LDOADD8".

**Arthur O'Dwyer** 3:38 PM\
"Local symbols" (2H, 2F, 2B) are described on page 150 of Volume 1.

**Arthur O'Dwyer** 3:39 PM\
If you know about "goto" in high-level programming languages: "2H" is like a goto label "L2:", and "JMP 2F" is like a goto statement "goto L2;"

**Miguel Iglesias** 3:40 PM\
Basic FTW

**Arthur O'Dwyer** 3:41 PM\
The "clever" bit in MMIXAL is that assembly language doesn't have "local scopes." In a high-level language, we can't have two different labels "L2:" in the same scope. In MMIXAL, we have only one scope. So in MMIXAL, we say "JMP 2F" with the meaning "goto the next L2 in the forward direction," and "JMP 2B" with the meaning "goto the next L2 in the backward direction."

**Michael Zalewski** 3:46 PM\
Wouldn't the target be called 2H (begins with a number)? I think L2 is an absolute address because it begins with a letter

**Arthur O'Dwyer** 3:46 PM\
@Michael: I'm confusingly code-switching between notations ;)\
See my earlier comment: "If you know about "goto" in high-level programming languages: "2H" is like a goto label "L2:", ..."

**Miguel Iglesias** 3:51 PM\
brb

**Michael Zalewski** 3:56 PM\
The Quantum version of MMIX will probably change the meaning of probable branch

**Arthur O'Dwyer** 4:02 PM\
https://en.wikipedia.org/wiki/Branch_predictor\
in particular, PBP is an example of https://en.wikipedia.org/wiki/Branch_predictor#Static_branch_prediction\
As Wikipedia says, "A [good heuristic] presumes that backward branches will be taken and that forward branches will not."

**Arthur O'Dwyer** 4:34 PM\
https://godbolt.org/ ?\
https://repl.it/ ?

**Miguel Iglesias** 4:36 PM\
I got to drop off, see you next Sat!

**Arthur O'Dwyer** 4:36 PM\
https://tio.run/

**Arthur O'Dwyer** 4:38 PM\
Apparently https://pypyjs.org/ is a client-side Python-interpreter-in-JS. But I doubt it's relevant to this MMIX-in-the-browser idea, really. :)

