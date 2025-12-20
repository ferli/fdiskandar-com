# Visual Guide: Research + Claude Code Workflow

Dokumentasi visual untuk memahami workflow end-to-end.

---

## Overall Workflow Timeline

```
DAY 1-2: RESEARCH PHASE (4-6 hours)
┌─────────────────────────────────┐
│ Hour 0-0.5: Define Scope        │ Quick scope & key questions
│ Hour 0.5-6: Conduct Research    │ Gather sources, extract findings
│ Hour 6-7: Compile Notes         │ Organize to template structure
│                                 │
│ OUTPUT: research/insights/[article]-notes.md
└─────────────────────────────────┘

DAY 3: CLAUDE CODE INTEGRATION (2-3 hours)
┌─────────────────────────────────┐
│ Hour 0-0.5: Submit Research     │ Provide notes file to Claude Code
│ Hour 0.5-1.5: Outline Review    │ Claude Code outlines, you approve
│ Hour 1.5-3: Section Writing     │ Write Sec 1,2,3,4 + Intro + Conclusion
│                                 │
│ OUTPUT: Article draft with citations
└─────────────────────────────────┘

DAY 4: REFINEMENT (1-2 hours)
┌─────────────────────────────────┐
│ Hour 0-0.5: Quality Check       │ Verify facts, citations, clarity
│ Hour 0.5-1: Final Edit          │ Polish writing, fix typos
│ Hour 1-2: Publish               │ Rebuild & deploy
│                                 │
│ OUTPUT: Published article on rinji.id
└─────────────────────────────────┘

TOTAL: 8-11 hours per article
```

---

## Research → Writing Flow (Detailed)

```
START: Decide on Article Topic
  │
  ├─ Article Title & Scope
  │  ├─ What's the article about?
  │  ├─ Who reads it?
  │  └─ What questions must it answer?
  │
  ├─ RESEARCH PHASE (You)
  │  ├─ Identify key sources (5-10+)
  │  │  ├─ Government reports
  │  │  ├─ Academic papers
  │  │  ├─ Industry publications
  │  │  └─ Case studies
  │  │
  │  ├─ Extract Findings
  │  │  ├─ Per-source findings documented
  │  │  ├─ Statistics & quotes extracted
  │  │  └─ Relevance to article noted
  │  │
  │  └─ Synthesize Research
  │     ├─ Identify common themes
  │     ├─ Note contradictions
  │     ├─ Extract original insights
  │     └─ Acknowledge limitations
  │
  ├─ COMPILE NOTES (You: 30 min - 1 hour)
  │  └─ Save to: research/insights/[article]-notes.md
  │     ├─ All sources documented
  │     ├─ Synthesis section complete
  │     ├─ Article structure proposed
  │     └─ Reference list compiled
  │
  ├─ CLAUDE CODE INTEGRATION (1-2 hours)
  │  │
  │  ├─ Step 1: Submit Research (You)
  │  │  └─ Share notes file path
  │  │
  │  ├─ Step 2: Outline Generation (Claude Code)
  │  │  ├─ Claude Code reads research notes
  │  │  ├─ Claude Code creates outline
  │  │  └─ Claude Code suggests structure
  │  │
  │  ├─ Step 3: Outline Review (You)
  │  │  ├─ You review structure
  │  │  ├─ You approve or request changes
  │  │  └─ Claude Code revises if needed
  │  │
  │  ├─ Step 4: Section Writing (Claude Code, You)
  │  │  │
  │  │  ├─ Section 1
  │  │  │  ├─ Claude Code writes draft
  │  │  │  ├─ You review (accuracy, clarity, citations)
  │  │  │  └─ You approve or request revision
  │  │  │
  │  │  ├─ Section 2, 3, 4... (repeat)
  │  │  │
  │  │  ├─ Introduction
  │  │  │  ├─ Claude Code writes
  │  │  │  └─ You review & approve
  │  │  │
  │  │  └─ Conclusion
  │  │     ├─ Claude Code writes
  │  │     └─ You review & approve
  │  │
  │  └─ Step 5: Draft Compilation (You)
  │     └─ Combine all sections into single article draft
  │
  ├─ REFINEMENT (1-2 hours)
  │  ├─ Quality Verification
  │  │  ├─ Facts accurate?
  │  │  ├─ Citations complete?
  │  │  ├─ Clear for audience?
  │  │  └─ All questions answered?
  │  │
  │  ├─ Final Editing
  │  │  ├─ Typos fixed
  │  │  ├─ Clarity improved
  │  │  ├─ Tone consistent
  │  │  └─ Citations formatted
  │  │
  │  └─ Publication
  │     ├─ Update: content/insights/[article].md
  │     ├─ Build: hugo --minify
  │     ├─ Test: hugo server
  │     └─ Deploy: wrangler pages deploy
  │
  └─ PUBLISHED
     └─ Article live at https://rinji.id/insights/[article]/
```

