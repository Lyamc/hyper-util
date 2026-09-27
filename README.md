# hyper-util

This is a fork of `hyper-util` 0.1.21, kept for [cabin](https://github.com/Lyamc/cabin). GPUI's HTTP client enables the `client-legacy` feature. Upstream turns on the `libc` crate for that feature because of one call, `if_nametoindex`, used only on Apple and Solaris. This fork declares that function directly and takes `c_char` from `std::ffi`, so `client-legacy` no longer depends on `libc`. The rest of the crate is unchanged.

[![crates.io](https://img.shields.io/crates/v/hyper-util.svg)](https://crates.io/crates/hyper-util)
[![Released API docs](https://docs.rs/hyper-util/badge.svg)](https://docs.rs/hyper-util)
[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

A collection of utilities to do common things with [hyper](https://hyper.rs).

## License

This project is licensed under the [MIT license](./LICENSE).
