### Assessment for HW3

Run on March 21, 01:10:52 AM.

+ Pass: Change into directory "hws/hw3".

+  _17.5_ / _43_ : Pass: 

#### Problem 1

+ Pass: Check that the result of evaluating
   ```
   divide_list (fun x -> true) []
   ```
   matches the pattern `([], [])`.


+ Fail: Check that the result of evaluating
   ```
   divide_list (fun x -> String.length x < 4) ["this"; "is"; "a"; "list"; "of"; "mixed"; "length"; "strings"]
   ```
   matches the pattern `(["is"; "a"; "of"], ["this"; "list"; "mixed"; "length"; "strings"])`.

   Your solution evaluated incorrectly and produced some part of the following:

```
- : string list * string list =
(["of"; "a"; "is"], ["strings"; "length"; "mixed"; "list"; "this"])

```


+ Fail: Check that the result of evaluating
   ```
   divide_list  (fun x -> x mod 2 = 0) [1;3;6;8;9;10]
   ```
   matches the pattern `([6; 8; 10], [1; 3; 9])`.

   Your solution evaluated incorrectly and produced some part of the following:
`- : int list * int list = ([10; 8; 6], [9; 3; 1])
`

+ Fail: Check that the result of evaluating
   ```
   divide_list  (fun x -> x > 0) [1;3;6;8;9;10]
   ```
   matches the pattern `([1;3;6;8;9;10], [])`.

   Your solution evaluated incorrectly and produced some part of the following:
`- : int list * int list = ([10; 9; 8; 6; 3; 1], [])
`

+ Fail: Check that the result of evaluating
   ```
   divide_list  (fun x -> x < 0) [1;3;6;8;9;10]
   ```
   matches the pattern `([], [1;3;6;8;9;10])`.

   Your solution evaluated incorrectly and produced some part of the following:
`- : int list * int list = ([], [10; 9; 8; 6; 3; 1])
`

+  _4_ / _5_ : Pass: Analysis of divide_list

    The order of the lists is reversed

#### Total score: _4_ / _5_

#### Problem 2

+ Pass: Check that the result of evaluating
   ```
   treemap (Node (7, Node (4, Node (2, Empty, Empty), Node (5, Empty,Empty)), Node (10, Node (9, Empty, Empty), Node (12, Node (11, Empty, Empty), Empty)))) (fun x -> x + 3)
   ```
   matches the pattern `Node (10, Node (7, Node (5, Empty, Empty), Node (8, Empty,Empty)), Node (13, Node (12, Empty, Empty), Node (15, Node (14, Empty, Empty), Empty)))`.


+ Pass: Check that the result of evaluating
   ```
   treemap (Node (7, Node (4, Node (2, Empty, Empty), Node (5, Empty,Empty)), Node (10, Node (9, Empty, Empty), Node (12, Node (11, Empty, Empty), Empty)))) (fun x -> (x mod 2 = 0))
   ```
   matches the pattern `Node (false, Node (true, Node (true, Empty, Empty), Node (false, Empty,Empty)), Node (true, Node (false, Empty, Empty), Node (true, Node (false, Empty, Empty), Empty))) `.


+  _5_ / _5_ : Pass: Problem 2

    

#### Total score: _5_ / _5_

#### Problem 3

+  _1.5_ / _4_ : Pass: reduce

    This is the right idea, but the reasoning behind the final type inference is not explicitly stated. Start with an initial type based on the number of arguments, and then refine the type based on each line of code. For this problem, start with "reduce : 'a -> 'b -> 'c -> 'd" and then further refine each part of the type based on the proceeding lines of code.

+  _1.5_ / _4_ : Pass: forall2

    See above feedback regarding reduce.

#### Total score: _3_ / _8_

#### Problem 4

###### Append

+ Pass: Check that the result of evaluating
   ```
   append [] []
   ```
   matches the pattern `[]`.


+ Pass: Check that the result of evaluating
   ```
   append [] [1;2;3]
   ```
   matches the pattern `[1;2;3]`.


+ Fail: Check that the result of evaluating
   ```
   append [1;2;3] []
   ```
   matches the pattern `[1;2;3]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 9-10:
  (append [1;2;3] []) = ([1;2;3]) ;; ;;
           ^
Error: This expression has type int but an expression was expected of type
         'a -> 'a

```


