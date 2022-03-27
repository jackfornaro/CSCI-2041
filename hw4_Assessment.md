### Assessment for HW4

Run on April 03, 21:51:02 PM.

+ Pass: Change into directory "hws/hw4".

+  _50.75_ / _54.5_ : Pass: 

#### Problem 1

###### `makePairLists`

+ Fail: Check that the result of evaluating
    ```ocaml
    makePairLists "b" ["a"; "c"; "d"; "e"]
    ```
    matches the pattern `[(("a", "b"), ["a"; "c"; "d"; "e"]); (("b", "c"), ["a"; "c"; "d"; "e"]); (("b", "d"), ["a"; "c"; "d"; "e"]); (("b", "e"), ["a"; "c"; "d"; "e"])]`
   Test failed. The following errors were reported:

```
 ;;
Characters 1-14:
  (makePairLists "b" ["a"; "c"; "d"; "e"]) = ([(("a", "b"), ["a"; "c"; "d"; "e"]); (("b", "c"), ["a"; "c"; "d"; "e"]); (("b", "d"), ["a"; "c"; "d"; "e"]); (("b", "e"), ["a"; "c"; "d"; "e"])]) ;; ;;
   ^^^^^^^^^^^^^
Error: Unbound value makePairLists

```


+ Fail: Check that the result of evaluating
    ```ocaml
    makePairLists "c" ["a"; "b"; "d"; "e"]
    ```
    matches the pattern `[(("a", "c"), ["a"; "b"; "d"; "e"]); (("b", "c"), ["a"; "b"; "d"; "e"]); (("c", "d"), ["a"; "b"; "d"; "e"]); (("c", "e"), ["a"; "b"; "d"; "e"])]`
   Test failed. The following errors were reported:

```
 ;;
Characters 1-14:
  (makePairLists "c" ["a"; "b"; "d"; "e"]) = ([(("a", "c"), ["a"; "b"; "d"; "e"]); (("b", "c"), ["a"; "b"; "d"; "e"]); (("c", "d"), ["a"; "b"; "d"; "e"]); (("c", "e"), ["a"; "b"; "d"; "e"])]) ;; ;;
   ^^^^^^^^^^^^^
Error: Unbound value makePairLists

```


###### `makeAllPairLists`

+ Fail: Check that the result of evaluating
    ```ocaml
    makeAllPairLists 
[ ("a", ["b"; "c"; "d"]);  ("b", ["a"; "c"; "d"; "e"]); ("c", ["a"; "b"; "d"; "e"]); ("d", ["a"; "b"; "c"; "e"]); ("e", ["b"; "c"; "d"]) ] 
    ```
    matches the pattern
    ```ocaml
    
 [[(("a", "b"), ["b"; "c"; "d"]); (("a", "c"), ["b"; "c"; "d"]); (("a", "d"), ["b"; "c"; "d"])];
 [(("a", "b"), ["a"; "c"; "d"; "e"]); (("b", "c"), ["a"; "c"; "d"; "e"]); (("b", "d"), ["a"; "c"; "d"; "e"]); (("b", "e"), ["a"; "c"; "d"; "e"])];
 [(("a", "c"), ["a"; "b"; "d"; "e"]); (("b", "c"), ["a"; "b"; "d"; "e"]); (("c", "d"), ["a"; "b"; "d"; "e"]); (("c", "e"), ["a"; "b"; "d"; "e"])];
 [(("a", "d"), ["a"; "b"; "c"; "e"]); (("b", "d"), ["a"; "b"; "c"; "e"]); (("c", "d"), ["a"; "b"; "c"; "e"]); (("d", "e"), ["a"; "b"; "c"; "e"])];
 [(("b", "e"), ["b"; "c"; "d"]); (("c", "e"), ["b"; "c"; "d"]); (("d", "e"), ["b"; "c"; "d"])]]

    ```
   Test failed. The following errors were reported:

```
 ;;
            Characters 1-17:
  (makeAllPairLists 
   ^^^^^^^^^^^^^^^^
Error: Unbound value makeAllPairLists

```


###### `intersect`

