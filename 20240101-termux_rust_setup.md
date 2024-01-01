# Installing Rust on Termux

Date: 2024-01-01

## Basic Installation

Install rust with the following command.

```
pkg install rust -y
```

Check the version of the rust installation.

```
rustc --version
```

Your Rust compiler should be ready to be used. Create any simple "Hello World!" program.

**HelloWorld.rs**
```rust
fn
main() {
    println!("Hello World!");
}
```

Then compile the program.

```
rustc HelloWorld.rs
```

If successful you will find `./HelloWorld` which you can execute.

```
~ $ ./Hello World
Hello World!
```

## Troubleshooting

Depending on whether or not you have `rustup` installed you may run into issues when running `rustc`. You may see this error.

```
~ $ rustc
error: rustup could not choose a version of rustc to run, because one wasn't specified explicitly, and no default configured.
help: run 'rustup default stable' to download the latest stable release of Rust and set it as your default toolchain.
```

You will quickly notice that the triple `aarch64-linux-android` is not supported.

```
~ $ rustup default stable
info: syncing channel updates for 'stable-aarch64-linux-android'
info: latest update on 2023-12-28, rust version 1.75.0 (82e1608df 2023-12-21)
error: target 'aarch64-linux-android' not found in channel. Perhaps check https://doc.rust-lang.org/nightly/rustc/platform-support.html for available targets
```

The workaround I found is to delete the folder at `~/.cargo`.

```
rm -r ~/.cargo
```

After this you may restart your shell and try using `rustc` again.
