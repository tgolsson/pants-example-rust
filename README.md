# Example repo for using Rust with Pants

Like most Rust programs, this requires a native C/C++ toolchain for `as`, `ar`, `cc`, `ld`, and the
like. Rust is provided by the plugin and will not interact with your host install of Rustup in any way.

To get started:

``` term
pants package ::
dist/axum-server/axum-server &
dist/client/client http://localhost:3000
```