+ Fail: Check that the result of evaluating
    ```ocaml
    intersect ["a"; "b"] ["b"; "c"]
    ```
    matches the pattern `["b"]`
   Test failed. The following errors were reported:

```
 ;;
Characters 1-10:
  (intersect ["a"; "b"] ["b"; "c"]) = (["b"]) ;; ;;
   ^^^^^^^^^
Error: Unbound value intersect

```


+ Fail: Check that the result of evaluating
    ```ocaml
    intersect ["a"; "b"; "c"; "d"] ["c"; "d"; "e"]
    ```
    matches the pattern `["c"; "d"]`
   Test failed. The following errors were reported:

```
 ;;
Characters 1-10:
  (intersect ["a"; "b"; "c"; "d"] ["c"; "d"; "e"]) = (["c"; "d"]) ;; ;;
   ^^^^^^^^^
Error: Unbound value intersect

```


###### `addOnePair`

+ Fail: Check that the result of evaluating
    ```ocaml
    addOnePair 
(("a", "c"), ["a"; "b"; "d"; "e"]) [(("b", "e"), ["b"; "c"; "d"]); (("c", "e"), ["b"; "c"; "d"]);
(("d", "e"), ["b"; "c"]); (("a", "d"), ["a"; "b"; "c"; "e"]); (("b", "d"), ["a"; "b"; "c"; "e"]); (("c", "d"), ["a"; "b"; "c"; "e"])]

    ```
    matches the pattern
    ```ocaml
    
[(("b", "e"), ["b"; "c"; "d"]); (("c", "e"), ["b"; "c"; "d"]); (("d", "e"), ["b"; "c"]); (("a", "d"), ["a"; "b"; "c"; "e"]);
 (("b", "d"), ["a"; "b"; "c"; "e"]); (("c", "d"), ["a"; "b"; "c"; "e"]); (("a", "c"), ["a"; "b"; "d"; "e"])]

    ```
   Test failed. The following errors were reported:

```
 ;;
            Characters 1-11:
  (addOnePair 
   ^^^^^^^^^^
Error: Unbound value addOnePair

```


+ Fail: Check that the result of evaluating
    ```ocaml
    addOnePair 
(("c", "e"), ["a"; "b"; "d"; "e"]) [(("b", "e"), ["b"; "c"; "d"]); (("c", "e"), ["b"; "c"; "d"]);
(("d", "e"), ["b"; "c"]); (("a", "d"), ["a"; "b"; "c"; "e"]); (("b", "d"), ["a"; "b"; "c"; "e"]); (("c", "d"), ["a"; "b"; "c"; "e"])]

    ```
    matches the pattern
    ```ocaml
    
[(("b", "e"), ["b"; "c"; "d"]); (("c", "e"), ["b"; "d"]); (("d", "e"), ["b"; "c"]); (("a", "d"), ["a"; "b"; "c"; "e"]); (("b", "d"), ["a"; "b"; "c"; "e"]); (("c", "d"), ["a"; "b"; "c"; "e"])]

    ```
   Test failed. The following errors were reported:

```
 ;;
          Characters 1-11:
  (addOnePair 
   ^^^^^^^^^^
Error: Unbound value addOnePair

```


###### `addAllPairs`

+ Fail: Check that the result of evaluating
    ```ocaml
    addAllPairs
[(("a", "c"), ["a"; "b"; "d"; "e"]); (("b", "c"), ["a"; "b"; "d"; "e"]); (("c", "d"), ["a"; "b"; "d"; "e"]); (("c", "e"), ["a"; "b"; "d"; "e"])]
[(("b", "e"), ["b"; "c"; "d"]); (("c", "e"), ["b"; "c"; "d"]); (("d", "e"), ["b"; "c"]); (("a", "d"), ["a"; "b"; "c"; "e"]); (("b", "d"), ["a"; "b"; "c"; "e"]); (("c", "d"), ["a"; "b"; "c"; "e"])]

    ```
    matches the pattern
    ```ocaml
    
[(("b", "e"), ["b"; "c"; "d"]); (("c", "e"), ["b"; "d"]); (("d", "e"), ["b"; "c"]); (("a", "d"), ["a"; "b"; "c"; "e"]);
(("b", "d"), ["a"; "b"; "c"; "e"]); (("c", "d"), ["a"; "b"; "e"]); (("a", "c"), ["a"; "b"; "d"; "e"]); (("b", "c"), ["a"; "b"; "d"; "e"])]

    ```
   Test failed. The following errors were reported:

