# Example 12: Functions

_Functions_ are central in Go. We’ll learn about functions with a few different examples. Here’s a function that takes two ints and returns their sum as an int.

```go
func plus(a int, b int) int{
    return a + b
}
```
Go requires explicit returns, i.e. it won’t automatically return the value of the last expression. When you have multiple consecutive parameters of the same type, you may omit the type name for the like-typed parameters up to the final parameter that declares the type.
```go
func plusPlus(a, b, c int) int{
    return a + b + c
}
```
Call a function just as you’d expect, with `name(args)`.
```go
plus(1, 2)
```
There are several other features to Go functions. One is multiple return values, which we’ll look at next.

Source code is shown in [`functions.go`](https://github.com/luangtatipsy/go-by-example/blob/main/12-functions/functions.go). After execute `go run functions.go`. The outputs are shown below
```
1 + 2 = 3
1 + 2 + 3 = 6
```