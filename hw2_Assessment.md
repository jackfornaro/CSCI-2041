### Assessment for HW2

Run on March 02, 08:13:30 AM.

+ Pass: Change into directory "hws/hw2".

+  _40.25_ / _83_ : Pass: 

#### Problem 1

+  _1_ / _3_ : Pass: Analysis of zip

    No analysis of how zip arrives at this type

+  _2_ / _3_ : Pass: Analysis of reverse

    Didn't analyze first match case or left side of second match case

#### Total score: _3_ / _6_

#### Problem 2

+  _3_ / _4_ : Pass: Definition of auxiliary fib'

    Your definition of fib' only has three arguments (x, fib1, fib2) but your recursive calls to fib' have 4 arguments

+  _1_ / _2_ : Pass: Comments before fib'

    More comments needed about precondition to fib'

+  _2_ / _2_ : Pass: Definition of fib

    Nice!

#### Total score: _6_ / _8_

#### Problem 3

+ Fail: Check that the result of evaluating
   ```
   find_phno [("NAME1", "111111", 111.);("NAME2", "222222", 222.);("NAME3", "333333", 333.);("NAME4", "444444", 444.)] "not-found"
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-10:
  (find_phno [("NAME1", "111111", 111.);("NAME2", "222222", 222.);("NAME3", "333333", 333.);("NAME4", "444444", 444.)] "not-found") = (None) ;; ;;
   ^^^^^^^^^
Error: Unbound value find_phno

```


+ Fail: Check that the result of evaluating
   ```
   find_phno [("NAME1", "111111", 111.);("NAME2", "222222", 222.);("NAME3", "333333", 333.);("NAME4", "444444", 444.)] "NAME3"
   ```
   matches the pattern `Some "333333"`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-10:
  (find_phno [("NAME1", "111111", 111.);("NAME2", "222222", 222.);("NAME3", "333333", 333.);("NAME4", "444444", 444.)] "NAME3") = (Some "333333") ;; ;;
   ^^^^^^^^^
Error: Unbound value find_phno

```


+ Fail: Check that the result of evaluating
   ```
   find_salary [("NAME1", "111111", 111.);("NAME2", "222222", 222.);("NAME3", "333333", 333.);("NAME4", "444444", 444.)] "not-found"
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-12:
  (find_salary [("NAME1", "111111", 111.);("NAME2", "222222", 222.);("NAME3", "333333", 333.);("NAME4", "444444", 444.)] "not-found") = (None) ;; ;;
   ^^^^^^^^^^^
Error: Unbound value find_salary

```


+ Fail: Check that the result of evaluating
   ```
   find_salary [("NAME1", "111111", 111.);("NAME2", "222222", 222.);("NAME3", "333333", 333.);("NAME4", "444444", 444.)] "NAME4"
   ```
   matches the pattern `Some 444.`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-12:
  (find_salary [("NAME1", "111111", 111.);("NAME2", "222222", 222.);("NAME3", "333333", 333.);("NAME4", "444444", 444.)] "NAME4") = (Some 444.) ;; ;;
   ^^^^^^^^^^^
Error: Unbound value find_salary

```


+  _2_ / _2_ : Pass: Explanation comment

    

+  _2_ / _2_ : Pass: find_salary explicit type

    

+  _1_ / _2_ : Pass: find_phno explicit type

    your code did not compile because of a syntax error. please run your code before submitting it ! ! ! ! ! ! ! ! ! !

#### Total score: _5_ / _6_

#### Problem 4

+  _4_ / _5_ : Pass: btree

    Your left/right nodes should be ('a,'b) btree, not ('a * 'b) btree

+  _1_ / _1.0_ : Pass: inittree

    Good

+  _4_ / _4.0_ : Pass: tree1 and tree2

    Good

+ Fail: Evaluating the following expression
   ```
   let bt1 = inittree
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 10-18:
  let bt1 = inittree;; ;;
            ^^^^^^^^
Error: Unbound value inittree

```


+ Fail: Evaluating the following expression
   ```
   let bt1 = insert bt1 3 "a"
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 10-16:
  let bt1 = insert bt1 3 "a";; ;;
            ^^^^^^
Error: Unbound value insert

```