```
 ;;
          Characters 1-12:
  (addAllPairs
   ^^^^^^^^^^^
Error: Unbound value addAllPairs

```


+  _3_ / _3_ : Pass: `makePairLists`

    Make sure your file compiles

+  _3_ / _3_ : Pass: `makeAllPairLists`

    

+  _3_ / _3_ : Pass: `intersect`

    

+  _4_ / _4_ : Pass: `addOnePair`

    

+  _3_ / _3_ : Pass: `addAllPairs`

    

#### Total score: _16_ / _16_

#### Problem 2

###### `insertOList/olistToList`

+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> (x mod 13) > (y mod 13)) in
   olistToList(initOList cmp)
    ```
    matches the pattern `[]`
   Test failed. The following errors were reported:

```
 ;;
    Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> (x mod 13) > (y mod 13)) in
   olistToList(iol (1) (initOList cmp))
    ```
    matches the pattern `[1]`
   Test failed. The following errors were reported:

```
 ;;
    Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> (x mod 13) > (y mod 13)) in
   olistToList(iol (1) (iol (3) (iol (2) (initOList cmp))))
    ```
    matches the pattern `[3;2;1]`
   Test failed. The following errors were reported:

```
 ;;
    Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> (x mod 13) > (y mod 13)) in
   olistToList(iol (62) (iol (53) (iol (19) (iol (46) (iol (3) (iol (89) (iol (91) (iol (47) (initOList cmp)))))))))
    ```
    matches the pattern `[89;62;47;46;19;3;53;91]`
   Test failed. The following errors were reported:

```
 ;;  
  Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> match (x, y) with (Some a,Some b) -> len a > len b | (Some _,_) | (None,None) -> true | _ -> false) in
   olistToList(iol (None) (iol (None) (iol (None) (initOList cmp))))
    ```
    matches the pattern `[None;None;None]`
   Test failed. The following errors were reported:

```
 ;;
    Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> match (x, y) with (Some a,Some b) -> len a > len b | (Some _,_) | (None,None) -> true | _ -> false) in
   olistToList(iol (Some []) (iol (None) (iol (None) (initOList cmp))))
    ```
    matches the pattern `[Some [];None;None]`
   Test failed. The following errors were reported:

```
 ;;
  Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> match (x, y) with (Some a,Some b) -> len a > len b | (Some _,_) | (None,None) -> true | _ -> false) in
   olistToList(iol (Some []) (iol (Some [1;2;3;4]) (iol (None) (iol (Some [1;2;3]) (iol (None) (initOList cmp))))))
    ```
    matches the pattern `[Some [1;2;3;4];Some [1;2;3];Some [];None;None]`
   Test failed. The following errors were reported:

```
 ;;
    Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


###### `isOrderedList`

+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> (x mod 13) > (y mod 13)) in
   isOrderedList(initOList cmp)
    ```
    matches the pattern `true`
   Test failed. The following errors were reported:

```
 ;;
    Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> (x mod 13) > (y mod 13)) in
   isOrderedList(iol (1) (initOList cmp))
    ```
    matches the pattern `true`
   Test failed. The following errors were reported:

```
 ;;
    Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> (x mod 13) > (y mod 13)) in
   isOrderedList(iol (1) (iol (3) (iol (2) (initOList cmp))))
    ```
    matches the pattern `true`
   Test failed. The following errors were reported:

```
 ;;
    Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> (x mod 13) > (y mod 13)) in
   isOrderedList(iol (62) (iol (53) (iol (19) (iol (46) (iol (3) (iol (89) (iol (91) (iol (47) (initOList cmp)))))))))
    ```
    matches the pattern `true`
   Test failed. The following errors were reported:

```
 ;;
    Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> match (x, y) with (Some a,Some b) -> len a > len b | (Some _,_) | (None,None) -> true | _ -> false) in
   isOrderedList(iol (None) (iol (None) (iol (None) (initOList cmp))))
    ```
    matches the pattern `true`
   Test failed. The following errors were reported:

```
 ;;
  Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> match (x, y) with (Some a,Some b) -> len a > len b | (Some _,_) | (None,None) -> true | _ -> false) in
   isOrderedList(iol (Some []) (iol (None) (iol (None) (initOList cmp))))
    ```
    matches the pattern `true`
   Test failed. The following errors were reported:

```
 ;;
  Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+ Fail: Check that the result of evaluating
    ```ocaml
    let len = List.length and iol = insertOList in
   let cmp = (fun x y -> match (x, y) with (Some a,Some b) -> len a > len b | (Some _,_) | (None,None) -> true | _ -> false) in
   isOrderedList(iol (Some []) (iol (Some [1;2;3;4]) (iol (None) (iol (Some [1;2;3]) (iol (None) (initOList cmp))))))
    ```
    matches the pattern `true`
   Test failed. The following errors were reported:

