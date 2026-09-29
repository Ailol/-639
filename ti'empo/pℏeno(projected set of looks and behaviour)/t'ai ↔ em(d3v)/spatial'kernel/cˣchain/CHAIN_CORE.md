# cˣchain / Chain Core

[BioChain](https://github.com/Ailol/BioChain) supplies the concrete chain implementation. Its README describes a domain independent BNF compiler that parses, validates, stores, simulates, and analyzes graph programs. The same grammar can take BioChain and LogicChain domain packs.

| Layer | Role in BioChain |
| --- | --- |
| BASE | nodes, edges, and integration/protocol operators |
| PLASTICITY | deltas and cascades |
| META | setpoints and structural/rule programs |
| CONVERGENCE | contours, trajectories, risk, and monitoring |

The implementation lives in [`chain-core/src`](https://github.com/Ailol/BioChain/tree/main/chain-core/src): parser, validator, executor, convergence engine, snapshots, reconstruction, and SpacetimeDB tables. Its EBNF lives in [`xgrammar`](https://github.com/Ailol/BioChain/tree/main/xgrammar). The domain specifications live in [`system-prompts`](https://github.com/Ailol/BioChain/tree/main/system-prompts).

This leaf is a pointer and a boundary: graph compilation and simulation are software behavior; an output about a body or mind needs separate validation before use as health guidance.
