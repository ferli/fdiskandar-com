# Research Workflow untuk Deep Article Writing

Dokumen ini outline workflow efisien untuk integrating deep research dengan Claude Code CLI untuk menulis artikel berkualitas tinggi.

## Overview Workflow

```
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 1: RESEARCH PREPARATION (1-2 jam)                        │
├─────────────────────────────────────────────────────────────────┤
│ • Define research scope & key questions                          │
│ • Identify source categories (academic, industry, regulatory)    │
│ • Create research note template                                  │
│ • Set up research folder structure                               │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 2: DEEP RESEARCH (3-6 jam per article)                    │
├─────────────────────────────────────────────────────────────────┤
│ • Conduct web research (web search, read articles, extract data) │
│ • Compile findings into structured notes                         │
│ • Synthesize data & identify key insights                        │
│ • Flag gaps & questions untuk follow-up                          │
│ • Save research notes as markdown files in /research/ folder     │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 3: CLAUDE CODE INTEGRATION (2-3 jam per article)          │
├─────────────────────────────────────────────────────────────────┤
│ • Run Claude Code with research notes as context                 │
│ • Claude Code reads research files → writes article draft        │
│ • Claude Code suggests citations & references                    │
│ • User review & refine draft                                     │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 4: REFINEMENT & PUBLICATION (1-2 jam)                     │
├─────────────────────────────────────────────────────────────────┤
│ • Final edit for clarity, flow, accuracy                         │
│ • Add citations & references                                     │
│ • Update file di /content/ folder                                │
│ • Rebuild & deploy                                               │
└─────────────────────────────────────────────────────────────────┘
```

## PHASE 1: Research Preparation

### 1.1 Define Article Scope

For each article, define:
- **Title & Scope** — What exactly are we covering?
- **Key Questions** — What does audience need to know?
- **Evidence Needed** — What data/research needed to support claims?
- **Source Strategy** — What types of sources will we use?

**Example for "Benchmark Kinerja PDAM":**
```
Title: Benchmark Kinerja PDAM Indonesia - Data & Analisis Terbaru

Key Questions:
1. Berapa NRW rata-rata PDAM Indonesia saat ini?
2. Apa variasi antar PDAM (Tier 1 vs 2 vs 3)?
3. Trend 5-10 tahun terakhir?
4. Apa best practice dari PDAM high-performer?

Evidence Needed:
- Latest statistics dari PERPAMSI, Kementerian PUPR
- Case studies dari 3-4 PDAM berbeda size/region
- Academic research tentang water utility performance
- International comparison untuk context

Source Strategy:
- Government reports & statistical agencies
- Industry association (PERPAMSI) publications
- Academic journals & research papers
- Case studies & best practice documentation
```

### 1.2 Create Research Note Template

Gunakan template consistent untuk semua research findings:

```markdown
# Research Notes: [Article Title]

**Article Scope:** [Brief description]
**Target Audience:** [Who this is for]
**Key Questions:** [List key questions]

---

## Source 1: [Source Name]
**Type:** [Government/Academic/Industry/Case Study]
**URL/Citation:** [Link atau full citation]
**Date Accessed:** [Date]

### Key Findings:
- Finding 1
- Finding 2
- Finding 3

### Data/Statistics:
- Stat 1: [value & source]
- Stat 2: [value & source]

### Relevant Quote:
> "Direct quote dari source"
- Citation: [author, year]

### Relevance to Article:
[Why this source matters untuk article]

---

## Source 2: [Next source...]
...

---

## Synthesis & Analysis

### Common Themes:
- Theme 1: [supported by sources X, Y, Z]
- Theme 2: [supported by sources...]

### Gaps/Questions:
- Question 1: [need to research more]
- Question 2: [potential limitation]

### Key Insights (Author Synthesis):
- Insight 1: [based on sources ABC]
- Insight 2: [based on sources DEF]

### Potential Article Structure:
1. [Section based on research]
2. [Section based on research]
3. [Synthesis/original analysis]

---

## References Ready for Article
[List all sources formatted for citation]
```

### 1.3 Folder Structure

Create directory untuk organize research:

```
rinji-id/
├── research/
│   ├── insights/
│   │   ├── benchmark-pdam-notes.md
│   │   ├── tren-industri-notes.md
│   │   └── regulasi-landscape-notes.md
│   ├── resources/
│   │   ├── grc-framework-notes.md
│   │   ├── checklist-nrw-notes.md
│   ├── template.md
│   └── README.md
├── content/
│   ├── insights/
│   │   ├── benchmark-pdam.md  ← Final article
│   │   └── ...
│   └── ...
```

## PHASE 2: Deep Research

### 2.1 Research Process

**Step 1: Identify & Access Sources**
- Government sources (PUPR, BPS, BPPN)
- Industry publications (PERPAMSI, water utility reports)
- Academic papers (Google Scholar, ResearchGate)
- News/media (for trends & case studies)
- International resources (WHO, World Bank, IWA untuk benchmarking)

**Step 2: Extract Key Information**
- Read with purpose (answer key questions)
- Extract findings in note template
- Note exact statistics dengan source reference
- Capture relevant quotes
- Document any limitations/caveats

**Step 3: Synthesize Findings**
- Identify patterns across sources
- Recognize contradictions & discuss
- Extract original insights (not just summarize)
- Identify gaps & limitations

**Step 4: Save as Markdown Notes**
- Use consistent format dari template
- Include URLs & citations
- Organize logically (by theme atau source type)
- Add synthesis section di akhir

### 2.2 Quality Checklist untuk Research

