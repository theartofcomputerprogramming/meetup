# TAOCP #2 - Algorithms (Chapter 1, Basic Concepts: Section 1.1)

**Date:** Saturday, 12 September 2020<br>
**Time:** 2-4pm America/New_York<br>
**Location:** Google Meet online

## Agenda

**2:00 - 2:10** Meet and greet<br>
**2:10 - 3:00** Read and discuss couple pages at a time from *Volume 1, Fundamental Algorithms*: *Chapter 1, Basic Concepts*

-  *1.1 Algorithms* (pp.1-9)
-  Skim *Appendix A*, *B*, and *C* (pp.619-629)

**3:00 - 3:10** Break<br>
**3:10 - 4:00** *Exercises* (p.9), shoot the breeze<br>

Well - We begin reading TAOCP in earnest today!

As its title suggests, TAOCP is about three things - "Art", "Computers" and "Programming". Knuth spoke at length on "Art" in his Turing Award lecture https://dl.acm.org/doi/pdf/10.1145/1283920.1283929. Today we look at the foundation of "Programming" that is built upon the concept of an algorithm. And we'll spend time on "Computers" in the coming sessions.

# Chat Copy

**Zartaj Majeed** 2:00 PM<br>
we'll get going around 2:10

**William Linkmeyer** 2:02 PM<br>
Philadelphia, PA, US
<3

**James Curran** 2:03 PM<br>
I'm on twice.  On my phone for video & audio, and on my desktop for seeing the shared screen.  (laptop undergoing an extended OS update)

**Zartaj Majeed** 2:03 PM<br>
no problem - more the merrier

**Akash Shingte** 2:03 PM<br>
Metuchen, NJ

**Zartaj Majeed** 2:04 PM<br>
we'll get going around 2:10
please feel free to chat amongst yourselves till then

**Akash Shingte** 2:06 PM<br>
Proving correctness

**William Linkmeyer** 2:07 PM<br>
does anyone have a good online copy or pdf for TAOCP? I read through a lot of it in college, but I'm home now without the library

**Thomson Kneeland** 2:08 PM<br>
agreed on proofs

**Michael Zalewski** 2:08 PM<br>
Search for it on Google. You will find several

**Jason Vigil** 2:08 PM<br>
having intuition about the correct algorithm for a given task

**Michael Zalewski** 2:08 PM<br>
Also, O'Reilly has it

**Arthur O'Dwyer** 2:08 PM<br>
Re hard about algorithms: I was going to say I often find it hard to imagine "coming up with a NEW algorithm," in the sense of "binary search tree" or "quicksort" or "priority heap" or whatever... but on more reflection, I think I disagree with myself. :)

**Zartaj Majeed** 2:25 PM<br>
do feel free to type in the chat as you're reading

**Arthur O'Dwyer** 2:27 PM<br>
Again with the trivia, I notice that Knuth goes out of his way to define a shorthand syntax "n <- m <- r". I wonder if this is influence from C, which supports chaining assignments "n = m = r;" or if chaining assignments existed in other programming languages of the era as well.
Chaining assignment is one of my pet peeves in C++ — it's idiomatic for every type to *support* chaining assignment, even as it's extremely discouraged for any programmer to ever *use* chaining assignment.

**Akash Shingte** 2:30 PM<br>
Which notation do you guys prefers -> CLRS or Knuth? Being familiar with CLRS this definitely feels weird.

**Zartaj Majeed** 2:37 PM<br>
James is holding up CLRS

**Akash Shingte** 2:37 PM<br>
Thanks for reference James!

**William Linkmeyer** 2:39 PM<br>
thank you James :)

**Arthur O'Dwyer** 2:40 PM<br>
I think the existence of MIX assembly language suffices to explain why Knuth's pseudocode is more goto-ish and less structured... but FWIW, here's the essay I briefly tried to refer to, from 1974: https://pic.plover.com/knuth-GOTO.pdf It was sort of a rebuttal to "Go To Considered Harmful," if I recall correctly.