+ Fail: Evaluating the following expression
   ```
   let bt1 = insert bt1 1 "b"
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 10-16:
  let bt1 = insert bt1 1 "b";; ;;
            ^^^^^^
Error: Unbound value insert

```


+ Fail: Evaluating the following expression
   ```
   let bt1 = insert bt1 1 "z"
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 10-16:
  let bt1 = insert bt1 1 "z";; ;;
            ^^^^^^
Error: Unbound value insert

```


+ Fail: Evaluating the following expression
   ```
   let bt1 = insert bt1 0 "x"
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 10-16:
  let bt1 = insert bt1 0 "x";; ;;
            ^^^^^^
Error: Unbound value insert

```


+ Fail: Evaluating the following expression
   ```
   let bt1 = insert bt1 2 "y"
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 10-16:
  let bt1 = insert bt1 2 "y";; ;;
            ^^^^^^
Error: Unbound value insert

```


+ Fail: Evaluating the following expression
   ```
   let bt2 = insert (insert (insert (insert (insert (insert bt1 6 "c") 4 "d") 7 "e") 15 "f") 12 "g") 13 "h"
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 10-16:
  let bt2 = insert (insert (insert (insert (insert (insert bt1 6 "c") 4 "d") 7 "e") 15 "f") 12 "g") 13 "h";; ;;
            ^^^^^^
Error: Unbound value insert

```


+ Fail: Evaluating the following expression
   ```
   let bt2 = insert (insert (insert (insert (insert (insert bt2 14 "i") 20 "j") 18 "k") 23 "l") 24 "m") 19 "n"
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 10-16:
  let bt2 = insert (insert (insert (insert (insert (insert bt2 14 "i") 20 "j") 18 "k") 23 "l") 24 "m") 19 "n";; ;;
            ^^^^^^
Error: Unbound value insert

```


+ Fail: Check that the result of evaluating
   ```
   keylist bt2
   ```
   matches the pattern `[0;1;2;3;4;6;7;12;13;14;15;18;19;20;23;24]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-8:
  (keylist bt2) = ([0;1;2;3;4;6;7;12;13;14;15;18;19;20;23;24]) ;; ;;
   ^^^^^^^
Error: Unbound value keylist

```


+  _5_ / _5.0_ : Pass: insert

    Logic looks correct

+ Fail: Check that the result of evaluating
   ```
   find bt2 3
   ```
   matches the pattern `Some "a"`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (find bt2 3) = (Some "a") ;; ;;
   ^^^^
Error: Unbound value find

```


+ Fail: Check that the result of evaluating
   ```
   find bt2 20
   ```
   matches the pattern `Some "j"`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (find bt2 20) = (Some "j") ;; ;;
   ^^^^
Error: Unbound value find

```


+ Fail: Check that the result of evaluating
   ```
   find bt2 32
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (find bt2 32) = (None) ;; ;;
   ^^^^
Error: Unbound value find

```


+  _2.5_ / _3.0_ : Pass: find

    No comments

+ Fail: Check that the result of evaluating
   ```
   keylist inittree
   ```
   matches the pattern `[]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-8:
  (keylist inittree) = ([]) ;; ;;
   ^^^^^^^
Error: Unbound value keylist

```


+ Fail: Check that the result of evaluating
   ```
   keylist bt1
   ```
   matches the pattern `[0;1;2;3]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-8:
  (keylist bt1) = ([0;1;2;3]) ;; ;;
   ^^^^^^^
Error: Unbound value keylist

```


+ Fail: Check that the result of evaluating
   ```
   keylist bt2
   ```
   matches the pattern `[0;1;2;3;4;6;7;12;13;14;15;18;19;20;23;24]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-8:
  (keylist bt2) = ([0;1;2;3;4;6;7;12;13;14;15;18;19;20;23;24]) ;; ;;
   ^^^^^^^
Error: Unbound value keylist

```


+  _3.5_ / _4.0_ : Pass: keylist

    No comments

+ Fail: Evaluating the following expression
   ```
   delete bt1 3
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 0-6:
  delete bt1 3;; ;;
  ^^^^^^
Error: Unbound value delete

```


