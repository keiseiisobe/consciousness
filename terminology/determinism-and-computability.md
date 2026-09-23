# Determinism and Computability

## Definitions

**Deterministic** describes a *process or system*: given a fixed starting state and inputs, it always produces the same outcome. There is no randomness or branching — the next state is fully fixed by the current one.

**Computable** describes a *problem or function*: whether some algorithm (formally, a Turing machine) can, in principle, produce the answer in finite time, given unlimited time and memory.

These are properties of different things and do not imply each other.

| | Deterministic | Computable |
|---|---|---|
| Applies to | Behavior of a process/system | Existence of an algorithm for a problem |
| Question answered | "Is the next state fixed, or random?" | "Can any algorithm solve this at all?" |
| Opposite | Stochastic / random | Uncomputable / undecidable |

## The Key Separation: Determined but Not Computable

A fact can be fully determined — fixed, well-defined, with no randomness involved — while no algorithm exists that can always compute it in finite time.

The canonical example is the **Halting Problem** (Turing, 1936):

- For any specific Turing machine `T` and input, whether `T` halts is a fixed fact. `T` either halts or runs forever; nothing about this is random. It is fully **determined**.
- However, there is no general algorithm that, given an arbitrary `T` and input, always correctly decides "halts" or "doesn't halt" in finite time. This is proven **undecidable** — the problem is **not computable**.

So: determinism concerns whether an *outcome* is fixed; computability concerns whether a *procedure* can always extract that outcome. The Halting Problem shows these can come apart — reality (or a formal system) can contain facts that are perfectly determinate yet impossible to universally compute.

## Relevance to Consciousness

This distinction matters for debates about whether the mind is computational:

- A system (e.g., the brain) could be entirely deterministic at the physical level, while some aspect of what it does (or produces) is non-computable.
- Roger Penrose uses Gödel's incompleteness theorems to argue that human mathematical understanding may be non-computational, even though brain processes could still be physically determined. "Deterministic ⇒ computable" is not a valid inference, so this is not a contradiction.
- See [Mathematical Proof](mathematical-proof.md) for the caution that such arguments require careful bridge premises connecting formal results to claims about minds.

## Related

- [Mathematical Proof](mathematical-proof.md)
