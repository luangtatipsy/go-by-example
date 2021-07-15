# Example 11: Range

range iterates over elements in a variety of data structures. Let’s see how to use range with some of the data structures we’ve already learned. Here we use range to sum the numbers in a slice. Arrays work like this too.
```go
nums := []int{2, 3, 4}
sum := 0
for _, num := range nums {
    sum += num
}
```
_range_ on arrays and slices provides both the index and value for each entry. Above we didn’t need the index, so we ignored it with the blank identifier _. Sometimes we actually want the indexes though.
```go
for i, num := range nums {
    if num == 3 {
        fmt.Println("index:", i)
    }
}
```
`range` on map iterates over key/value pairs.
```go
kvs := map[string]string{"a": "apple", "b": "banana"}
for k, v := range kvs {
    fmt.Printf("%s -> %s\n", k, v)
}
```
`range` can also iterate over just the keys of a map.
```go
for k := range kvs {
    fmt.Println("key:", k)
}
```
range on strings iterates over Unicode code points. The first value is the starting byte index of the rune and the second the rune itself.
```go
for i, c := range "go" {
    fmt.Println(i, c)
}
```

Source code is shown in [`range.go`](https://github.com/luangtatipsy/go-by-example/blob/main/11-range/range.go). After execute `go run range.go`. The outputs are shown below
```
sum: 9
index: 1
a -> apple
b -> banana
key: a
key: b
0 103
1 111
```