---

## Research Quality Spectrum

```
SHALLOW (❌ Don't do this)
│
├─ 1 source
├─ Generic findings
├─ No synthesis
├─ Quick write-up
├─ Result: Surface-level, not credible
│
│
MODERATE (✓ Acceptable)
│
├─ 3-5 sources
├─ Key findings documented
├─ Some synthesis
├─ Decent article (1500-2000 words)
├─ Result: Competent but not distinguished
│
│
DEEP (✓✓ Target this)
│
├─ 5-10+ diverse sources
├─ Thorough findings extraction
├─ Strong synthesis & original insights
├─ Research-backed article (2500-3500 words)
├─ Result: Credible thought leadership
│
│
EXHAUSTIVE (❌ Overkill unless specialist)
│
├─ 15+ sources
├─ Weeks of research
├─ Academic-level depth
├─ Result: Too much for time investment
```

**Target: DEEP level (5-6 hours research, 2500-3500 word article)**

---

## Claude Code Integration Patterns

```
PATTERN 1: Research First (Recommended)
┌────────────────────────────────────┐
│ 1. Complete Research (4-6 hours)   │ You work solo
│ 2. Compile Notes                   │ Structured notes
│ 3. Submit to Claude Code ────────► │ Claude Code reads
│ 4. Outline Review ◄────────────── │ You approve structure
│ 5. Section Writing ──────────────► │ Claude Code writes iteratively
│ 6. Review Each Section ◄────────── │ You review each section
│ 7. Refinement (1-2 hours)          │ You edit & publish
└────────────────────────────────────┘
BENEFIT: Clear research → coherent article
EFFORT: 8-11 hours total


PATTERN 2: Concurrent (Learning as you go)
┌────────────────────────────────────┐
│ 1. Quick Scope (30 min)            │ You define
│ 2. Initial Research (2 hours)      │ You gather quick sources
│ 3. Submit to Claude Code ────────► │ Outline + gap identification
│ 4. Focused Research (3-4 hours)    │ You research identified gaps
│ 5. Final Writing ────────────────► │ Claude Code writes
│ 6. Refinement (1-2 hours)          │ You edit & publish
└────────────────────────────────────┘
BENEFIT: Writing clarifies what you need to know
EFFORT: 8-10 hours total


PATTERN 3: Iterative (Section by section)
┌────────────────────────────────────┐
│ 1. Research Sec 1 (1-2 hours)      │ You research
│ 2. Write Sec 1 ──────────────────► │ Claude Code writes
│ 3. Review → identify what's needed │ Feedback loop
│ 4. Research Sec 2 (1-2 hours)      │ You research
│ 5. Write Sec 2 ──────────────────► │ Claude Code writes
│ ... repeat for remaining sections
│ 6. Refinement (1-2 hours)          │ You edit & publish
└────────────────────────────────────┘
BENEFIT: Natural iteration, continuous improvement
EFFORT: 9-12 hours total
```

---

## Files Organization

