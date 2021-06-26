# Example 1: Hello World

Our first program will print the classic “hello world” message. Source code is shown in [`hello-world.go`](https://github.com/luangtatipsy/go-by-example/blob/main/01-hello-world/hello-world.go).

To run the program, put the code in `hello-world.go` and use `go run`.

```sh
go run hello-world.go
# hello world
```

Sometimes we’ll want to build our programs into binaries. We can do this using `go build`.
```sh
go build hello-world.go
```
`hello-world` has created at the current directory after executing the command above. We can then execute the built binary directly.

```sh
./hello-world
# hello world
```

Now that we can run and build basic Go programs, let’s learn more about the language.
