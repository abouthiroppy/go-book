## install

Homebrewを使ってインストールする  
`brew install go`

```
$ brew install go
==> Downloading https://homebrew.bintray.com/bottles/go-1.4.2.yosemite.bottle.1.tar.gz
Already downloaded: /Library/Caches/Homebrew/go-1.4.2.yosemite.bottle.1.tar.gz
==> Pouring go-1.4.2.yosemite.bottle.1.tar.gz
==> Caveats
As of go 1.2, a valid GOPATH is required to use the `go get` command:
  https://golang.org/doc/code.html#GOPATH

You may wish to add the GOROOT-based install location to your PATH:
  export PATH=$PATH:/usr/local/opt/go/libexec/bin
==> Summary
🍺  /usr/local/Cellar/go/1.4.2: 4566 files, 155M
brew install go  2.03s user 2.24s system 92% cpu 4.630 total


```

## version

```
$ go version
go version go1.4.2 darwin/amd64
```

## Hello Word

`helloworld.go`
```
package main

import "fmt"

func main() {
    fmt.Printf("hello world\n")
}
```

---

```
$ go run helloworld.go
hello world
```
