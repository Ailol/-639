# BioChain — model a cascade and explicitly mark its limits

**Input:** defined signals, interactions, biological context, units, evidence and time.
**Output:** a simulation with assumptions and inspectable state transitions.
**Check:** compare each transform to its source code, inputs, test fixtures and domain vocabulary.

Observed pipeline in repository prompts: BASE → PLASTICITY → META → CONVERGENCE. Rust components include simulation, snapshot diff, reconstruction and convergence work. Domain-agnostic IR and some semantic validation remain incomplete.

Sources: https://github.com/Ailol/BioChain/tree/main/chain-core/src and https://github.com/Ailol/BioChain/tree/main/system-prompts

Pfeno/pheno, io/hum and chemistry/pharmacology can be useful conceptual boundaries. They do NOT license inferred patient diagnoses, genetic traits, intentions or treatments.