**Zartaj Majeed** 2:41 PM<br>
"an algorithm must be seen to be believed"

**Michael Zalewski** 2:42 PM<br>
Many algorithms are seen and not believed

**Miguel Angel Iglesias** 2:47 PM<br>
I still don't get why any number that divides m and n, also divides m-qn

**Zartaj Majeed** 2:47 PM<br>
say g divides both m and n
then m= k * g
n = l * g
then m - qn = kg + q * (lg)

**Zartaj Majeed** 2:48 PM<br>
= (k + ql) * g

**William Linkmeyer** 2:50 PM<br>
I have to go now, thank you for the meeting :)

**Zartaj Majeed** 2:51 PM<br>
thanks William

**Michael Zalewski** 2:53 PM<br>
Find a solution for x^n + y^n = z^n
It's been solved, and it has no inputs

**Arthur O'Dwyer** 2:54 PM<br>
Or is that an algorithm for \sum_X x^n = z^n, with input X hard-coded to {x,y}? ;)

**Michael Zalewski** 2:56 PM<br>
\\\\\\\\\\\\\\\\

**Jason Vigil** 2:57 PM<br>
perhaps it would be possible to define an ineffictive algorithm

**Jason Vigil** 2:58 PM<br>
same as what james said pretty much

**Michael Zalewski** 2:58 PM<br>
An algorithm is effective if you can do it. It's not effective if there is no way to do it, or if there is no reasonable way to do it.

**Arthur O'Dwyer** 2:58 PM<br>
I think Knuth would say that you can solve any problem in NP "definitely" but not "effectively."
The "definite" way to solve it is "Just find the answer." That's "definite" but not "effective."

**Miguel Angel Iglesias** 2:59 PM<br>
it could also be polynomial, like n^4
still not effective

