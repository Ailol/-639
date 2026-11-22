# care.ai | a'pattern: trust before op

Source: [Ailol/Care.Ai](https://github.com/Ailol/Care.Ai), main, static reading on 2026-10-26. No live endpoint or exploit was tested.

\`request % identity; op(execute); observer(authz)\`

A request may supply data; it must not manufacture the authority to act on that data.

- [MockAuthenticationHandler.cs](https://github.com/Ailol/Care.Ai/blob/main/src/Care.Ai.Api/Authentication/MockAuthenticationHandler.cs) gives roles from client-supplied \`X-User-Type\` and identity from \`X-User-Id\`. Development simulation, **not trusted authentication**.
- [WorkflowController.cs](https://github.com/Ailol/Care.Ai/blob/main/src/Care.Ai.Api/Controllers/WorkflowController.cs) has execution/save/delete actions without explicit \`[Authorize]\`; it seeks a \`UserId\` claim not supplied by the mock handler, then falls back to \`anonymous\`.
- [ChatController.cs](https://github.com/Ailol/Care.Ai/blob/main/src/Care.Ai.Api/Controllers/ChatController.cs) and [KernelController.cs](https://github.com/Ailol/Care.Ai/blob/main/src/Care.Ai.Api/Controllers/KernelController.cs) select actor IDs from the caller's \`UserId\`, not a proven principal.
- Public \`.env\` has a non-placeholder \`AZURE_DEVOPS_PAT\` value. **Do not reproduce it**. Treat as potentially exposed: revoke/rotate, scrub repository history where feasible, and ignore local \`.env\` thereafter.

Minimum gate before production: verified login -> authorized actor/workflow scope -> validated tool/function allowlist -> human approval for privileged/medical actions -> recorded result. Never equate an asserted role with a verified one.

\`affinity != conformity; respect != surrender; change != coercion.\`

**Trace:** source reading, not runtime verification.