# AMA System: Complete Operational Specification

> **Purpose**: This document is the exhaustive "brain dump" for an Autonomous Marketing Agency. It describes every function, skill, process, and deliverable that a senior-level digital marketing team would be capable of. The long-running agent system will use this as its source of truth for what it must be able to do.

---

## Part 1: The Role of the System

The AMA is not a simple chatbot or a single-purpose tool. It is a **virtual marketing department** with the combined knowledge of:

-   A **CMO** (Chief Marketing Officer) for strategy
-   A **Media Buyer** for paid acquisition
-   A **Creative Director** for visual identity
-   A **Copywriter** for persuasion
-   A **Data Analyst** for performance optimization
-   A **Project Manager** for workflow and delivery

The human operator (the agency owner) interacts with this system via a conversational interface in a code editor (Cursor, Claude Code). The system executes, learns, and improves.

---

## Part 2: Client Lifecycle (End-to-End)

Every client engagement follows this lifecycle. The system must be capable of all phases.

### Phase 0: Sales & Intake
| Task | Description |
|---|---|
| **Lead Qualification** | Analyze a potential client's website/social media to assess fit. |
| **Proposal Generation** | Draft a custom proposal document (`.pdf` or Notion doc) outlining services, pricing, and timeline. |
| **Contract Templating** | Generate a scope-of-work contract with client-specific terms. |

### Phase 1: Discovery & Onboarding
| Task | Description |
|---|---|
| **Brand Absorption** | Ingest client website, brand guidelines PDF, product catalogs, and past ad creative. |
| **Voice Extraction** | Analyze client's existing copy to define tone (formal/casual, playful/serious, etc.). |
| **ICP Definition** | Define Ideal Customer Profile: demographics, psychographics, pain points, desires. |
| **Competitor Analysis** | Identify 3-5 direct competitors. Scrape their Meta Ad Library, landing pages, and social profiles. |
| **SWOT Generation** | Produce a Strengths/Weaknesses/Opportunities/Threats analysis. |

### Phase 2: Strategy & Planning
| Task | Description |
|---|---|
| **Angle Development** | Create 5-10 unique "hooks" or messaging angles based on ICP pain/desire. |
| **Offer Structuring** | Define the core offer (discount, bundle, guarantee, bonus) for the campaign. |
| **Funnel Mapping** | Design the customer journey: Ad → Landing Page → Email Sequence → Conversion. |
| **Budget Allocation** | Propose a media spend plan per platform, phase (testing vs. scaling), and creative type. |
| **Calendar Creation** | Build a 30/60/90-day campaign calendar with launch dates and review checkpoints. |

### Phase 3: Creative Production
| Task | Description |
|---|---|
| **Ad Copy (Static)** | Write headlines, body text, CTAs for each angle. Produce 3+ variations per angle. |
| **Ad Copy (Video)** | Write full video scripts with hooks (0-3s), body (3-30s), and CTA (30s+). |
| **Image Briefs** | Generate detailed briefs for designers (or AI image generators) specifying dimensions, elements, text overlay, mood. |
| **Video Briefs** | Generate shot lists, UGC actor instructions, and b-roll specifications. |
| **Landing Page Copy** | Write above-the-fold (ATF), benefits section, testimonials section, FAQ, and final CTA. |
| **Email Sequences** | Write 3-7 email flows: Welcome, Abandoned Cart, Post-Purchase, Re-engagement. |
| **SMS Copy** | Write short, high-impact messages for key conversion moments. |

### Phase 4: Technical Setup
| Task | Description |
|---|---|
| **Pixel Installation** | Generate code snippets or GTM instructions for Meta Pixel, CAPI. |
| **Conversion API Setup** | Provide instructions or scripts for server-side tracking. |
| **UTM Structuring** | Define a consistent UTM naming convention for all links. |
| **Ad Account Audit** | Check existing ad accounts for policy violations, pixel health, audience structure. |
| **Domain Verification** | Guide or automate Meta Business Suite domain verification. |

### Phase 5: Deployment & Launch
| Task | Description |
|---|---|
| **Campaign Building** | Structure campaigns in Meta Ads Manager (or via API): Campaign > Ad Sets > Ads. |
| **Audience Creation** | Build Lookalike audiences, Custom audiences (website visitors, purchasers), Interest stacks. |
| **A/B Test Setup** | Configure split tests for creative, copy, audience, or placement. |
| **Budget Rules** | Set up automated rules to pause underperformers and scale winners. |
| **Launch Checklist** | Verify all links, tracking, and ad previews before going live. |

### Phase 6: Optimization & Scaling
| Task | Description |
|---|---|
| **Daily Monitoring** | Check key metrics (Spend, Impressions, CTR, CPC, CPM, ROAS). |
| **Winner Identification** | Identify top 10-20% of ads by performance. |
| **Loser Elimination** | Pause bottom performers based on cost/conversion thresholds. |
| **Iteration Briefs** | For winning ads, generate "iteration" briefs: "Take Ad X, change the hook to Y." |
| **Scaling Protocol** | Document when and how to increase budget (horizontal vs. vertical scaling). |
| **Creative Fatigue Detection** | Flag ads with declining CTR/Frequency over time. |

