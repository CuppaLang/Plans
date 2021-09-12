# Casting
Casting, in this language will mean _converting_ an object of one type to another type; not _asserting_

### Casting an object

```
a = 9
print(a.getClass()) // int
print(a + "8") // error because you cannot add a string to an integer
b = <String>a
print(b.getClass()) // string
print(b + "8") // 98
```

### Casting functions
You'll have to create a function for each type you want your type to be castable to

```
// MyClass
cast String {
  return JSON.toJson(this)
}
```
```
// somewhere else
print(myObj.getClass()) // MyClass
print((<String>myObj).getClass()) // String
```
