# Example 6: If/Else

Branching with `if` and `else` in Go is straight-forward. Here’s a basic example.
```go
if 7 % 2 == 0 {
    fmt.Println("7 is even")
} else {
    fmt.Println("7 is odd")
}
```
You can have an if statement without an else.
```go
if 8 % 4 == 0 {
        fmt.Println("8 is divisible by 4")
    }
```
A statement can precede conditionals; any variables declared in this statement are available in all branches.
```go
if num := 9; num < 0 {
    fmt.Println(num, "is negative")
} else if num < 10 {
    fmt.Println(num, "has 1 digit")
} else {
    fmt.Println(num, "has multiple digits")
}
```
You can also continue to the next iteration of the loop.
```go
for n := 0; n <= 5; n++ {
    if n%2 == 0 {
        continue
    }
    fmt.Println(n)
}
```
Note that you don’t need parentheses around conditions in Go, but that the braces are required. There is not ternary if (short-hand conditional statement) in Go, so you’ll need to use a full if statement even for basic conditions.

Source code is shown in [`if-else.go`](https://github.com/luangtatipsy/go-by-example/blob/main/06-if-else/if-else.go). After execute `go run if-else.go`. The outputs are shown below
```
7 is odd
8 is divisible by 4
9 has 1 digit
```