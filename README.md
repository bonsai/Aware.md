# Aware.md

> **Aware = Agent が現在、意識・認識しているもの。**

Aware は Concern と分ける。

- **Concern** = 何を心がける／見ようとする／見るべきとするか
- **Aware** = いま何に気づいている／認識しているか
- **Observation** = 実際に観測した事実

## Position

```text
AGENT
  ↓
CONCERN
  ↓
ATTENTION
  ↓
AWARENESS
  ↓
OBSERVATION
  ↓
STATE
```

Concern が「見る方向」を決め、Attention がその方向へ注意を向け、Aware はその結果として Agent の現在の認識に上がっているものを表す。

## Concern と Aware

### Concern

Agent ごとに異なる。

```text
Concern
├─ Care       心がけている
├─ Intention  見ようとしている
└─ Priority   見るべき
```

Concern は、まだ気づいていない対象も含む。

### Aware

Agent が現在認識しているもの。

「見るべき」と定めているだけでは Aware ではない。

```text
Concern
  ↓
「異常を見るべき」
  ↓
Observation
  ↓
「API の応答時間が急増した」
  ↓
Aware
```

## Aware is not

- **Concern** = 関心の方向
- **Aware** = 現在の認識
- **Observation** = 観測された事実
- **State** = System の現在状態
- **Health** = State に対する評価
- **Skill** = できること
- **Goal** = 到達したい状態
- **Issue** = 解決対象
- **Operation** = 状態を変化させる操作

## Minimal format

```yaml
aware:
  - subject: <認識している対象>
    observation: <観測内容>
    significance: <なぜ意識に上がっているか>
    confidence: <認識の確度>
    observed_at: <時刻>
```

最小構成なら、単に対象と観測内容だけでもよい。

```yaml
aware:
  - subject: repository
    observation: new_pull_request
```

## Stateとの関係

Aware は State そのものではない。

```text
STATE
  ↓
OBSERVATION
  ↓
AWARE
  ↓
ISSUE
  ↓
OPERATION
  ↓
STATE'
```

同じ State でも Agent の Concern が違えば、Aware になる対象は異なる。

## Agent

Aware は Agent が持つ現在の認識である。

```text
AGENT
├─ CONCERN   何を気にするか
├─ AWARE     今なにに気づいているか
├─ SKILL     なにができるか
├─ GOAL      どこへ進みたいか
├─ ISSUE     なにを解決するか
└─ OPERATION なにをするか
```

複数 Agent が同じ World を見ても、Concern と Observation が異なれば Aware は異なる。

## Principle

> **Concern は見る方向。Aware は、いま見えているもの。**

Aware は「意識そのもの」を哲学的に定義するための大きな概念ではなく、Agent が現在扱える認識を表す最小の状態として扱う。
