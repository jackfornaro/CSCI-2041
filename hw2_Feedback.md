### Feedback for Homework 2

Run on May 04, 16:51:25 PM.

+ Pass: Change into directory "hws/hw2".

#### Problem 1

+ Pass: Check that file "prob1.ml" exists.

#### Problem 2

+ Pass: Check that file "prob2.ml" exists.

+ Fail: Check that an OCaml file "prob2.ml" has no syntax or type errors.

    OCaml file prob2.ml has errors.

    Run "ocaml prob2.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

##### Test Cases

+ Skip: Check that the result of evaluating
    ```ocaml
    fib 1
    ```
    matches the pattern `1`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    fib 2
    ```
    matches the pattern `1`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    fib 3
    ```
    matches the pattern `2`

  This test was not run because of an earlier failing test.

#### Problem 3

+ Pass: Check that file "prob3.ml" exists.

+ Fail: Check that an OCaml file "prob3.ml" has no syntax or type errors.

    OCaml file prob3.ml has errors.

    Run "ocaml prob3.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

##### Test Cases

+ Skip: Check that the result of evaluating
    ```ocaml
    find_phno [("name", "12345", 123.)] "not-found"
    ```
    matches the pattern `None`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    find_salary [("name", "12345", 123.)] "name"
    ```
    matches the pattern `Some 123.`

  This test was not run because of an earlier failing test.

#### Problem 4

+ Pass: Check that file "prob4.ml" exists.

+ Fail: Check that an OCaml file "prob4.ml" has no syntax or type errors.

    OCaml file prob4.ml has errors.

    Run "ocaml prob4.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

##### Test Cases

+ Skip: Abstract test class.

  This test was not run because of an earlier failing test.

#### Problem 5

+ Pass: Check that file "prob5.ml" exists.

+ Fail: Check that an OCaml file "prob5.ml" has no syntax or type errors.

    OCaml file prob5.ml has errors.

    Run "ocaml prob5.ml" to see them.

    Make sure that you are using ocaml version 4.05.  Run "ocaml -version" to check the version number.

##### Test Cases

###### Base Cases

+ Skip: Check that the result of evaluating
    ```ocaml
    typeof_aux (Id "x") [("x", IntTy)]
    ```
    matches the pattern `Some IntTy`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    typeof_aux (Id "x") [("x", BoolTy)]
    ```
    matches the pattern `Some BoolTy`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    typeof_aux (Int 2041) []
    ```
    matches the pattern `Some IntTy`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    typeof_aux (True) []
    ```
    matches the pattern `Some BoolTy`

  This test was not run because of an earlier failing test.

###### Advanced Cases

+ Skip: Check that the result of evaluating
    ```ocaml
    typeof (Let ("x",Int 5,Let ("y",Int 7,(Plus (Id "x", Id "y")))))
    ```
    matches the pattern `Some IntTy`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    typeof (Let ("x",Int 5,Let ("y",Int 7,(Lss (Id "x", Id "y")))))
    ```
    matches the pattern `Some BoolTy`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    typeof (Let ("x",True,Let ("y",False,(And (Id "x", Id "y")))))
    ```
    matches the pattern `Some BoolTy`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    typeof 
    (Fun ("x",
	        IntTy,
		  (Fun ("y",BoolTy,Cond(Id "y",
					Plus (Id "x",Int 1),
					Minus (Id "x", Int 5))))))
    
    ```
    matches the pattern `Some (FunTy (IntTy, FunTy (BoolTy, IntTy)))`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    typeof 
    (App (Fun ("x",IntTy,
		       App (Fun ("y",IntTy,
		 		    Plus (Id "x",Id "y")), Id "x")),
	        Int 5))
    
    ```
    matches the pattern `Some IntTy`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    typeof 
    (Cond (Lss (Int 10, Plus (Int 5, Int 7)),
		   Int 5, Int 7))
           
    ```
    matches the pattern `Some IntTy`

  This test was not run because of an earlier failing test.

#### Problem 6

+ Fail: Check that file "prob6.ml" exists.

     "prob6.ml" not found.

+ Skip: Check that an OCaml file "prob6.ml" has no syntax or type errors.

  This test was not run because of an earlier failing test.

##### Test Cases

+ Skip: Check that the result of evaluating
    ```ocaml
    eval (Id "x") [("x", True)]
    ```
    matches the pattern `True`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    eval (Int 3) []
    ```
    matches the pattern `Int 3`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    eval (Plus ((Int 5), (Int 3))) []
    ```
    matches the pattern `Int 8`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    eval (Times ((Int 5), (Int 3))) []
    ```
    matches the pattern `Int 15`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    eval (Gtr ((Int 2041), (Int 2021))) []
    ```
    matches the pattern `True`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    eval (And (False, True)) []
    ```
    matches the pattern `False`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    eval (Cond (True, (Int 2041), (Int 2021))) []
    ```
    matches the pattern `Int 2041`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    eval (Let ("no", Int 2021, Plus (Id "no", Int 20))) []
    ```
    matches the pattern `Int 2041`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    eval (Let ("x",(Int 5),Let ("y",(Int 7),Plus ((Id "x"),(Id "y"))))) []
    ```
    matches the pattern `Int 12`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    eval (Let ("x",True,Cond (Not (Id "x"),True,False))) []
    ```
    matches the pattern `False`

  This test was not run because of an earlier failing test.

+ Skip: Check that the result of evaluating
    ```ocaml
    eval (Let ("x",
               False,
               Cond (Not (Id "x"),
                     Let ("x", Int 5, Plus (Id "x", Int 3)),
                     Let ("y", Int 7, Id "y")))) []
    ```
    matches the pattern `Int 8`

  This test was not run because of an earlier failing test.

