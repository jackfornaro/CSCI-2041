### Feedback for Lab 05

Run on February 20, 22:51:21 PM.

#### Preliminary Checks

+ Pass: Change into directory "labs/lab05".

+ Pass: Check that file "lab05.ml" exists.

+ Fail: Check that an OCaml file "lab05.ml" has warnings.

    OCaml file lab05.ml has warnings.

    Run "ocaml lab05.ml" to see them.



+ Skip: Check that an OCaml file "lab05.ml" has no syntax or type errors.

  This test was not run because of an earlier failing test.

#### Test Cases

##### Problem 1

###### Part 1

+ Skip: Check that the result of evaluating
   ```
   maxTree Empty
   ```
   matches the pattern `None`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   maxTree 
  (Node (5,
        Node (3,
          Node (1,Empty,Empty),
          Node (4,Empty,Empty)
        ),
        Node (8,
          Node (7,
            Node (6,Empty,Empty),
            Empty
          ),
          Node (9,
            Empty,
            Node(10,Empty, Empty)
          )
        )
      )
  )
   ```
   matches the pattern `Some 10`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   maxTree 
  (Node (8,
        Node (3,
          Node (1,
            Node ((-1), Empty,Empty),
            Empty
          ),
          Node (6,
            Node (4, Empty, Empty),
            Node (7, Empty, Empty)
          )
        ),
        Node (10,
          Empty,
          Node (14,
            Node (13,Empty,Empty),
            Empty
          )
        )
      )
  )
   ```
   matches the pattern `Some 14`.


  This test was not run because of an earlier failing test.

###### Part 2

+ Skip: Check that the result of evaluating
   ```
   minTree Empty
   ```
   matches the pattern `None`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   minTree 
  (Node (5,
        Node (3,
          Node (1,Empty,Empty),
          Node (4,Empty,Empty)
        ),
        Node (8,
          Node (7,
            Node (6,Empty,Empty),
            Empty
          ),
          Node (9,
            Empty,
            Node(10,Empty, Empty)
          )
        )
      )
  )
   ```
   matches the pattern `Some 1`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   minTree 
  (Node (8,
        Node (3,
          Node (1,
            Node ((-1), Empty,Empty),
            Empty
          ),
          Node (6,
            Node (4, Empty, Empty),
            Node (7, Empty, Empty)
          )
        ),
        Node (10,
          Empty,
          Node (14,
            Node (13,Empty,Empty),
            Empty
          )
        )
      )
  )
   ```
   matches the pattern `Some (-1)`.


  This test was not run because of an earlier failing test.

##### Problem 2

###### Part 1

+ Skip: Check that the result of evaluating
   ```
   typeof (Cond (True,Int 5, Int 7))
   ```
   matches the pattern `Some IntTy`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   typeof (And (Lss (Int 5,Int 7), Gtr (Int 3, Plus (Int 2,Int 5))))
   ```
   matches the pattern `Some BoolTy`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   typeof (Cond (Int 5, Int 5, Int 7))
   ```
   matches the pattern `None`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   typeof (Cond (True, Int 5, False))
   ```
   matches the pattern `None`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   typeof (And (True, Int 5))
   ```
   matches the pattern `None`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   typeof (Cond (Lss (Int 10, Plus (Int 5, Int 7)), Int 5, Int 7))
   ```
   matches the pattern `Some IntTy`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   typeof (Cond (Lss (Int 10, Plus (Int 5, Int 7)), Int 5, True))
   ```
   matches the pattern `None`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   typeof (Cond (And (Lss (Int 10, Plus (Int 5, Int 7)), True), False, True))
   ```
   matches the pattern `Some BoolTy`.


  This test was not run because of an earlier failing test.

###### Part 2

+ Skip: Check that the result of evaluating
   ```
   wellTyped (Cond (True,Int 5, Int 7))
   ```
   matches the pattern `true`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   wellTyped (And (Lss (Int 5,Int 7), Gtr (Int 3, Plus (Int 2,Int 5))))
   ```
   matches the pattern `true`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   wellTyped (Cond (Int 5, Int 5, Int 7))
   ```
   matches the pattern `false`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   wellTyped (Cond (True, Int 5, False))
   ```
   matches the pattern `false`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   wellTyped (And (True, Int 5))
   ```
   matches the pattern `false`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   wellTyped (Cond (Lss (Int 10, Plus (Int 5, Int 7)), Int 5, Int 7))
   ```
   matches the pattern `true`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   wellTyped (Cond (Lss (Int 10, Plus (Int 5, Int 7)), Int 5, True))
   ```
   matches the pattern `false`.


  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
   ```
   wellTyped (Cond (And (Lss (Int 10, Plus (Int 5, Int 7)), True), False, True))
   ```
   matches the pattern `true`.


  This test was not run because of an earlier failing test.

