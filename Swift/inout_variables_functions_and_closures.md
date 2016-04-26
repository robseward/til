`inout` variables have a shadow copy created of them that is passed back to the original
======

If you pass an `inout` variable into a function, then reference it in a closure, the closure creates a copy of it and then passes it back to the original when the function returns. In the following case this happens before the closure is executed, so the original is not modified when the closure is executed.

```swift
func foo(inout success: Bool) -> (()->()) {
    return { _ in
        success = true
        print (success)
    }
}

var success = false
let closure = foo(&success)

closure()          //prints "true"
print(success)     //prints "false"
```

Wrapping the variable in a class so it is passed by reference is one solution.

-----
Further reading:
http://stackoverflow.com/questions/36851616/swift-closure-capture-and-inout-variables/36852385#36852385
