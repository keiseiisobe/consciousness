## A set of all natural numbers (N)

N = {0, 1, 2, 3, ...}

A set is **recursively enumerable (RE)** if there is an algorithm that will eventually output every member of the set (but may run forever when given a non-member).

## A set of all propositions of a formal system (Q)

Propositions can be listed in lexicographic order and put into one-to-one correspondence with N:

```
N = { 0,  1,  2,  3, ... }
      |   |   |   |          (one-to-one correspondence)
Q = { Q0, Q1, Q2, Q3, ... }
```

## A set of all propositions with proofs (P)

An algorithm can check all possible proofs and output a proof P'i when it finds one. The last line of each proof is the proposition it proves:

```
N  = {  0,   1,   2,   3,  ... }
         |        |
Q  = { Q0,  Q1,  Q2,  Q3,  ... }
              |        |         (algorithm finds a proof)
P' = {       P'1,     P'3, ... } (a set of proofs)
              |        |         (last line of the proof is the proposition)
P  = {       P1,      P3,  ... } (provable propositions — a subset of Q)
```

```
complement(P) = { Q0, Q2, ... }  (propositions with no proof)
```

## Is a suspected element in P?

- If it **is** in P → the algorithm eventually halts and outputs a proof
- If it is **not** in P → the algorithm never halts

Now suppose we also had an algorithm for complement(P):

- If it is in complement(P) (i.e. not in P) → that algorithm halts

With both algorithms running in parallel, we could always get the answer to "Is a suspected element in P?" — one of them would eventually halt.

## The complement of P is not recursively enumerable

Logic:
1. P is recursively enumerable — we can enumerate provable propositions.
2. complement(P) is **not** recursively enumerable, because it would require deciding propositions of the form "the n-th Turing machine does not halt on input n," which is undecidable.
3. Therefore P is not recursive (not decidable) — no algorithm can always determine membership.

## Main thrust of Gödel

This means our formal system cannot be complete: there exist propositions that are neither provable nor disprovable within it.

The concept of mathematical truth is only partially accessible by the means of formal argument.

