# Description

This project uses Cargo, [Rust’s](https://www.rust-lang.org/) build system and package manager. It handles a lot of tasks for you, such as building your code, downloading the libraries your code depends on, and building those libraries. (We call the libraries that your code needs dependencies.)

## Commands

| Command                 | Description                                                                          |
| ----------------------- | ------------------------------------------------------------------------------------ |
| `cargo build`           | compile the code and creates an executable.                                          |
| `cargo run`             | compile the code and then run the resulting executable all in one command.           |
| `cargo check`           | quickly checks your code to make sure it compiles but doesn’t produce an executable. |
| `cargo build --release` | build and compile an optimized version of the code for production.                   |

## Creating a project with Cargo

Cargo generates two files and one directory for us: a Cargo.toml file and a src directory with a main.rs file inside.

It also initializes a new Git repository along with a `.gitignore` file. Git files won’t be generated if you run `cargo new` within an existing Git repository; you can override this behavior by using `cargo new --vcs=git`.

To create a new project, run the following command:

```bash
cargo new hello_cargo
cd hello_cargo
```

## Building a project with Cargo

To build a Rust project with Cargo, run `cargo build` from the root of the project (`hello_cargo`).

```bash
cargo build
  Compiling hello_cargo v0.1.0 (file:///projects/hello_cargo)
    Finished dev [unoptimized + debuginfo] target(s) in 2.85 secs
```

This command creates an executable file in `target/debug/hello_cargo` rather than in your current directory. You can run the executable with this command:

```bash
./target/debug/hello_cargo # or .\target\debug\hello_cargo.exe on Windows
Hello, world!
```

we can also use `cargo run` to compile the code and then run the resulting executable all in one command:

```bash
cargo run
    Finished dev [unoptimized + debuginfo] target(s) in 0.0 secs
     Running `target/debug/hello_cargo`
Hello, world!
```

Running cargo build for the first time also causes Cargo to create a new file at the top level: `Cargo.lock`. This file keeps track of the exact versions of dependencies in your project.

Cargo also provides a command called `cargo check`. This command quickly checks your code to make sure it compiles but doesn’t produce an executable.

## Additional notes

- In Cargo, packages are known as `crates`
- [Cargo docs](https://doc.rust-lang.org/cargo/)
- The `target` directory generate by cargo build can be ignored in the `.gitignore` file since it is auto-generated.
