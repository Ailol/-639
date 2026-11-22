# care.ai | ee'nit: mock != observed

Source: [Ailol/Care.Ai](https://github.com/Ailol/Care.Ai) main, code-read 2026-10-26. No build or runtime tests executed.

\`simulate % obs; op(validate); observer(effect)\`

Granular mismatches to test, not assumptions of failure:

1. [WorkflowController.cs](https://github.com/Ailol/Care.Ai/blob/main/src/Care.Ai.Api/Controllers/WorkflowController.cs): schedule action replies "Workflow scheduled" but explicitly contains no scheduling implementation. **Response != effect**.
2. [design/test_workflow.py](https://github.com/Ailol/Care.Ai/blob/main/design/test_workflow.py): mock AI, human approval, nested workflow and code handlers. YAML examples use \`Prompt\` / \`Ref\` / \`Assign\`, while the Python runner reads \`prompt\` / \`ref\` / \`assign\`. Test the case/schema contract.
3. [Care.Ai.sln](https://github.com/Ailol/Care.Ai/blob/main/Care.Ai.sln) and [Care.Ai.Api.csproj](https://github.com/Ailol/Care.Ai/blob/main/src/Care.Ai.Api/Care.Ai.Api.csproj) reference \`packages/Care.AI/Care.AI.csproj\`, absent from the current main tree. Establish dependency before build claims.
4. [Care.Ai.AppHost.csproj](https://github.com/Ailol/Care.Ai/blob/main/Care.Ai.AppHost/Care.Ai.AppHost.csproj) references a differently-cased \`src/Care.AI.Api\` directory than tracked \`src/Care.Ai.Api\`. Verify on case-sensitive filesystem.
5. [docs/ARYA.md](https://github.com/Ailol/Care.Ai/blob/main/docs/ARYA.md) describes conversational actions; distinguish documentation from implemented routes and durable scheduled work.

Observations required before \`d'term(success)\`: clean restore/build; schema tests; denied cross-user access; actual scheduler registration and firing; non-mock approval holding state until an authorized human acts.

\`mock % proposal; observed % evidence; d'term(success)\` only after evidence.