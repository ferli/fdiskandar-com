# How to Integrate Research with Claude Code

Practical guide untuk work dengan Claude Code CLI while doing research, untuk efficient article writing.

---

## Overview

**Goal:** Leverage Claude Code untuk synthesis & writing, while you do deep research

**Flow:**
```
You: Research (6 hours) → Save notes
You + Claude Code: Outline & structure (30 min)
Claude Code: Draft writing (1-2 hours)
You: Review & iterate (1 hour)
Claude Code: Refine (30 min)
You: Final edit & publish (1 hour)
```

---

## Method 1: Sequential (Research First, Then Write)

**Best for:** Thorough research before writing

### Step 1: Complete All Research
- [ ] Conduct 4-6 hours of research
- [ ] Extract findings to research notes file
- [ ] Synthesize patterns & insights
- [ ] Compile complete reference list
- [ ] Save: `research/insights/[article]-notes.md`

### Step 2: Open Claude Code & Load Research

**Option A: Direct File Path**
```bash
# In Claude Code, mention the research file
"I've compiled research into: C:\Repo\rinji-id\research\insights\benchmark-pdam-notes.md
Can you read this file and use it as basis for article?"
```

Claude Code will:
- Read the file
- Understand research findings
- Use as context untuk article writing

**Option B: Copy-Paste Key Findings**
If file not accessible, copy key sections dari notes into Claude Code prompt.

### Step 3: Outline & Structure Discussion

**Submit this:**
```
TASK: Outline article based on research

Research findings available in: [path/to/notes.md]

I need your help creating article outline based on research.

REQUIREMENTS:
1. Read research notes
2. Identify 4-5 main sections that make sense
3. For each section, propose:
   - Section title
   - Key points to cover (2-4 points per section)
   - Which research findings support this section
   - Approximate word count per section

GOAL: Create outline that flows logically & answers key research questions

Please propose outline & I'll review before you start writing.
```

**Expected output:** Detailed outline (1-2 pages)
**Your action:** Review outline
- Approve as-is, OR
- Request changes to structure/flow
- Clarify emphasis areas

### Step 4: Section-by-Section Writing

Once outline approved:

```
TASK: Write Section 1 - [Section Title]

Based on research notes & approved outline, please write first section.

SECTION BRIEF:
- Title: [Section title]
- Purpose: [What this section should accomplish]
- Key points: [3-4 main points to cover]
- Sources: [Which research sources support this]
- Word count target: [300-400 words, etc.]

REQUIREMENTS:
- Use research findings to support claims
- Cite sources (Author Year format)
- Target audience: [Describe audience - avoid jargon without explanation]
- Tone: Professional, analytical, accessible
- Include examples/case studies from Indonesia if relevant

Please write draft of Section 1.
```

**Expected:** Draft of 300-500 words with citations
**Your action:** Review
- Does it match outline & research?
- Clear & well-written?
- Accurate citations?
- Good examples?

Approve or request revisions. Once approved, move to Section 2, 3, etc.

### Step 5: Integration & Refinement

As sections completed:
1. Compile all sections into single document
2. Add introduction & conclusion
3. Review for flow & coherence across sections
4. Check citations format consistency
5. Compile complete reference list

Request Claude Code for help:
```
TASK: Add introduction & conclusion

I now have 4 main sections drafted. Please write:

INTRODUCTION (300-400 words):
- Set context for why article matters
- Introduce key questions article answers
- Preview main findings/structure

CONCLUSION (200-300 words):
- Summarize key insights
- Highlight implications for readers
- Suggest actionable next steps

Reference completed sections for tone & content alignment.
```

### Step 6: Final Polish & Publish

Submit final version for review:
```
TASK: Quality review & final suggestions

Here's complete article draft. Please review for:
1. Accuracy of facts & citations
2. Clarity for target audience
3. Logical flow between sections
4. Any glaring gaps or issues

Provide specific suggestions (don't rewrite—I'll do that).
```

Implement feedback, then publish.

---

## Method 2: Parallel (Research + Writing Concurrently)

**Best for:** Starting to write while still researching

### Step 1: Quick Scope Definition
- [ ] Define key questions (30 min)
- [ ] Identify major section topics (30 min)

### Step 2: Initial Research Snapshot
- [ ] Quick research on major sections (2 hours)
- [ ] Compile preliminary findings
- [ ] Do NOT require complete research yet

### Step 3: Outline Draft Writing

Submit to Claude Code:
```
TASK: Create article outline

I'm researching [Article Title]. Here's what I know so far:

[Brief summary of findings so far]

Key questions article must answer:
1. [Q1]
2. [Q2]
3. [Q3]

Based on this, propose logical article structure (4-5 main sections).
For each section, suggest what information would strengthen it.

This helps me know what to research next.
```

**Expected:** Outline + "research gaps" identified
**Your action:**
- See structure Claude Code recommends
- Identify what additional research needed to strengthen each section
- Focus remaining research on gap areas

### Step 4: Deepen Research Targeted

Now you know what to research. Focus remaining research (3-4 hours) on:
- Filling gaps identified by Claude Code
- Getting data/evidence needed for each section
- Case studies & examples

### Step 5: Write with Completed Research

Once research complete, follow Method 1 Section 4-6 for writing.

---

## Method 3: Hybrid (Iterative Research + Writing)

**Best for:** Learning as you go, refining understanding through writing

### Cycle (repeat for each section):

