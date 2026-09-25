# Analytical Mechanics

## Definition

**Analytical mechanics** is a reformulation of classical (Newtonian) mechanics that replaces vector forces with scalar functions—kinetic and potential energy—combined with a variational principle. Instead of writing Newton's second law directly for each body, one expresses the system's energies in **generalized coordinates** and derives the equations of motion from a single scalar quantity (the Lagrangian or Hamiltonian).

Its purpose is the same as Newtonian mechanics: given initial conditions, predict a system's position and velocity (its trajectory) at any later time. What changes is the method, not the goal.

## Core Distinctions

| | Newtonian mechanics | Analytical mechanics |
|---|---|---|
| Core law | F = ma (vector, per body) | Euler–Lagrange or Hamilton's equations (scalar, energy-based) |
| Input | Forces, including constraint forces (tension, normal force) | Kinetic and potential energy (T, V) in generalized coordinates |
| Output | x(t), v(t) | q(t), p(t) — same trajectory, different coordinates |
| Handling of constraints | Must solve for constraint forces explicitly | Constraint forces vanish automatically from the formalism |
| Coordinate system | Naturally Cartesian | Works in any generalized coordinates (angles, arc length, etc.) |

## Two Formulations

```text
Lagrangian mechanics:
  L(q, q̇, t) = T - V
  d/dt (∂L/∂q̇) - ∂L/∂q = 0        (Euler-Lagrange equation)

Hamiltonian mechanics:
  H(q, p, t) = T + V
  q̇ = ∂H/∂p,   ṗ = -∂H/∂q          (Hamilton's equations)
```

- **Lagrangian mechanics** is often more convenient for deriving equations of motion, especially with constraints.
- **Hamiltonian mechanics** recasts the same physics in phase space (position and momentum treated symmetrically), which generalizes more directly to statistical mechanics and quantum mechanics.

## Why It Matters

- **Generality**: Handles constrained and complex systems (pendulums, rigid bodies, orbital mechanics) more cleanly than raw force analysis.
- **Simplification**: Constraint forces drop out automatically, so there is no need to solve for tension, normal force, etc., separately.
- **Symmetry and conservation**: Noether's theorem connects continuous symmetries (e.g., time-translation invariance, rotational invariance) to conserved quantities (energy, momentum, angular momentum)—an insight not transparent in the Newtonian formulation.
- **Bridge to modern physics**: The Hamiltonian formulation leads directly into quantum mechanics (Hamiltonians, Poisson brackets → commutators) and statistical mechanics (phase space), making analytical mechanics a conceptual bridge rather than a mere alternative notation.

## Related

- [Phase Space](phase-space.md)
- [Determinism and Computability](determinism-and-computability.md)
