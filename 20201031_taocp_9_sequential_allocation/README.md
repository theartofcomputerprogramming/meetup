# TAOCP #9 - Sequential Allocation

Memory allocation schemes!

We've begun to look at lists of records that may grow and shrink. Now we consider how to manage these lists in memory. We'll look at a few algorithms for sequential allocation and work on some exercises

**A recording of this event is at https://www.youtube.com/channel/UCHOHy9Rjl3MlEfZ2HI0AD3g**

**Date:** Saturday, 31 October 2020\
**Time:** 2-4pm America/New_York\
**Location:** Google Meet online

## Agenda

**2:00 - 2:10** Meet and greet\
**2:10 - 3:00** Read and discuss couple pages at a time from *Chapter 2, Information Structures* (along with *MMIX Supplement*)

- *2.2 Linear Lists* (pp.244-251)

  - *2.2.2 Sequential Allocation* (pp.244-245)
  - *2.2.2 Sequential Allocation* (pp.245-246)
  - *2.2.2 Sequential Allocation* (pp.247-248)
  - *Algorithms G, R* (pp.248-250)
  - *2.2.2 Sequential Allocation* (pp.250-251)

**3:00 - 3:10** Break\
**3:10 - 4:00**
- *Exercises* (pp.251-254)
- Shoot the breeze

**Note on MMIX and MIX**

The **MMIX** is a hypothetical computer designed by Knuth. It is a successor to **MIX** which is still referred to in all printings of Vols. 1-3 of TAOCP. **MMIX** is significantly different from **MIX**. In order to use **MMIX** instead of **MIX** now means having to supplement TAOCP with two primary sources.

