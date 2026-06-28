# Consciousness Studies — Relationship Map

A map of key researchers and disciplines, and how they relate to each other.

```mermaid
classDiagram
    namespace PhilosophyOfMind {
        class Chalmers {
            Hard Problem of Consciousness
            Property Dualism
        }
        class Nagel {
            Phenomenal Consciousness
            What-it-is-like
        }
        class Dennett {
            Illusionism
            Heterophenomenology
        }
        class Frankish {
            Illusionism
            Quasi-phenomenal Properties
        }
        class Searle {
            Biological Naturalism
            Chinese Room
        }
        class Goff {
            Panpsychism
            Cosmopsychism
        }
    }

    namespace Neuroscience {
        class Tononi {
            Integrated Information Theory
            Phi
        }
        class Koch {
            Neural Correlates of Consciousness
        }
        class Baars {
            Global Workspace Theory
        }
        class Dehaene {
            Global Workspace Theory
            Ignition Model
        }
    }

    namespace CognitiveScience {
        class Friston {
            Free Energy Principle
            Active Inference
        }
        class Clark {
            Predictive Processing
            Extended Mind
        }
    }

    namespace Physics {
        class Penrose {
            Orch-OR
            Quantum Mind
            Mathematical Platonism
        }
        class Hameroff {
            Orch-OR
            Microtubule Hypothesis
        }
    }

    namespace PhilosophyOfMathematics {
        class Einstein_Math {
            Geometry and Experience
            Axiomatics / Formalism
        }
    }

    %% Influences / Inspirations
    Nagel --> Chalmers : inspires

    %% Collaborations
    Koch --> Tononi : collaborates on IIT
    Penrose --> Hameroff : collaborates on Orch-OR
    Einstein_Math --> Penrose : contrasts (formalism vs Platonism)
    Penrose --> Tononi : both raise math-structure-of-consciousness
    Clark --> Friston : collaborates on predictive processing

    %% Extensions / Builds on
    Frankish --|> Dennett : extends illusionism
    Dehaene --|> Baars : extends GWT

    %% Convergences
    Tononi --> Chalmers : converges on irreducibility
    Chalmers --> Goff : influences panpsychism

    %% Debates / Opposition
    Dennett --> Chalmers : opposes (no hard problem)
    Searle --> Dennett : opposes (AI cannot be conscious)
    Tononi --> Baars : debates (IIT vs GWT)
    Penrose --> Dennett : opposes (computation is not consciousness)
```

## Reading the Diagram

| Relation | Meaning |
|---|---|
| `A --> B : inspires` | A's work directly shaped B's framework |
| `A --> B : collaborates` | A and B developed a theory jointly |
| `A --|> B` | A extends or builds on B's position |
| `A --> B : converges on` | A and B arrive at compatible conclusions from different directions |
| `A --> B : opposes` | A's position directly challenges B's |
