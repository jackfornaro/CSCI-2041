### Assessment for HW5

Run on April 21, 17:58:31 PM.

+  _23.5_ / _39_ : Pass: 

#### Problem 1

+  _0.5_ / _3_ : Pass: Part a: fib_aux Property

    what is l in this case. There needs to be specifications on f and s for the sequence to be the fibonnaci numbers.

+  _0.5_ / _1_ : Pass: Part b: Inductive hypothesis

    Must do induction on the difference between n and m

+  _0.5_ / _1_ : Pass: Part b: Base case

    fib_aux 0 1 1 1 would not evaluate to 0.

+  _1_ / _3_ : Pass: Part b: Inductive case

    Need to use to the code to prove your property.

+  _0.5_ / _2_ : Pass: Part c: proving fib

    Need to show how fib_aux n 1 1 1 always produces the nth fibonnaci number using your proof

#### Total score: _3_ / _10_

#### Problem 2

+  _1.5_ / _2_ : Pass: Base case

    missing a step in LHS. also Zero != 0

+  _2.25_ / _3_ : Pass: Induction Step

    -.75 missing IH reference, known-fact reference

#### Total score: _3.75_ / _5_

#### Problem 3

+  _2_ / _2_ : Pass: Part a: rev Property

    

+  _1_ / _1.5_ : Pass: Part b: Base case

    you want to prove rev [] l2= []^R + l2 

+  _0.5_ / _0.5_ : Pass: Part b: Inductive hypothesis

    

+  _1_ / _2_ : Pass: Part b: Inductive step

    want to prove rev (x::l1) l2 evals to (x::l1)^R + l2

+  _2_ / _2_ : Pass: Part c: proving reverse

    

#### Total score: _6.5_ / _8.0_

#### Problem 4

+  _0.5_ / _2_ : Pass: Part a

    Incorrect property

+  _0.5_ / _1.25_ : Pass: Part b: Articulating base case and induction step

    For the given property in part (a), this is okay. The quantifier for l is missing, and the inductive hypothesis is not written out explicitly

+  _0.75_ / _1_ : Pass: Part b: Base case

    This works for the property provided

+  _0.25_ / _1.75_ : Pass: Part b: Induction step

    This proof significantly lacks in justification and does not make use of the inductive hypothesis

+  _0.25_ / _2_ : Pass: Part c

    This proof makes use of the property, but it does not use it for justification and it seems to make a big jump to the conclusion

#### Total score: _2.25_ / _8.0_

#### Problem 5

+  _2_ / _2_ : Pass: Base case `P(t = Empty)`

    

+  _0.5_ / _0.5_ : Pass: Inductive Hypothesis `P(l), P(r)`

    

+  _1.5_ / _1.5_ : Pass: Inductive Step set up `P(t = Node(i, l, r))`

    

+  _2_ / _2.0_ : Pass: Inductive Step Case `x < i`

    

+  _2_ / _2.0_ : Pass: Inductive Step Case `x >= i`

    

#### Total score: _8_ / _8.0_

#### Total score: _23.5_ / _39_

