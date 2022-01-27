TODO: represent nodes as JSON instead of functions here

This file is the concept of how the compiler will look at programs

Let's take this snippet:
```
var myVar = 3 + 4
```
The compiler will compile that into something like this:
```
CreateNewVariable("myVar", Plus(Integer(3), Integer(4)))
```
This is the compiler's nodes represented as functions

Another example:
```
var myVar = myFunction("Hello world", str -> str.replace("world", "world!"))
```
Will be compiled to something like:
```
CreateNewVariable("myVar", RunFunction("myFunction", [String("Hello world"), 
  CreateFunction(null /* name */, 
    {"str": "String" /* parameters */}, 
    GetParameter("str").RunMethod("replace". [String("world"), String("world!")]) /* nodes to run */)
]))
```
Very complicated thanks to the lambda
