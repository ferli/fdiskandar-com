# Quick Start: Deep Research + Claude Code Article Writing

Workflow praktis untuk menulis artikel berkualitas tinggi dengan deep research integration.

## TL;DR: 5 Steps

1. **Define scope** (15 min) — What's the article about? What questions must it answer?
2. **Research** (4-6 hours) — Gather sources, extract findings, synthesize
3. **Compile notes** (30 min) — Organize findings dalam template structure
4. **Claude Code write** (1-2 hours) — Claude Code synthesize + write draft
5. **Edit & publish** (1-2 hours) — Final review, citations, deploy

**Total per article: 7-11 hours for deep, substantive content**

---

## Step 1: Define Scope (15 minutes)

For the article you're researching, answer:

**What is this article about?**
- Title: [Article title]
- Scope: [1-2 sentences on what article covers]
- Audience: [Who will read this? PDAM leaders? Regulators? Managers?]

**What must it answer?** (4-5 key questions)
- Question 1: [Key question reader needs answered]
- Question 2: [Key question reader needs answered]
- Question 3: [Key question reader needs answered]
- Question 4: [Key question reader needs answered]

**What counts as evidence?**
- Type 1: [What kind of source? Government data? Case studies? Academic research?]
- Type 2: [...]
- Type 3: [...]

**Example - "Benchmark Kinerja PDAM":**
```
Title: Benchmark Kinerja PDAM Indonesia - Data Terbaru & Analisis

Scope: Article will compare PDAM performance across Indonesia (NRW, coverage,
cost recovery, service quality) dengan benchmarking framework, provide context
tentang variation antar tier/region, identify best practices.

Audience: PDAM leaders, regulators, consultants, media interested dalam
comparative performance data

Key Questions:
1. Berapa NRW rata-rata PDAM Indonesia saat ini? Variasi antar tier/region?
2. Berapa coverage & service quality metrics?
3. Apa trend 10 tahun terakhir?
4. Siapa best performer & apa characteristics mereka?
5. Apa improvement opportunities based on comparisons?

Evidence Needed:
- Government statistics (PUPR, BPS, BPPN)
- PERPAMSI reports & benchmarking data
- Individual PDAM annual reports (3-4 sample)
- Academic research on water utility performance
- International data untuk context (WHO, World Bank)
```

---

## Step 2: Research (4-6 hours)

### 2.1 Where to Find Information

**Government Sources:**
- Kementerian PUPR (pupr.go.id) — Infrastructure & water policy
- Badan Pusat Statistik (bps.go.id) — Official statistics
- BPPN (bppn.go.id) — Government data portal
- Individual PDAM websites & annual reports

**Industry Sources:**
- PERPAMSI (perpamsi.or.id) — Water utility association
- PDAM member publications & benchmarking reports
- Industry conferences & proceedings

**Academic & Research:**
- Google Scholar (scholar.google.com)
- ResearchGate (researchgate.net)
- University repositories
- Indonesian journals (JISI, Jurnal Teknik Sipil, etc.)

**International Context:**
- World Bank Water Reports
- WHO Guidelines & reports
- IWA (International Water Association) publications
- UNICEF Water & Sanitation reports

### 2.2 How to Extract Information

For EACH source you find:

1. **Record the source**
   - Full URL atau citation
   - Author/organization name
   - Date published
   - Date you accessed it

2. **Extract key findings**
   - What is the main finding?
   - What evidence supports it?
   - What statistics are provided?
   - Any case studies atau examples?

3. **Note relevant details**
   - Exact quotes jika important
   - Specific numbers & metrics
   - Geographic atau temporal scope (when/where data is from)
   - Caveats atau limitations mentioned

4. **Assess relevance**
   - How does this relate ke research questions?
   - Will it be cited in final article?
   - Does it provide essential context?

### 2.3 What You're Looking For

As you research, extract specifically:

**For Benchmark Article:**
- NRW percentages (national average, per tier, per region)
- Coverage percentages (urban vs rural, by region)
- Cost recovery ratios (how many PDAM achieve sustainability)
- Service quality metrics (hours of service, water quality)
- Trends (how have these metrics changed over time?)
- Best performers (which PDAM excel and why?)
- Case studies (detailed examples of improvement)

**Synthesize:** What patterns emerge? Which PDAM succeed and why? What's the landscape?

---

## Step 3: Compile Notes (30 minutes to 1 hour)

Use template structure: `research/template.md`

1. **Copy template:** `cp research/template.md research/insights/benchmark-pdam-notes.md`

2. **Fill in article scope:**
   - Title, target audience, key questions
   - Evidence needed, source strategy

3. **For each source found, document:**
   ```
   ### Source N: [Name]
   Type: [Government/Academic/Industry/etc.]
   URL: [link]
   Date accessed: [when you read it]

   Key findings:
   - Finding 1
   - Finding 2

   Relevant statistics:
   - Stat 1: [value + source]
   - Stat 2: [value + source]

   Relevance: [Why this matters untuk article]
   ```

4. **Synthesize findings:**
   - What themes appear across multiple sources?
   - Any contradictions you need to reconcile?
   - What original insights can you draw from combining these sources?

5. **Propose article structure:**
   - Based on research, what sections make sense?
   - What will each section cover?
   - Which sources support each section?

