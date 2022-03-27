### Feedback for Homework 1

Run on February 07, 20:21:57 PM.

#### Preliminary Checks

+ Pass: Change into directory "hws/hw1".

+ Pass: Check that file "hw1.ml" exists.

+ Fail: Check that an OCaml file "hw1.ml" has no syntax or type errors.

    OCaml file hw1.ml has errors.

    Run "ocaml hw1.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

#### Test Cases

##### Problem 3

+ Skip: Check that the result of evaluating
   ```
   gcd 3 3
   ```
   matches the pattern `3`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   gcd 8 4
   ```
   matches the pattern `4`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   gcd 8 6
   ```
   matches the pattern `2`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   gcd 13 7
   ```
   matches the pattern `1`.


  This test was not run because of an earlier failing test.

##### Problem 4

+ Skip: Check that the result of evaluating
   ```
   reduced_form (1, 3)
   ```
   matches the pattern `(1, 3)`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   reduced_form (3, 3)
   ```
   matches the pattern `(1, 1)`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   reduced_form (26, 34)
   ```
   matches the pattern `(13, 17)`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   reduced_form (4, 12)
   ```
   matches the pattern `(1, 3)`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   reduced_form (4, 2)
   ```
   matches the pattern `(2, 1)`.


  This test was not run because of an earlier failing test.

##### Problem 5

+ Skip: Check that the result of evaluating
   ```
   fromMtoN 3 7
   ```
   matches the pattern `[]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   fromMtoN 3 3
   ```
   matches the pattern `[3]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   fromMtoN 7 3
   ```
   matches the pattern `[7; 6; 5; 4; 3]`.


  This test was not run because of an earlier failing test.

##### Problem 6

+ Skip: Check that the result of evaluating
   ```
   everyOdd []
   ```
   matches the pattern `[]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   everyOdd [1; 2; 3; 4]
   ```
   matches the pattern `[1; 3]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   everyOdd [1; 2; 3]
   ```
   matches the pattern `[1; 3]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   everyOdd ["a"; "string"; "list"; "is"; "also"; "okay"]
   ```
   matches the pattern `["a"; "list"; "also"]`.


  This test was not run because of an earlier failing test.

##### Problem 7

+ Skip: Check that the result of evaluating
   ```
   everyNth [1;2;3;4] 1
   ```
   matches the pattern `[1; 2; 3; 4]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   everyNth [1;2;3;4] 2
   ```
   matches the pattern `[2; 4]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   everyNth [1;2;3;4] 3
   ```
   matches the pattern `[3]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   everyNth [1;2;3;4] 5
   ```
   matches the pattern `[]`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   everyThird [1;2;3;4]
   ```
   matches the pattern `[3]`.


  This test was not run because of an earlier failing test.

##### Problem 8

+ Skip: Check that the result of evaluating
   ```
   find_salary [("John", "651-418-3456", 50.1) ; ("Jane", "763-222-1234", 107.3) ; ("Joan", "unlisted", 12.7)] "Jane"
   ```
   matches the pattern `107.3`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   find_phno [("John", "651-418-3456", 50.1) ; ("Jane", "763-222-1234", 107.3) ; ("Joan", "unlisted", 12.7)] "Jane"
   ```
   matches the pattern `"763-222-1234"`.


  This test was not run because of an earlier failing test.

##### Problem 9

+ Skip: Check that the result of evaluating
   ```
   is_matrix [[3]; [1]]
   ```
   matches the pattern `true`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   is_matrix [[2;0]; [4;1]]
   ```
   matches the pattern `true`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   matrix_scalar_multiply [ [3; 17; 32]; [2; 10; 4]; [7; 5; 9] ] 5
   ```
   matches the pattern `[[15; 85; 160]; [10; 50; 20]; [35; 25; 45]]`.


  This test was not run because of an earlier failing test.

