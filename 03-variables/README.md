# Example 3: Variables

In Go, variables are explicitly declared and used by the compiler to e.g. check type-correctness of function calls.

`var` declares 1 or more variables. 
```go
var a = "initial"
```
You can declare multiple variables at once.
```go
var b, c int = 1, 2
```
Go will infer the type of initialized variables.
```go
var d = true
```
Variables declared without a corresponding initialization are zero-valued. For example, the zero value for an int is 0.
```go
var e int
```

The := syntax is shorthand for declaring and initializing a variable, e.g. for `var f string = "apple"` in this case.
```go
f := "apple"
```

Source code is shown in [`variables.go`](https://github.com/luangtatipsy/go-by-example/blob/main/03-variables/variables.go). After execute `go run variables.go`. The outputs are shown below
```
initial
1 2
true
0
0
apple
```