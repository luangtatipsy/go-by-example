# Example 7: If/Else

In go `switch` statements express conditionals across many branches. Here’s a basic `switch`.

```go
i := 2
switch i {
case 1:
    fmt.Println("one")
case 2:
    fmt.Println("two")
case 3:
    fmt.Println("three")
}
```
You can use commas to separate multiple expressions in the same case statement. We use the optional default case in this example as well.
```go
switch time.Now().Weekday() {
case time.Saturday, time.Sunday:
    fmt.Println("It's the weekend")
default:
    fmt.Println("It's a weekday")
}
```
`switch` without an expression is an alternate way to express if/else logic. Here we also show how the case expressions can be non-constants.
```go
t := time.Now()
switch {
case t.Hour() < 12:
    fmt.Println("It's before noon")
default:
    fmt.Println("It's after noon")
}
```
A type `switch` compares types instead of values. You can use this to discover the type of an interface value. In this example, the variable `t` will have the type corresponding to its clause.
```go
whatAmI := func(i interface{}) {
    switch t := i.(type) {
    case bool:
        fmt.Println("I'm a bool")
    case int:
        fmt.Println("I'm an int")
    default:
        fmt.Printf("Don't know type %T\n", t)
    }
}
whatAmI(true)
whatAmI(1)
whatAmI("hey")
```

Source code is shown in [`switch.go`](https://github.com/luangtatipsy/go-by-example/blob/main/07-switch/switch.go). After execute `go run switch.go`. The outputs are shown below
```
7 is odd
8 is divisible by 4
9 has 1 digit
```
