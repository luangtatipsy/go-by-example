# Example 4: Constants

Go supports constants of character, string, boolean, and numeric values.

`const` declares a constant value.
```go
const s string = "constant"
```
A `const` statement can appear anywhere a `var` statement can.
```go
const n = 500000000
```
Constant expressions perform arithmetic with arbitrary precision. 
```go
const d = 3e20 / n
```
A numeric constant has no type until it’s given one, such as by an explicit conversion.
```go
int64(d)
```
A number can be given a type by using it in a context that requires one, such as a variable assignment or function call. For example, here math.Sin expects a float64.
```go
math.Sin(n)
```
Variables declared without a corresponding initialization are zero-valued. For example, the zero value for an int is 0.
```go
var e int
```

Source code is shown in [`constants.go`](https://github.com/luangtatipsy/go-by-example/blob/main/04-constants/constants.go). After execute `go run constants.go`. The outputs are shown below
```
constant
6e+11
600000000000
-0.28470407323754404
```