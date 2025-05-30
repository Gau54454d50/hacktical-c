# Hacktical C
A practical hacker's guide to the C programming language.

*In memory of [Dennis Ritchie](https://en.wikipedia.org/wiki/Dennis_Ritchie),
one of the greatest hackers this world has known.*

## About the book
This book assumes basic programming knowledge. We're not going to spend a lot of time and space on explaining basic features, except where they behave differently in important ways compared to other mainstream languages. Instead we're going to focus on practical techniques for making the most out of the power and flexibility C offers.

The book is very much a work in progress. I'd say we're about half way there in terms of material; and it needs more polish, please mind the gaps. And please report any issues you come across or suggestions for improvements in the repo.

## About the author
You could say that there are two kinds of programmers, with very different motivations; academics and hackers. I've always identified as a hacker. I like solving tricky problems, and I prefer using powerful tools that don't get in my way. To me; software is all about practical application, about making a change in the real world.

I've been writing code for fun on a mostly daily basis since I got a Commodore 64 for Christmas in 1985, professionally in different roles/companies since 1998.

I started out with Basic on the Commodore 64, went on to learn Assembler on an Amiga 500, Pascal on PC; C++, Modula-3, Prolog, Ruby, Python, Perl, JavaScript, Common Lisp, Java, Forth, Haskell, SmallTalk, Go, C#, Swift.

For a long time, I didn't care much about C; the language felt primitive compared to other languages, especially C++. But gradually over time, I learned that the worst enemy in software is complexity, and started taking C more seriously.

Since then I've written a ton of C; and along the way I've picked up many interesting techniques that helped me make the most out of the language and appreciate it for its strengths.

## License
The content of this book is openly licensed via [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).

## Support
I've decided to release the project using an open license to benefit as many as possible, because I believe knowledge should be shared freely.

But I also believe in compensation for creators; and the less economic pressure I have to deal with, the more time and energy I can put into the project. 

The repository is set up for sponsoring via Stripe and Liberapay, alternatively you may use BTC (bitcoin:18k7kMcvPSSSzQtJ6hY5xxCt5U5p45rbuh) or ETH (0x776001F33F6Fc07ce9FF70187D5c034DCb429811). 

## Why C?
The reason I believe C is and always will be important is that it stands in a class of its own as a mostly portable assembler language, offering similar levels of freedom.

C doesn't try very hard to prevent you from making mistakes. It has very few opinions about your code and happily assumes that you know exactly what you're doing. Freedom with responsibility.

These days; many programmers will recommend choosing a stricter language, regardless of the problem being solved. Most of those programmers wouldn't trust themselves with the kind of freedom C offers, many haven't even bothered to learn the language properly.

Since most of the foundation of the digital revolution, including the Internet was built using C; it gets the blame for many problems that are more due to our immaturity in designing and building complicated software than about programming languages.

The truth is that any reasonably complicated software system created by humans will have bugs, regardless of what technology was used to create it. Using a stricter language helps with reducing some classes of bugs, at the cost of reduced flexibility in expressing a solution and increased effort creating the software.

Programmers like to say that you should pick 'the right tool for the job'; what many fail to grasp is that the only people who have the capability to decide which tools are right, are the people creating the software. Much effort has been wasted on arguing and bullying programmers into picking tools other people prefer.

## Building
The makefile requires `gcc`, `ccache` and `valgrind` to do its thing.

```
git clone https://github.com/codr7/hacktical-c.git
cd hacktical-c
mkdir build
make
```

## Platforms
Since Unix is all about C, and Linux is currently the best supported Unix out there; Linux is the platform I would recommend for writing C. Just having access to `valgrind` is priceless. Microsoft has unfortunately chosen to neglect C for a long time, its compilers dragging far behind the rest of the pack. Windows does however offer a way of running Linux in the form of WSL2, which works very well from my experience.

## Extensions
The code in this book uses several GNU extensions that are not yet in the C standard. Cleanup attributes, multi-line expressions and nested functions specifically.

Except for nested functions, extensions used in the code should work just as well in `clang`.

I can think of one feature, `hc_defer()`, which would currently be absolutely impossible to do without extensions. In other cases, alternative solutions are simply less convenient.

## Benchmarks
Some chapters come with benchmarks, `make build/benchmark` builds and runs all of them.

## Chapters
The content is arranged to form a natural progression, where later chapters build on concepts that have already been introduced. That being said; feel free to skip around, just be prepared to backtrack to fill in blanks.

An `ePUB`-book may be built by following these [instructions](./epub/README.md).

- [Macros](https://github.com/codr7/hacktical-c/tree/main/macro)
- [Fixed-Point Arithmetic](https://github.com/codr7/hacktical-c/tree/main/fix)
- [Intrusive Doubly Linked Lists](https://github.com/codr7/hacktical-c/tree/main/list)
- [Lightweight Concurrent Tasks](https://github.com/codr7/hacktical-c/tree/main/task)
- [Composable Memory Allocators - Part 1](https://github.com/codr7/hacktical-c/tree/main/malloc1)
- [Vectors](https://github.com/codr7/hacktical-c/tree/main/vector)
- [Exceptions](https://github.com/codr7/hacktical-c/tree/main/error)
- [Ordered Sets and Maps](https://github.com/codr7/hacktical-c/tree/main/set)
- [Composable Memory Allocators - Part 2](https://github.com/codr7/hacktical-c/tree/main/malloc2)
- [Dynamic Compilation](https://github.com/codr7/hacktical-c/tree/main/dynamic)
- [Extensible Streams - Part 1](https://github.com/codr7/hacktical-c/tree/main/stream1)
- [Structured Logs](https://github.com/codr7/hacktical-c/tree/main/slog)

