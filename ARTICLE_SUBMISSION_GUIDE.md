# Article Submission Guide: Research to Publication

Simplified workflow: **You do research → Save file → Claude Code writes & publishes article**

---

## Quick Overview

```
YOUR WORK:
1. Conduct deep research (use ChatGPT, Gemini, Claude.ai, whatever)
2. Save findings to file (PDF, DOCX, or MD format)
3. Submit file to Claude Code with brief instruction

CLAUDE CODE'S WORK:
1. Read your research file
2. Extract key findings & organize
3. Write polished article with citations
4. Auto-commit to git + auto-deploy to rinji.id
5. Send you confirmation + live URL

RESULT: Article published & live within 1-2 hours
```

---

## How to Submit Research File

### Step 1: Do Your Research
- Use ChatGPT, Claude.ai, Gemini, or your preferred tool
- Gather sources, compile findings, synthesize
- No specific format required—just capture what you need

### Step 2: Save Your Research

**Option A: Save as PDF**
- Copy findings to PDF file
- Filename: `[article-title]-research.pdf`
- Example: `benchmark-pdam-research.pdf`
- Save to: Desktop or preferred location

**Option B: Save as DOCX (Microsoft Word)**
- Use Word document format
- Filename: `[article-title]-research.docx`
- Organized with sections & key points
- Save to: Desktop or preferred location

**Option C: Save as Markdown (.md)**
- Create markdown file with sections
- Filename: `[article-title]-research.md`
- Use simple formatting (headers, bullets, etc.)
- Save to: Desktop or preferred location

### Step 3: Submit to Claude Code

**Send me a message with:**

```
FILE: [Attach your research file]

ARTICLE DETAILS:
- Title: [Article title]
- Section: [insights / resources / pemikiran]
- Target length: [2000-3000 words typical]
- Target audience: [PDAM leaders / Regulators / General / etc.]

KEY INSTRUCTIONS:
[Any specific requirements or emphasis areas]

RESEARCH FILE CONTAINS:
[Brief description of what's in the research]
```

**Example submission:**
```
FILE: benchmark-pdam-research.pdf

ARTICLE DETAILS:
- Title: Benchmark Kinerja PDAM Indonesia
- Section: insights
- Target length: 2500-3000 words
- Target audience: PDAM leaders and regulators

KEY INSTRUCTIONS:
- Emphasize practical implications for PDAM leaders
- Include financial impact calculation example
- Highlight top performers with characteristics

RESEARCH FILE CONTAINS:
- NRW statistics from government sources
- PERPAMSI benchmark data
- Case studies from 4 PDAM different tiers
- Cost recovery analysis
- Service coverage comparison
```

---

## How Claude Code Processes Your Research

### Stage 1: File Reading & Analysis
- Claude Code reads your research file (PDF, DOCX, or MD)
- Extract key findings, data, examples
- Identify sources & citations needed

### Stage 2: Article Structure
- Determine logical section organization
- Based on research content & target audience
- Create outline with flow

### Stage 3: Article Writing
- Write polished, professional article
- 2000-3500 words (adjust based on content)
- Include citations throughout
- Add complete reference list at end

### Stage 4: Publication
- Create markdown file: `content/[section]/[article-slug].md`
- Add proper frontmatter (title, description, date)
- Commit to git with message
- Run Hugo build
- Deploy to Cloudflare Pages
- Article live at: https://rinji.id/[section]/[article-slug]/

### Stage 5: Confirmation
- Send you confirmation message
- Include live URL
- Ready for sharing/promotion

---

## Research File Format (Best Practices)

While any format works, structured research is easier to convert. Suggested structure:

### PDF/DOCX Format
```
RESEARCH NOTES: [Article Title]

TARGET AUDIENCE:
[Who this article is for]

KEY SECTIONS:
1. [Section title]
   - Key point 1
   - Key point 2
   - Key point 3

2. [Section title]
   - Key point 1
   - Key point 2

KEY STATISTICS:
- Statistic 1: [value + source]
- Statistic 2: [value + source]

CASE STUDIES/EXAMPLES:
- Example 1: [brief description + source]
- Example 2: [brief description + source]

SOURCES & REFERENCES:
- Source 1: [URL/citation]
- Source 2: [URL/citation]

SYNTHESIS/INSIGHTS:
[Your synthesis of findings, not just summaries]
```

### Markdown Format
```markdown
# Research Notes: [Article Title]

**Target Audience:** [...]

## Key Sections

### Section 1: [Title]
- Key point 1
- Key point 2
- Key point 3

### Section 2: [Title]
- Key point 1
- Key point 2

## Key Statistics
- Stat 1: [value] (Source: ...)
- Stat 2: [value] (Source: ...)

## Case Studies
- Example 1: [description]
- Example 2: [description]

## Sources
- [Source 1](URL)
- [Source 2](URL)

## Synthesis
[Your analysis]
```

---

## What Makes Good Research Input

✅ **Good Research Input:**
- Clear organization (sections, key points)
- Specific data & statistics (with sources mentioned)
- Concrete examples & case studies
- Original analysis/synthesis (not just summaries)
- Multiple perspectives/sources referenced

❌ **Problematic Research Input:**
- Completely unstructured text dump
- No sources mentioned
- Only summaries, no original thinking
- Vague statements without backing data
- All from single source

**Note:** Even mediocre research will be improved through Claude Code writing, but better research → better article. Garbage in = garbage out still applies.

---

## Turnaround Time

### Timeline
- Submit research file
- Claude Code processes: 30-60 minutes (reading, analysis, writing)
- Publish & deploy: 10-15 minutes
- **Total: 45-75 minutes** from submission to live URL