+ Fail: Check that the result of evaluating
   ```
   keylist (delete bt1 3)
   ```
   matches the pattern `[0;1;2]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-8:
  (keylist (delete bt1 3)) = ([0;1;2]) ;; ;;
   ^^^^^^^
Error: Unbound value keylist

```


+ Fail: Evaluating the following expression
   ```
   delete bt1 2
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 0-6:
  delete bt1 2;; ;;
  ^^^^^^
Error: Unbound value delete

```


+ Fail: Check that the result of evaluating
   ```
   keylist (delete bt1 2)
   ```
   matches the pattern `[0;1;3]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-8:
  (keylist (delete bt1 2)) = ([0;1;3]) ;; ;;
   ^^^^^^^
Error: Unbound value keylist

```


+ Fail: Evaluating the following expression
   ```
   delete bt2 21
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 0-6:
  delete bt2 21;; ;;
  ^^^^^^
Error: Unbound value delete

```


+ Fail: Check that the result of evaluating
   ```
   keylist (delete bt2 21)
   ```
   matches the pattern `[0;1;2;3;4;6;7;12;13;14;15;18;19;20;23;24]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-8:
  (keylist (delete bt2 21)) = ([0;1;2;3;4;6;7;12;13;14;15;18;19;20;23;24]) ;; ;;
   ^^^^^^^
Error: Unbound value keylist

```


+ Fail: Evaluating the following expression
   ```
   delete bt2 3
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 0-6:
  delete bt2 3;; ;;
  ^^^^^^
Error: Unbound value delete

```


+ Fail: Check that the result of evaluating
   ```
   keylist (delete bt2 3)
   ```
   matches the pattern `[0;1;2;4;6;7;12;13;14;15;18;19;20;23;24]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-8:
  (keylist (delete bt2 3)) = ([0;1;2;4;6;7;12;13;14;15;18;19;20;23;24]) ;; ;;
   ^^^^^^^
Error: Unbound value keylist

```


+ Fail: Evaluating the following expression
   ```
   delete bt2 15
   ```

   Test failed. The following errors were reported:

```
 ;;
Characters 0-6:
  delete bt2 15;; ;;
  ^^^^^^
Error: Unbound value delete

```


+ Fail: Check that the result of evaluating
   ```
   keylist (delete bt2 15)
   ```
   matches the pattern `[0;1;2;3;4;6;7;12;13;14;18;19;20;23;24]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-8:
  (keylist (delete bt2 15)) = ([0;1;2;3;4;6;7;12;13;14;18;19;20;23;24]) ;; ;;
   ^^^^^^^
Error: Unbound value keylist

```


+  _0_ / _6.0_ : Pass: delete

    No substantial implementation or comment

#### Total score: _20_ / _28.0_

#### Problem 5

+  _3.5_ / _6_ : Pass: Part 1 expr representation

    exp3 uses App, and second part of Fun should be a type