+ Fail: Check that the result of evaluating
   ```
   append [1;2;3] [4;5;6]
   ```
   matches the pattern `[1;2;3;4;5;6]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 9-10:
  (append [1;2;3] [4;5;6]) = ([1;2;3;4;5;6]) ;; ;;
           ^
Error: This expression has type int but an expression was expected of type
         'a -> 'a

```


+ Fail: Check that the result of evaluating
   ```
   append [1;2] [3;4;5]
   ```
   matches the pattern `[1;2;3;4;5]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 9-10:
  (append [1;2] [3;4;5]) = ([1;2;3;4;5]) ;; ;;
           ^
Error: This expression has type int but an expression was expected of type
         'a -> 'a

```


+ Fail: Check that the result of evaluating
   ```
   append [1;2;3] [4;5]
   ```
   matches the pattern `[1;2;3;4;5]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 9-10:
  (append [1;2;3] [4;5]) = ([1;2;3;4;5]) ;; ;;
           ^
Error: This expression has type int but an expression was expected of type
         'a -> 'a

```


###### Reverse

+ Fail: Check that the result of evaluating
   ```
   reverse []
   ```
   matches the pattern `[]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 15-19:
  (reverse []) = ([]) ;; ;;
                 ^^^^
Error: This expression has type 'a list
       but an expression was expected of type 'b -> 'b

```


+ Fail: Check that the result of evaluating
   ```
   reverse ["a";"b";"c";"d";"e"]
   ```
   matches the pattern `["e";"d";"c";"b";"a"]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 10-13:
  (reverse ["a";"b";"c";"d";"e"]) = (["e";"d";"c";"b";"a"]) ;; ;;
            ^^^
Error: This expression has type string but an expression was expected of type
         'a -> 'a

```


###### Filter

+ Fail: Check that the result of evaluating
   ```
   filter (fun x -> true) []
   ```
   matches the pattern `[]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 24-26:
  (filter (fun x -> true) []) = ([]) ;; ;;
                          ^^
Error: This expression has type 'a list
       but an expression was expected of type 'b -> 'c -> 'c

```


+ Fail: Check that the result of evaluating
   ```
   filter (fun x -> match x with Some _ -> true | _ -> false) [Some 5486; None; Some 5106; None; None; Some 5451; Some 5581; Some 8442]
   ```
   matches the pattern `[Some 5486; Some 5106; Some 5451; Some 5581; Some 8442]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 60-133:
  (filter (fun x -> match x with Some _ -> true | _ -> false) [Some 5486; None; Some 5106; None; None; Some 5451; Some 5581; Some 8442]) = ([Some 5486; Some 5106; Some 5451; Some 5581; Some 8442]) ;; ;;
                                                              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Error: This expression has type 'a list
       but an expression was expected of type 'b -> 'c -> 'c

```


+ Fail: Check that the result of evaluating
   ```
   filter (fun x -> match x with Some l -> List.length l mod 2 = 0 | _ -> true) [Some []; None; Some [1;2]; None; Some [3;4;5]; None; None]
   ```
   matches the pattern `[Some []; None; Some [1;2]; None; None; None]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 78-137:
  (filter (fun x -> match x with Some l -> List.length l mod 2 = 0 | _ -> true) [Some []; None; Some [1;2]; None; Some [3;4;5]; None; None]) = ([Some []; None; Some [1;2]; None; None; None]) ;; ;;
                                                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Error: This expression has type 'a list
       but an expression was expected of type 'b -> 'c -> 'c

```


+ Fail: Check that the result of evaluating
   ```
   filter (fun x -> match x with Some s -> s = "csci" | _ -> false) [Some "math"; None; Some "ee"; None; Some "phys"; None; Some "ast"]
   ```
   matches the pattern `[]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 66-133:
  (filter (fun x -> match x with Some s -> s = "csci" | _ -> false) [Some "math"; None; Some "ee"; None; Some "phys"; None; Some "ast"]) = ([]) ;; ;;
                                                                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Error: This expression has type 'a list
       but an expression was expected of type 'b -> 'c -> 'c

```


+  _1_ / _3_ : Pass: `append`

    Passing in incorrect function.

