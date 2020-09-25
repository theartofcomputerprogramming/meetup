# TAOCP #3 - Introduction to MMIX (Fascicle 1, 1.3' MMIX) (Chapter 1, Basic Concepts: 1.3 MIX)

**Date:** Saturday, 19 September 2020<br>
**Time:** 2-4pm America/New_York<br>
**Location:** Google Meet online

## Agenda

**2:00 - 2:10** Meet and greet<br>
**2:10 - 3:00** Read and discuss couple pages at a time from *Fascicle 1, MMIX* (corresponding to *Chapter 1, Basic Concepts*)

- *Preface* (pp.iii-v)
- *1.3' MMIX* (p.2)
- *1.3.1' Description of MMIX* (pp.2-8)

  - *Bits and bytes* (pp.2-4)
  - *Memory and registers* (pp.4-5)
  - *Instructions* (pp.5-6)
  - *Loading and storing* (pp.6-8)

**3:00 - 3:10** Break<br>
**3:10 - 4:00** MMIX Visual Debugger, shoot the breeze<br>

We introduce the MMIX computer used throughout TAOCP!

Algorithms in TAOCP are described in pseudocode and implemented as programs written in assembly language for the MMIX computer. But an MMIX computer has never been manufactured. It can only be used in simulator programs. Outside of TAOCP, there are almost no code examples, guides, tutorials or videos. This can be a dealbreaker for many people used to an abundance of information for other programming languages readily available at popular websites.

The next few TAOCP meetups will cover enough of MMIX to attain a working knowledge sufficient to read and write simple programs. Side by side we will learn to use tools to run and debug our programs. Hopefully by the time we're done, our meetup notes, discussions and videos will lower the barrier to learning and working with MMIX.

In this first meetup on MMIX, we learn how data is represented and stored in MMIX memory. Data is operated upon using instructions from the MMIX instruction set. We'll start with instructions for moving data between memory and registers where data may be manipulated. We'll continue with more instructions in the following meetups.

We'll begin to use some invaluable tools for working with MMIX in the second half of the meetup. We'll see how to use the MMIX Visual Debugger GUI https://mmix.cs.hm.edu/mmixvd to edit, run and step through MMIX assembly language programs. The MMIX simulator and assembler https://mmix.cs.hm.edu/src are commandline tools that will be demoed in upcoming meetups. All these tools are free and open source and available for Linux, Windows and Mac.


## Chat Copy

**Uri Segal** 2:02 PM<br>
IBM PC AT
no... XT

**Zartaj T Majeed** 2:04 PM<br>
Miguel heard me so I think it's at your end

**Michael Zalewski** 2:04 PM<br>
Time sharing system... PDP or maybe a IBM mainframe

**Jason Vigil** 2:05 PM<br>
thanks -- I'll try to figure it out

**Zartaj T Majeed** 2:09 PM<br>
Is anyone having a problem hearing us?

**Jason Vigil** 2:10 PM<br>
Denver, CO

**Deepa Annamalai** 2:10 PM<br>
i am connecting from Bay Area, California

**Uri Segal** 2:11 PM<br>
i think it was IBM PC first
then they split into an XT and AT version

**Miguel Angel Iglesias** 2:11 PM<br>
MSX Basic

**Jason Vigil** 2:11 PM<br>
Probably some unknown make/model win95 machine, or a TI graphing calculator

**Uri Segal** 2:11 PM<br>
early 80s

**Deepa Annamalai** 2:14 PM<br>
Not sure microprocessor programming counts on 8085/8086

**Michael Zalewski** 2:15 PM<br>
I think in my case it was an IBM mainframe

**Miguel Angel Iglesias** 2:20 PM<br>
http://mmix.cs.hm.edu/doc/fasc1.pdf

**Jason Vigil** 2:26 PM<br>
I wonder if the series will ever be "finished"

**Uri Segal** 2:27 PM<br>
he states his numbers as powers of 2
$2.56 reward
128 page fascicle

**Uri Segal** 2:29 PM<br>
father of mips2000 no?
and now chairman of alphabet

**Uri Segal** 2:30 PM<br>
\*MIPS
DEC

**Michael Zalewski** 2:31 PM<br>
I would like to see a comparison between MMIX and a modern 64 bit processor like Pentium or maybe powerPC. I think there are lots of differences

**Uri Segal** 2:31 PM<br>
yes

**Michael Zalewski** 2:32 PM<br>
Things about real microprocessors that you would never learn if you study MMIX. Especially how the processor interracts with the O/S

**Zartaj T Majeed** 2:35 PM<br>
Knuth also wrote MMIXWare mentioned in sec  1.3'
MMIXWare has the complete specification of MMIX and how it interacts with an OS

**Miguel Angel Iglesias** 2:41 PM<br>
as a self taught, this is the first time I find out why we use hexadecimals in computers o_O

**Uri Segal** 2:46 PM<br>
dword for tetra

**Uri Segal** 2:47 PM<br>
one's complemmentand add 1

