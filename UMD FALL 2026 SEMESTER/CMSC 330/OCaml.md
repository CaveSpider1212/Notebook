---
tags: CMSC_330
created: 2026-9-3
description: 9/3, 9/8 notes
---

### Functional Programming

> [!info] Functional Programming
> **Functional programming**: A programming paradigm based on functions
> 
> **Programming paradigm**: Classification of programming approach based behavior of code
> 
> Programming paradigm used interchangeably with language features.

Features of functional languages:
- Immutable state: Data cannot be modified after it is created
- Declarative programming: Describe what you want the program to accomplish instead of writing out the exact step-by-step instructions of how to achieve it
- Referential transparency: Any expression in the code can be replaced by its evaluated result without changing the program's overall behavior
- Realistic about the machine: Language acknowledging how physical hardware actually operates

> [!info] Program State
> **Program state**: State of the machine at any given time
> 
> Typically described as the contents of variables
> ```
> x = x + 1
> a[0] = 42
> ```

### OCaml

```
(* hello.ml *)
print_string "Hello world!\n"
```

```
ocamlc hello.ml
```

Compiling an OCaml file like above generates an executable `a.out` file, a compiled object (`.o`) file `hello.cmo`, and a compiled interface (like `.h`) file `hello.cmi`.

### Functions and Expressions

- Everything is an expression (e)
- Expressions evaluate to values (v)
- All values are expressions, but not all expressions are values
- Expressions have types (t)
- `e: t` means an expression has type `t`

```
(if e1:bool then e2:t else e3:t): t
```

> [!tip] `if` statements
> It is important that the `if` statements also have an `else` branch, otherwise there will be a syntax error.

Function definition syntax: `let f x1 ... xn = e` ^41d90f

- `f`: Function name
- `x1 ... xn`: All arguments
- `e`: Function body

Function calling syntax: `f x1 ... xn`

- Each argument `x` is evaluated to a value `v`
- Substitute all `x` in `e` with `v`
- Call the new expression `e'`
- Evaluate `e'` to value `v'`

Types in functions are *inferred* by the operations they use. They are represented as a list of types, starting from the type of the first argument, second argument, and so on, with the last type being the return type of the function.

```
let area l w = l * w
(* int -> int -> int *)
```

```
let f a b = a ^ b in f (* string -> string -> string *)
let f a b = a ^ b in f "hi" (* string -> string, since one of them was taken up by the argument *)
```

### Let Expressions

```
let x = e1 in e2
```

**Let expressions** bind local variables for `e2`, NOT the same as [[OCaml#^41d90f|let definitions]].

`e1` is the binding expression, and `e2` is the body expression, so the entire `let` expression evaluates to the result of `e2`.

> [!info] `in`
> The `in` keyword is used to define a local variable binding, or a local function. It restricts the scope of a variable so that it is only accessible in what comes after the `in` keyword.

Let expressions can be nested and used for local variables.

Variables in nested let expressions are overshadowed, meaning if the same variable is declared in an inner let expression that variable's value is used in the remaining expression (note that they are 2 different variables though).

```
let x = 3 in let y = 4 in x + y (* 7 *)
let x = 3 in let x = 4 in x (* 4 *)
let x = 3 in let z = 4 + x in let x = 1 in x + z (* 8 *)
```

### Lists and Pattern Matching

> [!info] Lists
> **Lists** are the basic data structure in OCaml.
> 
> ```
> [1; 2; 3; 4; 5]
> ```
> 
> Uses `;` as a separator, and bracket syntax.
> 
> There is no indexing, but has a head and a tail.
> 
> Homogenous: All elements must be the same data type

```
(* List creation *)
e1::e2::[]
```

`[]` means an empty list (nil)

`h` means "head", while `t` means tail

##### Pattern Matching

**Pattern matching** is the way to deconstruct any data structure in OCaml, using the `match` expression.

```
let x = 5
match x with
	0 -> 0
	|1 -> 1
	|3 -> 2
	|5 -> 3
	|_ -> 4 (*wildcard*)
```

A `match` expression takes in an expression or value and then checks to see if it has the same structure as any of the cases, and will perform the expression linked to the case if there is a match.

### Data Types

##### Tuples

> [!info] Tuples
> ```
> (1, 2)
> (* int * int *)
> ```
> 
> Surrounded by `()` and separated with commas.
> 
> Heterogenous: They can have different data types
> 
> Fixed size

Tuples have a type based on size, and can pattern match.

