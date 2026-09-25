# Phase Space

## Definition

**Phase space** is a mathematical space where each point represents the *complete state* of a system — not just where it is, but also how it's moving. For a single particle moving in 1D, a point in phase space is `(q, p)` = (position, momentum). Knowing that one point tells you everything needed to predict the future (and past) motion.

### Why not just use ordinary space?

Ordinary space (position only) doesn't tell you which way something is heading. Two identical positions with different velocities will evolve completely differently. Phase space fixes this by adding momentum as its own axis.

```
      p (momentum)
      ^
      |        ●  (q, p) = full state:
      |           position AND momentum
      |
      +------------------> q (position)
```

## Example: Simple Harmonic Oscillator

In ordinary space, a mass on a spring just oscillates back and forth on a line — hard to picture the full behavior. In phase space, its state traces a clean **ellipse** (or circle if scaled right):

```
      p
      ^
   ___|___
  /   |   \
 |    |    |---> q
  \___|___/
      |
```

- Top of ellipse: max momentum, q = 0 (moving fastest through equilibrium)
- Right/left edges: p = 0, q = max (momentarily at rest, at the turning points)
- The system endlessly loops around this ellipse — one full loop = one oscillation period.

## Relation to Hamilton's Equations

Phase space is the **stage**; Hamilton's equations are the **rule that moves a point across that stage**.

```
Phase space:      the (q, p) plane — the set of all possible states
Hamilton's eqs:    the velocity field on that plane — which way each point flows
```

```
q̇ = ∂H/∂p          (rate of change of position)
ṗ = -∂H/∂q          (rate of change of momentum)
```

where `H(q, p)` is the Hamiltonian, usually total energy = kinetic + potential.

At every point `(q, p)` in phase space, Hamilton's equations compute an **arrow** — a velocity vector telling that point which direction to move next instant. Doing this at every point produces a **flow field** covering all of phase space:

```
      p
      ^
      |  ↖ ↑ ↗
      |  ← ●  →      each ● has an arrow (q̇, ṗ)
      |  ↙ ↓ ↘        computed from H at that point
      +------------> q
```

A system's actual trajectory is one point riding along this flow, tracing out a curve (e.g., the ellipse for the harmonic oscillator above).

Hamilton's equations require exactly the `(q, p)` pairing — one equation for `q̇` in terms of `∂H/∂p`, one for `ṗ` in terms of `∂H/∂q` — to stay first-order (only single time-derivatives) and symmetric. This is why phase space uses **(position, momentum)** rather than (position, velocity): the math only closes cleanly in this pairing.

| Concept | Role |
|---|---|
| Phase space `(q,p)` | The space of all possible states |
| Hamiltonian `H(q,p)` | A scalar "energy landscape" over that space |
| Hamilton's equations | Turn `H`'s slopes into a flow field on phase space |
| A trajectory | One curve following that flow, starting from one initial point |

Because the flow field from Hamilton's equations is *divergence-free* (like an incompressible fluid), any blob of initial points keeps its volume as it flows — deforming but never compressing or expanding. This is Liouville's theorem, restated in terms of the flow itself, and it is exactly the fact Penrose leans on below.

## Why It Matters

| Feature | Meaning |
|---|---|
| A point in phase space | One exact state of the system (all positions + all momenta) |
| A curve in phase space | The full history/trajectory of the system over time |
| Different starting points | Never cross the same curve (determinism — one state, one future) |
| A *region* (blob) of points | A set of possible states (e.g., uncertain initial conditions) |
| **Liouville's theorem** | Under Hamilton's equations, that blob's *volume* never changes — it can stretch, shear, twist, but never compress or expand |

## Multi-Particle Systems

For N particles in 3D, phase space has `6N` dimensions (3 position + 3 momentum per particle). You can't draw it, but the same logic holds: one point = the entire system's state at an instant.

## The Connection to Penrose

Roger Penrose treats *the entire universe's* configuration as one point in an enormous phase space. His argument: the Big Bang's point sat in an absurdly tiny region of that space (compared to the total volume consistent with the known laws of physics) — quantified by his famous figure of roughly `1` part in `10^10^123`. Because Liouville's theorem says phase-space volume is conserved (never shrinks) under the dynamics, this tiny initial volume cannot be explained as a generic or "typical" starting condition; it demands special explanation.

This is the basis for Penrose's **Weyl curvature hypothesis**: he proposes that gravitational degrees of freedom (encoded in the Weyl tensor) must have been in an exceptionally constrained, low-entropy state at the Big Bang, and that any future theory of quantum gravity should build in a time-asymmetric law forcing this. It is a separate argument from his Gödel-based non-computability claims about consciousness — both appear in his work, but they rest on different formal machinery (phase-space/entropy vs. formal-logic/incompleteness).

- Roger Penrose, *The Road to Reality*, ch. 20 (Lagrangians and Hamiltonians), ch. 27–28 (phase space, entropy, Weyl curvature hypothesis)
- Roger Penrose, *The Emperor's New Mind*, ch. 7

## Related

- [Analytical Mechanics](analytical-mechanics.md)
- [Determinism and Computability](determinism-and-computability.md)