###### Base Cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Id "x") [("x", IntTy)]
   ```
   matches the pattern `Some IntTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Id "x") [("x", IntTy)]) = (Some IntTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Id "x") [("x", BoolTy)]
   ```
   matches the pattern `Some BoolTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Id "x") [("x", BoolTy)]) = (Some BoolTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Int 2041) []
   ```
   matches the pattern `Some IntTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Int 2041) []) = (Some IntTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (True) []
   ```
   matches the pattern `Some BoolTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (True) []) = (Some BoolTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (False) []
   ```
   matches the pattern `Some BoolTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (False) []) = (Some BoolTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+  _0.25_ / _1_ : Pass: Part 2 Base cases

    True False instead of bool x, no matching case for Id

###### Arithmetic Expressions: correctly type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Plus ((Int 1), (Int 1))) []
   ```
   matches the pattern `Some IntTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Plus ((Int 1), (Int 1))) []) = (Some IntTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Minus ((Int 1), (Int 1))) []
   ```
   matches the pattern `Some IntTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Minus ((Int 1), (Int 1))) []) = (Some IntTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Times ((Int 2), (Int 2))) []
   ```
   matches the pattern `Some IntTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Times ((Int 2), (Int 2))) []) = (Some IntTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Div ((Int 4), (Int 2))) []
   ```
   matches the pattern `Some IntTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Div ((Int 4), (Int 2))) []) = (Some IntTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


###### Arithmetic Expressions: ill type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Plus ((Int 1), True)) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Plus ((Int 1), True)) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Minus ((Int 1), True)) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Minus ((Int 1), True)) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Times ((Int 2), True)) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Times ((Int 2), True)) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Div ((Int 4), True)) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Div ((Int 4), True)) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+  _0.25_ / _1.5_ : Pass: Part 2 Arithmetic operator cases

    typeof_aux takes 2 args and return a type, so cannot use *

###### Comparison Expressions: correctly type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Eq ((Int 1), (Int 1))) []
   ```
   matches the pattern `Some BoolTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Eq ((Int 1), (Int 1))) []) = (Some BoolTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Lss ((Int 1), (Int 2))) []
   ```
   matches the pattern `Some BoolTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Lss ((Int 1), (Int 2))) []) = (Some BoolTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Gtr ((Int 2), (Int 1))) []
   ```
   matches the pattern `Some BoolTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Gtr ((Int 2), (Int 1))) []) = (Some BoolTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


###### Comparison Expressions: ill type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Eq ((Int 1), True)) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Eq ((Int 1), True)) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Lss ((Int 1), True)) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Lss ((Int 1), True)) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Gtr ((Int 2), True)) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Gtr ((Int 2), True)) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+  _0.25_ / _1.5_ : Pass: Part 2 Comparison operator cases

    

###### Logical Expressions: correctly type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (And (True, False)) []
   ```
   matches the pattern `Some BoolTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (And (True, False)) []) = (Some BoolTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Or (False, False)) []
   ```
   matches the pattern `Some BoolTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Or (False, False)) []) = (Some BoolTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Not (False)) []
   ```
   matches the pattern `Some BoolTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Not (False)) []) = (Some BoolTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


###### Logical Expressions: ill type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (And ((Int 1), False)) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (And ((Int 1), False)) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Or ((Int 1), False)) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Or ((Int 1), False)) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Not (Int 1)) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Not (Int 1)) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+  _0_ / _1.5_ : Pass: Part 2 Logical operator cases

    No matching cases for And and Or

###### Condition Expressions: correctly type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Cond (False, False, True)) []
   ```
   matches the pattern `Some BoolTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Cond (False, False, True)) []) = (Some BoolTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Cond (False, (Int 1), (Int 2))) []
   ```
   matches the pattern `Some IntTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Cond (False, (Int 1), (Int 2))) []) = (Some IntTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


###### Condition Expressions: ill type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Cond ((Int 1), False, True)) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Cond ((Int 1), False, True)) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Cond (False, False, (Int 2))) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Cond (False, False, (Int 2))) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+  _1.5_ / _2.5_ : Pass: Part 2 Cond operator cases

    type of e1 should be BoolTy

###### Let Expressions: correctly type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Let ("x", Int 1, Id "x")) []
   ```
   matches the pattern `Some IntTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Let ("x", Int 1, Id "x")) []) = (Some IntTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Let ("x", (Plus ((Int 1), (Int 1))), Id "x")) []
   ```
   matches the pattern `Some IntTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Let ("x", (Plus ((Int 1), (Int 1))), Id "x")) []) = (Some IntTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


###### Let Expressions: ill type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Let ("x", Int 1, (Plus (Id "x", True)))) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Let ("x", Int 1, (Plus (Id "x", True)))) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Let ("x", (Plus ((Int 1), True)), Id "x")) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Let ("x", (Plus ((Int 1), True)), Id "x")) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+  _0.25_ / _2_ : Pass: Part 2 Let operator cases

    check for type of e2, then bind e1 to that type by adding to the list, then check for type of e3

###### Fun Expressions: correctly type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Fun ("x", IntTy, Plus (Id "x", Int 1))) []
   ```
   matches the pattern `Some (FunTy (IntTy, IntTy))`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Fun ("x", IntTy, Plus (Id "x", Int 1))) []) = (Some (FunTy (IntTy, IntTy))) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux 
    (Fun ("x",
	        IntTy,
		  (Fun ("y",BoolTy,Cond(Id "y",
					Plus (Id "x",Int 1),
					Minus (Id "x", Int 5)))))) []
    
   ```
   matches the pattern `Some (FunTy (IntTy, FunTy (BoolTy, IntTy)))`.

   Test failed. The following errors were reported:

```
 ;;
            Characters 1-11:
  (typeof_aux 
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


###### Fun Expressions: ill type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (Fun ("x", IntTy, Plus (Id "x", True))) []
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (Fun ("x", IntTy, Plus (Id "x", True))) []) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux 
    (Fun ("x",
	        IntTy,
		  (Fun ("y",BoolTy,Cond(Id "y",
					Plus (Id "x",Int 1),
					Minus (Id "x", True)))))) []
    
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
            Characters 1-11:
  (typeof_aux 
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+  _0_ / _2_ : Pass: Part 2 Fun operator cases

    

###### App Expressions: correctly type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (App (Id "foo",Int 5)) [("foo", FunTy (IntTy, IntTy))]
   ```
   matches the pattern `Some IntTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (App (Id "foo",Int 5)) [("foo", FunTy (IntTy, IntTy))]) = (Some IntTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (App ((App (Id "foo",Int 5)),True)) [("foo", FunTy (IntTy, FunTy (BoolTy, IntTy)))]
   ```
   matches the pattern `Some IntTy`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (App ((App (Id "foo",Int 5)),True)) [("foo", FunTy (IntTy, FunTy (BoolTy, IntTy)))]) = (Some IntTy) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


