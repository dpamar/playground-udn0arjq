# Welcome!

Welcome to this new playground about the BF language. Make sure you already read 
* [Getting started with BrainFuck](https://tech.io/playgrounds/50426/getting-started-with-brainfuck/welcome)
* [BrainFuck part 2 - Working with arrays](https://tech.io/playgrounds/50443/brainfuck-part-2---working-with-arrays/welcome)
* [BrainFuck part 3 - Write a BF interpreter in BF](https://www.codingame.com/playgrounds/50446/brainfuck-part-3---write-a-bf-interpreter-in-bf/welcome)
* [BrainFuck part 4 - Advanced maths](https://www.codingame.com/playgrounds/50446/brainfuck-part-3---write-a-bf-interpreter-in-bf/welcome)
* [BrainFuck part 5 - Math sequences](https://www.codingame.com/playgrounds/50478/brainfuck-part-5---math-sequences/welcome)
* [BrainFuck part 6 - 16-bit integers](https://www.codingame.com/playgrounds/50482/brainfuck-part-6---16-bit-integers/be-smart)
* [BrainFuck part 7 - Quine (+ some non-BF quine theory)](https://www.codingame.com/playgrounds/50485/brainfuck-part-7---quine-some-non-bf-quine-theory/welcome)

playgrounds if you didn't already !

The goal of this playground is to create our own _multi quine_ using BF, and other languages.

Previous playground is mandatory in order to understand this one...

# So, multiquine ?

A multiquine over a set S of Turing-complete languages is set of programs, one for each language in S, that
* prints itself when called without any parameter
* prints the version of language X when called with parameter X

Wow.

So, this means we are going to write a BF quine, that will, let's say
* prints itself when called without any parameter (a regular quine)
* prints a C# source code when called with parameter CS
* prints a JS source code when called with parameter JS

The C# source code
* prints itself when called without any parameter (a regular quine)
* prints previous JS source code when called with parameter JS
* prints previous BF source code when called with parameter BF

The JS source code
* prints itself when called without any parameter (a regular quine)
* prints previous BF source code when called with parameter BF
* prints previous C# source code when called with parameter CS

Easy, right ?

_Note:_ having the same parameter values for all languages is not mandatory (but more fun ^^)
