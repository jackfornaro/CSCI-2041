### Feedback for Homework 3

Run on May 04, 16:54:16 PM.

+ Pass: Change into directory "hws/hw3".

#### Problem 1

+ Pass: Check that file "prob1.ml" exists.

+ Pass: Check that an OCaml file "prob1.ml" has no syntax or type errors.

    OCaml file "prob1.ml" has no syntax or type errors.



##### Test Cases

+ Pass: Check that the result of evaluating
    ```ocaml
    divide_list (fun x -> true) []
    ```
    matches the pattern `([], [])`

+ Fail: Check that the result of evaluating
    ```ocaml
    divide_list (fun x -> String.length x < 4) ["this"; "is"; "a"; "list"; "of"; "mixed"; "length"; "strings"]
    ```
    matches the pattern `(["is"; "a"; "of"], ["this"; "list"; "mixed"; "length"; "strings"])`
   Your solution evaluated incorrectly and produced some part of the following:

```
- : string list * string list =
(["of"; "a"; "is"], ["strings"; "length"; "mixed"; "list"; "this"])

```


+ Fail: Check that the result of evaluating
    ```ocaml
    divide_list  (fun x -> x mod 2 = 0) [1;3;6;8;9;10]
    ```
    matches the pattern `([6; 8; 10], [1; 3; 9])`
   Your solution evaluated incorrectly and produced some part of the following:
`- : int list * int list = ([10; 8; 6], [9; 3; 1])
`

#### Problem 2

+ Pass: Check that file "prob2.ml" exists.

+ Pass: Check that an OCaml file "prob2.ml" has no syntax or type errors.

    OCaml file "prob2.ml" has no syntax or type errors.



##### Test Cases

+ Pass: Check that the result of evaluating
    ```ocaml
    treemap (Node (4, Node (2, Empty, Empty), Node (5, Empty,Empty))) (fun x -> x + 3)
    ```
    matches the pattern `Node (7, Node (5, Empty, Empty), Node (8, Empty, Empty))`

+ Pass: Check that the result of evaluating
    ```ocaml
    treemap (Node (4, Node (2, Empty, Empty), Node (5, Empty,Empty))) (fun x -> (x mod 2 = 0))
    ```
    matches the pattern `Node (true, Node (true, Empty, Empty), Node (false, Empty, Empty))`

#### Problem 3

+ Pass: Check that file "prob3.ml" exists.

#### Problem 4

+ Pass: Check that file "prob4.ml" exists.

+ Pass: Check that an OCaml file "prob4.ml" has no syntax or type errors.

    OCaml file "prob4.ml" has no syntax or type errors.



##### Test Cases

+ Pass: Check that the result of evaluating
    ```ocaml
    append [] []
    ```
    matches the pattern `[]`

+ Pass: Check that the result of evaluating
    ```ocaml
    reverse []
    ```
    matches the pattern `[]`

+ Pass: Check that the result of evaluating
    ```ocaml
    filter (fun x -> true) []
    ```
    matches the pattern `[]`

+ Pass: Check that the result of evaluating
    ```ocaml
    append [] [1;2;3;4;5;6]
    ```
    matches the pattern `[1;2;3;4;5;6]`

+ Pass: Check that the result of evaluating
    ```ocaml
    reverse [1;2;3;4;5;6]
    ```
    matches the pattern `[6;5;4;3;2;1]`

+ Pass: Check that the result of evaluating
    ```ocaml
    filter (fun x -> x mod 2 = 1) [1;2;3;4;5;6]
    ```
    matches the pattern `[1;3;5]`

+ Pass: Check that the result of evaluating
    ```ocaml
    filter (fun x -> match x with [] _ -> true | _ -> false) [[]; []; [1]; []; [1;2;3]; [1;2;3;4]; []]
    ```
    matches the pattern `[[]; []; []; []]`

#### Problem 5

+ Pass: Check that file "prob5.ml" exists.

+ Fail: Check that an OCaml file "prob5.ml" has no syntax or type errors.

    OCaml file prob5.ml has errors.

    Run "ocaml prob5.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

##### Test Cases

###### `freeIn`

+ Skip: Check that the result of evaluating
    ```ocaml
    freeIn True "x"
    ```
    matches the pattern `false`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    freeIn (Id "x") "x"
    ```
    matches the pattern `true`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    freeIn (Plus (Id "x", Id "y")) "x"
    ```
    matches the pattern `true`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    freeIn (Plus (Id "x", Id "y")) "z"
    ```
    matches the pattern `false`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    freeIn (Let ("x", Id "x", Plus (Id "x", Id "y"))) "x"
    ```
    matches the pattern `true`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    freeIn (Let ("x", Id "z", Plus (Id "x", Id "y"))) "x"
    ```
    matches the pattern `false`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    freeIn (Fun ("x", Id "x")) "x"
    ```
    matches the pattern `false`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    freeIn (Fun ("y", Id "x")) "x"
    ```
    matches the pattern `true`

  This test was not run because of an earlier failing test.

###### `subst`

###### `base case`

+ Skip: Check that the result of evaluating
    ```ocaml
    subst True "x" (Int 0)
    ```
    matches the pattern `True`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Int 1) "x" (Int 0)
    ```
    matches the pattern `(Int 1)`

  This test was not run because of an earlier failing test.

###### `Id case`

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Id "x") "x" (Int 0)
    ```
    matches the pattern `(Int 0)`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Id "y") "x" (Int 0)
    ```
    matches the pattern `(Id "y")`

  This test was not run because of an earlier failing test.

###### `recursive case`

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Plus ((Id "x"), (Int 1))) "x" (Int 0)
    ```
    matches the pattern `(Plus ((Int 0), (Int 1)))`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Minus ((Id "x"), (Int 1))) "x" (Int 0)
    ```
    matches the pattern `(Minus ((Int 0), (Int 1)))`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Times ((Id "x"), (Int 1))) "x" (Int 0)
    ```
    matches the pattern `(Times ((Int 0), (Int 1)))`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Div ((Id "x"), (Int 1))) "x" (Int 0)
    ```
    matches the pattern `(Div ((Int 0), (Int 1)))`

  This test was not run because of an earlier failing test.

###### `Let case`

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Let ("x", Id "y", (Plus (Id "x", Id "z")))) "x" (Int 0)
    ```
    matches the pattern `(Let ("x", Id "y", (Plus (Id "x", Id "z"))))`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Let ("x", Id "x", (Plus (Id "x", Id "z")))) "x" (Int 0)
    ```
    matches the pattern `(Let ("x", (Int 0), (Plus (Id "x", Id "z"))))`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Let ("x", Id "y", (Plus (Id "x", Id "z")))) "z" (Plus (Id "x", Int 1))
    ```
    matches the pattern `(Let ("var1", Id "y", (Plus (Id "var1", Plus (Id "x", Int 1)))))`

  This test was not run because of an earlier failing test.

###### `Fun case`

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Fun ("x", (Plus (Id "x", Id "z")))) "x" (Int 0)
    ```
    matches the pattern `(Fun ("x", (Plus (Id "x", Id "z"))))`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Fun ("x", (Plus (Id "x", Id "z")))) "z" (Int 0)
    ```
    matches the pattern `(Fun ("x", (Plus (Id "x", Int 0))))`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    subst (Fun ("x", (Plus (Id "x", Id "z")))) "z" (Plus (Id "x", Int 1))
    ```
    matches the pattern `(Fun ("var1", (Plus (Id "var1", Plus (Id "x", Int 1)))))`

  This test was not run because of an earlier failing test.

