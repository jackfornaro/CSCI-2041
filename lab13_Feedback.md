### Feedback for Lab 13

Run on April 30, 17:17:36 PM.

#### Preliminary Checks

+ Pass: Change into directory "labs/lab13".

+ Pass: Check that file "lab13.ml" exists.

+ Fail: Check that an OCaml file "lab13.ml" has no syntax or type errors.

    OCaml file lab13.ml has errors.

    Run "ocaml lab13.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

#### Test Cases

##### Problem 1

+ Skip: Check that the result of evaluating
    ```ocaml
    
    let ns = nextStream in
    let rec take s n = if n = 0 then [] else let (x, rst) = ns s in (x :: take rst (n - 1)) in
    let paired = zipStreams natStream natStream in
    take paired 5

    ```
    matches the pattern `[(0, 0); (1, 1); (2, 2); (3, 3); (4, 4)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    
    let ns = nextStream in
    let evenStream = let rec h n = mkStream (fun () -> (n, h (2 + n))) in h 0 in
    let oddStream = let rec h n = mkStream (fun () -> (n, h (2 + n))) in h 1 in
    let rec take s n = if n = 0 then [] else let (x, rst) = ns s in (x :: take rst (n - 1)) in
    let eos = zipStreams evenStream oddStream in
    take eos 5

    ```
    matches the pattern `[(0, 1); (2, 3); (4, 5); (6, 7); (8, 9)]`

  This test was not run because of an earlier failing test.

##### Problem 3

###### Part 1

+ Skip: Check that the result of evaluating
    ```ocaml
    is_RBTree_aux Empty
    ```
    matches the pattern `(0, true)`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    is_RBTree_aux (Node(B, 1, Empty, Empty))
    ```
    matches the pattern `(1, true)`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    is_RBTree_aux (Node(R, 1, Empty, Empty))
    ```
    matches the pattern `(0, true)`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    let irba = is_RBTree_aux in let (h, tf) = irba (Node(B, 1, Node(B, 2, Empty, Empty), Empty)) in tf
    ```
    matches the pattern `false`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    let irba = is_RBTree_aux in let (h, tf) = irba (Node(B, 1, Empty, Node(B, 2, Empty, Empty))) in tf
    ```
    matches the pattern `false`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    let irba = is_RBTree_aux in let (h, tf) = irba (Node(R, 1, Node(R, 3, Empty, Empty), Node(R, 2, Empty, Empty))) in tf
    ```
    matches the pattern `false`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    
    let irba = is_RBTree_aux in
    irba (Node (R, 5, Node(B, 3, Node(R, 1, Empty, Empty),
                                 Empty),
                      Node(B, 7, Empty, Empty)))
    ```
    matches the pattern `(1, true)`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    
    let irba = is_RBTree_aux in
    irba (Node (B, 5, Node(B, 3, Node(R, 1, Empty, Empty),
                                 Empty),
                      Node(B, 7, Empty, Empty)))
    ```
    matches the pattern `(2, true)`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    
    let irba = is_RBTree_aux in
    let (_, tf) = irba (Node (B, 5, Node(R, 3, Node(R, 1, Empty, Empty),
                                               Empty),
                                    Node(B, 7, Empty, Empty)))
    in tf
    ```
    matches the pattern `false`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    
    let irba = is_RBTree_aux in
    let (_, tf) = irba (Node (R, 5, Node(B, 3, Node(B, 1, Empty, Empty),
                                               Empty),
                                    Node(B, 7, Empty, Empty)))
    in tf
    ```
    matches the pattern `false`

  This test was not run because of an earlier failing test.

