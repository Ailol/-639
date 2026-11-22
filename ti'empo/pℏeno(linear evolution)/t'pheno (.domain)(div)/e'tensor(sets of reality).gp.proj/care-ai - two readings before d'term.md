# care.ai | e'tensor: two readings before d'term

Linked system: [Ailol/Care.Ai](https://github.com/Ailol/Care.Ai), source read twice on 2026-10-26.

Directional data can guide **attention to evidence** without preloading the direction of speech or its conclusion. \`e'tensor\` here is a proposed reading discipline, **not** a claim that Care.Ai already implements it.

\`data % db; op(d'term); observer(a'termion)\`

- **Read 1 / gather:** identify source, observed structure, intended behavior, possible meanings. Preserve original material.
- **Read 2 / challenge:** follow execution paths, compare claims to code, mark contradiction, uncertainty, missing evidence and simulation.
- **d'term / determine:** emit typed, inspectable output only for claims the evidence supports. Otherwise \`pending\`.
- **observer / after:** record actual effect, refusal, error or no-op; do not relabel an intention as completed execution.

Possible JSON-shaped trace (illustrative schema, not a running feature):

\`\`\`json
{
  "source": {"repo": "Ailol/Care.Ai", "ref": "main"},
  "read_1": {"claim": "a workflow can be scheduled"},
  "read_2": {
    "evidence": "WorkflowController.ScheduleWorkflow returns a message but has no scheduler call",
    "status": "unverified_behavior"
  },
  "d_term": {"result": "pending", "needs": "observe registered and triggered job"},
  "observer": {"effect": "not_tested", "trace": []},
  "human_gate": {"required_for_privileged_action": true, "approved": false}
}
\`\`\`

Keep this small: gather -> verify -> determine -> observe. Preserve the mismatch between proposed and actual behavior. This is a **design note**, not executable Care.Ai code or medical authorization.