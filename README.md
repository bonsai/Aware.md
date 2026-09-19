# Aware.md

> **Aware = 関心・気づき・注意の向き。**

`Aware.md` は、Agent・Team・Repository・MicroWorld が **何に関心を向け、何を認識するか** を宣言する小さなメタデータ規約。

Aware は Skill や Action ではない。  
**世界の状態に対して、何を意識するか** を表す。

## Position

```text
WORLD
  ↓
MicroWorld
  ↓
SYSTEM
  ↓
STATE
  ↓
AWARE
  ↓
SCRUM
  ↓
OPERATION
  ↓
STATE'
```

- **World** = マイクロワールドの総体
- **System** = 構成要素と関係
- **State** = System の現在状態
- **Aware** = State の何に関心を向けるか
- **Scrum** = State に応じて解決する活動
- **Operation** = State を変化させる操作

## Aware = Interest

このプロジェクトでは、基本的に **Aware と Interest を分離しない**。

```text
Aware
= Interest
= 関心・気づき・注意の向き
```

主体が世界のどこを見るか、何を気にするか、何を信号として拾うかを Aware と呼ぶ。

## Aware is not Skill

- **Aware** = 何に気づくか
- **Skill** = 何ができるか
- **Operation** = 実際に何をするか
- **State** = 今どうなっているか
- **Event** = State が変化した記録
- **Health** = State に対する評価

したがって、同じ Skill を持つ Agent でも Aware が異なれば、見るもの・拾うもの・解決するものが異なる。

## Minimal format

```markdown
# Aware

## Mission
<この関心が存在する理由>

## Attention
- <関心 1>
- <関心 2>
- <関心 3>

## Observe
- <何を見るか>

## Detect
- <何の変化・状態を捉えるか>

## Output
- signal
- deviation
- opportunity
- next_attention
```

## Repository Observer

```markdown
# Aware

## Mission
Repository の現在 State と変化に関心を持つ。

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
- significant_change
- inactivity
- new_agent
- blocked_work
- technical_debt
- unusual_activity

## Output
- signal
- deviation
- opportunity
- next_attention
```

## Bonsai / bons.ai

World において、**Bonsai は Scrum を組織する**。

```text
WORLD
  ↓
AWARE
  ↓
Bonsai
  ↓
SCRUM / TEAM
  ↓
Agent
  ↓
Operation
  ↓
STATE'
```

**bons.ai は World に関与する代表的な AI** として、State を観測し、Aware に基づいて Scrum の活動を支援する。

## Design principle

> **World をモデルに合わせるのではなく、World に関心を向け、State を観測し、Scrum を組織する。**

Aware は大きな Ontology ではない。  
**誰が、世界の何に関心を向けているかを表す最小の宣言**である。