6. **Create reference list:**
   - Complete citation untuk every source
   - Formatted consistently

---

## Step 4: Claude Code Write (1-2 hours)

Once research notes complete, you're ready untuk Claude Code.

### 4.1 Prepare

- [ ] Research notes file complete & well-organized
- [ ] All key questions addressed in research
- [ ] Synthesis section includes original analysis
- [ ] Reference list prepared
- [ ] Proposed article structure clear

### 4.2 Submit Task to Claude Code

Use Claude Code CLI (or continue conversation):

```
TASK: Write article based on research

I've completed deep research (6+ hours) untuk article: [Article Title]

Research findings compiled di: research/insights/[article]-notes.md

REQUEST:
1. Read research notes file completely
2. Synthesize findings into well-structured article (2500-3000 words)
3. Maintain academic rigor & cite sources throughout
4. Write for audience: [describe audience]
5. Include citations (Author Year format minimum)
6. Add complete reference section at end
7. Organize with clear section headers & logical flow

TONE: Professional, analytical, accessible (avoid jargon without explanation)

OUTPUT FORMAT:
- Markdown format ready untuk website
- Include frontmatter (title, description, date)
- Citations integrated into text
- Reference section at bottom

START BY:
- Summarizing key insights dari research (3-5 main insights)
- Proposing logical article structure (3-5 main sections)
- Then write article draft section by section
```

### 4.3 Work with Claude Code

Typical iteration:
1. Claude Code summarize research & propose structure → You review, approve or adjust
2. Claude Code writes Section 1 → You review, provide feedback
3. Claude Code revises Section 1 based on feedback
4. Claude Code writes Section 2, 3, etc. (same cycle)
5. Final draft complete → Move to editing

---

## Step 5: Edit & Publish (1-2 hours)

### 5.1 Quality Check

- [ ] Facts & statistics accurate & sourced?
- [ ] Clear untuk target audience?
- [ ] Logical flow between sections?
- [ ] All key questions answered?
- [ ] Proper citations throughout?
- [ ] Complete reference list?
- [ ] Professional tone consistent?

### 5.2 Add Final Polish

- Fix typos & grammar
- Improve clarity (rewrite dense sentences)
- Check citations format is consistent
- Ensure references formatted properly

### 5.3 Publish

1. Update file: `content/insights/[article-title].md`
2. Add frontmatter:
   ```yaml
   ---
   title: "[Full Article Title]"
   description: "[1-2 sentence summary]"
   date: 2025-12-20
   ---
   ```
3. Rebuild: `hugo --minify`
4. Deploy: `wrangler pages deploy public/ --project-name rinji-id`

---

## Example: Starting with "Benchmark Kinerja PDAM"

**Time estimate: 8-10 hours total**

### Phase 1: Define (15 min)
```
Article: Benchmark Kinerja PDAM Indonesia
Key questions:
1. Current NRW rates?
2. What variation by PDAM tier?
3. 10-year trends?
4. Best practices?
Evidence: Gov stats, PERPAMSI data, case studies, academic research
```

### Phase 2: Research (5-6 hours)
- Search government statistics (PUPR, BPS)
- Find PERPAMSI benchmark reports
- Read 3-4 academic papers on water utility performance
- Get data dari 3-4 sample PDAM (annual reports)
- Compile statistics & findings

### Phase 3: Compile Notes (1 hour)
- Copy template to `research/insights/benchmark-pdam-notes.md`
- Fill in all sections (sources, findings, synthesis)
- Propose article structure
- Create reference list

### Phase 4: Claude Code (1-2 hours)
- Submit research file + writing task
- Review proposed structure
- Get draft written
- Iterate on sections
- Final draft ready

### Phase 5: Polish & Publish (1 hour)
- Final edit for clarity & accuracy
- Check all citations
- Rebuild & deploy

**Result: Professional, research-backed article (~2500-3000 words) vs shallow 1000-word article**

---

## When You're Ready

1. **Pick first article** (recommend: Benchmark Kinerja PDAM)
2. **Define scope** using section Step 1
3. **Conduct research** using tips in Step 2
4. **Compile notes** using template in Step 3
5. **Submit to Claude Code** using guidance in Step 4
6. **Edit & publish** following Step 5

Entire process can be iterative—start with research, iterate with Claude Code based on what you learn.

---

## Pro Tips

1. **Start with research you know** — If you already have subject matter expertise, capture that knowledge in notes. Claude Code can then validate & deepen with additional research.

2. **Save research for future updates** — Once article published, research notes become basis for future updates. Periodically revisit & refresh data.

3. **Reuse research across articles** — Research untuk one article often provides context untuk others. Benchmark article data useful untuk Insights about trends & industry landscape.

4. **Quality over speed** — 8-10 hours invested in one great article beats publishing 3 shallow articles. Focus on depth & rigor.

5. **Build research discipline** — Consistent research → consistent quality → builds reputation as thought leader.

---

## Questions?

See full documentation:
- `RESEARCH_WORKFLOW.md` — Complete workflow with all phases
- `research/template.md` — Research note template with detailed guidance
- `research/README.md` — Research directory guide

---

**Ready to start? Pick your first article & begin research!**
