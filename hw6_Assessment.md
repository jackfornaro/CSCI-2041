### Assessment for HW6

Run on April 24, 15:02:39 PM.

#### Sanity Checks

+ Pass: Change into directory "hws/hw6".

+ Pass: Check that file "prob1.ml" exists.

##### Problem 1

+  _6_ / _6_ : Pass: Problem 1: Code structure

    

+ Pass: Is the problem solved using exceptions?

    yes

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041] [(2041, [])] ["csci"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041] [(2041, [])] ["csci"; "ocaml"; "fun"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041; 4011] [(2041, []); (4011, [])] ["csci"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041; 5165] [(2041, []); (5165, [])] ["csci"; "math"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041; 5165] [(2041, [5165]); (5165, [2041])] ["csci"; "math"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041; 5581] [(2041, [5581]); (5581, [2041])] ["csci"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [1901; 1902; 2041] [(1901,[1902]);(1902,[1901;2041]);(2041,[1902])] ["csci";"scheme"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [1901; 1902; 8441; 8442] [(1901,[1902]);(1902,[1901]);(8441,[8442]);(8442,[8441])] ["csci";"math"]
  ```

#### Sanity Checks

+ Pass: Check that file "prob2.ml" exists.

##### Problem 2

+  _6_ / _6_ : Pass: Problem 2: Code structure

    

+ Pass: Is the problem solved using continuations?

    yes

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041] [(2041, [])] ["csci"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041] [(2041, [])] ["csci"; "ocaml"; "fun"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041; 4011] [(2041, []); (4011, [])] ["csci"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041; 5165] [(2041, []); (5165, [])] ["csci"; "math"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041; 5165] [(2041, [5165]); (5165, [2041])] ["csci"; "math"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [2041; 5581] [(2041, [5581]); (5581, [2041])] ["csci"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [1901; 1902; 2041] [(1901,[1902]);(1902,[1901;2041]);(2041,[1902])] ["csci";"scheme"]
  ```

+  _0.5_ / _0.5_ : Pass: Verifies that all graph colorings are found for:
  ```ocaml
  color_graph [1901; 1902; 8441; 8442] [(1901,[1902]);(1902,[1901]);(8441,[8442]);(8442,[8441])] ["csci";"math"]
  ```

#### Total score: _20_ / _20.0_

