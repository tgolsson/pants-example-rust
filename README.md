# Example repo for using Rust with Pants

Like most Rust programs, this requires a native C/C++ toolchain for `as`, `ar`, `cc`, `ld`, and the
like. Rust is provided by the plugin and will not interact with your host install of Rustup in any way.

To get started:

``` term
$ pants package ::
12:05:15.27 [INFO] Initializing scheduler...
12:05:15.49 [INFO] Scheduler initialized.
12:05:15.67 [INFO] Wrote dist/axum-server/axum-server
12:05:15.67 [INFO] Wrote dist/client/client

$ dist/axum-server/axum-server &
[1] 15972
listening on 127.0.0.1:3000

$ dist/client/client http://localhost:3000
Fetching "http://localhost:3000"...
Response: HTTP/1.1 200 OK
Headers: {
    "content-type": "text/html; charset=utf-8",
    "content-length": "22",
    "date": "Sat, 28 Oct 2023 10:04:42 GMT",
}

<h1>Hello, World!</h1>
```
