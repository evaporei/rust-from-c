# rust-from-c

Code based of: https://doc.rust-lang.org/nomicon/ffi.html#calling-rust-code-from-c

To compile the C code:

```bash
gcc call_rust.c -o call_rust -lrust_from_c -L./target/debug
```

To run:

```bash
LD_LIBRARY_PATH=./target/debug ./call_rust
```

Simple [cbindgen](https://github.com/mozilla/cbindgen) header generation from Rust code:

```bash
cbindgen --config cbindgen.toml --crate rust-from-c --output call_rust.h --lang c
```
