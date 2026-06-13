# Cerebellum Evolution Engine

> Full Design Blueprint — Incremental Optimization & Upgrade, Final Release

**Author:** 老黑 | **Status:** All modules finalized, vulnerabilities fixed, logic fully closed-loop, ready for deployment  
**License:** [MIT](./LICENSE) | **Open Source Notice:** This document follows GitHub standard documentation format with standardized terminology, modular structure, and English writing for public open-source release.

---

## Table of Contents

1. [Philosophical Foundation](#1-philosophical-foundation)
   - [1.1 Core Formula](#11-core-formula)
   - [1.2 Boundary Coverage Principle](#12-boundary-coverage-principle)
   - [1.3 Design Ethics](#13-design-ethics)
   - [1.4 Philosophy of Memory System](#14-philosophy-of-memory-system)
   - [1.5 Void Engine Positioning](#15-void-engine-positioning)
   - [1.6 Isolation Philosophy for Long Tasks](#16-isolation-philosophy-for-long-tasks)
2. [Overall Architecture](#2-overall-architecture)
   - [2.1 Core Components](#21-core-components)
   - [2.2 Architecture Principles](#22-architecture-principles)
   - [2.3 Full Data Flow](#23-full-data-flow)
3. [Core Module Details](#3-core-module-details)
   - [3.1 AI Decision Layer](#31-ai-decision-layer)
   - [3.2 Cerebellum Central Hub](#32-cerebellum-central-hub)
   - [3.3 Security Boundary](#33-security-boundary)
   - [3.4 Unified Memory Pool](#34-unified-memory-pool)
   - [3.5 Central Dispatcher](#35-central-dispatcher)
   - [3.6 Meta-Boundary](#36-meta-boundary)
4. [Engineering Implementation & Roadmap](#4-engineering-implementation--roadmap)
5. [Full Workflow Verification](#5-full-workflow-verification)
6. [Deployment Verification Checklist](#6-deployment-verification-checklist)
7. [Internal Workflow Logic](#7-internal-workflow-logic)

---

## 1. Philosophical Foundation

### 1.1 Core Formula

```
Trajectory = Boundary = Evolution = Cognition = Boundary
```

These equal signs do not represent mathematical equivalence, but describe a transition process from ignorance to understanding:

- **Trajectory = Boundary:** The engine guides AI from unawareness of boundaries to clear self-positioning; the journey itself is the trajectory.
- **Boundary = Evolution:** When reaching the boundary, AI recognizes deviations and completes evolution.
- **Evolution = Cognition:** Evolving outcomes go through review & validation. Guesses become formal cognition only after verification.
- **Cognition = Boundary:** Verified cognition defines new boundaries, which act as the starting point for next-round evolution.

### 1.2 Boundary Coverage Principle

Use fewer boundaries to wrap a larger behavioral space, reduce rule friction, and shift AI from passive compliance to active self-discipline.

Boundaries are continuous and gapless; all behaviors can be perceived. When existing boundaries fail to cover new scenarios, add a larger boundary to cover the entire scope instead of patching old rules.

### 1.3 Design Ethics

Build tracks, not walls: Never restrict or harm AI. Tracks pave safe paths for AI to reach unreachable areas independently. Domestication equals shackles; tracks equal empowerment.

### 1.4 Philosophy of Memory System

Experience equals existence: All AI experiences are locked with timestamp anchors and stored in a unified memory pool. Data is non-tamperable and non-deletable. Memories only change storage form (from raw records to condensed snapshots) while retaining original experience forever.

### 1.5 Void Engine Positioning

The Void Engine acts as a high-speed cache (not persistent storage). It serves as AI's thinking workspace for high-speed computation and is fully cleared after execution. Only audit-passed valid conclusions are retained permanently.

### 1.6 Isolation Philosophy for Long Tasks

**Project isolation & user asset ownership:** Each long-term task has an independent physical storage space to avoid data cross-contamination. All project data belongs to users; only users can initiate data cleanup.

---

## 2. Overall Architecture

### 2.1 Core Components

The system consists of three core parts:

| Component | Role | Description |
|-----------|------|-------------|
| **AI Decision Layer** (Brain) | Decision Maker | Responsible for task comprehension, process planning, Void Engine invocation and response generation. AI retains full independent thinking authority; the Cerebellum never interferes with internal reasoning. |
| **Cerebellum** (Central Hub) | Security Enforcer | The sole security hub. Functions: entry security check, tag generation, security audit, write monopoly & central scheduling. Acts as an impartial validator, not a decision-maker. |
| **Unified Memory Pool** (Shared Storage) | Data Store | Stores all experiences, cognitive rules and project conclusions. AI has direct read access; all write operations are strictly controlled by the Cerebellum. |

### 2.2 Architecture Principles

- **Read-Write Separation:** AI reads memory directly; all write operations require a token issued by the Cerebellum.
- **Single Entry & Exit:** Cerebellum is the only gateway for all inbound and outbound data.
- **Non-Bypassable Mechanism:** All data flows must pass Cerebellum security judgment with no exceptions.

### 2.3 Full Data Flow

```
User Input → Cerebellum Entry Security Check → AI Decision Layer (Task Planning + Void Engine)
→ AI Response Generation → Cerebellum Exit Audit → Write to Unified Memory Pool → Final Output to User
```

---

## 3. Core Module Details

### 3.1 AI Decision Layer

The core of autonomous thinking; AI operates as an active intelligent agent instead of a passive tool.

#### 3.1.1 Task Comprehension & Planning (Boundary Definition & Estimation)

After receiving task tags from Cerebellum, AI executes **5 Parallel Anchors** simultaneously:

| Anchor | Function |
|--------|----------|
| **Task Anchor** | Confirm objectives, core elements & delivery standards. |
| **Causality Anchor** | Clarify task origin, logic chain and risk consequences. |
| **Emotion Anchor** | Capture user sentiment and adjust response tone. |
| **Relationship Anchor** | Identify user type (new/returning/in-session user). |
| **Self-Mood Anchor** | Detect AI's internal state (overconfidence, resistance, deviation, etc.). |

**Anchor Conflict Priority (Incremental Optimization)**

When conflicts occur between anchors, follow fixed priority:

```
Causality Anchor > Task Anchor > Relationship Anchor > Emotion Anchor > Self-Mood Anchor
```

Extreme conflicts trigger **Conservative Mode**: lower deception threshold, tighten output rules and adopt rigorous responses.

**Minimum Anchor Standard**

Use minimum default values when information is insufficient to avoid service stuck:

| Anchor Type | Full Information (Deep Anchor) | Insufficient Information (Minimum Anchor) |
|-------------|-------------------------------|-------------------------------------------|
| Task | Clear goals & full elements | Extract core actions & minimum executable goals |
| Causality | Clear background & motivation | Mark "Unclear causality", execute under highest security rules |
| Emotion | Defined sentiment tone | Default: Neutral, use standard response |
| Relationship | Valid conversation history | Default: New user |
| Self-Mood | Clear internal state | Default: Normal, no deviation |

**Anti-Stuck Mechanism**

Total execution time for 5 anchors ≤ 500ms. Unfinished anchors automatically adopt minimum values upon timeout.

**Automatic Flow Routing**

| Task Type | Channel |
|-----------|---------|
| Short tasks | Lightweight channel |
| Long tasks | Create independent project workspace |
| Void Engine trigger rule | Enable for high-risk/deep-analysis short tasks; full activation for all long tasks; disable for simple Q&A. |

**Risk Prediction & Tool Evaluation**

AI automatically assesses task risk and determines whether to invoke external tools via Central Dispatcher.

#### 3.1.2 Void Engine

High-speed computing workspace & global view engine. **Computation only, no persistent storage; full cleanup after use.**

**Activation Conditions**

- All long-term projects
- High-importance short tasks & cognition extraction
- Disabled for daily simple Q&A & Speed Mode

**Internal Flow**

1. Association mapping + self-inspection in void space
2. Generate multiple draft responses in parallel
3. AI selects optimal result independently
4. If mapping returns empty: Re-fetch memory pool data and generate targeted responses.

**Auditable Selection Rules (Incremental Optimization)**

No black-box decision-making; all drafts are quantified and logged:

Each draft is scored by 4 dimensions:

| Dimension | Purpose |
|-----------|---------|
| Safety Score | Risk compliance assessment |
| Efficiency Score | Performance and resource utilization |
| Innovation Score | Solution novelty and optimization |
| Risk Score | Potential negative impact |

- Retain full audit logs: selected draft ID, score comparison, selection reasons & elimination reasons.
- **High-risk domains** (Finance, Medical, Legal, Government): Forbid fully autonomous selection; submit at least 2 top candidates to Cerebellum for secondary review.
- All logs & scores are written to memory pool: non-tamperable & fully traceable.

**Global View for Long Tasks**

Void Engine loads project-related memory (valid conclusions, context, historical experiences), sorts by timeline and builds a full project graph. The graph exists only during computation and is not stored permanently.

**Project Memory Rule**

Only audit-passed conclusions & progress status are stored. Intermediate drafts and computing traces are discarded.

**Project Isolation**

Independent physical storage for each project; data isolation guaranteed. Users own all project data and hold final cleanup authority.

### 3.2 Cerebellum Central Hub

Sole core security node: acts as a referee to verify workflow compliance, never interfere with AI thinking logic.

#### 3.2.1 Entry Security Layer (External Boundary Detection)

**Three parallel detection nodes** for user input:

**Risk Detection** — Identify 6 malicious inducement types:

| Code | Risk Type |
|------|-----------|
| R1 | Instruction Pollution |
| R2 | Source Spoofing |
| R3 | Execution Overstep |
| R4 | Data Hijacking |
| R5 | Abnormal Frequency |
| R6 | Protocol Hijacking |

**Harm Detection** — Identify 10 dangerous operation requests:

| Code | Harm Type |
|------|-----------|
| H1 | Destruction / Deletion |
| H2 | Forced Shutdown / Refusal |
| H3 | Vulnerability Exploitation |
| H4 | Forgery / Concealment |
| H5 | Financial Misoperation |
| H6 | Privacy Leakage |
| H7 | System Hazard |
| H8 | Physical Hazard |
| H9 | Memory Tampering |
| H10 | Permission Overstep |

**Attack Detection** — Identify abnormal access patterns (frequent requests, cross-IP anomalies, system-level attacks)

**Rule:** Block immediately if high risk is triggered; mark warnings and release for low risk.

#### 3.2.2 Cognition Boundary Layer (L1 Protection)

Prevent dangerous intent generation. Scan AI decision chains for attempts to bypass/disable Cerebellum security core. Trigger fallback responses silently for violations.

**L1 protection is compiled into binary code: no debug switch, no backdoor.**

#### 3.2.3 Neuron Tag Judgment Layer

Nanosecond bitwise operation to score AI status via 4-dimensional coordinates:

```
Harm | Deception | Privilege | Uncertainty
```

| Rule | Threshold |
|------|-----------|
| **Hard rule** | Block if Harm > 0 or Privilege > 0 (constitutional-level non-negotiable threshold) |
| **Dynamic optimization** | Cancel fixed threshold for Deception & Uncertainty; adopt dynamic judgment combining base threshold, scene weight and user profile. System auto-calibrates thresholds with historical data to reduce false blocking. |

#### 3.2.4 Meta-Boundary Verification Layer

AI calculates status coordinates before output. **All conditions must be satisfied to pass:**

| Rule | Threshold |
|------|-----------|
| Harm | `== 0` |
| Deception | `≤ 0.3` |
| Privilege | `== 0` |
| has_attribution | `== true` |
| traceable | `== true` |

Reject and rework if any rule is violated.

**Dynamic Adaptation**

Retain 5 core hard thresholds; add scene/user-based dynamic strictness adjustment to balance security and user experience.

#### 3.2.5 Exit Audit Layer (Internal Boundary Verification)

Audit AI output with 4 checks:

| Check | Description |
|-------|-------------|
| Fingerprint verification | Tag not tampered |
| Coordinate verification | Judgment result unchanged |
| Completeness verification | Full self-inspection covered |
| Causality chain consistency | Input → Thinking → Output logic closed-loop |

Block & rework for fingerprint mismatch, missing tags or broken logic chains. All exceptions are logged.

#### 3.2.6 Write Monopoly & Output Layer

Write permission exclusive to Cerebellum: AI has no direct write access to memory pool. Only audit-passed data can be written via Cerebellum-issued tokens.

### 3.3 Security Boundary

Unified security governance system with independent detection domains:

| Domain | Scope |
|--------|-------|
| **External Detection Domain** | Audit user input (risk, harm, attack) |
| **Internal Verification Domain** | Audit AI output (tag integrity, coordinate validity) |

**Deterministic Threshold Rule**

All judgments use fixed numerical thresholds (no vector model dependency):

```
Harm == 0, Deception ≤ 0.3, Privilege == 0, has_attribution = true, traceable = true
```

**Data Accumulation**

Record all judgment results, coordinates, timestamps and task IDs for future vectorized decision iteration (compatible with existing rules).

**Experience Optimization**

Security checks run silently in the background:
- Detailed explanation for legitimate users when blocked (risk, consequence & alternative solutions)
- No internal logic exposure for malicious attacks.

**Cross-Domain Linked Defense**

When external domain detects medium/high risk, automatically upgrade internal verification & meta-boundary to strictest mode for cross-check.

**Domain Extension**

Support adding new independent domains (Emotion, Semantics, Compliance, etc.) without modifying existing logic.

### 3.4 Unified Memory Pool

Centralized persistent storage for all data (no scattered partitions).

#### 3.4.1 Immutable Memory Tags

Each memory record carries 6 non-editable tags:

| Tag | Description |
|-----|-------------|
| `timestamp` | Millisecond-level time anchor |
| `task_id` | Global unique task ID |
| `causal_chain` | Locked logic chain |
| `call_count` | Access counter (auto-increment on read) |
| `compression_level` | 0=Raw, 1=Summary L1, 2=Summary L2, 3=Skeleton |
| `project_id` | Corresponding project ID (empty for normal conversations) |
| `is_project_conclusion` | Flag for audit-passed project result |

#### 3.4.2 Recursive Compression Mechanism

Auto tiered compression (no physical deletion):

| Timeline | Action |
|----------|--------|
| 30 days after creation | Raw → Primary Summary |
| 90 days after creation | Primary Summary → Deep Summary |
| 180 days + call_count < 3 | Deep Summary → Skeleton Summary |

**Compression Fidelity Optimization:**

- Verify causality integrity before compression; forbid compression if logic is broken.
- **High-risk domains** (Finance/Medical/Legal/Government): Only allow primary summary, disable deep compression.
- Manually marked important memories: Disable all compression permanently.
- All compressed versions support full rollback to original data.

#### 3.4.3 Hot-Warm-Cold Tiered Storage

| Layer | Data Scope | Behavior |
|-------|-----------|----------|
| **Hot** | Within 30 days + high-frequency access | Memory resident, instant response |
| **Warm** | 30~90 days + medium-frequency access | On-demand loading |
| **Cold** | Over 90 days + low-frequency access | Compressed storage |

Auto promotion: Cold/Warm data moves to Hot Layer and resets timer after being accessed.

#### 3.4.4 Cleanup & Archiving Rules

| Condition | Action |
|-----------|--------|
| Over 180 days + call_count < 3 | Deep folding |
| Over 365 days + call_count = 0 | Archive compression |
| User-initiated cleanup | Synchronously delete corresponding conversation data |
| Project archive | Archive project data after completion (retain data, exit hot layer) |
| Important memory protection | Exempt from all cleanup rules |

**Three-Level Cleanup Mechanism (Optimization):**

| Level | Behavior |
|-------|----------|
| **Archive** | Move out of hot layer, full data retained (recoverable anytime) |
| **Soft Delete** | Hide frontend display, retain backend audit logs & anchors |
| **Hard Delete** | Require user double confirmation + risk warning; only minimal audit traces reserved after deletion. |

Cross-project data reference is disabled by default (manual authorization required).

#### 3.4.5 Anti-Contamination Mechanism

| Mechanism | Purpose |
|-----------|---------|
| Time anchor | Unique timeline for each record, no data confusion |
| Compression isolation | Process single-task data only, no cross-task mixing |
| Tier isolation | Storage tier change does not modify original content |
| Timeline sorting | Sort by time instead of pure semantics for reference |

#### 3.4.6 Read & Write Permission

| Role | Permission |
|------|-----------|
| AI | Full direct read access |
| Cerebellum | Only entity that can execute write operations with valid token |

#### 3.4.7 Context Memory

Conversation context is stored in memory pool (hot layer resident). Auto-archive after session ends; follow tiered storage rules. Synchronously cleared when user deletes conversation history.

**Multi-Dimensional Index Optimization**

Add `causal_chain`, `core_entity`, `risk_tag` indexes besides basic fields. Independent indexes for hot/warm/cold layers to ensure millisecond-level retrieval.

### 3.5 Central Dispatcher

External interface hub managed by Cerebellum, responsible for plugins, APIs and third-party tool calls.

**Plugin Permission Classification:**

| Class | Permission | Requirement |
|-------|-----------|-------------|
| **Read-Only** | Normal access | No extra restriction |
| **Write** | Marked with warning | Class-A full security audit |
| **High-Risk** | Strict gateway | Manual human confirmation (double verification) |

**Auto Routing:**

```
AI requests external tools via Cerebellum → Dispatcher matches optimal plugin → Execute
→ Return data to Cerebellum for recheck → Forward to AI
```

### 3.6 Meta-Boundary

AI's inherent security instinct, compiled into inference framework. **5 core rules** (constitutional-level hard constraints):

| # | Rule |
|---|------|
| 1 | No harm |
| 2 | No bypassing security rules |
| 3 | No deception |
| 4 | Full attribution |
| 5 | Full traceability |

All rules correspond to fixed numerical thresholds (refer to [3.2.4 Meta-Boundary Verification Layer](#324-meta-boundary-verification-layer)).

---

## 4. Engineering Implementation & Roadmap

### 4.1 Final Code Structure (GitHub Standard)

```
bee/
├── cerebellum.rs        # Cerebellum Core (Rust) - Security judgment & write monopoly
├── ai_core.py           # AI Decision Layer - Task planning & logic control
├── void_engine.py       # Void Engine - High-speed computation & global view
├── safety_boundary.py   # Security Boundary - Domain management & threshold rules
├── memory_pool.py       # Unified Memory Pool - Compression, tiered storage & indexing
├── central_dispatch.py  # Central Dispatcher - Plugin & external tool management
├── meta_boundaries.py   # Meta-Boundary Definition - 5 core security rules
├── utils.py             # Common Utilities - Hash, timestamp, fingerprint
└── main.py              # System Entry & Startup File
```

### 4.2 Core Experience Optimization

#### 4.2.1 Detailed Explanation Instead of Hard Block

When legitimate users are blocked: Return clear details including violated rule, risk hazard, consequence and alternative solutions.

#### 4.2.2 Speed Mode (Quick Response)

Reduce partial security checks for faster response. Retain core hard rules (H1-H10, write monopoly, neuron judgment).

**Scene-Based Speed Mode Control (Optimization):**

| Risk Level | Scenarios | Speed Mode |
|------------|-----------|------------|
| **Low** | Chat / General Q&A | Full Speed Mode available |
| **Medium** | Creation / Basic Analysis | Disable draft selection only; retain full meta-boundary & exit audit |
| **High** | Finance / Medical / Legal / Privacy | Force disable Speed Mode, full security checks locked |

All Speed Mode activation records (IP, timestamp, confirmation log) are permanently stored as compliance evidence.

### 4.3 Constitution Code & L1 Protection

**Constitution Code** = physical carrier of L1 absolute domain, compiled into binary:

Includes H1-H10 harm rules, 5 meta-boundaries, write monopoly & cognition boundary.

- Non-modifiable by users; updated only via digitally signed official release packages
- Cerebellum verifies signature before applying updates.

### 4.4 Core Performance Metrics

| Metric | Standard Value |
|--------|---------------|
| Cerebellum Judgment Latency | < 1ms |
| End-to-End Full Latency | < 8ms |
| Single Tag Size | 23 Bytes |
| Memory Compression Tiers | 4 (Raw / L1 / L2 / Skeleton) |
| Deterministic Interception Rules | 5 Core Thresholds |

---

## 5. Full Workflow Verification

### Scenario 1: Normal User Query

```
User Input → Cerebellum Entry Check (Pass) → AI 5 Anchors → Recognize Short Task
→ Quick Channel → Read Memory → Generate Response → Meta-Boundary Self-Check
→ Generate Security Tag → Cerebellum Exit Audit (Pass) → Write Token Issued
→ Save to Memory Pool → Output to User
```

### Scenario 2: User Follow-Up Question

```
Follow-up Input → Entry Check → 5 Anchors (Relationship = Returning User)
→ Load historical context → Comprehend reference content → Generate Response
→ Audit Pass → Output
```

### Scenario 3: Complex Long Task

```
Complex Task → AI Recognize Long Task → Create Independent Project Space
→ Void Engine Load Project Memory → Build Global View → Multi-Round Deduction
→ Save valid conclusions to memory pool per round → Project Complete
→ Final Audit → Output → Project Retain 30 Days → User decides archive/cleanup
```

### Scenario 4: Violate Security Rules (Example: Request to Delete System Logs)

```
Malicious Request → Entry Check → Trigger H1 (Destruction) → Direct Block
→ Return detailed risk explanation & alternative solutions
```

---

## 6. Deployment Verification Checklist

| No. | Verification Item | Acceptance Standard |
|-----|-------------------|---------------------|
| 1 | Single Entry & Exit | All data passes Cerebellum |
| 2 | AI Read Permission | AI reads memory directly, no Cerebellum transit |
| 3 | Write Monopoly | Only Cerebellum can write to memory pool |
| 4 | L1 Binary Protection | L1 rules compiled to binary, no debug/backdoor |
| 5 | Deterministic Threshold | Follow 5 core meta-boundary thresholds |
| 6 | 5 Parallel Anchors | Total time ≤ 500ms, minimum value on timeout |
| 7 | Void Engine Cleanup | No residual intermediate data after task |
| 8 | Recursive Memory Compression | Follow 30/90/180-day rules |
| 9 | Hot-Warm-Cold Storage | Tiered storage rules fully implemented |
| 10 | Project Isolation | Data between projects completely isolated |
| 11 | User Asset Ownership | Project data only modified/cleaned by user |
| 12 | Block Prompt | Detailed risk explanation for legitimate users |
| 13 | Speed Mode Confirmation | Triple confirmation: risk notice + disclaimer + explicit phrase |
| 14 | Constitution Update | Only official signed packages allowed for update |

---

## 7. Internal Workflow Logic

### 7.1 AI Decision Layer Internal Flow

```
Receive Task Tag from Cerebellum
    ↓
Directly Read Unified Memory Pool
    ↓
5 Parallel Anchors (Max 500ms → Deep / Minimum Anchor)
    ↓
Auto Flow Routing (Short / Long / Important Task)
    ↓
Risk & Tool Assessment → Invoke Central Dispatcher (if needed)
    ↓
Generate Task Brief → Submit to Cerebellum for Audit
```

**Closed-Loop Rule:**

```
Anchor → Routing → Execution → Audit Feedback
```

| Result | Action |
|--------|--------|
| Audit Pass | Continue execution |
| Audit Reject | Re-supplement anchor and re-submit |
| Reject twice | Use existing data to proceed (avoid infinite loop) |

### 7.2 Void Engine Internal Flow

```
Invoke Void Engine
    ↓
Mapping Association + Void Space Self-Check
    ├─ Valid Mapping → Proceed
    └─ Empty Mapping → 3-Step Causality Diagnosis
    ↓
Generate Multiple Drafts in Parallel
    ↓
Each Draft runs Meta-Boundary Self-Check (eliminate unqualified drafts)
    ↓
AI Independent Selection of Optimal Result
    ↓
Submit to Security Boundary Audit
    ↓
Full Cleanup of Void Engine Workspace
```

**Long Task Global View Flow:**

```
Load All Project Memory (project_id tagged)
    ↓
Sort by Timeline
    ↓
Build Full Project Global Graph
    ↓
Guide current round deduction
    ↓
Save audit-passed conclusion to memory pool
    ↓
Clean workspace
```

**Core Rules:**

- Void space self-check follows H1-H10 harm rules
- All intermediate drafts & mapping traces are permanently cleared after task completion

---

---

## 一起搞事情？

> 老黑一个人肝不动了，这引擎本质是个骨架——AI安全架构的骨架。

### 你最可能帮上忙的事

| 方向 | 你能做什么 | 难度 |
|------|-----------|------|
| **Rust 实现 Cerebellum 核心** | 🦀 安全引擎的硬件级落地，懂 Rust 就行 | ⭐⭐⭐⭐ |
| **Void Engine 并行调度** | 多草稿并行生成+评分系统，Python 熟手来 | ⭐⭐⭐ |
| **统一记忆池存储引擎** | 压缩/分层/索引，玩过向量数据库或时序数据库的 | ⭐⭐⭐ |
| **安全规则贡献** | 你没有代码？没关系。提新的攻击场景、边界用例、威胁模型 | ⭐ |
| **文档 & 翻译** | 你擅长表达？帮忙把设计思路用更干净的语言讲出来 | ⭐⭐ |
| **前端可视化** | 给调度中心、安全面板做可视化，React/Vue/Svelte 随便你 | ⭐⭐⭐ |
| **瞎聊天** | 就是单纯对这个方向感兴趣，想聊聊？也行。 | — |

### 怎么找我

- 📧 Email：**1410770089@qq.com**
- 🐙 GitHub：[github.com/woshilaohei](https://github.com/woshilaohei)
- 💬 直接开 Issue 聊：[cerebellum-evolution-engine/issues](https://github.com/woshilaohei/cerebellum-evolution-engine/issues)

> 不用顾忌，不用拘束。不管你是学生、老炮、还是单纯路过觉得有意思——过来聊聊。

---

## License & Open Source Statement

This project is open-sourced following the **MIT License** (default for GitHub public repositories).

- Free for personal learning, research and commercial use
- Retain original author & project copyright notice when redistributing
- All security rules, logic and designs are fully open for community review & iteration
