 # Internal flag
 Cuppa lang will not have visibility modifiers, allowing doing weird things without some kind of reflection
 
 However we *do* need something to tell people that this variable or function should usually not be used, that is what the **internal** flag is for
 
 ```
 internal fun getRequest(String path): Any {
  return /* Some kind of request library here */.get("api.longwebsitenameorsomething.com/${path}")
 }
 
 fun getDownloads() = getRequest("downloads") // internal functions can be used like normal functions in the class they are in
 ```

```
// (in some other function in another class)

api.getRequest("downloads") // will error

api.getDownloads() // will not error

api.internal.getRequest("downloads") // will not error
```
