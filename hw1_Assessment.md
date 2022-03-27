### Assessment for HW1

Run on February 14, 18:51:12 PM.

+ Pass: Change into directory "hws/hw1".

+ Pass: Check that file "hw1.ml" exists.

+ Fail: Check that an OCaml file "hw1.ml" has no syntax or type errors.

    OCaml file hw1.ml has errors.

    Run "ocaml hw1.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

+  _48.9_ / _57_ : Pass: 

#### Problem 1

+  _6_ / _8_ : Pass: Problem 1: type checking

    -0.5 For part 5, the problem is that the two branches of the if are of different types; one is anint while the other is a string. -0.5 For part 6, the issue is NOT that there is no else clause. In the absence of an else clause, OCaml implicitly treats the else part as (). The problem is therefore that the two branches of the if don't have matching types, as they are int and unit, respectively. -1 Part 8 is actually well-typed, and evaluates to a tuple containing a function and the string "hello".

#### Total score: _6_ / _8_

#### Problem 2

+  _5_ / _5_ : Pass: Problem 2: syntax checking

    Looks good

#### Total score: _5_ / _5_

#### Problem 3

+ Pass: Check that the result of evaluating
   ```
   gcd 3 3
   ```
   matches the pattern `3`.


+ Pass: Check that the result of evaluating
   ```
   gcd 8 4
   ```
   matches the pattern `4`.


+ Pass: Check that the result of evaluating
   ```
   gcd 8 6
   ```
   matches the pattern `2`.


+ Pass: Check that the result of evaluating
   ```
   gcd 13 7
   ```
   matches the pattern `1`.


+  _3_ / _5_ : Pass: Problem 3: gcd

    Doesn't use required algorithm stated in homework writeup.

#### Total score: _3_ / _5_

#### Problem 4

+ Pass: Check that the result of evaluating
   ```
   reduced_form (1,3)
   ```
   matches the pattern `(1,3)`.


+ Pass: Check that the result of evaluating
   ```
   reduced_form (29,29)
   ```
   matches the pattern `(1,1)`.


+ Pass: Check that the result of evaluating
   ```
   reduced_form (26, 34)
   ```
   matches the pattern `(13,17)`.


+ Pass: Check that the result of evaluating
   ```
   reduced_form (74,37)
   ```
   matches the pattern `(2,1)`.


+ Pass: Check that the result of evaluating
   ```
   reduced_form (3928, 7484)
   ```
   matches the pattern `(982,1871)`.


+  _0_ / _0.5_ : Pass: reduced_form: Comments 

    no mention that the integers must be positive

+  _2.5_ / _2.5_ : Pass: reduced_form: Correctness

    good

+  _2_ / _2.0_ : Pass: reduced_form: Quality and Structure

    good

#### Total score: _4.5_ / _5.0_

#### Problem 5

###### Comments

+  _0.5_ / _0.5_ : Pass: Comments

    

###### Boundary Cases

+ Pass: Check that the result of evaluating
   ```
   fromMtoN 2021 2041
   ```
   matches the pattern `[]`.


+ Pass: Check that the result of evaluating
   ```
   fromMtoN 2041 2041
   ```
   matches the pattern `[2041]`.


+ Pass: Check that the result of evaluating
   ```
   fromMtoN 2042 2041
   ```
   matches the pattern `[2042; 2041]`.


+  _2_ / _2.0_ : Pass: Boundary Cases

    

###### Correctness (ignore boundary in case of failure)

+ Pass: Check that the result of evaluating
   ```
   fromMtoN 89 87
   ```
   matches the pattern `[89; 88; 87]`.


+ Pass: Check that the result of evaluating
   ```
   fromMtoN 89 86
   ```
   matches the pattern `[89; 88; 87; 86]`.


+ Pass: Check that the result of evaluating
   ```
   fromMtoN 89 85
   ```
   matches the pattern `[89; 88; 87; 86; 85]`.


+ Pass: Check that the result of evaluating
   ```
   fromMtoN 89 84
   ```
   matches the pattern `[89; 88; 87; 86; 85; 84]`.


+ Pass: Check that the result of evaluating
   ```
   fromMtoN 89 78
   ```
   matches the pattern `[89; 88; 87; 86; 85; 84; 83; 82; 81; 80; 79; 78]`.


+  _1.5_ / _1.5_ : Pass: Correctness

    

###### Quality and Structure

+  _1_ / _1.0_ : Pass: Quality and Structure

    

#### Total score: _5_ / _5.0_

#### Problem 6

###### Comments

+  _0.5_ / _0.5_ : Pass: Comments

    

###### Boundary Cases

+ Pass: Check that the result of evaluating
   ```
   everyOdd []
   ```
   matches the pattern `[]`.


+ Pass: Check that the result of evaluating
   ```
   everyOdd [1;2]
   ```
   matches the pattern `[1]`.


+ Pass: Check that the result of evaluating
   ```
   everyOdd [1;2;3]
   ```
   matches the pattern `[1;3]`.


+  _1.5_ / _1.5_ : Pass: Boundary Cases

    

###### Correctness (ignore boundary in case of failure)

+ Pass: Check that the result of evaluating
   ```
   everyOdd [41; 42; 43; 44]
   ```
   matches the pattern `[41; 43]`.


+ Pass: Check that the result of evaluating
   ```
   everyOdd [41; 42; 43; 44; 45]
   ```
   matches the pattern `[41; 43; 45]`.


+ Pass: Check that the result of evaluating
   ```
   everyOdd [true; false; true; false; true]
   ```
   matches the pattern `[true; true; true]`.


+  _2_ / _2.0_ : Pass: Correctness

    

###### Quality and Structure

+  _0.5_ / _1.0_ : Pass: Quality and Structure

    third case isn't needed

