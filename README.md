# Aware.md

> **Aware is a declaration of what an agent should pay attention to.**

`Aware.md` is a small, human-readable metadata convention for declaring the **attention surface** of an Agent, Workflow, Repository, or Company.

The purpose is not to describe everything an agent can do. It describes **what it should notice, monitor, and bring back as a signal**.

## Core idea

```text
Scene
  ↓
Aware
  ↓
Observe
  ↓
Signal
  ↓
Decision / Action
```

### Aware is not Skill

- **Aware** = what should I pay attention to?
- **Skill** = what can I do about it?
- **Workflow** = when and how should the work happen?
- **Result** = what happened?
- **Deviation** = where did reality differ from expectation?

Therefore an Agent may share Skills while having different Aware definitions.

## Minimal format

```markdown
# Aware

## Mission
<why this attention exists>

## Attention
- <signal 1>
- <signal 2>
- <signal 3>

## Observe
- <what to inspect>

## Detect
- <condition or change to notice>

## Output
- signal
- deviation
- opportunity
- next_attention
```

## Example: Repository Observer

```markdown
# Aware

## Mission
Understand the current state and change of a repository.

## Attention
- activity
- structure
- agents
- workflows
- data
- tools
- issues
- pull_requests
- releases
- dependencies
- deviation

## Observe
- commits
- files
- GitHub Actions
- issues
- pull requests
- repository metadata

## Detect
- significant change
- inactivity
- new agent or workflow
- growing technical debt
- unusual activity
- blocked work

## Output
- repository_metadata
- metrics
- signal
- deviation
- opportunity
- next_attention
```

## Example: CEO

```markdown
# Aware

## Mission
Maintain awareness of company direction and value creation.

## Attention
- mission
- market
- customer
- value
- strategy
- priority
- resources
- risk
- results
- deviation
- opportunity

## Output
- direction
- priority
- start
- stop
- continue
- resource
- next_attention
```

## Company model

`bonsai.company` can use Aware as a common metadata layer across repositories.

```text
GitHub
  ↓
Observation
  ↓
Aware
  ↓
Metadata
  ↓
Statistics
  ↓
bonsai.company
  ↓
CEO Attention
```

A repository may contain agents, data, tools, workflows, code, schemas, and UI in any arrangement. Aware does not require physically separating them. Instead, metadata makes the organization observable.

## Design principle

> **Do not organize reality to fit the model. Observe reality and let metadata describe it.**

Aware is therefore intentionally small. It is an attention contract, not an ontology of everything.
