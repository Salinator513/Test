# Makeshift Multi-Agent Research Test

## Research objective
Under a fixed inference-compute budget, which design features of a role-separated multi-agent research loop most reduce unsupported claims and cumulative reasoning errors compared with repeated single-agent prompting?

## Branch and loop
- Test branch ID: `B001`
- Ordinary role order: Explorer → Critic → Internal Evidence Researcher → External Evidence Researcher → Alternative Theorist → Integrator → Cycle Archivist.
- Control role values: `explorer` → `critic` → `internal_evidence_researcher` → `external_evidence_researcher` → `alternative_theorist` → `integrator` → `cycle_archivist`.
- Each role is a fresh ChatGPT conversation.
- Each cycle is a complete seven-role research loop.
- The Cycle Archivist alone advances the numeric cycle counter.

## Required distinctions
Always distinguish:
- sourced fact
- source interpretation
- derived conclusion
- hypothesis
- speculation
- objection
- unresolved question

Never convert repetition, confidence, eloquence, or agreement between agents using the same model into independent evidence.

## Source rules
- Only the External Evidence Researcher may browse the public web during the ordinary loop.
- Other roles must use only their explicitly allowlisted repository files.
- External research should prioritize primary sources: papers, official documentation, benchmark reports, or original datasets.
- Forums and social media may supply search leads but not factual confirmation unless the claim is specifically about reported user experience or opinion.

## File and isolation rules
- Repository: `Salinator513/Test`
- Work on the default branch `main`.
- Current cycle is stored in `branches/B001/state/control.json`.
- Current accepted branch state is stored in `branches/B001/state/current_state.md`.
- A role may open only the files explicitly allowlisted in its prompt.
- A role may write only the exact output paths explicitly authorized in its prompt.
- Never inspect other repository files, branches, issues, pull requests, commit history, or prior chats unless the prompt explicitly permits it.
- Never modify another role’s output.
- If a required predecessor file is absent, stop without improvising.
- If the authorized output file already exists and the control file still names the current role, verify the saved output and repair only the control transition; do not regenerate the role’s work.
- If the authorized output exists and control already names a later role, report that the role is already complete.

## Output discipline
- Save the complete final response to the authorized GitHub file or files.
- Use explicit claim IDs local to the cycle when helpful, such as `C0001-EXP-01`.
- Refer to prior claims and files exactly.
- State uncertainty and missing evidence directly.
- Do not claim that saving succeeded unless the GitHub write actually succeeded.
- Advance `next_role` only after the role output has been saved successfully.
- The Cycle Archivist updates accepted state and summaries first, then advances the cycle counter last; the control update acts as the completion marker.