+  _0_ / _3_ : Pass: `reverse`

    Incorrect function and no initial list

+  _0_ / _3_ : Pass: `filter`

    

+ Pass: General Comments

    

#### Total score: _1_ / _9_

#### Problem 5

###### `freeIn`

####### Base Cases

+ Fail: Check that the result of evaluating
   ```
   freeIn (Id "ee") "ee"
   ```
   matches the pattern `true`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Id "ee") "ee") = (true) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Id "math") "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Id "math") "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Int 5581) "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Int 5581) "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn True "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn True "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn False "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn False "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


####### Non-Binding Cases

+ Fail: Check that the result of evaluating
   ```
   freeIn (Plus (Id "ee", Id "y")) "ee"
   ```
   matches the pattern `true`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Plus (Id "ee", Id "y")) "ee") = (true) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Minus (Id "x", Id "y")) "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Minus (Id "x", Id "y")) "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Times (Div(Id "x", Id "y"), Div(Id "ee", Id "y"))) "ee"
   ```
   matches the pattern `true`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Times (Div(Id "x", Id "y"), Div(Id "ee", Id "y"))) "ee") = (true) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Lss (Gtr(Id "ee", Id "y"), Gtr(Id "x", Id "y"))) "ee"
   ```
   matches the pattern `true`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Lss (Gtr(Id "ee", Id "y"), Gtr(Id "x", Id "y"))) "ee") = (true) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Eq (And(Id "x", Id "y"), And(Id "x", Id "y"))) "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Eq (And(Id "x", Id "y"), And(Id "x", Id "y"))) "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Or ((Not (App (Id "x", Id "y"))), False)) "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Or ((Not (App (Id "x", Id "y"))), False)) "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


####### Let Expression

+ Fail: Check that the result of evaluating
   ```
   freeIn (Let ("math", Plus(Minus(Id "ee", Id "csci"), Int 5581), Id "stat")) "ee"
   ```
   matches the pattern `true`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Let ("math", Plus(Minus(Id "ee", Id "csci"), Int 5581), Id "stat")) "ee") = (true) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Let ("ee", Plus(Minus(Id "stat", Id "phys"), Int 5581), Id "ee")) "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Let ("ee", Plus(Minus(Id "stat", Id "phys"), Int 5581), Id "ee")) "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Let ("ee", Plus(Minus(Id "stat", Id "phys"), Int 5581), Id "stat")) "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Let ("ee", Plus(Minus(Id "stat", Id "phys"), Int 5581), Id "stat")) "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Let ("math", Plus(Minus(Id "stat", Id "phys"), Int 5581), Id "ee")) "ee"
   ```
   matches the pattern `true`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Let ("math", Plus(Minus(Id "stat", Id "phys"), Int 5581), Id "ee")) "ee") = (true) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Let ("math", Plus(Minus(Id "stat", Id "phys"), Int 5581), Id "stat")) "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Let ("math", Plus(Minus(Id "stat", Id "phys"), Int 5581), Id "stat")) "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


####### Fun Expression

+ Fail: Check that the result of evaluating
   ```
   freeIn (Fun ("ee", Plus(Times(Id "math", Int 8441), Div(Id "ee", Int 5581)))) "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Fun ("ee", Plus(Times(Id "math", Int 8441), Div(Id "ee", Int 5581)))) "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Fun ("ee", Plus(Times(Id "math", Int 8441), Div(Id "math", Int 8442)))) "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Fun ("ee", Plus(Times(Id "math", Int 8441), Div(Id "math", Int 8442)))) "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Fun ("phys", Plus(Times(Id "math", Int 8441), Div(Id "ee", Int 5561)))) "ee"
   ```
   matches the pattern `true`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Fun ("phys", Plus(Times(Id "math", Int 8441), Div(Id "ee", Int 5561)))) "ee") = (true) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


+ Fail: Check that the result of evaluating
   ```
   freeIn (Fun ("phys", Plus(Times(Id "math", Int 8441), Div(Id "math", Int 8442)))) "ee"
   ```
   matches the pattern `false`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (freeIn (Fun ("phys", Plus(Times(Id "math", Int 8441), Div(Id "math", Int 8442)))) "ee") = (false) ;; ;;
   ^^^^^^
Error: Unbound value freeIn

```


###### `subst`