**Michael Zalewski** 3:00 PM<br>
I think a 'definite' algorithm is one where all the steps are correctly defined. If there are corner cases, then there are some inputs where the algorithm does not work, and it is not definite
(Corner cases where the steps don't work or cannot be applied)

**Arthur O'Dwyer** 3:01 PM<br>
(Part of my interpretation is that Knuth doesn't even care at all about _incorrect_ algorithms.)

**Michael Zalewski** 3:01 PM<br>
I guess i should say 'where all the steps are not completely defined
Definiteness

**Akash Shingte** 3:02 PM<br>
+1 for thinking in terms of defining corner cases for a 'definite' algorithm

**Jason Vigil** 3:02 PM<br>
The example knuth uses for an ineffective algorithm is applying the euclid algorithm to irrational numbers

**Michael Zalewski** 3:02 PM<br>
You can have an algorithm that requires division, but if some input requires division by zero, then the algorithm is not definite, because it won't always work

**Akash Shingte** 3:03 PM<br>
An example of `ineffective` algorithm would be -  `calculate size of universe`

**Arthur O'Dwyer** 3:04 PM<br>
"The example knuth uses for an ineffective algorithm is applying the euclid algorithm to irrational numbers" — Hmm, true. I interpreted that as meaning that it would take infinitely much time for the non-omnipotent-reader-with-pencil-and-paper to divide those numbers. But it's also the case that Algorithm E on real numbers might *never terminate*. Which would definitely violate "Finiteness" as well.
"Algorithm E on real numbers" violates a whole bunch of these properties all at once, unfortunately.

**Thomson Kneeland** 3:08 PM<br>
+1 Arthur.  What I keep coming back to in this discussion is that a definition of the domain over which we are operating is essential. Operating over integers vs Real vs irrational vs complex yield violating edge cases
could be solved by inclusion of a terminating condition

**Arthur O'Dwyer** 3:09 PM<br>
Right, what these days we'd call "data types." I'm waiting to see when/if Knuth uses the notion of "type."

**Jason Vigil** 3:12 PM<br>
He also uses an example of "If 4 is the largest integer n for which there is a solution to the equation w^n + x^n + y^n = z^n" as an ineffective operation because the algorithm to compute that isn't defined. More intersection between effectiveness and definiteness

**Zartaj Majeed** 3:15 PM<br>
we're back

**Arthur O'Dwyer** 3:16 PM<br>
I'm seeing "effectiveness" as meaning "do I know how to do it" and "definiteness" as meaning "am I sure I'm doing it right." Which is the same abstract distinction as P vs NP — "do I know a way to solve it" versus "do I know a way to verify my solution." But yeah, his examples don't support *quite* such a clear-cut categorization. :)

**James Curran** 3:26 PM<br>
Exactly my feeling...

**Jason Vigil** 3:28 PM<br>
What is Q supposed to be?
others make sense, but I don't quite understand what Q is

**Michael Zalewski** 3:29 PM<br>
Q is the state of the machine

**Miguel Angel Iglesias** 3:30 PM<br>
Q = I + Omega?

**Michael Zalewski** 3:33 PM<br>
Q is much bigger than I + Omega. It contains I and Omega, and all the states that got from I to Omega. Probably also all the states even if they were never arrived at in the algorithm (that is, there are elements in Q which are not the target of applying f to I, and not f(f(I)), f(f(f(i)))

**Michael Zalewski** 3:34 PM<br>
The algorithm starts with I (the input) which could be empty. The first step of the algorithm is f(I)

**Akash Shingte** 3:35 PM<br>
Q  = { I } U { Omega } U { intermediate states }

**Michael Zalewski** 3:36 PM<br>
Q is even much bigger than that (if by intermediate state you mean something that is reachable by applying f)

**Akash Shingte** 3:37 PM<br>
Yeah, I did.
Need to give it another read

**Arthur O'Dwyer** 3:37 PM<br>
Right, in this specific instance, Q contains the quadruple (1,2,0,3), which is not f(x) for any x.

**Jason Vigil** 3:38 PM<br>
f(q) should equal q for all elements q of omega
input & output?

**Arthur O'Dwyer** 3:39 PM<br>
But Knuth *could* have carefully defined this specific Q so that it wouldn't contain the quadruple (1,2,0,3) at all. There's just no real benefit to doing so — it'd be difficult and/or tedious to define, and doesn't help us solve the "greatest common divisor" problem any better.

**Michael Zalewski** 3:39 PM<br>
When f takes one argument, it is the input. So f(q) is the application of the first step of the algorithm

**Michael Zalewski** 3:40 PM<br>
f((m,n)) is a single input element from I, which is the set of all possible tuples. That's why there are double parens

**Miguel Angel Iglesias** 3:41 PM<br>
well an intermediate state is _also_ a valid input right?

**Arthur O'Dwyer** 3:42 PM<br>
We could insert a case corresponding to Step E0, like this:
f((m,n)) = (m,n,0,0)  [replaces the first equation]
f((m,n,0,0)) = (m,n,0,1) if m > n, (n,m,0,1) otherwise
[all other equations as before]

**Jason Vigil** 3:42 PM<br>
Yeah by input & output I meant the equations f((m,n))=(m,n,0,1) and f((n))=n

**Arthur O'Dwyer** 3:44 PM<br>
Relevant to my earlier talking about "data types": It's important to realize that Knuth is typing `f` as a function of type `Q -> Q`... but `Q` itself has elements of different "shapes". Some elements of Q are integers; some are quadruples of integers; some are pairs of integers.

**Michael Zalewski** 3:44 PM<br>
I'm not sure I follow f((n)). f is defined on I (so you have f((m,n)), and on omega, which is just a single number and not a tuple. So you might have f(n) = n -- but you don't really need it
Once application of f arrives in some element of Omega, you are done

**Michael Zalewski** 3:47 PM<br>
So I guess Q is even bigger than the state of all possible machine states. You have to add all possible inputs  .. I, and all possible outputs .. Omega

**Michael Zalewski** 3:48 PM<br>
Turing complete?

**Jason Vigil** 3:48 PM<br>
halting problem?

**Arthur O'Dwyer** 3:49 PM<br>
@Michael: "So you might have f(n) = n -- but you don't really need it" — I suspect that this wrinkle is just so that you can say "The machine halts within k steps if-and-only-if x_k\in\Omega."  If you didn't have that last wrinkle, you'd have to say something like "The machine halts within k steps if-and-only-if there exists some j<k such that x_j\in\Omega" (and x_k wouldn't necessarily be defined for all k).

**Arthur O'Dwyer** 3:51 PM<br>
You can also tell we're programmers and not mathematicians because we're all writing `n` when we mean `(n)`. The parens are significant. But I messed it up first. ;)

**Michael Zalewski** 3:51 PM<br>
Nothing really about halting. You define f on I, Omega, and Q. Why do you even need it defined when I and Q is empty. The algorithm terminates because the function arrived in Omega

**James Curran** 3:51 PM<br>
t <- A A<-B, B<-C, c<-D, D<-T

**Michael Zalewski** 3:51 PM<br>
< Math major
But that was so long ago

**Miguel Angel Iglesias** 3:52 PM<br>
thanks everyone! gotta go, but this was very helpful

**James Curran** 3:54 PM<br>
E1  )  r <- m % n

**Zartaj Majeed** 3:54 PM<br>
thanks Miguel

**James Curran** 3:54 PM<br>
new E3 )   m= n% r

**Michael Zalewski** 3:59 PM<br>
This is related to the line in the text where he states that Tn converges to (12(ln 2)/ pi ^2) ln n
Tn for large n
He is asking to work it for T5
It will be 9/5

**Arthur O'Dwyer** 4:01 PM<br>
13/5, because I think people are forgetting that the first time you hit step E1, it just exchanges the numbers.
(For m=1, n=5, E1 is executed 2 times.)

**Thomson Kneeland** 4:01 PM<br>
are inputs equiprobable?

**Arthur O'Dwyer** 4:02 PM<br>
As far as the definition of T is concerned, yes inputs are equiprobable.

**Thomson Kneeland** 4:02 PM<br>
(assumption)

**James Curran** 4:05 PM<br>
Thomson, is that a guitar or a cello in your picture?

**Jason Vigil** 4:05 PM<br>
thank you! enjoyed the session

**Thomson Kneeland** 4:05 PM<br>
thanks

**Akash Shingte** 4:05 PM<br>
Thanks guys! See you next saturday!

**James Curran** 4:05 PM<br>
I probably will not be able to make the next sessions

# Zartaj

Zartaj's notes


p.1
remarkable ada quote that she sussed out the nature of computers, more like philosopher than scientist

p.2

stunning level of historical detail and authenticity
just historical references could be book of its own

by 1950 word algorithm associated with, how about 2020?

I think algorithm began as this recipe-like approach to solving a problem
now it connotes some computer/programmer derived heuristics for decision making and choices and recommendations like netflix recommendations or search results or delivery job assignment and other giglike selections

algorithm now connotes data ie algorithm is subsumed to data
also has become a singular the algorithm
like youtube's algorithm, tiktok's algorithm, google's algorithm, netflix's algorithm
this unseen omniscient presence that is constantly interacting with its environment and can be manipulated

choice of euclid's algorithm to introduce concept

pp.4-6
five key features of algorithm
does it jibe with your concept of algorithm?

p.6
difference from cookbook recipe
problem with all analogies, always with human processes
reasonably finite number not just finite

p.7
algorithm analysis to choose best algorithm
nature of T_n
difference from theory of algorithms

pp.7-9
formal mathematical definition of algorithm and computational method
euclid: I is input ie domain which is pairs (m, n), omega is output ie range which is single values g
Q is set of states
f is transition function
why does Q need to include I and omega?
what's the fixed-point requirement for?

how does this map to 5 features of algorithm?
Finiteness: requirement that there is a k st x_k+1 = f(x_k)
Definiteness: definiteness is the mapping definition of f, interesting to see how states show up in quadruples for euclid
Input: obvious
Output: obvious
Effectiveness: extra restriction of finite encoding

why markov strings instead of turing machine?