**Michael Zalewski** 2:47 PM<br>
Flip the bits and then add 1
Uri said same

**Deepa Annamalai** 2:49 PM<br>
Could you pls give me a simple example say with number 4 -- 0100

**Michael Zalewski** 2:49 PM<br>
Flip the bits, get 1011
Add 1, get 1100

**Miguel Angel Iglesias** 2:50 PM<br>
I think the one I found is slightly different...

**Uri Segal** 2:50 PM<br>
0100 --> 1011 --> 1100
that's -4 in 2's complement

**Deepa Annamalai** 2:50 PM<br>
thank you

**Zartaj T Majeed** 2:51 PM<br>
that would be 4 -> -4

**Deepa Annamalai** 2:51 PM<br>
ahhh got it... :)

**Zartaj T Majeed** 2:51 PM<br>
try it the other way: -4 -> 4

**Deepa Annamalai** 2:51 PM<br>
the first bit identifies as negative...

**Zartaj T Majeed** 2:51 PM<br>
the technique is the same

**Michael Zalewski** 2:52 PM<br>
-4 is 1111 1100. Flip the bits and get 0000 0011. Then add 1 to get 0000 0100

**Zartaj T Majeed** 2:53 PM<br>
Marc - do you have the text? Fascicle 1, MMIX?

**Miguel Angel Iglesias** 2:54 PM<br>
I actually need one more min
http://mmix.cs.hm.edu/doc/fasc1.pdf

**Miguel Angel Iglesias** 2:57 PM<br>
it took me a second read

**Uri Segal** 2:57 PM<br>
$ + number

**Miguel Angel Iglesias** 2:57 PM<br>
I mean it took me a second read to understand the Mx
 

**Michael Zalewski** 2:57 PM<br>
Kind of. But if you are accessing a Tetra, then M[0] = M[1] = M[2] = M[3]
Which is wierd

**Miguel Angel Iglesias** 2:58 PM<br>
M1[0] = M[0]M[1]

**Uri Segal** 2:59 PM<br>
the subscript indicates the number of bytes pulled out

**Miguel Angel Iglesias** 2:59 PM<br>
\*M2

**Jason Vigil** 2:59 PM<br>
so M_4[0] = M_4[1] = M_4[2] = M_4[3]

**Miguel Angel Iglesias** 3:01 PM<br>
M_2[1] = M[2]M[3] = M[2*1]M[2*1 +1]
8 bits

**Uri Segal** 3:01 PM<br>
bytes

**Miguel Angel Iglesias** 3:02 PM<br>
yeah it's an octa

**Zartaj T Majeed** 3:19 PM<br>
we're back

**Uri Segal** 3:19 PM<br>
only 256 opcodes....

**Miguel Angel Iglesias** 3:20 PM<br>
ADD $X $Y $Z reminded me of lisp

**Uri Segal** 3:20 PM<br>
few...
guess i'm used to modern processors
x86...

**Miguel Angel Iglesias** 3:21 PM<br>
(+ 1 2)
1 + 2

**Uri Segal** 3:21 PM<br>
he uses GNU style assembly: left to riht
as oppoed to Intel style assembly for the operands, which is right to left

**Zartaj T Majeed** 3:24 PM<br>
I'm going to set up the demo screenshare now
so the slides will go away and will be replaced by the MMIX Visual Debugger in a bit

**Miguel Angel Iglesias** 3:27 PM<br>
I guess is time to install wine...

**Zartaj T Majeed** 3:27 PM<br>
I believe there are binaries for Mac and Linux

**Miguel Angel Iglesias** 3:27 PM<br>
there are! http://mmix.cs.hm.edu/bin/index.html

**Zartaj T Majeed** 3:28 PM<br>
for now I suggest just following the demo

**Zartaj Majeed** 3:28 PM<br>
demo program is https://github.com/theartofcomputerprogramming/mmixsamples/blob/master/load_and_store/loadstore.mms

**Uri Segal** 3:36 PM<br>
does MMIX store in LSB or MSB order?
or rather interpret
the opcodes

**Uri Segal** 3:37 PM<br>
\*instructions

**Uri Segal** 3:42 PM<br>
initial value of program counter?

**Uri Segal** 3:44 PM<br>
and the general registers...

**Michael Zalewski** 3:45 PM<br>
Copy one byte from memory

**Uri Segal** 3:45 PM<br>
load M[$2 + $3] into $4
$2 + $3

**Miguel Angel Iglesias** 3:45 PM<br>
but isn't $2 and $3 empty yet?

**Uri Segal** 3:45 PM<br>
is the address

**Miguel Angel Iglesias** 3:45 PM<br>
\*arent

**Miguel Angel Iglesias** 3:47 PM<br>
oh, basically the first instruction says to put whatever is in M[0] to $4

**Uri Segal** 3:48 PM<br>
argv[0] is the name i think

**Uri Segal** 3:51 PM<br>
address of the current instruction
to eecute
execute

