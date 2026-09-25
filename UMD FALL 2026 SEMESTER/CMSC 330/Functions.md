---
tags: CMSC_330
created: 2026-9-17
description: 9/17 notes
---

### Higher Order Programming

> [!info] Anonymous Functions
> **Anonymous function**: Function not bound to a variable
> 
> ```
> fun x -> x + 3
> (* Syntax: fun x1 x2 ... xn -> e *)
> ```

Functions are expressions, and should be treated as such.

```
let add3 x = x + 3;;
(* can also say let add3 = fun x -> x + 3 *)

add3 5;; (* 8 *)
(* can also say (fun x -> x + 3) 5;; ----> 7 *)

let plus3 = add3;;
plus3 4;; (* 7 *)
```

Functions can be passed into other functions as arguments.

```
let apply_to_int f x = f x;;
(* ('a -> 'b) -> 'a -> 'b *)

let sub3 x = x - 3;;

apply_to_int sub3 4;; (* 1 *)
apply_to_int add3 4;; (* 7 *)
```

> [!tip]
> When we write a regular function, like `let f x y z = x + y * z`, OCaml sees it as a bunch of nested anonymous functions, like `let f = (fun x -> (fun y -> (fun z -> x + y * z)))`.

### Map and Fold

> [!info] Map
> A **map** takes in a function on a list, iterates through all elements in the list (considered the domain) and calls the function on them, and returns a new list of the corresponding output (called the co-domain).
> 
> ```
> let rec map f l = match l with
> [] -> []
> |h::t -> (f h)::(map f t)
> ```

> [!info] Fold
> A `fold` aggregates a list to a single value, going from left to right in the list.
> 
> ```
> let rec fold f a l = match l with
> |[] -> a
> |h::t -> f (f a h) t;;
> ```
> 
> `a` is the **accumulator**, a running value updated at each step of the field.
> 
> `f` is the function that takes in the current accumulator and the current element (or vice versa) and returns a new accumulator.
> 
> `l` is the list.
> 
> Reduces stack frames.

In `foldr`, the order of evaluation is reversed.

Fold left is tail-recursive, starts from the left, and is memory safe.

Fold right is not tail-recursive or memory safe and has a risk of stack overflow on large lists, and starts from the end.