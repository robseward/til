# MIXINS/COMPOSITION

You can add functionality to a class by extending protocols. It's a way of composing classes as an alternative to class inheritance.

```swift
protocol Foo {
    func doSomething()
}

extension Foo {
    func doSomething(){
        print("Hello!")
    }
}

class Bar: Foo {
}

Bar().doSomething()  // "Hello!"
```