Before moving to writing phase:
- [ ] Covered all key questions identified di scope?
- [ ] Have 5-10+ sources minimum per article?
- [ ] Sources diverse (government, academic, industry, case study)?
- [ ] Statistics verified & sourced?
- [ ] Contradictions/nuance identified & discussed?
- [ ] Synthesis section reflects original analysis?
- [ ] Gaps/limitations acknowledged?

## PHASE 3: Claude Code Integration

### 3.1 Research File Preparation

Before running Claude Code:
1. Save research notes file: `research/insights/[article]-notes.md`
2. Ensure notes are well-structured & complete
3. Have notes file ready untuk Claude Code to read

### 3.2 Claude Code Task Prompt

Gunakan prompt seperti ini untuk Claude Code:

```
TASK: Write article: [Article Title]

CONTEXT:
I have completed 5-10 hours of deep research tentang topik ini.
Research findings sudah compiled dalam file: [path/to/research/notes.md]

YOUR JOB:
1. Read research notes file completely
2. Synthesize findings into coherent, well-structured article
3. Maintain academic rigor & cite sources properly
4. Target audience: [describe audience]
5. Desired article length: [2000-3000 words typically]
6. Tone: [professional, analytical, accessible to non-specialists]

OUTPUT:
- Write article draft dalam markdown format
- Include citations untuk all key claims (author, year format minimum)
- Add reference section di akhir
- Organize with clear headers & logical flow
- Include synthesis/original insights dari research, not just summaries

START BY:
- Summarizing key insights dari research
- Proposing logical article structure
- Writing draft section by section
```

### 3.3 How to Run Claude Code

**Option A: Direct CLI with file context**
```bash
# Terminal 1: Start Claude Code server
claude

# Terminal 2 (separate): Run specific task with research context
# (Describe your request, mentioning research file path)
# Claude Code CLI akan dapat read file dan integrate into response
```

**Option B: Read research first, then write**
```
1. Open research notes file
2. Provide path to Claude Code when submitting writing task
3. Ask Claude to read & synthesize from that file
```

### 3.4 Claude Code Writing Process

Expected workflow:
1. Claude Code reads research notes
2. Claude Code outlines proposed structure
3. User reviews structure (approve atau suggest changes)
4. Claude Code writes draft section-by-section
5. User review each section, provide feedback
6. Claude Code refine based on feedback
7. Final draft ready untuk editing

## PHASE 4: Refinement & Publication

### 4.1 Editing Checklist

- [ ] Accuracy: All facts & statistics correct & sourced?
- [ ] Clarity: Clear untuk target audience? (avoid jargon unless explained)
- [ ] Coherence: Logical flow between sections?
- [ ] Completeness: All key questions answered?
- [ ] Citations: Proper attribution throughout?
- [ ] References: Complete reference list at end?
- [ ] Length: Appropriate untuk article purpose?
- [ ] Tone: Consistent professional tone throughout?

### 4.2 Citation Format

Use consistent format throughout. Recommend:
- **In-text:** (Author Year) atau "Author (Year) found that..."
- **References:**
  ```
  Author First Name, Last Name. (Year). "Article Title."
  Publication Name, Volume(Issue), pages. URL [if available]
  ```

Example:
```
Sutrisno, Ari. (2019). "Non-Revenue Water Management dalam Utilitas Air Indonesia."
Jurnal Teknik Sipil, 15(2), 45-67.

World Bank. (2021). "Water Utility Performance: Global Benchmarks."
https://www.worldbank.org/...
```

### 4.3 File Update & Deployment

Once article complete:
1. Update file: `content/insights/[article-title].md`
2. Ensure frontmatter correct (title, description, date)
3. Run `hugo --minify` to rebuild
4. Test locally: `hugo server`
5. Deploy: `wrangler pages deploy public/ --project-name rinji-id`

---

## Timeline Estimate

**Per Article (Insights section example):**
- Phase 1 (Prep): 1-2 hours
- Phase 2 (Research): 4-6 hours
- Phase 3 (Claude integration): 2-3 hours
- Phase 4 (Refinement): 1-2 hours
- **Total: 8-13 hours per article**

**3 Insights Articles: 24-39 hours total**

---

## Tools & Resources

### Research Tools
- **Web Search:** Google Scholar, ResearchGate, direct site searches
- **Government Data:** BPS (bps.go.id), PUPR websites, regulatory sites
- **Industry:** PERPAMSI publications, utility annual reports
- **Academic:** Google Scholar, ResearchGate, university repositories
- **Claude Code:** For synthesis & writing

### File Editing
- VS Code atau text editor (untuk research notes)
- Hugo local server untuk preview

### Deployment
- Wrangler CLI (untuk Cloudflare Pages)

---

## Tips untuk Success

1. **Research thoroughly first** — Spend time in Phase 2. Good research = easy writing.
2. **Use consistent note format** — Makes Claude Code integration smoother.
3. **Include synthesis** — Don't just summarize sources; add original analysis.
4. **Cite everything** — Build trust through proper attribution.
5. **Get feedback early** — Share structure dengan Claude Code before full write.
6. **Iterate** — First draft rarely perfect; expect 2-3 rounds of refinement.
7. **Document sources** — Makes future updates & verification easier.

---

## Next Steps

Ready to start deep research on 3 Insights articles?

1. Pick article to research first (recommend: Benchmark Kinerja PDAM)
2. Define scope & key questions (Step 1.1)
3. Create research notes file using template (Step 1.2)
4. Conduct research & fill notes file (Phase 2)
5. Submit notes + writing task ke Claude Code (Phase 3)

Let me know when you ready to start!
