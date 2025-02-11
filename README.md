# Off-by-One Error in Vector Iteration

This example demonstrates a common off-by-one error in C++ when iterating over a `std::vector`.  The loop condition `i <= vec.size()` is incorrect; it should be `i < vec.size()` to avoid accessing the element beyond the vector's bounds.

**Bug:** The original code attempts to access `vec[vec.size()]`, which is one element past the end of the vector, leading to undefined behavior (likely a crash or unexpected results).  This is a classic off-by-one error.

**Solution:** The corrected code uses `i < vec.size()` to ensure the loop iterates only within the valid range of indices.