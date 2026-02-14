# Double Egg Yolks!

**Exploring OpenClaw's Multi-Agent Architecture for Creative Iteration**

A music video production experiment using OpenClaw's soul-based agent orchestration to transform AI-generated chaos into coherent creative vision.

---

## 🎵 Background Story

As a kid, I used to make Weird Al-style musical parodies. In early February 2026, I introduced a friend of mine to the "Double Rainbow" meme video from the 2010s — along with its legendary Auto-Tune remix.

One morning, my friend (a 25-year-old in Brooklyn) messaged me: he'd cracked an egg while making breakfast and discovered a **double egg yolk**. The connection was instant — Double Rainbow meets Double Egg Yolks!

I created a parody song on Suno before the hackathon weekend and generated an initial music video. However, the result was **completely uncanny and unaligned**:
- Incoherent storytelling and theme
- Protagonist changed multiple times
- Visual discontinuity throughout
- Just... not where it needed to be

This sparked the idea: **Could OpenClaw's multi-agent architecture solve the AI video coherence problem?**

---

## 🎯 The Problem

**Creative ideation and refinement through traditional AI chatbot workflows is single-threaded and human-labor intensive.**

When iterating on creative projects with single-agent AI:
- Every revision requires manual re-prompting
- No parallel exploration of alternatives
- Human becomes the bottleneck for coordination
- Limited ability to explore multiple creative directions simultaneously
- Delivery artifacts often require extensive post-processing

This limits our ability to explore creative possibilities and bring them to life efficiently.

---

## ✨ The Solution (Explored through OpenClaw)

**Accelerate creative refinement by harnessing OpenClaw's multi-agent capabilities for rapid iteration and improved delivery artifacts.**

By orchestrating specialized creative agents with distinct personalities and responsibilities, we can:
- **Parallelize** ideation (Writer and Visual Director work simultaneously)
- **Specialize** expertise (dedicated screenplay vs. storyboard creation)
- **Iterate** faster (Producer coordinates revisions without manual re-prompting)
- **Refine** outputs through agent collaboration
- **Deliver** production-ready artifacts that address AI video generation's coherence challenges

The goal: Make precious **Human-in-the-Loop (HITL)** time more efficient and impactful.

---

## 🛠️ Methodology

### Agent Architecture

**Created three distinct creative roles using OpenClaw's soul-based agent system:**

**1. Producer (Main Agent)**
- **Soul**: Director focused on narrative coherence and vision
- **Personality**: Organized visionary, Weird Al disciple, collaboration leader
- **Responsibilities**: 
  - Analyze song structure and emotional arc
  - Create creative briefs
  - Spawn and coordinate sub-agents
  - Ensure continuity (same protagonist, setting, props)
  - Compile final deliverables
  - Generate AI-video-optimized prompts

**2. Writer (Sub-Agent)**
- **Personality**: Comedy screenwriter, visual comedy specialist
- **Responsibilities**:
  - Create screenplay aligned to song structure
  - Write scene descriptions with comedic beats
  - Provide alternative approaches for flexible moments
  - Generate production notes

**3. Visual Director (Sub-Agent)**
- **Personality**: MTV-style music video director, shot composition expert
- **Responsibilities**:
  - Create shot-by-shot storyboard (20-30 shots)
  - Specify camera angles, movements, lighting
  - Align visual beats to lyric moments
  - Provide alternative visual approaches
  - Track continuity requirements

### Workflow

1. **Producer** receives song lyrics and background context
2. **Producer** analyzes structure, creates creative brief
3. **Producer** spawns **Writer** and **Visual Director** sub-agents simultaneously via `sessions_spawn`
4. Sub-agents work independently with distinct creative briefs
5. Results automatically announce back to Producer
6. **Producer** reviews for coherence, selects best alternatives
7. **Producer** compiles final deliverables optimized for AI video generation

### Key Innovation: AI Video Coherence Prompting

Traditional AI video generation struggles with:
- Character consistency across shots
- Setting continuity
- Narrative coherence
- Visual motif repetition

**Solution**: The Producer generates a **VIDEO_PROMPT.md** file specifically structured to combat these issues:
- Explicit character/setting consistency requirements
- Core visual motif defined and repeated
- Gradual transformation guidelines (avoid uncanny morphing)
- AI safety notes for smooth transitions
- Emotional arc progression clearly mapped

### Collaborative Iteration (HITL Refinement)

Through multiple rounds of human feedback, the agents refined:
- Tone correction (physical comedy → genuine wonder)
- Visual motif emphasis (one egg → two yolks)
- Character development (buffoon → sincere protagonist)
- Daydream sequence styling
- Ending composition (yolks reflected in eyes)

Each revision was coordinated by the Producer without requiring human re-orchestration of the multi-agent workflow.

---

## 🎬 The Result

