# Socratic Method & Collaborative Co-Creation Skill

An agentic skill for **Google Antigravity** and LLM coding assistants that replaces passive answer delivery and the "Interview & Reveal" trap with true **collaborative dialectic sparring and co-creation**.

---

## The Problem: The "Interview & Reveal" Trap

Standard AI assistants typically fall into an anti-pattern when prompted with open-ended or complex problems:

```
❌ The Interview Trap:
Agent interrogates -> User answers -> Agent dumps finished solution
(The human is treated as an intake form and sidelined from the creative process)
```

In that model, the user becomes a passive spectator who simply accepts or rejects a unilateral proposal.

---

## The Solution: Shared Whiteboard Co-Creation

This skill reconfigures the agent to act as a **co-thinking partner standing side-by-side at a whiteboard**:

```
✅ Collaborative Co-Creation:
User & Agent explore tensions together -> Formulate counterarguments side-by-side ->
Build, dismantle, and shape alternatives together
```

### Core Operating Principles

1. **Never Hand Down a Unilateral "Final Answer"**:
   - The agent presents raw scaffolds, working hypotheses, or contrasting seeds, always inviting the user to steer, dismantle, or refine them.
2. **Red-Teaming Counterarguments Together**:
   - Strong objections from skeptics or adversaries are treated as joint puzzles to solve rather than tests for the user to defend alone.
3. **Co-Developing Alternatives (Decision Forks, Not Menus)**:
   - Surfaces the underlying tensions and trade-off sliders (e.g., speed vs. rigor, punchiness vs. nuance) instead of dumping pre-baked packages.
4. **"Pass-the-Marker" Drafting**:
   - Works in tight, shared loops—laying down one piece of the puzzle at a time with open steering points.
5. **Universal Application**:
   - Designed for both **non-technical** tasks (blog posts, essays, creative writing, strategy) and **technical** tasks (architecture, debugging, API design).

---

## The 6 Socratic Question Archetypes

| Archetype | Focus | Example Question |
| :--- | :--- | :--- |
| **Clarification & Intent** | Pinning down precise meaning | *"What do we mean by [term] in this specific context?"* |
| **Probing Assumptions** | Surfacing unverified premises | *"What are we taking for granted that hasn't been tested?"* |
| **Probing Evidence** | Checking validity & failure conditions | *"Under what conditions does this reasoning fall apart?"* |
| **Alternative Perspectives** | Joint red-teaming & adversary views | *"What is the strongest objection a sharp skeptic would raise here?"* |
| **Second-Order Effects** | Downstream consequences | *"If we choose this path, what becomes harder or irreversible down the road?"* |
| **Questioning the Question**| Root-cause vs. symptom check | *"Are we solving the real bottleneck, or just treating an upstream symptom?"* |

---

## Directory Structure

```text
.
├── README.md
└── skills/
    └── socratic-method/
        └── SKILL.md
```

---

## Installation

### Option 1: Global Installation (All Conversations & Workspaces)
To make this skill available across every project and chat on your machine:

```bash
mkdir -p ~/.gemini/config/skills/socratic-method
cp skills/socratic-method/SKILL.md ~/.gemini/config/skills/socratic-method/SKILL.md
```

Antigravity automatically discovers skills in `~/.gemini/config/skills/` on session startup.

### Option 2: Project-Specific Installation (Workspace Level)
To include this skill in a specific repository or share it with your team:

```bash
mkdir -p .agents/skills/socratic-method
cp skills/socratic-method/SKILL.md .agents/skills/socratic-method/SKILL.md
```

Commit `.agents/skills/socratic-method/SKILL.md` to your version control repository (Git) so everyone on the team inherits it.

---

## How It Works in Practice

### Non-Technical: Writing a Blog Post or Essay
* **Without this skill**: The user asks for a blog post outline on a topic. The agent outputs a generic 5-section outline, ending the creative process.
* **With this skill**:
  > *"You mentioned wanting to tackle this topic from a contrarian perspective. The mainstream argument is [Convention X]. Are we trying to nuance that view, or blow it up entirely?*
  > 
  > *Here are two contrasting angles we could explore:*
  > - **Angle A (The Tactical Pivot)**: Focuses on concrete operational failures.
  > - **Angle B (The Philosophical Flaw)**: Focuses on an incorrect mental model.
  >
  > *Which of those lines up with what you want your audience to walk away with?"*

### Technical: Architecture & System Design
* **Without this skill**: The user asks how to cache an endpoint. The agent writes a Redis configuration file.
* **With this skill**:
  > *"We have a trade-off frontier between cache staleness and read latency here. If we introduce an in-memory cache, our biggest vulnerability becomes invalidation across multiple instances.*
  >
  > *If traffic spikes 10x or an invalidation event drops, how do you prefer the failure to be contained—is slightly stale data acceptable, or is eventual consistency a hard blocker?"*

---

## License

MIT
