# gruid-js

[![pkg.go.dev](https://pkg.go.dev/badge/github.com/anaseto/gruid-js.svg)](https://pkg.go.dev/github.com/anaseto/gruid-js)
[![godocs.io](https://godocs.io/github.com/anaseto/gruid-js?status.svg)](https://godocs.io/github.com/anaseto/gruid-js)

The *gruid-js* module provides a [gruid](https://github.com/anaseto/gruid)
Driver for making wasm gruid applications that run in the browser. The module's
package is called js.

To build a browser application, you have to build it with the following
variables:

    GOOS=js GOARCH=wasm go build -o app.wasm /path/to/your/application

Then, you have to serve using an http server a directory containing the
app.wasm file along with an index.html file such as the basic example one in
[files/index.html](files/index.html) (the html page containing the canvas of
your application), and the `$(go env GOROOT)/misc/wasm/wasm_exec.js` file of
your Go distribution.
