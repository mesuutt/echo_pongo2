## echo pongo2 renderer

Use pongo2 templates in the [echo](https://github.com/labstack/echo) web framework

### Installation

```
go get github.com/mesuutt/echopongo2
```


### Usage
echopongo2 implements the echo [Renderer](http://godoc.org/github.com/labstack/echo#Renderer) interface

```go
e := echo.New()
r, err := echopongo2.NewRenderer("./template")
e.Renderer = r
```

Somewhere in a handler

```go
func Hello(c *echo.Context) error {
    data := map[string]string{"World":"mayowa"}
    return c.Render(http.StatusOK, "hello.html", data)
}
```
