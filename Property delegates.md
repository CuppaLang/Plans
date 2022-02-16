Property delegates will allow the programmer to delegate a property's value through a custom method, removing the need to do things like ``object.property.get()`` (instead, ``object.property``) 

For a better description, see Kotlin's

Example:

```
class MyObj {
  // the string "Hello World!" will only be initialized on the first access of this property
  val myProperty = > lazy { "Hello World!" } < 
  // > ... < "packs" an object into the property
}

// .......

myObj.myProperty // = "Hello World!"

// you can also "unpack" properties

(< myObj.myProperty >) // = an instance of Lazy
(< myObj.myProperty >).get() // = "Hello World!"
```
