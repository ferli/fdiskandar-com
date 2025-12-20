# Simplified Article Workflow: Research to Publication

**The Simple Version**: You research → Save file → Claude Code publishes

---

## What Changed

### Before (Complex)
- You do research using template.md
- Compile findings into structured notes
- Submit to Claude Code for writing
- Long process, lots of documentation

### Now (Simple)
- You do research however you want (ChatGPT, Claude.ai, Gemini, etc.)
- Save findings to file (PDF, DOCX, or MD—doesn't matter)
- Submit file to Claude Code
- Article published within 1 hour

---

## The Workflow (Simple Version)

```
STEP 1: You Research (2-6 hours)
├─ Use ChatGPT, Claude.ai, Gemini, or any tool
├─ Gather findings, sources, data
├─ Synthesize insights
└─ No special format required

STEP 2: Save to File (5 minutes)
├─ PDF: Copy findings to PDF
├─ DOCX: Paste into Word document
├─ MD: Create markdown file with sections
└─ Save with descriptive filename

STEP 3: Submit to Claude Code (2 minutes)
├─ Attach research file
├─ Fill out simple intake form
├─ Describe what you want
└─ Send

STEP 4: Claude Code Processes (45-75 minutes)
├─ Reads your research file
├─ Extracts key findings
├─ Writes professional article (2500-3500 words)
├─ Adds citations & references
├─ Commits to git + deploys to Cloudflare
└─ Article live at rinji.id

RESULT: Published article, live URL, ready to share
```

---

## What You Need to Do

### 1. Do Your Research
- **Tools**: Any tool (ChatGPT, Claude.ai, Gemini, browser research, whatever)
- **Format**: No specific format needed
- **Depth**: 4-6 hours is fine (more is better)
- **Content**: Key findings, data, examples, sources, synthesis

### 2. Save Your Research
- **PDF**: Most common, easiest
  - Copy text + paste into PDF
  - Or print webpage to PDF

- **DOCX**: Microsoft Word
  - Type or paste findings
  - Organize into sections

- **MD**: Markdown
  - Create markdown file with sections
  - Use simple formatting

### 3. Submit to Claude Code
- Attach research file
- Fill out intake form (2 minutes)
- Describe article details
- Send

### 4. Wait 1 Hour
- Claude Code processes research
- Writes article
- Publishes automatically
- Sends you live URL

---

## Submission Template (Copy & Fill)

```
FILE: [your-research-file.pdf/docx/md]

ARTICLE DETAILS:
- Title: [Article Title]
- Section: [insights / resources / pemikiran]
- Target audience: [Who reads this]
- Target length: [2000-3000 words, or flexible]

KEY INSTRUCTIONS:
[Any specific guidance]

RESEARCH CONTAINS:
[Brief description of findings]
```

**Example:**
```
FILE: benchmark-pdam-research.pdf

ARTICLE DETAILS:
- Title: Benchmark Kinerja PDAM Indonesia
- Section: insights
- Target audience: PDAM leaders and regulators
- Target length: 2500-3000 words

KEY INSTRUCTIONS:
- Focus on practical implications for PDAM managers
- Include financial ROI calculations
- Highlight best practices from top performers

RESEARCH CONTAINS:
- NRW statistics 2015-2025 (government & PERPAMSI)
- Case studies from 4 PDAM different tiers
- Cost recovery analysis with examples
- Service quality benchmarks
```

---

## What I (Claude Code) Do

### 1. Read Your Research File
- Accept PDF, DOCX, or MD format
- Extract key findings, data, examples
- Identify sources & citations

### 2. Understand Context
- Article title & purpose
- Target audience (affects tone & complexity)
- Special instructions/emphasis

### 3. Write Article
- Professional 2500-3500 word article
- Clear organization (4-5 sections)
- Citations integrated throughout
- Complete reference list
- Polished, publication-ready

### 4. Publish Automatically
- Create markdown file: `content/[section]/[article-slug].md`
- Add frontmatter (title, description, date)
- Commit to git: `git add` + `git commit`
- Build Hugo: `hugo --minify`
- Deploy: `wrangler pages deploy`
- Send you live URL

### 5. Send Confirmation
- Live URL: https://rinji.id/...
- Git commit hash (for reference)
- Ready for sharing

---

## Turnaround Time

| Task | Time |
|------|------|
| Read research file | 15 min |
| Extract findings | 15 min |
| Write article | 30-45 min |
| Add citations | 10 min |
| Commit & deploy | 10 min |
| **Total** | **45-75 min** |

**Fastest:** Simple, well-organized research → 45 min
**Slower:** Complex research, many sources → 75 min

---

## What Makes Good Research Input

✅ **Good:**
- Substantive findings (from multiple sources)
- Key data & statistics with sources mentioned
- Concrete examples & case studies
- Original synthesis (not just summaries)
- Clear sections/organization

❌ **Not Good:**
- Unstructured text dump
- No sources mentioned
- Only summaries
- Single source
- Vague claims without backing

---

## Files You Need to Know About

### For Submitting Research
1. **ARTICLE_SUBMISSION_GUIDE.md** — Read this first
   - How to submit research file
   - What happens at each stage
   - Examples & best practices

2. **ARTICLE_INTAKE_FORM.md** — Use this to submit
   - Copy & fill out template
   - Example completed form
   - Structured intake process

### Legacy (For Reference)
3. **RESEARCH_WORKFLOW.md** — Complex version (not needed now)
4. **README_RESEARCH_WORKFLOW.md** — Old comprehensive guide (not needed)
5. **research/template.md** — Old template (not needed)

---

## Examples: Research to Article

### Example 1: PDF Research
```
INPUT:
- File: benchmark-pdam-research.pdf
- Content: NRW stats, PERPAMSI data, case studies, analysis

PROCESS:
1. Claude Code reads PDF (15 min)
2. Extracts findings & sources (10 min)
3. Writes article (35 min)
4. Publishes (10 min)

OUTPUT:
Article live: https://rinji.id/insights/benchmark-kinerja-pdam/
Confirmation sent within 1.5 hours
```

### Example 2: ChatGPT Research Output
```
INPUT:
- File: tren-industri-research.docx (exported from ChatGPT)
- Content: Structured findings from ChatGPT research

PROCESS:
1. Claude Code reads DOCX (15 min)
2. Organizes findings (15 min)
3. Writes enhanced article (40 min)
4. Publishes (10 min)

OUTPUT:
Professional article using ChatGPT research as foundation
Same quality as if you did manual research
```

### Example 3: Multiple Source Files
```
INPUT:
- Files:
  - research-part1.pdf
  - research-part2.docx
  - research-part3.md
- Content: Findings from different research sessions

PROCESS:
1. Claude Code reads all 3 files (20 min)
2. Integrates findings (20 min)
3. Writes coherent article (35 min)
4. Publishes (10 min)

OUTPUT:
Single integrated article combining all research
Coherent flow despite multiple source files
```

---

## Frequently Asked Questions

**Q: Can I use research from ChatGPT/Claude.ai?**
A: Absolutely. That's the point. Use whatever tool works.

**Q: Do I need to organize research in specific way?**
A: No. Rough notes are fine. I'll organize & enhance.

**Q: What if research file is messy/unstructured?**
A: Still works. Structured is better, but I can handle unstructured.

**Q: How long until article is live?**
A: 45-75 minutes from file submission.

**Q: Can I request changes after publication?**
A: Yes. Tell me what to change. I'll update & redeploy (30 min).

**Q: What if I want to review before publishing?**
A: Check "review first" on intake form. I'll send draft URL for your approval.

**Q: Can I submit multiple articles at once?**
A: Yes. I'll process them sequentially. Each takes 1-1.5 hours.

**Q: Will citations be included?**
A: Yes. I'll add citations throughout article. Reference list at end.

**Q: Can I track what was published?**
A: Yes. I send you live URL + git commit info + deployment details.

---

## Getting Started: Your First Article

### Today
1. Read: **ARTICLE_SUBMISSION_GUIDE.md** (10 min)
2. Review: **ARTICLE_INTAKE_FORM.md** (5 min)

### This Week
1. Do deep research on your chosen topic (2-6 hours)
   - Use ChatGPT, Claude.ai, Gemini, whatever works
   - Gather findings, data, examples
   - Save sources for citations

2. Save research to file (5 min)
   - PDF, DOCX, or MD format
   - Descriptive filename

3. Submit to Claude Code (2 min)
   - Copy intake form
   - Fill it out
   - Attach research file
   - Send message

### Within 1 Hour
- Article written & published
- Live URL received
- Ready to share

---

## Success Indicator: Good Submission

✅ **Before Submitting:**
- [ ] Research is substantive (multiple sources)
- [ ] Key data & examples included
- [ ] Sources are mentioned (even if not perfectly formatted)
- [ ] Original analysis/synthesis included
- [ ] File is clear & readable (doesn't need to be perfect)

✅ **After Publishing:**
- [ ] 2500-3500 word professional article
- [ ] Clear organization (4-5 sections)
- [ ] Proper citations throughout
- [ ] Complete reference list
- [ ] Serves target audience well
- [ ] Ready for sharing/promotion

---

## Next Steps: Now What?

### Option 1: Start Right Now
1. Pick article topic
2. Do research (however you want)
3. Save to file
4. Submit using intake form
5. Published in ~1 hour

### Option 2: Understand First
1. Read ARTICLE_SUBMISSION_GUIDE.md completely
2. Review example submission
3. Clarify any questions
4. Then start

### Option 3: Test It Out
1. Try with simpler article first
2. See process in action
3. Then tackle bigger research project

---

## The Bottom Line

**Old way:** Research using template → compile notes → submit → wait → get article

**New way:** Research however → save file → submit → article published in 1 hour

Same quality output. Much simpler process.

---

**Ready to submit your first research file? Use ARTICLE_SUBMISSION_GUIDE.md + ARTICLE_INTAKE_FORM.md!** 🚀

---

Last updated: December 20, 2025
