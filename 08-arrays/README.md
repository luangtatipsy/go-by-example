# Example 8: Arrays

In Go, an _array_ is a numbered sequence of elements of a specific length. Here we create an array a that will hold exactly 5 ints. The type of elements and length are both part of the array’s type. By default an array is zero-valued, which for ints means 0s.
```go
var a [5]int
```
We can set a value at an index using the array[index] = value syntax, and get a value with array[index].
```go
a[4] = 100
```
The builtin len returns the length of an array.
```go
```
Use this syntax to declare and initialize an array in one line.
```go
b := [5]int{1, 2, 3, 4, 5}
```
Array types are one-dimensional, but you can compose types to build multi-dimensional data structures.
```go
var twoD [2][3]int
for i := 0; i < 2; i++ {
    for j := 0; j < 3; j++ {
        twoD[i][j] = i + j
    }
}
```
Note that arrays appear in the form [v1 v2 v3 ...] when printed with fmt.Println. You’ll see slices much more often than arrays in typical Go. We’ll look at slices next.

Source code is shown in [`arrays.go`](https://github.com/luangtatipsy/go-by-example/blob/main/08-arrays/arrays.go). After execute `go run arrays.go`. The outputs are shown below
```
emp: [0 0 0 0 0]
set: [0 0 0 0 100]
get: 100
len: 5
dcl: [1 2 3 4 5]
2d:  [[0 1 2] [1 2 3]]
```