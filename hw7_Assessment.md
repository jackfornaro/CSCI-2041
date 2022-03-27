### Assessment for HW7

Run on May 08, 23:10:01 PM.

+ Pass: Change into directory "hws/hw7".

+  _55_ / _59_ : Pass: 

#### Problem 1

+  _4_ / _4_ : Pass: Part 1, call-by-name

    

+  _4_ / _4_ : Pass: Part 2, call-by-value

    

#### Total score: _8_ / _8_

#### Problem 2

+ Fail: Check that the result of evaluating
    ```ocaml
    
    (let ms = mapStream in
    let nat = natStream in
    let ns = nextStream in
    let rec take s n = if n = 0 then [] else let (x, rst) = ns s in (x :: take rst (n - 1)) in
    take (ms (fun x -> x mod 3 == 0) nat) 6)
    ```
    matches the pattern `[true; false; false; true; false; false]`
   Test failed. The following errors were reported:

```
 ;;
        Characters 16-25:
      (let ms = mapStream in
                ^^^^^^^^^
Error: Unbound value mapStream

```


+ Fail: Check that the result of evaluating
    ```ocaml
    
    (let ms = mapStream in
    let nat = natStream in
    let ns = nextStream in
    let rec take s n = if n = 0 then [] else let (x, rst) = ns s in (x :: take rst (n - 1)) in
    take (ms (fun x -> x * (-1)) nat) 3)
    ```
    matches the pattern `[0; (-1); (-2)]`
   Test failed. The following errors were reported:

```
 ;  ;
        Characters 16-25:
      (let ms = mapStream in
                ^^^^^^^^^
Error: Unbound value mapStream

```


+ Fail: Check that the result of evaluating
    ```ocaml
    
    (let ms = mapStream in
    let nat = natStream in
    let ns = nextStream in
    let rec take s n = if n = 0 then [] else let (x, rst) = ns s in (x :: take rst (n - 1)) in
    take (ms (fun x -> if x mod 2 = 0 then Some x else None) nat) 4)
    ```
    matches the pattern `[Some 0; None; Some 2; None]`
   Test failed. The following errors were reported:

```
 ;;
        Characters 16-25:
      (let ms = mapStream in
                ^^^^^^^^^
Error: Unbound value mapStream

```


+  _4_ / _4_ : Pass: mapStream

    

+ Fail: Check that the result of evaluating
    ```ocaml
    
    (let ns = nextStream in
    let rec take s n = if n = 0 then [] else let (x, rst) = ns s in (x :: take rst (n - 1)) in
    take squareStream 8)
    ```
    matches the pattern `[0; 1; 4; 9; 16; 25; 36; 49]`
   Test failed. The following errors were reported:

```
 ;;
      Characters 16-26:
      (let ns = nextStream in
                ^^^^^^^^^^
Error: Unbound value nextStream

```


+ Fail: Check that the result of evaluating
    ```ocaml
    
    (let ns = nextStream in
    let rec take s n = if n = 0 then [] else let (x, rst) = ns s in (x :: take rst (n - 1)) in
    take cubeStream 8)
    ```
    matches the pattern `[0; 1; 8; 27; 64; 125; 216; 343]`
   Test failed. The following errors were reported:

```
 ;;
      Characters 16-26:
      (let ns = nextStream in
                ^^^^^^^^^^
Error: Unbound value nextStream

```


+ Fail: Check that the result of evaluating
    ```ocaml
    
    (let ns = nextStream in
    let rec take s n = if n = 0 then [] else let (x, rst) = ns s in (x :: take rst (n - 1)) in
    take squarecubeStream 8)
    ```
    matches the pattern `[0; 1; 64; 729; 4096; 15625; 46656; 117649]`
   Test failed. The following errors were reported:

```
 ;;
      Characters 16-26:
      (let ns = nextStream in
                ^^^^^^^^^^
Error: Unbound value nextStream

```


+  _3_ / _3_ : Pass: squareStream

    

+  _3_ / _3_ : Pass: cubeStream

    

+  _2_ / _5_ : Pass: squarecubeStream

    General idea is there, but is not well put together and causes compilation error. 

#### Total score: _12_ / _15_

#### Problem 3

+  _2_ / _2_ : Pass: Part 1, `mkstream` definition

    Looks good

+  _5_ / _5_ : Pass: Part 1, `nextStream` definition

    2

+  _2_ / _2_ : Pass: Part 2, `natStream` definition

    Looks good

#### Total score: _9_ / _9_

#### Problem 4

+  _9_ / _9_ : Pass: Part 1, `BTree` definition

    

+  _6_ / _6_ : Pass: Part 2, `IntData` definition

    

+  _2_ / _3_ : Pass: Part 2, `IntBTree` definition

    Should use `BTree`, not `BTREE`

+  _6_ / _6_ : Pass: Part 3, `StringData` definition

    

+  _3_ / _3_ : Pass: Part 3, `StringBTree` definition

    Ok given the above

#### Total score: _26_ / _27_

#### Total score: _55_ / _59_