###### App Expressions: ill type checked cases

+ Fail: Check that the result of evaluating
   ```
   typeof_aux (App (Id "foo",Int 5)) [("foo", IntTy)]
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (App (Id "foo",Int 5)) [("foo", IntTy)]) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (App (Id "foo",True)) [("foo", FunTy (IntTy, IntTy))]
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (App (Id "foo",True)) [("foo", FunTy (IntTy, IntTy))]) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+ Fail: Check that the result of evaluating
   ```
   typeof_aux (App ((App (Id "foo",Plus (True, Int 5))),True)) [("foo", FunTy (IntTy, FunTy (BoolTy, IntTy)))]
   ```
   matches the pattern `None`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-11:
  (typeof_aux (App ((App (Id "foo",Plus (True, Int 5))),True)) [("foo", FunTy (IntTy, FunTy (BoolTy, IntTy)))]) = (None) ;; ;;
   ^^^^^^^^^^
Error: Unbound value typeof_aux

```


+  _0_ / _2_ : Pass: Part 2 App operator cases

    

+  _0_ / _1_ : Pass: Part 2 Quality and Structure

    no comment on type, precondition and postcondition, incorrect logic

+  _0.25_ / _2_ : Pass: Part 3 typeof function

    only needs to call typeof_aux expr []

#### Total score: _6.25_ / _23.0_

#### Problem 6

###### Base Cases

+ Fail: Check that the result of evaluating
   ```
   eval (Id "ocaml") [("ocaml", Int 2041)]
   ```
   matches the pattern `Int 2041`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Id "ocaml") [("ocaml", Int 2041)]) = (Int 2041) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Id "ocaml") [("Go", False);("scheme", Int 1901);("ocaml", Int 2041);("ocaml",False)]
   ```
   matches the pattern `Int 2041`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Id "ocaml") [("Go", False);("scheme", Int 1901);("ocaml", Int 2041);("ocaml",False)]) = (Int 2041) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Int 1901) []
   ```
   matches the pattern `Int 1901`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Int 1901) []) = (Int 1901) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (True) []
   ```
   matches the pattern `True`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (True) []) = (True) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (False) []
   ```
   matches the pattern `False`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (False) []) = (False) ;; ;;
   ^^^^
Error: Unbound value eval