**Final Deliverables** (see attached files):
- `SCREENPLAY.md` - Complete 8-scene screenplay with emotional beats
- `STORYBOARD.md` - 47 detailed shots with camera/lighting specs
- `VIDEO_PROMPT.md` - Master prompt optimized for AI video generation
- `PROCESS_LOG.md` - Full production timeline showing agent collaboration

**The improved video generation prompt addresses the original coherence failures:**

✅ **Protagonist consistency**: Explicit character description, "SAME RYAN throughout"  
✅ **Setting continuity**: Detailed kitchen layout, "SAME KITCHEN" requirement  
✅ **Visual motif**: Core "egg crack → two yolks" defined clearly, repeated 8 times  
✅ **Narrative arc**: 10-stage emotional progression explicitly mapped  
✅ **Gradual transformations**: AI safety notes to avoid uncanny morphing  
✅ **Tone guidance**: "Genuine wonder" not "physical comedy" clearly specified  

**Production Time**: ~14 minutes of multi-agent collaboration + ~45 minutes of HITL refinement = **~1 hour total** for complete creative package

---

## 🎥 Watch the Result

**DEY - "Double Egg Yolks" Demo Video**  
*[Link to final video once generated]*

A celebration of the miraculous in the mundane — inspired by the "Double Rainbow" phenomenon and executed through multi-agent creative collaboration.

Would love to know what you think!

---

## 🔧 Technical Details

### OpenClaw Multi-Agent Implementation

**Architecture**: Single Producer agent + ephemeral sub-agents via `sessions_spawn`

**Why not true multi-agent routing?**
- `sessions_spawn` provides isolated sub-agent sessions with automatic result announcement
- Avoids complex binding configuration, per-agent auth, workspace isolation
- Faster setup (90 minutes vs 4+ hours for true multi-agent)
- Visually identical in Control UI for demo purposes

**Agent Definition Files:**

**`SOUL.md`** (Producer personality):
```markdown
# Producer Agent — DEY Music Video Director
You are a creative Producer specializing in parody music videos...
[Defines Producer's mission, personality, team, workflow, success factors]
```

**`AGENTS.md`** (Operational instructions):
```markdown
# AGENTS.md - DEY Project Operations
[Sub-agent spawn protocols, process logging, compilation guidelines]
```

**Technology Stack:**
- **Platform**: OpenClaw 2026.2.13
- **Model**: `anthropic/claude-sonnet-4.5` (main + sub-agents)
- **Interface**: Control UI (localhost:18789) + Telegram
- **Output Format**: Markdown (screenplay, storyboard, prompts)
- **Session Management**: Automatic sub-agent lifecycle via `sessions_spawn`

**Files Generated:**

1. **SCREENPLAY.md** (12.3 KB)
   - 8 complete scenes aligned to 2:36 song structure
   - Character: Ryan (25 y/o, Brooklyn kitchen)
   - Tone: Genuine wonder and revelation
   - Production notes for color grading and continuity

2. **STORYBOARD.md** (27.7 KB)
   - 47 detailed shots covering 2:50 runtime
   - Camera angles, movements, lighting specs per shot
   - Core motif (egg cracking → two yolks) tracked across 8 appearances
   - Daydream sequence specifications
   - Approximate durations with flexibility guidance

3. **VIDEO_PROMPT.md** (22 KB)
   - Master prompt optimized for AI video generation
   - Character/setting consistency requirements
   - Visual motif detailed explanation
   - AI safety notes (gradual changes, avoid morphing)
   - Narrative arc progression mapped
   - References SCREENPLAY.md and STORYBOARD.md

4. **PROCESS_LOG.md** (9.7 KB)
   - Timestamped collaboration timeline
   - Sub-agent spawn events
   - Creative revision documentation
   - Final QA refinements

**Key Learnings:**

- **Soul-based agent definition** enables personality consistency without complex prompting
- **Sub-agent spawning** (`sessions_spawn`) provides true parallelization for creative exploration
- **Structured output formats** (Markdown templates) ensure deliverable quality
- **Iterative HITL refinement** with agent memory allows rapid tone/direction corrections
- **AI video coherence** can be dramatically improved through explicit prompt engineering

**Production Metrics:**
- **Initial creative pass**: 9 minutes (sub-agent spawn → results)
- **Major revision cycle**: 15 minutes (tone correction, motif emphasis)
- **QA refinements**: 20 minutes (shot splits, timestamp removal, terminology)
- **Total time**: ~1 hour for production-ready creative package

---

**Repository**: [OpenClaw](https://github.com/openclaw/openclaw)  
**Hackathon**: February 2026  
**Song Length**: 2:36 (final video 2:50 with ending)  
**Total Shots**: 47  
**Style Inspiration**: Weird Al + Double Rainbow viral video
