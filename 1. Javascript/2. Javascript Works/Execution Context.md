# Execution Context

Code in JavaScript is `always run inside a type of execution context`. Execution context is simply `the environment within which your code is ran` and created when javascript engine sees `()`

There are 2 types of execution context in JavaScript

## 1. Global Execution Context

There are 2 phases

### Creation Phase

1. Global object is created (window in browser or global in NodeJS)
2. Initializes this keyword to global object

### Execution Phase

3. Memory space for variables and functions created
4. Initializes all variables to undefined and places them into memory with any new functions

## 2. Function Execution Context

`Only when a function is invoked`, does a function execution context get created

### Creation Phase

1. `Argument object created` with any arguments
2. `Initializes this keyword to point called` or `to the global object` if not specified

### Execution Phase

3. Memory space for variables and functions created
4. Initializes all variables to undefined and places them into memory with any new functions