**Uri Segal** 3:52 PM<br>
can we assume all opcodes execute in one 'clock-cycle', whatever that mean in this context ?

**Uri Segal** 3:55 PM<br>
so the label 'Main' is required ?
yes

**Uri Segal** 4:08 PM<br>
why did rL highlight ?
for the instruction on line 61

**Uri Segal** 4:12 PM<br>
the sign bit was set

**Miguel Angel Iglesias** 4:12 PM<br>
mod 264?

**Uri Segal** 4:12 PM<br>
so it sign extended

**Michael Zalewski** 4:13 PM<br>
\#83 is signed byte, so sign was extended

**Uri Segal** 4:13 PM<br>
8
the upper bit

**Uri Segal** 4:16 PM<br>
byte-lane mapping

**Uri Segal** 4:23 PM<br>
$3 + an offset

**Deepa Annamalai** 4:24 PM<br>
gotit

**Uri Segal** 4:27 PM<br>
yes. and flag was set

**Jason Vigil** 4:28 PM<br>
have to go now, thanks

**Miguel Angel Iglesias** 4:32 PM<br>
this was great! thanks

**Thomson Kneeland** 4:32 PM<br>
all good, thanks for all that!

**Alan Lin** 4:32 PM<br>
Thank you!

**Uri Segal** 4:32 PM<br>
thanks!

**Deepa Annamalai** 4:32 PM<br>
this was wonderful. i was little scared to join
thank you so much

**Marc Vreuls** 4:32 PM<br>
Thanks a lot! Very nice presentation.


## Zartaj

Zartaj's notes

Expanding on topics that came up in meetup

### MMIX is Big-endian

MMIX is bigendian or MSB or Most Significant Byte memory layout order

Why?

Endianness only makes a difference when storing (writing) or loading (reading) a value that takes up more than 1 byte in memory

Suppose we use a 2-byte hex value 0x1234 which is decimal 4660

This is where Miguel's comment above about appreciating the use of hex in computers makes sense

In hex it's really easy to see the bits and bytes in memory for any value. Something you can't do with the decimal value or even in binary because it's very hard to count so many bits individually and keep them separated in groups of 8

anyway 0x1234 needs 2 bytes 12 34

when MMIX stores 0x1234 at memory address say 0 - it places the bytes as follows:

address 0: 12\
address 1: 34

this means the address of the full value which is address 0 is the address of the high-order or most significant or the big-end byte

similarly when MMIX reads this 2 byte value from address 0 it loads it into a register as 0x1234 meaning it takes the first byte at address 0 to be the high byte and the second byte as the low byte

the alternative is little-endian that I won't explain and people can look up in wikipedia

### What is $0 and $1 at program startup?

So $0 is what we call register 0 and $1 is register 1

When a program starts $0 is set to argc - the number of program arguments on the commandline

and $1 is set to the **address** of argv - the argument vector or the array of argument strings - so $1 is an address of an array of addresses

When I ran the `loadstore.mms` program for the debugger demo, I did not set a commandline for the program - it's actually an option in the Run menu

Since the commandline was empty, argc was zero, and argv pointed to an empty array

This is highly abnormal - it only happened because `loadstore.mms` is an artificially constructed program to try out individual instructions

A normal program would run as a command and its commandline would have at least the program executable name as the first argument

So a normal program would have argc >= 1 and $0 would not be zero. Also argv would not be empty and the address in $1 would be of an array with at least one address - that of the first argument.

### Why did the debugger highlight $2 after the first instruction?

I believe the debugger only highlights fields that change after an instruction runs. The first instruction was `LDB $4,$2,$3`. This only changes $4 but the debugger highlighted $2 as well but not $3. This is because $2 was actually not zero when the program starts. However the simulator sets it to zero before running the first instruction. This is why $2 was highlighted after the instruction ran.

The status window for the demo program `loadstore.mms` shows $2 as a local register before Main starts. Its value is 2. So $2 is being used by the simulator before Main starts. I don't know why it is 2 and what the 2 means.

Anyway when Main starts, rL - explained below - is 2. This is because Main starts out with 2 local registers $0 and $1, for argc and argv. And I think this means that all other previously local registers numbered 2 and above are zeroed out when Main starts. This is why $2 got highlighted after the first instruction ran even though the instruction itself did not change it.

All this has to do with the register stack and function calls but because Main is called by the simulator and not our code it is difficult to see what happened before Main runs.

We could look at the simulator code or ask Martin Ruckert about this.

### Why did rL keep changing?

rL is the local threshold register - it has the count of local registers. This is the number of registers designated local for the current function.

A register becomes local when it is set by an instruction. Not just that but all lower-numbered registers become local - and rL changes to show the new count. So in a way the value of rL is the lowest-numbered non-local register. Knuth calls the non-local registers marginal registers, excluding global registers.

The demo program `loadstore.mms` uses a new destination register for nearly all instructions. This is why rL kept changing and being highlighted as we stepped through the program.

Local registers are important to understand the register stack used for function/subroutine calls but knowing or using rL does not seem important for applications.

