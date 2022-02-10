A concept of how our executables can be formatted (in bytecode)

Our executables can be zip-like and have these files:

# Byte classes

This file will use its own set of classes to make these formats more readable, here's a list:

### String
First contains how many bytes the string will take up, and then the actual bytes of the string

```
5 // length (unsigned varint)
72, 101, 108, 108, 111 // string bytes ("Hello")
```

# Qualifier index
Compiled Cuppa code can address object members by a number to save on bytes, so each executable will have an index mapping numbers to qualified member names

Example:
```
// entry start
1 // ordinal of a member type enum (method, property, class, etc...), 1 byte
com/example/project/Main:start // qualifier, of byte class String
// entry end
```

This is index should only be used for launching that executable, it is not an API index because that would break all dependants on some slight order changes
