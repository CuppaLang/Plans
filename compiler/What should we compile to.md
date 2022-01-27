# What should we compile to?

This file holds my current knowledge of compilers and my reasonings for the methods

## Compiling to machine code
This seems like the best choice, but I currently lack the knowledge to actually do this, especially for making it portable

* I did manage to get a machine code program running in C++ but how the operations work is still magic to me:
They somehow have overloads with different amounts of parameters while also not having anything to separate them
* I dont' know how to package this machine code into executables for any platform

## Compiling to assembly
We can also compile to assembly and use a third party compiler to compile that into machine code,
but then we also need to compile that to an executable ourselves or with another tihrd party compilers and thats a lot of third party compilers

* Assembly is easy
* We either need to compile this assembly ourselves or use a third party compiler
* We will *still* need to somehow turn the machine code into an executable somehow just like with machine code



Currently, as there hasn't been much work on the language yet, it's probably fine to compile it to soemthing inneficent like a JSON of [nodes](compiler/CompilerNodes.md)
with our own runtime