####### Id Expression

+ Fail: Check that the result of evaluating
   ```
   subst (Id "x") "x" (Int 0)
   ```
   matches the pattern `(Int 0)`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Id "x") "x" (Int 0)) = ((Int 0)) ;; ;;
   ^^^^^
Error: Unbound value subst

```


+ Fail: Check that the result of evaluating
   ```
   subst (Id "x") "y" (Int 0)
   ```
   matches the pattern `(Id "x")`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Id "x") "y" (Int 0)) = ((Id "x")) ;; ;;
   ^^^^^
Error: Unbound value subst

```


####### Constant  Cases

+ Fail: Check that the result of evaluating
   ```
   subst True "x" (Int 0)
   ```
   matches the pattern `True`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst True "x" (Int 0)) = (True) ;; ;;
   ^^^^^
Error: Unbound value subst

```


+ Fail: Check that the result of evaluating
   ```
   subst False "x" (Int 0)
   ```
   matches the pattern `False`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst False "x" (Int 0)) = (False) ;; ;;
   ^^^^^
Error: Unbound value subst

```


+ Fail: Check that the result of evaluating
   ```
   subst (Int 100) "x" (Int 0)
   ```
   matches the pattern `(Int 100)`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Int 100) "x" (Int 0)) = ((Int 100)) ;; ;;
   ^^^^^
Error: Unbound value subst

```


####### Non-binding  Cases

+ Fail: Check that the result of evaluating
   ```
   subst (Plus ((Id "x"),(Minus ((Id "x"),(Times ((Id "x"),(Div ((Id "x"),(Id "y"))))))))) "x" (Int 0)
   ```
   matches the pattern `(Plus ((Int 0),(Minus ((Int 0),(Times ((Int 0),(Div ((Int 0),(Id "y")))))))))`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Plus ((Id "x"),(Minus ((Id "x"),(Times ((Id "x"),(Div ((Id "x"),(Id "y"))))))))) "x" (Int 0)) = ((Plus ((Int 0),(Minus ((Int 0),(Times ((Int 0),(Div ((Int 0),(Id "y")))))))))) ;; ;;
   ^^^^^
Error: Unbound value subst

```


+ Fail: Check that the result of evaluating
   ```
   subst (Lss ((Id "x"),(Eq ((Id "x"),(Gtr ((Id "x"),(Id "y"))))))) "x" (Int 0)
   ```
   matches the pattern `(Lss ((Int 0),(Eq ((Int 0),(Gtr ((Int 0),(Id "y")))))))`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Lss ((Id "x"),(Eq ((Id "x"),(Gtr ((Id "x"),(Id "y"))))))) "x" (Int 0)) = ((Lss ((Int 0),(Eq ((Int 0),(Gtr ((Int 0),(Id "y")))))))) ;; ;;
   ^^^^^
Error: Unbound value subst

```


+ Fail: Check that the result of evaluating
   ```
   subst (Not (And ((Id "x"),(Or ((Id "x"),(Id "y")))))) "x" (Int 0)
   ```
   matches the pattern `(Not (And ((Int 0),(Or ((Int 0),(Id "y"))))))`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Not (And ((Id "x"),(Or ((Id "x"),(Id "y")))))) "x" (Int 0)) = ((Not (And ((Int 0),(Or ((Int 0),(Id "y"))))))) ;; ;;
   ^^^^^
Error: Unbound value subst

```


+ Fail: Check that the result of evaluating
   ```
   subst (App ((Id "x"),(Id "x"))) "x" (Int 0)
   ```
   matches the pattern `(App ((Int 0),(Int 0)))`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (App ((Id "x"),(Id "x"))) "x" (Int 0)) = ((App ((Int 0),(Int 0)))) ;; ;;
   ^^^^^
Error: Unbound value subst

```


####### Let Expression

+ Fail: Check that the result of evaluating
   ```
   subst (Let ("x", Id "y", (Plus (Id "x", Id "z")))) "x" (Int 0)
   ```
   matches the pattern `(Let ("x", Id "y", (Plus (Id "x", Id "z"))))`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Let ("x", Id "y", (Plus (Id "x", Id "z")))) "x" (Int 0)) = ((Let ("x", Id "y", (Plus (Id "x", Id "z"))))) ;; ;;
   ^^^^^
Error: Unbound value subst

```


