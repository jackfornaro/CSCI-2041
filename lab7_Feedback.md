### Feedback for Lab 07

Run on March 06, 14:17:14 PM.

#### Preliminary Checks

+ Pass: Change into directory "labs/lab07".

+ Pass: Check that file "lab07.ml" exists.

+ Pass: Check that an OCaml file "lab07.ml" has no syntax or type errors.

    OCaml file "lab07.ml" has no syntax or type errors.



#### Test Cases

##### map2

+ Pass: Check that the result of evaluating
   ```
   map2 (fun x y -> x + y) [1;2;3] [4;5;6;7]
   ```
   matches the pattern `[5;7;9]`.


+ Pass: Check that the result of evaluating
   ```
   map2 (fun x y -> x^y) ["Hello "; "CSCI"] ["World!"; "2041"]
   ```
   matches the pattern `["Hello World!"; "CSCI2041"]`.


##### union (Any permutation of the list is correct)

+ Fail: Check that the result of evaluating
   ```
   union [1;2;3;4] [3;4;5;6]
   ```
   matches the pattern `[1;2;3;4;5;6]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (union [1;2;3;4] [3;4;5;6]) = ([1;2;3;4;5;6]) ;; ;;
   ^^^^^
Error: Unbound value union

```


##### unzip

+ Fail: Check that the result of evaluating
   ```
   unzip [(4,3);(6,7);(3,5);(9,2)]
   ```
   matches the pattern `([4; 6; 3; 9], [3; 7; 5; 2])`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (unzip [(4,3);(6,7);(3,5);(9,2)]) = (([4; 6; 3; 9], [3; 7; 5; 2])) ;; ;;
   ^^^^^
Error: Unbound value unzip

```


+ Fail: Check that the result of evaluating
   ```
   unzip [("a","d");("b","e");("c","f")]
   ```
   matches the pattern `(["a";"b";"c"], ["d";"e";"f"])`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-6:
  (unzip [("a","d");("b","e");("c","f")]) = ((["a";"b";"c"], ["d";"e";"f"])) ;; ;;
   ^^^^^
Error: Unbound value unzip

```


##### zip

+ Fail: Check that the result of evaluating
   ```
   zip [1;2;3] [4;5;6;7]
   ```
   matches the pattern `[(1, 4); (2, 5); (3, 6)]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-4:
  (zip [1;2;3] [4;5;6;7]) = ([(1, 4); (2, 5); (3, 6)]) ;; ;;
   ^^^
Error: Unbound value zip

```


+ Fail: Check that the result of evaluating
   ```
   zip [] [1]
   ```
   matches the pattern `[]`.

   Test failed. The following errors were reported:

```
 ;;
Characters 1-4:
  (zip [] [1]) = ([]) ;; ;;
   ^^^
Error: Unbound value zip

```


