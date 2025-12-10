# Autonomous Marketing Agency (AMA) System Architecture

This document outlines the architectural vision for a self-improving, autonomous marketing agency system. It integrates cutting-edge concepts from Anthropic's "Effective Harnesses" research and the "MAKER" framework (Maximal Agentic Decomposition with Voting).

---

## 1. System Philosophy & Core Concepts

The goal is to build a "Company-in-a-Box" that doesn't just execute tasks but evolves, critiques itself, and adapts to market trends.

### 1.1 The "Harness" (Operating System)

Inspired by Anthropic's *Effective Harnesses*, the system is not a single long-running loop but a structured environment that manages state.

-   **Environment Management**: The system maintains a "Clean State" at all times. Every action is a commit to a repository (Git) with a corresponding update to a structured log (`progress.json` / `features.json`).
-   **Incremental Execution**: The system does not attempt to "do marketing." Instead, it executes thousands of micro-tasks (e.g., "Crop image to 4:5", "Write headline option A", "Check Facebook API balance").
-   **Initializer Agent**: When a new client is onboarded, an "Initializer Agent" writes the entire "SOP Backend" — a list of thousands of potential tasks and requirements, initially marked as `pending`.

### 1.2 The MAKER Framework (Decision Engine)

To ensure reliability and high-quality creative output, we utilize the **MAKER** (Maximal Agentic Decomposition) framework.

-   **Maximal Decomposition**: Every complex task (e.g., "Create a Campaign") is broken down into atomic steps (m=1 steps).
-   **The "Congress" (Voting & Quality Control)**:
    -   For every decision or creative output (e.g., "Is this ad copy compliant?"), multiple "Worker Agents" generate potential solutions in parallel.
    -   A **Voting Protocol** (First-to-ahead-by-k) determines the winner. If 5 agents draft an email and 4 are similar/excellent while 1 is hallucinated, the consensus wins.
    -   **Red-Flagging**: If the agents disagree significantly (high entropy), the task is flagged for "Red Team" review or User intervention.

---

## 2. Infrastructure Layer

The system runs on a cloud-based development environment (e.g., Cursor/Cloud Code) backed by a Git repository.

### 2.1 File Structure

```
/agency_core
  /sops               # Standard Operating Procedures (Live code/prompts)
  /clients            # Client Data
    /client_A
      /brand_voice    # Extracted knowledge (tone, rules)
      /assets         # Images, Videos
      /campaigns      # Active Campaign Data
  /memory
    /market_intel     # Competitor analysis database
    /performance      # What works (Global learning)
  /src
    /agents           # Agent definitions (Worker, Critic, Manager)
    /harness          # The control loop code
  progress.json       # The global state of the agency
```

### 2.2 The Control Loop

1.  **Scanner**: Checks `progress.json` for `pending` tasks and External Triggers (Calendar, Market Alert).
2.  **Dispatcher**: Assigns a `pending` task to a specific Agent Type.
3.  **Execution (MAKER Mode)**:
    -   Agent spins up.
    -   Generates N solutions.
    -   **Congress** votes.
    -   Winner is selected.
4.  **Commit**: Result is written to the file system, `progress.json` is updated to `completed`, and code is committed to Git.

---

## 3. The Agent "Congress" Roles

The system is composed of specialized agents that interact via the Harness.

### 3.1 The Strategist (The Manager)

-   **Role**: Decomposes high-level goals into the `features.json` list.
-   **MAKER Function**: When the user says "Launch Black Friday," the Strategist breaks this into 500 atomic tasks (Update Banner, Write Email 1, Create Ad Set 3...) using Maximal Decomposition.

### 3.2 The Creator (The Worker)

-   **Role**: Executes atomic creative tasks.
-   **Variants**: `CopywriterAgent`, `DesignerAgent`, `VideoScriptAgent`.
-   **Process**: Always runs in parallel batches to allow for Voting.

### 3.3 The Critic (The Judge)

-   **Role**: The "Voter" in the MAKER framework.
-   **SOP**: "Does this image violate Meta Ad Policy 23.1?" "Is this tone consistent with the Client Brand Voice file?"
-   **Auto-Correction**: If the Critic rejects the output, the task is sent back to the Creator with specific feedback loops.

### 3.4 The Spy (Market Analyst)

