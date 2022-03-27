### Feedback for Lab 03

Run on February 06, 17:47:17 PM.

#### Preliminary Checks

+ Pass: Change into directory "labs/lab03".

+ Pass: Check that file "lab03.ml" exists.

+ Fail: Check that an OCaml file "lab03.ml" has warnings.

    OCaml file lab03.ml has warnings.

    Run "ocaml lab03.ml" to see them.



+ Skip: Check that an OCaml file "lab03.ml" has no syntax or type errors.

  This test was not run because of an earlier failing test.

#### Test Cases

##### Problem 1

+ Skip: Check that the result of evaluating
   ```
   sumup 0
   ```
   matches the pattern `0`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   sumup 6
   ```
   matches the pattern `21`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   sumup 11
   ```
   matches the pattern `66`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   sumup 2041
   ```
   matches the pattern `2083861`.


  This test was not run because of an earlier failing test.

##### Problem 2

+ Skip: Check that the result of evaluating
   ```
   flip_pair (1, 2)
   ```
   matches the pattern `(2, 1)`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   flip_pair ("andy", 500)
   ```
   matches the pattern `(500, "andy")`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   flip_pair ([41], ["20"])
   ```
   matches the pattern `(["20"], [41])`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   flip_list []
   ```
   matches the pattern `[]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   flip_list [("andy",500)]
   ```
   matches the pattern `[(500, "andy")]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   flip_list [("andy",500); ("mary",700)]
   ```
   matches the pattern `[(500, "andy"); (700, "mary")]`.


  This test was not run because of an earlier failing test.

##### Problem 3

+ Skip: Check that the result of evaluating
   ```
   destutter []
   ```
   matches the pattern `[]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   destutter [1]
   ```
   matches the pattern `[1]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   destutter [1; 2; 3]
   ```
   matches the pattern `[1; 2; 3]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   destutter [1; 2; 2; 3]
   ```
   matches the pattern `[1; 2; 3]`.


  This test was not run because of an earlier failing test.

##### Problem 4

+ Skip: Check that the result of evaluating
   ```
   sum_diffs []
   ```
   matches the pattern `0`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   sum_diffs [0]
   ```
   matches the pattern `0`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   sum_diffs [5]
   ```
   matches the pattern `0`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   sum_diffs [4; 5]
   ```
   matches the pattern `-1`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   sum_diffs [4; 5; 2]
   ```
   matches the pattern `2`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   sum_diffs [4; 5; 2; -2]
   ```
   matches the pattern `6`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   sum_diffs [4; 5; 2; -2; 0]
   ```
   matches the pattern `4`.


  This test was not run because of an earlier failing test.

##### Problem 5

+ Skip: Check that the result of evaluating
   ```
   unzip []
   ```
   matches the pattern `([], [])`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   unzip [(1,2)]
   ```
   matches the pattern `([1], [2])`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   unzip [(true, false); (true, false)]
   ```
   matches the pattern `([true; true], [false; false])`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   unzip [(1,2); (3,4); (5,6)]
   ```
   matches the pattern `([1; 3; 5], [2; 4; 6])`.


  This test was not run because of an earlier failing test.

##### Problem 6

+ Skip: Check that the result of evaluating
   ```
   f 20
   ```
   matches the pattern `13`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   f 41
   ```
   matches the pattern `25`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   f 51
   ```
   matches the pattern `32`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   f 61
   ```
   matches the pattern `38`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   m 20
   ```
   matches the pattern `12`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   m 41
   ```
   matches the pattern `25`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   m 51
   ```
   matches the pattern `32`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   m 61
   ```
   matches the pattern `38`.


  This test was not run because of an earlier failing test.

