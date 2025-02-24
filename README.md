# Unsafe Rust: Direct Pointer Manipulation on Vec
This repository demonstrates a common error in Rust when working with raw pointers and vectors. The `bug.rs` file contains code that directly manipulates a vector's raw pointer using unsafe code.  Modifying the memory location via the raw pointer bypasses Rust's safety mechanisms, leading to undefined behavior and potential crashes.  The `bugSolution.rs` provides a safe and correct way to modify vector elements.

## How to reproduce
1. Clone this repository.
2. Navigate to the repository's directory.
3. Compile and run `bug.rs` using `rustc bug.rs && ./bug`.
4. Observe the unexpected and potentially erratic output.
5. Compile and run `bugSolution.rs` using `rustc bugSolution.rs && ./bugSolution` for the correct approach.

## Lesson Learned
Avoid directly manipulating vector's raw pointers. Rust's built-in methods provide safe and efficient ways to modify vector elements. Using unsafe operations should be reserved only when absolutely necessary and with a thorough understanding of the potential risks.