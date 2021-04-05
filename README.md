# Rust Commands
Commands and other info for rust

## Install rust
Link: https://www.rust-lang.org/tools/install
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
In `zsh` shell, check the `$HOME/.zshenv` file to get the rust init command. It is something like `source "$HOME/.cargo/env"`

#### Check installed version
```
cargo --version
rustup --version
rustc --version
```
cargo - rust package manager
rustup - for upgrades
rustc - the compiler

#### Update Rust
```
rustup update
```

#### Uninstall
```
rustup self uninstall
```

## Compile
```
rustc program.rs
```

## Cargo commands
Init in current directory
```
cargo init
```
Create new directory and init
```
cargo new <new-directory>
```