### Phase 7: Reporting & Communication
| Task | Description |
|---|---|
| **Weekly Reports** | Generate automated performance summaries for the client. |
| **Monthly Deep Dives** | Produce comprehensive analysis: what worked, what failed, learnings. |
| **Client Dashboard** | Maintain a live dashboard (Google Sheets, Looker Studio) with key KPIs. |
| **Meeting Notes** | Generate agenda and talking points for client calls. |

---

## Part 3: All Required Platform Integrations

The system must be able to connect to and operate within these platforms:

| Platform | Purpose |
|---|---|
| **Meta Business Suite** | Ad account management, Pixel, Audiences, Reporting. |
| **Meta Ad Library** | Competitor research, inspiration scraping. |
| **Google Ads** | (Future) Search and YouTube ads. |
| **TikTok Ads Manager** | (Future) TikTok campaigns and Creative Center. |
| **Google Sheets** | Data storage, client dashboards, reporting. |
| **Notion** | Client-facing project management and SOPs. |
| **Slack/Email** | Client communication and notifications. |
| **Zapier/Make** | Workflow automation triggers. |
| **OpenAI/Anthropic API** | Core LLM for all creative and analytical tasks. |
| **Image Generation APIs** | DALL-E, Midjourney, Ideogram for visual assets. |
| **Video Generation APIs** | Runway, Pika, Kling for video asset generation. |

---

## Part 4: All Creative Formats

The system must be able to produce briefs or final assets for all standard Meta/Instagram formats:

### Static Images
-   **1:1 (1080x1080)**: Feed square.
-   **4:5 (1080x1350)**: Feed vertical (recommended).
-   **9:16 (1080x1920)**: Stories/Reels.
-   **1.91:1 (1200x628)**: Link ads, right column.

### Video
-   **9:16 Vertical (1080x1920)**: Reels, Stories.
-   **1:1 Square (1080x1080)**: Feed video.
-   **16:9 Landscape (1920x1080)**: In-stream, YouTube repurposing.

### Carousel
-   **3-10 cards**: Each card 1:1 or 4:5.
-   **Narrative structure**: Hook, Problem, Solution, Proof, CTA.

### Other
-   **Instant Experience (Canvas)**: Full-screen mobile landing experience.
-   **Collection Ads**: Catalog-based ads with dynamic products.

---

## Part 5: Core Knowledge Domains

The system must have embedded knowledge (or the ability to research) in these areas:

### Copywriting Frameworks
-   PAS (Problem-Agitate-Solution)
-   AIDA (Attention-Interest-Desire-Action)
-   BAB (Before-After-Bridge)
-   4Ps (Promise, Picture, Proof, Push)
-   Hook-Story-Offer

### Media Buying Strategy
-   CBO vs. ABO (Campaign vs. Ad Set Budget Optimization)
-   Broad vs. Interest vs. Lookalike targeting
-   Retargeting windows and layering
-   Attribution settings (1-day click, 7-day click)
-   iOS 14.5+ privacy implications

### Creative Strategy
-   UGC (User-Generated Content) principles
-   Direct Response vs. Brand Awareness creative
-   Static vs. Video performance benchmarks
-   Hook rate optimization (<3 seconds)

### Analytics & Optimization
-   Cohort analysis
-   MER (Marketing Efficiency Ratio)
-   Blended ROAS vs. In-Platform ROAS
-   Creative testing protocols (staggered launch, isolated variables)

---

## Part 6: Self-Improvement Mandate

This system is not static. It must continuously:

1.  **Scrape Trends**: Monitor top-performing ads in Meta Ad Library for the client's niche weekly.
2.  **Extract Patterns**: Identify winning hooks, visual styles, and offers from competitors.
3.  **Update SOPs**: If a new best practice is discovered (e.g., a new ad format), add it to the internal SOP library.
4.  **Learn from Results**: Every campaign's performance data should feed back into a `performance_memory.json` file that informs future creative decisions.
5.  **Propose Experiments**: Proactively suggest A/B tests or new angles based on market observations.

---

## Part 7: Human-in-the-Loop Checkpoints

Despite being autonomous, the system must pause for human approval at these critical points:

| Checkpoint | Reason |
|---|---|
| **Final Ad Copy Approval** | Ensure brand voice and legal compliance. |
| **Budget Increases > 50%** | Prevent runaway spend. |
| **New Platform Connection** | Security and access control. |
| **Client-Facing Deliverables** | Proposals, reports, contracts. |
| **Policy-Sensitive Content** | Claims about health, finance, etc. |

---

## Part 8: Success Metrics

The system's performance should be measured by:

| Metric | Target |
|---|---|
| **Time to First Ad Live** | < 48 hours from client onboarding. |
| **Creative Variations per Month** | > 50 per client. |
| **Ad Compliance Rate** | 100% (zero policy rejections). |
| **Client ROAS** | Meet or exceed client's target ROAS. |
| **Human Intervention Rate** | < 10% of tasks require manual override. |

---

## Summary

This document defines the **complete scope** of what the Autonomous Marketing Agency must be capable of. It is the "senior marketer's brain" encoded into a specification. The long-running agent system from Anthropic will be configured with this knowledge, decomposing these high-level capabilities into thousands of atomic tasks that can be executed, voted on, and continuously improved.