The first supplement is *Fascicle 1, MMIX*, a booklet written by Knuth describing the computer and its assembly programming language. It replaces Sections 1.3 and 1.4 of *Chapter 1, Basic Concepts*. The section numbers in the fascicle have a prime (') suffix to distinguish them from the originals, e.g. fascicle section 1.3.1' replaces TAOCP section 1.3.1.

The second supplement is *The MMIX Supplement* by Martin Ruckert that has **MMIX** versions of all programs and content in TAOCP that currently refer to the older **MIX** computer. It uses the same section numbers as in TAOCP with page references and text snippets from TAOCP to help sync the **MMIX** version of the content with its location in TAOCP.


## Chat Copy


**Miguel Iglesias** 2:14 PM\
I will be silent for a while, too much family noise around me

**Miguel Iglesias** 2:19 PM\
ah for some reason I mixed what Arthur said with the idea of not moving F

**Zartaj Majeed** 2:30 PM\
M=4, F=R=0\
F/R  --  --  --\
F     R  --  --\
F     X  R  --\
--     F  R  --\
--     F  X  R\
--     --  F  R

**Michael Zalewski** 2:35 PM\
You guys are reading too much into it. In Section 2.1 we talked about stacks, queues and dequeues in the abstract, without implementation. In Section 2.2, we are told that the simplest implementation is sequential allocation -- but it's not so simple because you have to deal with UNDERFLOW and OVERFLOW (and the creeping of real data through all your memory in the case of a queue)

**Michael Zalewski** 2:39 PM\
To me, the use of the term UNDERFLOW and OVERFLOW means we are talking about stacks (and possibly queues and dequeues)

**Arthur O'Dwyer** 2:40 PM\
OVERFLOW and UNDERFLOW are defined on page 245, in the context of stacks and queues (only).

**Michael Zalewski** 2:41 PM\
I suppose trying to find the first item in an empty list is considered UNDERFLOW.

**Miguel Iglesias** 2:41 PM\
which is an issue even in high level langs like Scala, where List().head is allowed, and it throws an exception

**Michael Zalewski** 2:42 PM\
Doesn't List().head = Nil in Scala?

**Miguel Iglesias** 2:42 PM\
nope, it's equal to BOOM\
specifically: RuntimeException("Head of )empty list"

**Arthur O'Dwyer** 2:47 PM\
Similarly in C++, where std::stack<T> has a pop() method, and popping an empty stack [UNDERFLOW] is "undefined behavior" (meaning that the programmer _must_ ensure that (not stack.empty()) before trying to pop); but stack.push(x) has no precondition — if we run out of memory [OVERFLOW] then we throw an exception.

**Zartaj Majeed** 2:48 PM\
underflow is trying to delete from an empty list\
overflow is trying to add to a full list

**Arthur O'Dwyer** 2:48 PM\
s/list/stack or queue/; he defines these terms on page 245.

**Zartaj Majeed** 3:05 PM\
break till 3:15

**Zartaj Majeed** 3:15 PM\
we're back

**Zartaj Majeed** 3:26 PM\
delete from rear of deque?

**Arthur O'Dwyer** 3:28 PM\
Delete from rear of queue:\
if R=F, then UNDERFLOW;\
if R=1, then R <- M, otherwise R - 1;\
Y <- X[R].

**Arthur O'Dwyer** 3:29 PM\
except that "R - 1" should say "R <- R - 1"\
and "X[R]" should say "X[(R mod M) + 1]", I think

**Zartaj Majeed** 3:31 PM\
delete from front of deque?

**Zartaj Majeed** 3:32 PM\
same as delete from front of queue\
inser into front of deque?

**Arthur O'Dwyer** 3:34 PM\
Insert at front of queue:\
if F=1, then F <- M, otherwise F <- F - 1;\
if R=F, then OVERFLOW;\
X[(F mod M) + 1] <- Y.

**Miguel Iglesias** 3:34 PM\
can you explain why F mod M?

**Arthur O'Dwyer** 3:35 PM\
Insert at front of queue:\
Set O <- F;\
if F=1, then F <- M, otherwise F <- F - 1;\
if R=F, then OVERFLOW;\
X[O] <- Y.

**Arthur O'Dwyer** 3:39 PM\
Insert at front of queue, Michael's version, I think it's OK:\
X[F] <- Y;\
if F=1, then F <- M, otherwise F <- F - 1;\
if R=F, then OVERFLOW.

**Arthur O'Dwyer** 3:42 PM\
Knuth's answer (page 540) matches Michael's version. He does the unconditional write X[F] <- Y.

**Arthur O'Dwyer** 3:44 PM\
Steps G1/G2: Sneaky handwavey for-loop in disguise! :P

**Michael Zalewski** 3:45 PM\
I think going forward they are all like that... Step n says Execute Step n+1 for k times, then go to Step n + 2

**Arthur O'Dwyer** 3:48 PM\
In Step G3: Why "SUM < 0" instead of "SUM = 0"? (I'm not sure, but the answer probably involves 1-indexing.)

**Michael Zalewski** 3:48 PM\
Because BASE[1] starts out as 0, and TOP[n] starts out as M
So if SUM = 0, there is one word left somewhere

**Arthur O'Dwyer** 3:50 PM\
I don't fully grok that, but it sounds plausible.\
Step R4 is an even crazier control-flow tree crammed into a single step. :P

**Zartaj Majeed** 3:51 PM\
maybe 2 more minutes

**Arthur O'Dwyer** 3:59 PM\
The "further study of Algorithm G" mentioned on page 251 is a paper titled "Tuning Garwick's algorithm for repacking sequential storage"; I can't find it online anywhere.

**Arthur O'Dwyer** 4:07 PM\
25/25 . 0/25 . 0/25 . 0/25\
25/97 . 1/1 . 0/1 . 0/1\
26/97 . 1/1 . 0/1 . 0/1

**Arthur O'Dwyer** 4:10 PM\
26/61 . 1/36 . 0/1 . 0/1\
26/61 . 2/36 . 0/1 . 0/1

**Michael Zalewski** 4:10 PM\
Cool!

**Arthur O'Dwyer** 4:15 PM\
Abstract: "Garwick’s algorithm, for repacking LIFO lists stored in a contiguous block of memory, bases the allocation of remaining space upon both sharing and previous stack growth. A system whereby the weight applied to each method can be adjusted according to the current behaviour of the stacks is discussed.

We also investigate the problem of determining during memory repacking that the memory is used to saturation and the driving program should therefore be aborted. The tuning parameters...\
...studied here seem to offer no new grasp on this problem."


