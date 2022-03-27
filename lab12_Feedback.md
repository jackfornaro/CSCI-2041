### Feedback for Lab 12

Run on April 24, 14:50:39 PM.

#### Preliminary Checks

+ Pass: Change into directory "labs/lab12".

+ Pass: Check that file "lab12.ml" exists.

+ Fail: Check that an OCaml file "lab12.ml" has no syntax or type errors.

    OCaml file lab12.ml has errors.

    Run "ocaml lab12.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

#### Test Cases

##### Problem 2

###### Part 1

+ Skip: Check that the result of evaluating
    ```ocaml
    IntItem.leq(3,5)
    ```
    matches the pattern `true`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    IntItem.leq(5,4)
    ```
    matches the pattern `false`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    StringItem.leq("malfurion", "garrosh")
    ```
    matches the pattern `false`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    StringItem.leq("jaina", "jaina")
    ```
    matches the pattern `true`

  This test was not run because of an earlier failing test.

###### Part 2

+ Skip: Check that the result of evaluating
    ```ocaml
    IntHeap.size (IntHeap.initHeap 4)
    ```
    matches the pattern `15`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    IntHeap.maxHeap (IntHeap.initHeap 4)
    ```
    matches the pattern `0`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    StringHeap.maxHeap (let (i, sh) = StringHeap.replace("string", StringHeap.initHeap 3) in sh)
    ```
    matches the pattern `"string"`

  This test was not run because of an earlier failing test.

