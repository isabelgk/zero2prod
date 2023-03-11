# Zero to Production in Rust


## Tools

### Cargo watch

```
cargo install cargo-watch
```

Use like
```
cargo watch -x check
# or, with chaining:
cargo watch -x check -x test -x run
```


### Cargo tarpaulin (code coverage)

Currently only supported on x86_64 Linux
```
cargo install cargo-tarpaulin
# compute code coverage for application code, ignoring test functions
cargo tarpaulin --ignore-tests
```


### Clippy (linting)

```
rustup component add clippy
cargo clippy
```

To fail on linter checks:
```
cargo clippy -- -D warnings
```

To mute a warning, use `#[allow(clippy::lint_name)]` or add to `clippy.toml`.


### rustfmt (formatting)

```
rustup component add rustfmt
cargo fmt                # formats whole project
cargo fmt -- --check     # fails when something isn't formatted
```

### Cargo audit (security vulnerabilities)

```
cargo install cargo-audit
cargo audit
```