#### Total score: _4.5_ / _5.0_

#### Problem 7

###### Comments

+  _0.4_ / _0.5_ : Pass: Comments

    the result list should be a list of every nth element in the original list

###### Boundary Cases

+ Pass: Check that the result of evaluating
   ```
   everyNth [] 1
   ```
   matches the pattern `[]`.


+ Pass: Check that the result of evaluating
   ```
   everyNth [1] 4
   ```
   matches the pattern `[]`.


+ Pass: Check that the result of evaluating
   ```
   everyNth [1;2;3;4] 2
   ```
   matches the pattern `[2;4]`.


+  _1.5_ / _1.5_ : Pass: Boundary Cases

    good job

###### Correctness (ignore boundary in case of failure)

+ Pass: Check that the result of evaluating
   ```
   everyNth [41; 42; 43; 44; 45; 46; 47; 48; 49] 1
   ```
   matches the pattern `[41; 42; 43; 44; 45; 46; 47; 48; 49]`.


+ Pass: Check that the result of evaluating
   ```
   everyNth [41; 42; 43; 44; 45; 46; 47; 48; 49] 2
   ```
   matches the pattern `[42; 44; 46; 48]`.


+ Pass: Check that the result of evaluating
   ```
   everyNth [false; false; false; true; false; false; false; true; false] 4
   ```
   matches the pattern `[true; true]`.


+  _2_ / _2.0_ : Pass: Correctness

    good job

###### Quality and Structure

+  _1_ / _1.0_ : Pass: Quality and Structure

    good job

###### `everyThird`

+  _1_ / _1.0_ : Pass: everyThird

    good job

#### Total score: _5.9_ / _6.0_

#### Problem 8

+ Pass: Check that the result of evaluating
   ```
   find_salary [("John", "651-418-3456", 50.1) ; ("Jane", "763-222-1234", 107.3) ; ("Joan", "unlisted", 12.7)] "Jane"
   ```
   matches the pattern `107.3`.


+ Pass: Check that the result of evaluating
   ```
   find_phno [("John", "651-418-3456", 50.1) ; ("Jane", "763-222-1234", 107.3) ; ("Joan", "unlisted", 12.7)] "Jane"
   ```
   matches the pattern `"763-222-1234"`.


+ Pass: Check that the result of evaluating
   ```
   find_salary [("John", "651-418-3456", 50.1) ; ("Jane", "763-222-1234", 107.3) ; ("Joan", "unlisted", 12.7)] "John"
   ```
   matches the pattern `50.1`.


+ Pass: Check that the result of evaluating
   ```
   find_phno [("John", "651-418-3456", 50.1) ; ("Jane", "763-222-1234", 107.3) ; ("Joan", "unlisted", 12.7)] "John"
   ```
   matches the pattern `"651-418-3456"`.


+  _7_ / _8_ : Pass: Problem 8: find_salary

    No comments for base case for find_phno and find_salary as per specified in the problem (-1)

#### Total score: _7_ / _8_

#### Problem 9

+ Fail: Check that the result of evaluating
   ```
   is_matrix []
   ```
   matches the pattern `false`.

   Your solution evaluated incorrectly and produced some part of the following:
`- : bool = true
`

+ Fail: Check that the result of evaluating
   ```
   is_matrix [[]]
   ```
   matches the pattern `false`.

   Your solution evaluated incorrectly and produced some part of the following:
`- : bool = true
`

+ Fail: Check that the result of evaluating
   ```
   is_matrix [[];[]]
   ```
   matches the pattern `false`.

   Your solution evaluated incorrectly and produced some part of the following:
`- : bool = true
`

+ Pass: Check that the result of evaluating
   ```
   is_matrix [[3;2;1];[6;5;4];[2;3]]
   ```
   matches the pattern `false`.


+ Pass: Check that the result of evaluating
   ```
   is_matrix [[3;2];[6;5];[];[]]
   ```
   matches the pattern `false`.


+ Pass: Check that the result of evaluating
   ```
   is_matrix [[1;2;3;4;5];[6;7;8;9;10]]
   ```
   matches the pattern `true`.


+ Pass: Check that the result of evaluating
   ```
   is_matrix [[1]]
   ```
   matches the pattern `true`.


+ Pass: Check that the result of evaluating
   ```
   is_matrix [[2;3];[3;4];[5;6]]
   ```
   matches the pattern `true`.


+ Fail: Check that the result of evaluating
   ```
   matrix_scalar_multiply [[1;2];[2;3];[3;4]] 3
   ```
   matches the pattern `[[3;6];[6;9];[9;12]]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-23:
  (matrix_scalar_multiply [[1;2];[2;3];[3;4]] 3) = ([[3;6];[6;9];[9;12]]) ;; ;;
   ^^^^^^^^^^^^^^^^^^^^^^
Error: Unbound value matrix_scalar_multiply

```


+ Fail: Check that the result of evaluating
   ```
   matrix_scalar_multiply [[1;2;3];[6;7;8]] 1
   ```
   matches the pattern `[[1;2;3];[6;7;8]]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-23:
  (matrix_scalar_multiply [[1;2;3];[6;7;8]] 1) = ([[1;2;3];[6;7;8]]) ;; ;;
   ^^^^^^^^^^^^^^^^^^^^^^
Error: Unbound value matrix_scalar_multiply

```


+  _2_ / _3_ : Pass: Part 1: matrix representation

    not noting that a matrix needs to have at least one row and at least one column.

+  _4_ / _4_ : Pass: Part 2: is_matrix

    

+  _2_ / _3_ : Pass: Part 3: matrix_scalar_multiply

    matrix_scalar_mutiply takes 2 args causing it to fail our tests. Small mismatch of variables in help function.

#### Total score: _8_ / _10_

#### Total score: _48.9_ / _57_

