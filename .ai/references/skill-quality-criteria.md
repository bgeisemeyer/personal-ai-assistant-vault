# Skill Quality Criteria

## Purpose
- This reference defines criteria for new and existing skills in the framework.
- It acts as a checklist for design, maintenance, and refactoring.

## Required Criteria

### Name And Description
- The skill name is clear, stable, and descriptive.
- The `description` states the purpose and usage concretely.

### Activation
- It is clear when the skill should be activated.
- Activation cases are concrete and observable.

### Working Method
- The workflow is described in a sensible order.
- Preconditions and required reading steps are clear.
- The skill describes not just goals, but also the order of work.

### Safety Rules
- Risky actions are clearly marked.
- Default behavior is conservative.
- It is clear what must not be done without approval.
- For deletions, it is clearly stated that affected objects must be listed beforehand.
- For deletions, explicit confirmation before execution is required.

### Ask-Before Rules
- It is clear when clarification is required.
- Clarification especially covers risk, ambiguity, permissions, uncertainty, and irreversible steps.
- Deletions and bulk deletions always require a question after a prior list.

### Output Format
- The skill produces a usable output form.
- When later reuse or MCP usage matters, the output is structured enough.

## Architecture Criteria

### Separation Of Central And Local
- Reusable logic lives in the skill.
- Topic-specific rules live in `Index.md` under local context.
- Usage-near templates live close to the topic.

### Reference Need
- Complex decision logic, data models, or source collections are extracted into references.
- The skill is not unnecessarily overloaded.

### No Unnecessary Duplication
- The skill does not duplicate global rules unnecessarily.
- The skill does not duplicate local context unnecessarily.
- The skill does not duplicate existing references unnecessarily.

## Integration Criteria

### MCP And Tool Proximity
- Tool or MCP usage is clearly described when relevant.
- Read-only, write, and risky operations are distinguishable.
- Account, folder, or system differences are considered when relevant.
- If a skill depends on MCPs, servers, or special tools, it includes an early technical availability check.
- That check happens before deeper content work and before further clarification loops.
- If the technical basis is missing, failure communication is clear and direct.
- In that case, the skill does not pretend that substantive work is happening.

### External Sources
- Relevant sources are named.
- It is clear whether sources may be read, described, or modified.

## AI-Agnostic Criteria
- The skill is written so different AIs or tools can continue work consistently.
- Working state, context, and output remain understandable.
- Where needed, local logging is considered.

## Maintenance Criteria For Existing Skills
- Does the skill still fit the current task model?
- Are the references still current?
- Has the skill grown too large?
- Should it be split or merged with another skill?
- Is the language clear enough without unnecessary style policing?

## Final Check
- Is the skill understandable for a future user without extra background?
- Is it clear what the skill does and does not do?
- Is the safety logic clear?
- Is the output useful for the intended work?
- Is the skill more too large than too small?
- Were small, correct structures preferred over larger all-in-one solutions?
