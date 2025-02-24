# Rust Undefined Behavior Example

This repository demonstrates a common error in Rust leading to undefined behavior: directly manipulating a vector's contents using a raw pointer after modifying the vector's length or capacity. The original code attempts to change the first element, but since the vector's internals might be reallocated, this leads to memory safety issues. The solution provides a safer, idiomatic Rust approach.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's root directory.
3. Run `rustc bug.rs && ./bug`.
4. Observe the unexpected output, illustrating undefined behavior.
5. Then run `rustc bugSolution.rs && ./bugSolution` to see the safe and corrected version.