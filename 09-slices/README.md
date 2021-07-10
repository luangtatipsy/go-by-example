# Example 9: Slices

Slices are a key data type in Go, giving a more powerful interface to sequences than arrays. Unlike arrays, slices are typed only by the elements they contain (not the number of elements). To create an empty slice with non-zero length, use the builtin make. Here we make a slice of strings of length 3 (initially zero-valued).
```go
s := make([]string, 3)
```
We can set and get just like with arrays.
```go
s[0] = "a"
s[1] = "b"
s[2] = "c"
```
len returns the length of the slice as expected.
```go
```
In addition to these basic operations, slices support several more that make them richer than arrays. One is the builtin append, which returns a slice containing one or more new values. Note that we need to accept a return value from append as we may get a new slice value.
```go
s = append(s, "d")
s = append(s, "e", "f")
```
Slices can also be copy’d. Here we create an empty slice c of the same length as s and copy into c from s.
```go
c := make([]string, len(s))
copy(c, s)
```
Slices support a “slice” operator with the syntax slice[low:high]. For example, this gets a slice of the elements s[2], s[3], and s[4].
```go
l := s[2:5]
```
This slices up to (but excluding) s[5].
```go
l = s[:5]
```
And this slices up from (and including) s[2].
```go
l = s[2:]
```
We can declare and initialize a variable for slice in a single line as well.
```go
t := []string{"g", "h", "i"}
```
Slices can be composed into multi-dimensional data structures. The length of the inner slices can vary, unlike with multi-dimensional arrays.
```go
twoD := make([][]int, 3)
for i := 0; i < 3; i++ {
    innerLen := i + 1
    twoD[i] = make([]int, innerLen)
    for j := 0; j < innerLen; j++ {
        twoD[i][j] = i + j
    }
}
```
Note that while slices are different types than arrays, they are rendered similarly by fmt.Println.

Source code is shown in [`slices.go`](https://github.com/luangtatipsy/go-by-example/blob/main/09-slices/slices.go). After execute `go run slices.go`. The outputs are shown below
```
emp: [  ]
set: [a b c]
get: c
len: 3
apd: [a b c d e f]
cpy: [a b c d e f]
sl1: [c d e]
sl2: [a b c d e]
sl3: [c d e f]
dcl: [g h i]
2d:  [[0] [1 2] [2 3 4]]
```