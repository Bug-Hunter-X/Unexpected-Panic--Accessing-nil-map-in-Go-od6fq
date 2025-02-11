# Unexpected Panic: Accessing a nil map in Go

This repository demonstrates a common error in Go: attempting to access a value from an uninitialized map, which results in a runtime panic.  The `bug.go` file shows the problematic code, while `bugSolution.go` provides a solution.

## Problem

In Go, maps are reference types.  If you declare a map but don't initialize it, it's `nil`.  Attempting to access an element from a `nil` map will cause a runtime panic.

## Solution

The solution involves checking if the map is `nil` before attempting to access its elements.  This can be done using an `if` statement or the comma ok idiom.

## How to run the code

1. Clone the repository.
2. Navigate to the repository's directory.
3. Run `go run bug.go` to see the panic.
4. Run `go run bugSolution.go` to see the corrected version.