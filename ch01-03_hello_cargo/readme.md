# Description

This project uses Cargo, [Rust’s](https://www.rust-lang.org/) build system and package manager. It handles a lot of tasks for you, such as building your code, downloading the libraries your code depends on, and building those libraries. (We call the libraries that your code needs dependencies.)

## Creating a project with Cargo

Cargo generates two files and one directory for us: a Cargo.toml file and a src directory with a main.rs file inside.

It also initializes a new Git repository along with a `.gitignore` file. Git files won’t be generated if you run `cargo new` within an existing Git repository; you can override this behavior by using `cargo new --vcs=git`.

To create a new project, run the following command:

```bash
cargo new hello_cargo
cd hello_cargo
```
