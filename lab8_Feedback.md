### Feedback for Lab 08

Run on March 27, 15:39:38 PM.

#### Preliminary Checks

+ Pass: Change into directory "labs/lab08".

+ Pass: Check that file "lab08.ml" exists.

+ Fail: Check that an OCaml file "lab08.ml" has no syntax or type errors.

    OCaml file lab08.ml has errors.

    Run "ocaml lab08.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

#### Test Cases

##### Problem 1

###### `processWord`

+ Skip: Check that the result of evaluating
    ```ocaml
    processWord [] "ocaml"
    ```
    matches the pattern `[("ocaml", 1)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    processWord [("ocaml", 1)] "ocaml"
    ```
    matches the pattern `[("ocaml", 2)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    processWord [("java", 1)] "ocaml"
    ```
    matches the pattern `[("java", 1); ("ocaml", 1)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    processWord [("java", 1); ("ocaml", 1)] "ocaml"
    ```
    matches the pattern `[("java", 1); ("ocaml", 2)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    processWord [("java", 1); ("rust", 1)] "ocaml"
    ```
    matches the pattern `[("java", 1); ("ocaml", 1); ("rust", 1)]`

  This test was not run because of an earlier failing test.

###### `processOneList`

+ Skip: Check that the result of evaluating
    ```ocaml
    processOneList []
    ```
    matches the pattern `[]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    processOneList ["ocaml"]
    ```
    matches the pattern `[("ocaml", 1)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    processOneList ["ocaml"; "java"; "ocaml"]
    ```
    matches the pattern `[("java", 1); ("ocaml", 2)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    processOneList ["ocaml"; "java"; "ocaml"; "perl"]
    ```
    matches the pattern `[("java", 1); ("ocaml", 2); ("perl", 1)]`

  This test was not run because of an earlier failing test.

###### `assimilateWordCount`

+ Skip: Check that the result of evaluating
    ```ocaml
    assimilateWordCount [] ("ocaml", 2041)
    ```
    matches the pattern `[("ocaml", 2041)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    assimilateWordCount [("ocaml", 1)] ("ocaml", 2041)
    ```
    matches the pattern `[("ocaml", 2042)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    assimilateWordCount [("java", 1)] ("ocaml", 2041)
    ```
    matches the pattern `[("java", 1); ("ocaml", 2041)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    assimilateWordCount [("java", 1); ("ocaml", 1)] ("ocaml", 2041)
    ```
    matches the pattern `[("java", 1); ("ocaml", 2042)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    assimilateWordCount [("java", 1); ("prolog", 1)] ("ocaml", 2041)
    ```
    matches the pattern `[("java", 1); ("ocaml", 2041); ("prolog", 1)]`

  This test was not run because of an earlier failing test.

###### `assimilateWCList`

+ Skip: Check that the result of evaluating
    ```ocaml
    assimilateWCList [] []
    ```
    matches the pattern `[]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    assimilateWCList [] [("java", 1); ("ocaml", 2041); ("prolog", 1)]
    ```
    matches the pattern `[("java", 1); ("ocaml", 2041); ("prolog", 1)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    assimilateWCList [("java", 1); ("ocaml", 2041); ("prolog", 1)] [("java", 1); ("ocaml", 2041); ("prolog", 1)]
    ```
    matches the pattern `[("java", 2); ("ocaml", 4082); ("prolog", 2)]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    assimilateWCList [("java", 1);("ocaml", 2041);("prolog", 1)] [("c", 1113); ("python", 1133)]
    ```
    matches the pattern `[("c", 1113); ("java", 1); ("ocaml", 2041); ("prolog", 1); ("python", 1133)]`

  This test was not run because of an earlier failing test.

##### Problem 2

+ Skip: Check that the result of evaluating
    ```ocaml
    let empty = Empty in
   let bst_empty = { data = empty; lss = (<) } in
   (insert 2041 bst_empty).data
    ```
    matches the pattern `Node(2041, Empty, Empty)`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    let st = Node(2, Node(1, Empty, Empty), Node(3, Empty, Empty)) in
   let bst_st = { data = st; lss = (<) } in
   (insert 2041 bst_st).data
    ```
    matches the pattern `Node(2, Node(1, Empty, Empty), Node(3, Empty, Node(2041, Empty, Empty)))`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    let t = Node(8,
        Node(3, Node(1, Empty, Empty), Node(6, Node(4, Empty, Empty), Node(7, Empty, Empty))),
        Node(10, Empty, Node(14, Node(13, Empty, Empty), Empty))) in
   let bst_t = { data = t; lss = (<) } in
   (insert 2041 bst_t).data
    ```
    matches the pattern
    ```ocaml
    Node(8,
        Node(3, Node(1, Empty, Empty), Node(6, Node(4, Empty, Empty), Node(7, Empty, Empty))),
        Node(10, Empty, Node(14, Node(13, Empty, Empty), Node(2041, Empty, Empty))))
    ```

  This test was not run because of an earlier failing test.

##### Problem 3

+ Skip: Check that the result of evaluating
    ```ocaml
    cont_append [1;2;3;4] [5;6] (fun x -> x)
    ```
    matches the pattern `[1;2;3;4;5;6]`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    cont_append ['a'; 'b'; 'c'] ['d';'e'] (List.rev)
    ```
    matches the pattern `['e';'d';'c';'b';'a']`

  This test was not run because of an earlier failing test.

##### Problem 4

+ Skip: Check that the result of evaluating
    ```ocaml
    fib 7
    ```
    matches the pattern `13`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    fib 1
    ```
    matches the pattern `1`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    fib 13
    ```
    matches the pattern `233`

  This test was not run because of an earlier failing test.

