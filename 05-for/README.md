# Example 5: For Loop

`for` is Go’s only looping construct. Here are some basic types of for loops.

The most basic type, with a single condition.
```go
i := 1
for i <= 3 {
    fmt.Println(i)
    i = i + 1
}
```
A classic initial/condition/after for loop.
```go
for j := 7; j <= 9; j++ {
    fmt.Println(j)
}
```
for without a condition will loop repeatedly until you break out of the loop or return from the enclosing function.
```go
for {
    fmt.Println("loop")
    break
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

Source code is shown in [`for.go`](https://github.com/luangtatipsy/go-by-example/blob/main/05-for/for.go). After execute `go run for.go`. The outputs are shown below
```
1
2
3
7
8
9
loop
1
3
5
```