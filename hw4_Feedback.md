### Feedback for Homework 4

Run on March 27, 20:21:04 PM.

+ Pass: Change into directory "hws/hw4".

#### Problem 1

+ Pass: Check that file "prob1.ml" exists.

+ Fail: Check that an OCaml file "prob1.ml" has no syntax or type errors.

    OCaml file prob1.ml has errors.

    Run "ocaml prob1.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

##### Test Cases

+ Skip: Check that the result of evaluating
    ```ocaml
    makePairLists "a" ["b"; "c"]
    ```
    matches the pattern `[(("a", "b"), ["b"; "c"]); (("a", "c"), ["b"; "c"])]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    makeAllPairLists [("a",["b";"c"]);("b", ["c";"d"])]
    ```
    matches the pattern `[[(("a", "b"), ["b"; "c"]); (("a", "c"), ["b"; "c"])]; [(("b", "c"), ["c"; "d"]); (("b", "d"), ["c"; "d"])]]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    intersect ["a"; "b"] ["b"; "c"]
    ```
    matches the pattern `["b"]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    addOnePair (("a", "b"), ["c"; "d"]) [(("a", "b"), ["b"; "c"]); (("a", "c"), ["b"; "c"])]
    ```
    matches the pattern `[(("a", "b"), ["c"]); (("a", "c"), ["b"; "c"])]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    addAllPairs [(("a", "b"), ["c"; "d"]); (("a", "b"), ["d"; "e"])] [(("a", "b"), ["b"; "c"; "d"]); (("a", "c"), ["b"; "c"])]
    ```
    matches the pattern `[(("a", "b"), ["d"]); (("a", "c"), ["b"; "c"])]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    commonFriends [("a", ["b"; "c"]); ("b", ["c"; "d"])]
    ```
    matches the pattern `[(("b", "c"), ["c"; "d"]); (("b", "d"), ["c"; "d"]); (("a", "b"), ["b"; "c"]); (("a", "c"), ["b"; "c"])]`

  This test was not run because of an earlier failing test.

#### Problem 2

+ Pass: Check that file "prob2.ml" exists.

+ Fail: Check that an OCaml file "prob2.ml" has no syntax or type errors.

    OCaml file prob2.ml has errors.

    Run "ocaml prob2.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

##### Test Cases

+ Skip: Abstract test class.

  This test was not run because of an earlier failing test.

+ Skip: Abstract test class.

  This test was not run because of an earlier failing test.

#### Problem 3

+ Pass: Check that file "prob3.ml" exists.

+ Pass: Check that an OCaml file "prob3.ml" has no syntax or type errors.

    OCaml file "prob3.ml" has no syntax or type errors.



##### Test Cases

+ Pass: Check that the result of evaluating
    ```ocaml
    cont_reverse  ["!"; "1"; "@"; "a"] (fun x -> x)
    ```
    matches the pattern `["a"; "@"; "1"; "!"]`

+ Pass: Check that the result of evaluating
    ```ocaml
    cont_sumTree (Node (3, Node (1, Empty, Node (2,Empty,Empty)), Node (4,Empty,Empty))) (fun x -> x + 1)
    ```
    matches the pattern `11`

#### Problem 4

+ Pass: Check that file "prob4.ml" exists.

+ Fail: Check that an OCaml file "prob4.ml" has no syntax or type errors.

    OCaml file prob4.ml has errors.

    Run "ocaml prob4.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

##### Test Cases

+ Skip: Check that the result of evaluating
    ```ocaml
    dostat (fun x -> x < 10) (fun y -> y + 1) 0
    ```
    matches the pattern `10`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    sumup (0,0,3)
    ```
    matches the pattern `(3, 6, 3)`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    sumToN 10
    ```
    matches the pattern `55`

  This test was not run because of an earlier failing test.