### What Affects Timeline
- Research file complexity (structured = faster)
- Article length (2500 words vs 3500 words)
- Number of revisions requested
- Time of day (no delays for timezone)

---

## Examples: From Research to Published Article

### Example 1: PDF Research → Article
```
INPUT:
File: benchmark-pdam-research.pdf
Contains: NRW statistics, PERPAMSI data, case studies

PROCESS:
1. Claude Code reads PDF
2. Extracts key findings
3. Organizes into article structure
4. Writes 2800-word article
5. Adds citations
6. Commits & deploys

OUTPUT:
Article published at:
https://rinji.id/insights/benchmark-kinerja-pdam/
```

### Example 2: DOCX Research → Article
```
INPUT:
File: tren-industri-research.docx
Contains: Structured notes with trends, predictions, case studies

PROCESS:
1. Claude Code reads DOCX
2. Extracts sections
3. Creates article flow
4. Writes 3000-word article with examples
5. Formats references
6. Publishes

OUTPUT:
Article live & shareable within 1 hour
```

### Example 3: Markdown Research → Article
```
INPUT:
File: regulasi-landscape-research.md
Contains: Regulatory info, compliance requirements, implications

PROCESS:
1. Claude Code reads markdown
2. Enhances structure & clarity
3. Writes comprehensive article
4. Includes all regulatory details
5. Auto-publishes

OUTPUT:
Professional article with proper citations
```

---

## Common Questions

**Q: What if my research file is messy/unorganized?**
A: Claude Code will organize it. But cleaner input = better output. Spend 10 min organizing before submitting.

**Q: Can I submit multiple research files for one article?**
A: Yes. Send them all in one message. Claude Code will integrate findings.

**Q: What if I want to edit the article after publication?**
A: Tell me what to change. I'll update the file, commit, and redeploy. Quick turnaround.

**Q: Can I request specific article structure/sections?**
A: Yes. Mention in submission. Example: "Please structure as: Intro → Problem → Solution → Case Study → Implications"

**Q: What if research is from ChatGPT/AI and I want human verification?**
A: Mention it. I'll try to verify key claims or flag uncertain areas. But trust your research source.

**Q: How are citations handled?**
A: I'll add them throughout article (Author Year format). Make sure your research file mentions sources—makes citations easier.

**Q: Can I track what was published?**
A: Yes. I'll send you live URL, git commit hash, and deployment confirmation. Everything traceable.

---

## Checklist: Before Submitting Research

### Research Quality
- [ ] Research is substantive (5-10+ sources worth of findings)
- [ ] Key statistics included (with sources)
- [ ] Multiple perspectives considered
- [ ] Original synthesis included (not just summaries)
- [ ] Gaps/limitations acknowledged

### File Preparation
- [ ] File saved in PDF/DOCX/MD format
- [ ] Filename is descriptive
- [ ] Content is organized (sections/key points)
- [ ] References/sources mentioned
- [ ] Clear & readable (even if rough)

### Submission
- [ ] Research file attached/shared
- [ ] Article details provided (title, section, audience)
- [ ] Key instructions mentioned
- [ ] Reasonable expectations (2-3 hour turnaround)

---

## Workflow at a Glance

```
YOU:
1. Research (2-6 hours, your pace, tools of choice)
2. Save file (PDF/DOCX/MD)
3. Submit to Claude Code (5 min)

CLAUDE CODE:
1. Read research file (15 min)
2. Write article (30-45 min)
3. Commit & deploy (10 min)

RESULT:
✓ Article published & live
✓ URL provided
✓ Ready for sharing
```

---

## Setting Expectations

### What Claude Code Will Do
✅ Read your research carefully
✅ Write professional, well-organized article
✅ Include proper citations
✅ Publish immediately
✅ Revise if requested

### What Claude Code Won't Do
❌ Fact-check your research (assumes you did that)
❌ Find additional sources (work from what you provide)
❌ Change fundamental article angle (based on your research)
❌ Rewrite multiple times without feedback

### Speed Expectation
- Simple research → 45 min turnaround
- Complex research → 75 min turnaround
- Requested revisions → +15-30 min per round

---

## Getting Started

### First Submission
1. Do your research (use your preferred tools/methods)
2. Save findings to file (any of 3 formats)
3. Message me with file + article details (copy template below)
4. Check back in 1-2 hours—article will be live

### Template for Submission

```markdown
FILE: [your-research-file.pdf/docx/md]

ARTICLE DETAILS:
- Title: [Article Title]
- Section: [insights / resources / pemikiran]
- Target length: [2000-3000 words, or flexible]
- Target audience: [Who reads this]

KEY INSTRUCTIONS:
[Any specific requirements]

BRIEF DESCRIPTION:
[What's in the research file]

PUBLISH AS:
https://rinji.id/[section]/[article-slug]/
```

---

## Success Indicators

**Good Research Submission:**
- [ ] Substantive findings (not surface-level)
- [ ] Multiple sources evident
- [ ] Clear sections/organization
- [ ] Statistics with sources
- [ ] Examples/case studies
- [ ] Original analysis included

**Good Published Article:**
- [ ] 2500-3500 words (substantive length)
- [ ] Clear organization (4-5 sections)
- [ ] Proper citations throughout
- [ ] Complete reference list
- [ ] Professional tone & quality
- [ ] Serves target audience well

---

## Next Steps

Ready to submit your first research?

1. **Do your research** (2-6 hours, your pace)
2. **Save to file** (PDF, DOCX, or MD)
3. **Send me message with:**
   - File attachment
   - Article details (title, section, audience)
   - Key instructions
4. **Check back in 1-2 hours**
   - Article will be published & live
   - You get URL + confirmation

That's it! Simple workflow: Research → File → Claude Code → Published Article

---

Last updated: December 20, 2025