```


###### Arithmetic Expressions

+ Fail: Check that the result of evaluating
   ```
   eval (Plus ((Int 1901), (Int 1))) []
   ```
   matches the pattern `Int 1902`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Plus ((Int 1901), (Int 1))) []) = (Int 1902) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Minus ((Int 1902), (Int 1))) []
   ```
   matches the pattern `Int 1901`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Minus ((Int 1902), (Int 1))) []) = (Int 1901) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Times ((Int 2), (Int 951))) []
   ```
   matches the pattern `Int 1902`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Times ((Int 2), (Int 951))) []) = (Int 1902) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Div ((Int 1902), (Int 2))) []
   ```
   matches the pattern `Int 951`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Div ((Int 1902), (Int 2))) []) = (Int 951) ;; ;;
   ^^^^
Error: Unbound value eval

```


###### Comparison Expressions

+ Fail: Check that the result of evaluating
   ```
   eval (Eq ((Int 1901), (Int 1901))) []
   ```
   matches the pattern `True`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Eq ((Int 1901), (Int 1901))) []) = (True) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Lss ((Int 1901), (Int 2041))) []
   ```
   matches the pattern `True`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Lss ((Int 1901), (Int 2041))) []) = (True) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Gtr ((Int 1901), (Int 2041))) []
   ```
   matches the pattern `False`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Gtr ((Int 1901), (Int 2041))) []) = (False) ;; ;;
   ^^^^
Error: Unbound value eval

```


###### Logical Expressions

+ Fail: Check that the result of evaluating
   ```
   eval (And (True, False)) []
   ```
   matches the pattern `False`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (And (True, False)) []) = (False) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Or (False, False)) []
   ```
   matches the pattern `False`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Or (False, False)) []) = (False) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Not (False)) []
   ```
   matches the pattern `True`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Not (False)) []) = (True) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Cond (False, False, True)) []
   ```
   matches the pattern `True`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Cond (False, False, True)) []) = (True) ;; ;;
   ^^^^
Error: Unbound value eval

```


###### Let Expressions

+ Fail: Check that the result of evaluating
   ```
   eval (Let ("x", Int 1901, Id "x")) []
   ```
   matches the pattern `Int 1901`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-5:
  (eval (Let ("x", Int 1901, Id "x")) []) = (Int 1901) ;; ;;
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Let ("x",
               Int 5,
               Cond (And (Lss (Plus (Id "x",Int 3), Int 15),
                          Gtr (Times (Int 4, Id "x"), Int 15)),
                     True,
                     False))) []
   ```
   matches the pattern `True`.

   Test failed. The following errors were reported:

```
 ;;
          Characters 1-5:
  (eval (Let ("x",
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Let ("x",
               Int 1,
               Let ("y",
                    Id "x",
                    Let ("y",
                         Minus(Plus(Id "x", Id "y"), Int 2),
                         Id "y")))) []
   ```
   matches the pattern `Int 0`.

   Test failed. The following errors were reported:

```
 ;;
            Characters 1-5:
  (eval (Let ("x",
   ^^^^
Error: Unbound value eval

```


+ Fail: Check that the result of evaluating
   ```
   eval (Let ("x",
               Cond (Gtr (Int 2041, Int 2021),
                     True,
                     False),
               Let ("y",
                    Cond (Not (And (Id "x", False)),
                          Times (Int 21, Int 2),
                          Div (Int 1, Int 0)),
                    Cond (Or ((Lss (Id "y", Int 43)), Id "x"),
                          Eq (Id "y", Int 42),
                          False)))) []
   ```
   matches the pattern `True`.

   Test failed. The following errors were reported:

```
 ;;
                  Characters 1-5:
  (eval (Let ("x",
   ^^^^
Error: Unbound value eval

```


+  _0_ / _3_ : Fail: Base cases

The file was not found.


+  _0_ / _2_ : Fail: Arithmetic Expressions

The file was not found.


+  _0_ / _1_ : Fail: Comparison Expressions

The file was not found.


+  _0_ / _3_ : Fail: Logical Expressions

The file was not found.


+  _0_ / _2_ : Fail: Let Expressions

The file was not found.


+  _0_ / _1_ : Fail: Quality and Structure

The file was not found.


+ Fail: General Comments

The file was not found.


#### Total score: _0_ / _12_

#### Total score: _40.25_ / _83_