1. **Research 1-2 sections** (1-2 hours)
2. **Write 1-2 sections with Claude Code** (1 hour)
3. **Review draft** → What else do you need to know?
4. **Research gaps identified by draft** (1 hour)
5. **Request Claude Code revise based on new research** (30 min)
6. **Move to next section**

Benefit: Writing clarifies what you still need to understand. You can refocus research accordingly.

---

## Best Practices: Working with Claude Code

### Do's

✓ **Provide research context** — Share your research notes so Claude Code has material to work with
✓ **Be specific about audience** — "Write for PDAM directors, not technical engineers" shapes tone/complexity
✓ **Request iteration** — First draft rarely perfect; revise based on feedback
✓ **Use section-by-section approach** — Easier to review, revise specific sections
✓ **Cite clearly** — Ask Claude Code to use consistent citation format throughout
✓ **Save all drafts** — Version control of article development

### Don'ts

✗ **Don't skip research** — Claude Code can write well, but without deep research, it's surface-level
✗ **Don't treat Claude Code as fact-checker** — You verify facts in research; Claude Code writes based on what you provide
✗ **Don't demand full article in one go** — Better to iterate section-by-section
✗ **Don't ignore gaps Claude Code flags** — If Claude Code says "more evidence needed here," listen
✗ **Don't use without understanding** — Review every section. Claude Code is tool, not magic

---

## Prompt Template: Submitting Research to Claude Code

```
TASK: [Write article / Outline article / Revise section]

ARTICLE: [Article Title]

RESEARCH CONTEXT:
[One of the following:]

Option A - File reference:
"Deep research findings compiled in: [filepath]"

Option B - Copy key findings:
[Key research findings & insights]

KEY RESEARCH QUESTIONS ARTICLE MUST ANSWER:
1. [Q1]
2. [Q2]
3. [Q3]
4. [Q4]

TARGET AUDIENCE:
[Describe who will read this: PDAM leaders? Regulators? Technical managers?]

ARTICLE REQUIREMENTS:
- Length: [2000-3000 words / as needed]
- Citations: [Author Year format]
- Reference list: [Include all sources]
- Sections: [Number & type of sections, if preference]
- Tone: [Professional / Accessible / Technical / Mixed]

YOUR TASK:
[Specific request: outline / write Section 1 / revise draft / etc.]

PLEASE START BY:
[e.g., "Summarizing 3-5 key insights from research"]
[e.g., "Proposing logical article structure"]
[e.g., "Highlighting any research gaps you notice"]
```

---

## Handling Research Gaps

**When Claude Code says "Need more evidence here":**

1. **Acknowledge gap** — You're missing research in that area
2. **Decide approach:**
   - **Deepen research** — Find sources to fill gap
   - **Reframe section** — Focus on what you DO know
   - **Note limitation** — Acknowledge gap in article ("Limited data on this topic...")
3. **Communicate back** — Give Claude Code updated info or context
4. **Request revision** — Ask Claude Code to rewrite section with new info

Example:
```
You said we need more data on PDAM cost recovery ratio.
I found [cite new source] which shows [new data].
Can you revise Section 2 using this additional data?
```

---

## Version Control & Iteration

Keep track of article development:

```
content/
└── insights/
    ├── benchmark-pdam.md (final published version)
    └── _drafts/
        ├── benchmark-pdam-v1-outline.md
        ├── benchmark-pdam-v2-sections-1-2.md
        ├── benchmark-pdam-v3-all-sections.md
        ├── benchmark-pdam-v4-refined.md
        └── benchmark-pdam-v5-final.md
```

Or use git to track versions:
```bash
git add content/insights/benchmark-pdam.md
git commit -m "V2: Add research from [source], revise Section 2"
```

---

## Example Workflow: "Benchmark Kinerja PDAM"

**Timeline: 8 hours total**

**Hour 1:** Scope definition
- Article must answer: NRW rates? Variation? Trends? Best practices?
- Submit to Claude Code for outline

**Hours 2-5:** Research
- Government stats on NRW (BPS, PUPR)
- PERPAMSI benchmark data
- Academic papers (3-4)
- Sample PDAM data (3 case studies)
- Compile to research/insights/benchmark-pdam-notes.md

**Hour 6:** Claude Code outline + structure review
- Submit research notes
- Review & approve outline
- Identify any research gaps

**Hour 7:** Claude Code writing
- Write Section 1 (introduction + context) → review & approve
- Write Section 2 (NRW data & variation) → review & approve
- Write Section 3 (trends & analysis) → review & approve
- Write Section 4 (best practices) → review & approve
- Write conclusion → approve

**Hour 8:** Polish & publish
- Final edit for clarity
- Check citations format
- Add frontmatter
- Rebuild & deploy

**Result:** Professional, research-backed, 2500-3000 word article

---

## Summary

**Working with Claude Code for research-backed articles:**

1. Do deep research (4-6 hours)
2. Compile findings to structured notes
3. Outline article with Claude Code (30 min)
4. Write section-by-section with Claude Code (1-2 hours)
5. Review & iterate based on Claude Code feedback
6. Final edit & publish (1 hour)

**Total: 8-11 hours per article**
**Result: Substantive, research-backed, well-written content**

---

**Questions about workflow? Check:**
- `QUICK_START_RESEARCH.md` — Quick overview
- `RESEARCH_WORKFLOW.md` — Detailed workflow documentation
- `research/template.md` — Research note template
