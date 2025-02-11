# Go Race Condition Example

This repository demonstrates a common race condition in Go programs. When multiple goroutines access and modify shared variables concurrently without proper synchronization mechanisms (like mutexes or atomic operations), the final result might be incorrect.

The `bug.go` file shows a simple counter incremented by 1000 goroutines. Without proper synchronization, the final count will likely be less than 1000 due to race conditions.

The `bugSolution.go` file demonstrates a solution to this problem using a mutex to protect access to the shared `count` variable.  This ensures that only one goroutine can modify `count` at a time.