+ Fail: Check that the result of evaluating
   ```
   subst (Let ("x", Id "x", (Plus (Id "x", Id "z")))) "x" (Int 0)
   ```
   matches the pattern `(Let ("x", Int 0, (Plus (Id "x", Id "z"))))`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Let ("x", Id "x", (Plus (Id "x", Id "z")))) "x" (Int 0)) = ((Let ("x", Int 0, (Plus (Id "x", Id "z"))))) ;; ;;
   ^^^^^
Error: Unbound value subst

```


+ Fail: Check that the result of evaluating
   ```
   subst (Let ("x", Id "y", (Plus (Id "x", Id "z")))) "z" (Plus (Id "x", Int 1))
   ```
   matches the pattern `(Let ("var1", Id "y", (Plus (Id "var1", Plus (Id "x", Int 1)))))`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Let ("x", Id "y", (Plus (Id "x", Id "z")))) "z" (Plus (Id "x", Int 1))) = ((Let ("var1", Id "y", (Plus (Id "var1", Plus (Id "x", Int 1)))))) ;; ;;
   ^^^^^
Error: Unbound value subst

```


####### Fun Expression

+ Fail: Check that the result of evaluating
   ```
   subst (Fun ("x", (Plus (Id "x", Id "z")))) "x" (Int 0)
   ```
   matches the pattern `(Fun ("x", (Plus (Id "x", Id "z"))))`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Fun ("x", (Plus (Id "x", Id "z")))) "x" (Int 0)) = ((Fun ("x", (Plus (Id "x", Id "z"))))) ;; ;;
   ^^^^^
Error: Unbound value subst

```


+ Fail: Check that the result of evaluating
   ```
   subst (Fun ("x", (Plus (Id "x", Id "z")))) "z" (Int 0)
   ```
   matches the pattern `(Fun ("x", (Plus (Id "x", Int 0))))`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Fun ("x", (Plus (Id "x", Id "z")))) "z" (Int 0)) = ((Fun ("x", (Plus (Id "x", Int 0))))) ;; ;;
   ^^^^^
Error: Unbound value subst

```


+ Fail: Check that the result of evaluating
   ```
   subst (Fun ("x", (Plus (Id "x", Id "z")))) "z" (Plus (Id "x", Int 1))
   ```
   matches the pattern `(Fun ("var1", (Plus (Id "var1", Plus (Id "x", Int 1)))))`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (subst (Fun ("x", (Plus (Id "x", Id "z")))) "z" (Plus (Id "x", Int 1))) = ((Fun ("var1", (Plus (Id "var1", Plus (Id "x", Int 1)))))) ;; ;;
   ^^^^^
Error: Unbound value subst

```


+  _0.5_ / _1_ : Pass: `freeIn`: Base Cases

    Doesn't handle Int/True cases correctly

+  _1.5_ / _1.5_ : Pass: `freeIn`: Non-Binding Cases

    

+  _0_ / _2.0_ : Pass: `freeIn`: Let Expression

    Performs a recursive call on the wrong variable, thus missing all required checks

+  _1.5_ / _1.5_ : Pass: `freeIn`: Fun Expression

    

+  _0.5_ / _1.5_ : Pass: `subst`: Id Expression

    Checks if a substitution is needed, but uses incorrect and incomplete syntax to perform the substitution.

+  _0_ / _1_ : Pass: `subst`: Constant Cases

    Does not handle constant cases

+  _0_ / _2_ : Pass: `subst`: Non-Binding Cases

    Does not correctly substitute in any case due to incorrect logic and syntax

+  _0_ / _2.5_ : Pass: `subst`: Let Expression

    Does not perform a substitution nor does it check if a rename is necessary

+  _0_ / _2_ : Pass: `subst`: Fun Expression

    Does not check for a rename, uses incorrect substitution syntax, and substitutes only in the incorrect case

+  _0.5_ / _1_ : Pass: Quality and Structure

    Missing comment defining type, precondition, and postcondition of subst.

+ Pass: General Comments

    Please make sure your code compiles before submitting; i.e., please try to remove syntax errors if possible.

#### Total score: _4.5_ / _16.0_

#### Total score: _17.5_ / _43_