```
rinji-id/
│
├── WORKFLOW DOCUMENTATION
│   ├── QUICK_START_RESEARCH.md ←── START HERE
│   ├── RESEARCH_WORKFLOW.md
│   ├── CLAUDE_CODE_RESEARCH_INTEGRATION.md
│   ├── RESEARCH_WORKFLOW_SUMMARY.md
│   ├── RESEARCH_ARTICLE_CHECKLIST.md
│   └── RESEARCH_WORKFLOW_VISUAL.md (you are here)
│
├── research/ ←── RESEARCH NOTES FOLDER
│   ├── README.md
│   ├── template.md ←── COPY THIS FOR EACH ARTICLE
│   ├── insights/
│   │   ├── benchmark-pdam-notes.md (when you research it)
│   │   ├── tren-industri-notes.md
│   │   └── regulasi-landscape-notes.md
│   ├── resources/
│   │   ├── grc-framework-notes.md
│   │   └── checklist-nrw-notes.md
│   └── pemikiran/
│       ├── masa-depan-air-notes.md
│       └── kepemimpinan-transformasi-notes.md
│
├── content/ ←── PUBLISHED ARTICLES
│   ├── _index.md
│   ├── about.md
│   ├── contact.md
│   ├── expertise/
│   │   ├── _index.md
│   │   ├── digital-transformation.md
│   │   ├── grc.md
│   │   ├── nrw.md
│   │   └── cybersecurity.md
│   ├── insights/ ←── NEW SECTION
│   │   ├── _index.md
│   │   ├── benchmark-pdam.md (published article)
│   │   ├── tren-industri.md
│   │   └── regulasi-landscape.md
│   ├── resources/ ←── NEW SECTION
│   │   ├── _index.md
│   │   ├── grc-framework.md
│   │   └── checklist-nrw.md
│   └── pemikiran/ ←── NEW SECTION
│       ├── _index.md
│       ├── masa-depan-air.md
│       └── kepemimpinan-transformasi.md
│
└── public/ ←── BUILD OUTPUT (generated)
```

---

## Time Investment vs Output Quality

```
Time Investment (Hours)    │ Output Quality
────────────────────────   ├─────────────────────────────────────
1-2 hours                  │ ❌ Too shallow
(quick summary)            │    └─ Generic, no citations, surface
                           │
2-4 hours                  │ ✗ Still shallow
(limited research)         │   └─ Better but lacks depth
                           │
4-6 hours ┐                │ ✓ GOOD
(moderate) ├─ TARGET ZONE  │   └─ Professional, research-backed
8-11 hours┘(8-11 total)    │       2500-3500 words, 5-10 sources
                           │
12-16 hours                │ ✓✓ EXCELLENT
(extensive research)       │   └─ Comprehensive, thought leadership
                           │
20+ hours                  │ ❌ Diminishing returns
(exhaustive)               │    └─ Overkill for web articles
```

**Sweet spot: 6 hours research + 2 hours writing = 8 hours investment = professional article**

---

## Decision Tree: Which Integration Method?

```
START: Choosing Integration Method
│
├─ Do you have 4-6 hours to research first?
│  │
│  ├─ YES ──► Use METHOD 1: Research First (Recommended)
│  │          └─ Complete all research before writing
│  │          └─ Best for coherent, well-structured articles
│  │          └─ Timeline: 1-2 weeks per article
│  │
│  └─ NO ──┐
│          │
│          ├─ Do you want learning feedback during writing?
│          │  │
│          │  ├─ YES ──► Use METHOD 3: Iterative (Section-by-section)
│          │  │          └─ Research → Write → Learn → Research more
│          │  │          └─ Good for exploring topics
│          │  │          └─ Timeline: 2-3 weeks per article
│          │  │
│          │  └─ NO ──► Use METHOD 2: Concurrent (Parallel)
│          │           └─ Quick initial research + outline guidance
│          │           └─ Then deepen research for gaps
│          │           └─ Timeline: 1.5-2 weeks per article
```

---

## Article Quality Checklist (Visual)