-   **Role**: Continuously scrapes competitors and market trends (Meta Ad Library, TikTok Creative Center).
-   **Output**: Updates `market_intel/trends.json`. This triggers the Strategist to create new tasks (e.g., "Competitor X is using hook Y, generate 3 variations for Client Z").

---

## 4. Operational Workflow (The Life of a Campaign)

### Phase 1: Onboarding & Decomposition

1.  **User Input**: "Here is the client URL and 3 PDFs of product info."
2.  **Absorption**: The system runs a "Knowledge Extraction" job, populating `/brand_voice` and `/sops`.
3.  **Setup**: The Initializer Agent creates the `campaign_roadmap.json` with 200+ steps (Setup Pixel, Verify Domain, Draft Angles...).

### Phase 2: Production (The Factory)

1.  **Task**: "Draft Ad Body Text for Angle: 'Money Saver'".
2.  **Drafting**: 3 Parallel Copywriter Agents generate 3 versions.
3.  **Voting**: The Congress reviews them against high-performing benchmarks in `performance` memory. The best version is selected.
4.  **Refinement**: If the vote is split, a "Senior Editor Agent" reconciles the differences.

### Phase 3: Deployment & Verification

1.  **Action**: Agent connects to Meta Marketing API.
2.  **Verification**: Using browser automation (Puppeteer/Playwright) or API "dry-runs," the system validates that the ad is correctly staged (correct image, correct link, correct budget).
3.  **Commit**: The Ad ID is logged to `state.json`.

### Phase 4: Optimization (The Self-Improving Loop)

1.  **Feedback**: Every 24h, the Analyst Agent pulls ROAS/CTR data.
2.  **Learning**: High-performing elements are saved to `global_best_practices.md`.
3.  **Action**: Underperforming ads are paused. New tasks are added to the queue: "Iterate on Ad #123 (High CTR, Low Conversion) -> Generate new Landing Page Hook".

---

## 5. Self-Improvement & Quality Checks

### 5.1 The "Constitution"

A core file `constitution.md` governs the agents. It contains:

-   **Meta Policy Rules**: Strict rules to avoid account bans.
-   **Quality Standards**: "No generic AI copy (e.g., 'Unlock the power of...')."
-   **Brand Guidelines**: Client-specific "DO NOTs."

### 5.2 Red-Flagging (from MAKER)

If the "Congress" cannot reach a consensus (e.g., 3 votes for A, 3 votes for B), the system flags this as **"Ambiguous Strategy."**

-   The system pauses this specific branch.
-   It notifies the Human User: "Congress failed to decide on Ad Hook for 'Product B'. Input required."
-   This "Human-in-the-Loop" ensures the system doesn't spiral on difficult creative decisions.

---

## 6. Key Deliverables (The Output Library)

The AMA is designed to produce all assets a full-stack marketing agency would deliver:

| Category | Deliverables |
|---|---|
| **Copywriting** | Ad headlines, body text, landing page copy, email sequences, SMS scripts |
| **Visual Assets** | Static ad images (1:1, 4:5, 1.91:1), carousels, UGC-style thumbnails |
| **Video** | Full video scripts, storyboards, UGC editing instructions, caption overlays |
| **Strategy** | Audience research docs, competitor breakdowns, A/B test plans, campaign calendars |
| **Technical** | Pixel setup guides, API integration code, tracking spreadsheets |

---

## 7. Implementation Notes (Next Steps)

To build this system, follow a phased approach:

1.  **Phase 1 - The Harness**: Build the Git-backed state manager (`progress.json`, the commit loop).
2.  **Phase 2 - The Primitives**: Create the `Vote(options, criteria)` function using the MAKER logic. Implement `RedFlag()`.
3.  **Phase 3 - The Initializer**: Build the prompt that decomposes a client URL into a robust set of initial files (/brand_voice, /sops).
4.  **Phase 4 - The Workers**: Build the individual creator agents (Copywriter, Designer, etc.) and integrate with the voting system.
5.  **Phase 5 - The Spy Network**: Integrate with Meta Ad Library scrapers to feed `market_intel`.

---

## 8. Source References

-   **Anthropic Harnesses**: [Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
-   **MAKER Paper**: [Solving a Million-Step LLM Task with Zero Errors](https://arxiv.org/html/2511.09030v1)
-   **Autonomous Coding Quickstart**: [claude-quickstarts/autonomous-coding](https://github.com/anthropics/claude-quickstarts/tree/main/autonomous-coding)
