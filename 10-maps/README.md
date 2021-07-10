# Example 10: Maps

Maps are Go’s built-in associative data type (sometimes called hashes or dicts in other languages). To create an empty map, use the builtin make: make(`map[key-type]val-type`). Set key/value pairs using typical name`[key]` = `val` syntax.
```go
m := make(map[string]int)
```
Set key/value pairs using typical name[key] = val syntax.
```go
m["k1"] = 7
m["k2"] = 13
```
Printing a map with e.g. fmt.Println will show all of its key/value pairs. This is how to get a value for a key with `name[key]`.
```go
v1 := m["k1"]
```
The builtin len returns the number of key/value pairs when called on a map.
```go
len(m)
```
The builtin delete removes key/value pairs from a map.
```go
delete(m, "k2")
```
The optional second return value when getting a value from a map indicates if the key was present in the map. This can be used to disambiguate between missing keys and keys with zero values like 0 or "". Here we didn’t need the value itself, so we ignored it with the _blank identifier_ _.
```go
_, prs := m["k2"]
```
You can also declare and initialize a new map in the same line with this syntax.
```go
n := map[string]int{"foo": 1, "bar": 2}
```
Note that maps appear in the form map[k:v k:v] when printed with fmt.Println.

Source code is shown in [`maps.go`](https://github.com/luangtatipsy/go-by-example/blob/main/10-maps/maps.go). After execute `go run maps.go`. The outputs are shown below
```
map: map[k1:7 k2:13]
v1:  7
len: 2
map: map[k1:7]
prs: false
map: map[bar:2 foo:1]
```