```
Research Thoroughness:     [████████░░] 80%
┌─────────────────────────────────────┐
│ ✓ 5-10+ diverse sources             │
│ ✓ All key questions addressed       │
│ ✓ Original synthesis included       │
│ ✗ Gaps acknowledged (still needed)  │
└─────────────────────────────────────┘

Writing Quality:           [███████░░░] 70%
┌─────────────────────────────────────┐
│ ✓ Clear & well-organized            │
│ ✓ Proper citations throughout       │
│ ✓ Good examples included             │
│ ✗ Some redundancy (needs editing)   │
└─────────────────────────────────────┘

Publication Readiness:     [██████░░░░] 60%
┌─────────────────────────────────────┐
│ ✓ Facts verified                    │
│ ✓ Format correct (frontmatter, etc) │
│ ✗ Typos remain                      │
│ ✗ Citation formatting inconsistent  │
└─────────────────────────────────────┘

OVERALL QUALITY SCORE:     [██████░░░░] 70%
Status: Ready for Publication (with minor edits)
```

---

## Weekly Progress Template

```
WEEK 1: Article - "Benchmark Kinerja PDAM"
┌─────────────────────────────────────┐
│ Mon-Tue: Research (6 hours)         │ ████░░░░░░
│ Wed:     Compile Notes (1 hour)     │ █░░░░░░░░░
│ Thu:     Claude Code Outline (1 hr) │ █░░░░░░░░░
│ Fri:     Claude Code Writing (2 hr) │ ██░░░░░░░░
│          Refinement (1.5 hr)        │ █░░░░░░░░░
├─────────────────────────────────────┤
│ TOTAL EFFORT: 11.5 hours            │
│ STATUS: Published ✓                 │
└─────────────────────────────────────┘

WEEK 2: Article - "Tren Industri Air Indonesia"
┌─────────────────────────────────────┐
│ Mon-Tue: Research (6 hours)         │ ████░░░░░░
│ Wed:     Compile Notes (1 hour)     │ █░░░░░░░░░
│ Thu:     Claude Code Outline (1 hr) │ █░░░░░░░░░
│ Fri:     Claude Code Writing (2 hr) │ ██░░░░░░░░
│          Refinement (1.5 hr)        │ █░░░░░░░░░
├─────────────────────────────────────┤
│ TOTAL EFFORT: 11.5 hours            │
│ STATUS: Published ✓                 │
└─────────────────────────────────────┘

WEEK 3: Article - "Landscape Regulasi Industri Air"
┌─────────────────────────────────────┐
│ Mon-Tue: Research (6 hours)         │ ████░░░░░░
│ Wed:     Compile Notes (1 hour)     │ █░░░░░░░░░
│ Thu:     Claude Code Outline (1 hr) │ █░░░░░░░░░
│ Fri:     Claude Code Writing (2 hr) │ ██░░░░░░░░
│          Refinement (1.5 hr)        │ █░░░░░░░░░
├─────────────────────────────────────┤
│ TOTAL EFFORT: 11.5 hours            │
│ STATUS: Published ✓                 │
└─────────────────────────────────────┘

TOTAL 3-WEEK EFFORT: ~34 hours
RESULT: 3 professional articles published
```

---

## Success Indicators

```
Article: "Benchmark Kinerja PDAM"

❌ SHALLOW ARTICLE (What we're avoiding)
├─ 1000 words
├─ 2-3 sources
├─ Generic analysis
├─ No citations
└─ Audience reaction: "Nice, but I already knew this"

✓ GOOD ARTICLE (Acceptable)
├─ 2000 words
├─ 5 sources
├─ Decent analysis
├─ Basic citations
└─ Audience reaction: "Informative, useful reference"

✓✓ EXCELLENT ARTICLE (Target)
├─ 2500-3500 words
├─ 7-10 diverse sources
├─ Original insights & synthesis
├─ Proper citations throughout
└─ Audience reaction: "This is authoritative. Bookmarking."
```

---

## Next Steps (Visual)

```
TODAY:
└─ Read QUICK_START_RESEARCH.md (15 min)

THIS WEEK:
├─ Define first article scope (30 min)
├─ Conduct research (4-6 hours)
└─ Compile notes to template (30 min)

NEXT WEEK:
├─ Submit research to Claude Code
├─ Work through section writing
└─ Publish first article

FOLLOWING WEEKS:
├─ Article 2 (same process)
├─ Article 3 (same process)
└─ Build into sustainable rhythm
```

---

**Ready to start? Begin with QUICK_START_RESEARCH.md** 🚀
