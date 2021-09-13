# Extensions

You should be able to add extension functions

```
extension String fun remove(String toRemove) = replace(toRemove, "")
```

Or if you want to define many extensions for one class:

```
extension String {
  fun remove(String toRemove) = replace(toRemove, "")
  fun remove(Regex toRemove) = replace(toRemove, "")
}
```

TODO: come up with something for extension properties?
TODO: add examples for calling the extension functions