```
 ;;
  Characters 33-44:
  (let len = List.length and iol = insertOList in
                                   ^^^^^^^^^^^
Error: Unbound value insertOList

```


+  _3_ / _3_ : Pass: Type definition

    Looks good

+  _2_ / _2_ : Pass: `initOList`

    Looks good

+  _4_ / _4_ : Pass: List definitions

    Looks good

+  _3_ / _3_ : Pass: `isOrderedList`

    Looks good

+  _3_ / _3_ : Pass: `insertOList`

    This looks correct

+  _2_ / _2_ : Pass: `olistToList`

    Looks

+ Pass: General comments

    All the functions seem to be named correctly, but for some reason the automated tests did not read in your functions. If this causes any issues in your grade feel free to talk to a TA.

#### Total score: _17_ / _17_

#### Problem 3

+  _1_ / _1_ : Pass: Part 1: recursive case includes `l @ [h]`

    good

+  _1_ / _1_ : Pass: Part 1: recursive case passes a continuation that calls the provided continuation `c`

    good

+  _1_ / _1_ : Pass: Part 1: base case `[] -> (c [])

    good

+  _1_ / _1_ : Pass: Part 1: is tail recursive

    good

+  _2_ / _2_ : Pass: Part 2: basic structure

    good

+  _1.5_ / _1.5_ : Pass: Part 2: the second recursive call is passed along inside of the continuation

    good

+  _0.5_ / _1.5_ : Pass: Part 2: the details of the continuation are right

    need to call the continuation within the second call's function passed to make this tail recursive

+  _1_ / _1_ : Pass: Part 2: base case `Empty -> (c 0)`

    good

#### Total score: _9_ / _10.0_

#### Problem 4

+  _0_ / _2_ : Pass: type definition of dostat in comment

    The goal is to represent a do-while loop. The first step is the define the type of the construct which models do-while. That construct is dostat. Define the type of dostat : (state -> bool) -> (state -> state) -> state.

+ Fail: Check that the result of evaluating
    ```ocaml
    dostat (fun (i, sum, n) -> i < n) (fun (i, sum, n) -> (i+1, sum+i, n)) (0,0,10)
    ```
    matches the pattern `(11, 55, 10)`
   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (dostat (fun (i, sum, n) -> i < n) (fun (i, sum, n) -> (i+1, sum+i, n)) (0,0,10)) = ((11, 55, 10)) ;; ;;
   ^^^^^^
Error: Unbound value dostat

```


+  _2_ / _2_ : Pass: definition of dostat

    

+  _1_ / _1_ : Pass: comment describing state type and actual type definition

    

+  _0.75_ / _1.5_ : Pass: definition of get and put functions

    For your put functions, you need to do exp s, not just s.

+  _3.5_ / _3.5_ : Pass: definition of sumup function

    

+ Fail: Check that the result of evaluating
    ```ocaml
    sumToN 5
    ```
    matches the pattern `15`
   Test failed. The following errors were reported:

```
 ;;
Characters 1-7:
  (sumToN 5) = (15) ;; ;;
   ^^^^^^
Error: Unbound value sumToN

```


+  _1.5_ / _1.5_ : Pass: definition of sumToN

    

#### Total score: _8.75_ / _11.5_

#### Total score: _50.75_ / _54.5_

