# Learn with Rustlings

Learn Rustlings, read rustc error code and then read a rust book. run a hint after done the task to see additional information.

- [Rustlings](https://github.com/rust-lang/rustlings)
- [Rust Compiler Error Index](https://doc.rust-lang.org/error-index.html)
- [Rust book](https://doc.rust-lang.org/stable/book/title-page.html)

## Command

```bash
rustlings watch
rustlings run myExercise1
rustlings verify
rustlings hint myExercise1
rustlings list
rustc --explain <CODE>
```

## Variables

- https://doc.rust-lang.org/stable/book/ch03-01-variables-and-mutability.html

- variables are immutable by default, define with `let` keyword.
- adding `mut` in front of the variable name to make them mutable.
- `const` is constants like immutable variables that are bound to a name and can't be change have to set a type.
- Constants are valid for the entire time a program runs.
- shadowing is a variable that you declare with the same name as previous variable. (first variable is shadowed by the second) - [Ref](https://doc.rust-lang.org/stable/book/ch03-01-variables-and-mutability.html#shadowing)
- scalar type represets a single value. (integer, float, char, boolean)
- integer type - unsigned and (start with `u`) signed integer (start wit `i`)
- default integer is `i32`
- hex `0xff`, binary `0b1111_0000`, Byte (u8 only) `b'A'`
- floating point numbers have `f32` and `f64` (32 bits and 64 bits in size) all are signed.
- floating point default is `f64` , `f32` is single-precision and `f64` has double precision.

#### `variables1.rs`

```rust
// error because it try to bound 5 to x mutable variable that did not exist.
x = 5;
```

#### `variables2.rs`

```rust
fn main() {
  let x = 1;
  if x == 10 {
    ...
```

- What if you give x a value? - ✅
- What if you do both? - ✅
- What type should x be, anyway? - integer
- What if x is the same type as 10? What if it's a different type? - interger passed otherwise `E0308`

#### `variables3.rs`

- variable bindings are immutable by default.
- use `mut` keyword. `E0384` - An immutable variable was reassigned.

#### `variables4.rs`

- `E0381` - possibly-uninitialized variable, we can't print out or not allowed to use an uninitialized variable.

#### `variables5.rs`

- use shadowing to reuse existing variable with different type.
- link : https://doc.rust-lang.org/book/ch03-01-variables-and-mutability.html#shadowing

#### `variables6.rs`

- `const` must declare a type
