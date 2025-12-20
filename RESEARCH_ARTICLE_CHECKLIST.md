# Research Article Writing Checklist

Use this checklist untuk track progress on each article dari research → publication.

---

## Article: [ARTICLE TITLE]

**Status:** Planned / In Progress / Draft / Published

**Start Date:** _______ | **Target Date:** _______

---

## PHASE 1: PREPARATION (Est. 0.5-1 hour)

### Scope Definition
- [ ] Article title finalized
- [ ] 1-2 sentence scope written
- [ ] Target audience clearly defined
- [ ] 4-5 key research questions identified
- [ ] Evidence types needed specified
- [ ] Source strategy outlined

### Research Setup
- [ ] Research folder created: `research/[section]/[article-title]-notes.md`
- [ ] Template copied & customized
- [ ] Frontmatter filled in (title, scope, questions, evidence)
- [ ] Source search strategy documented

### Sign-off
- [ ] Scope clarity: ___/10 (1=confusing, 10=crystal clear)
- [ ] Ready for research: ☐ YES ☐ NO

---

## PHASE 2: DEEP RESEARCH (Est. 4-6 hours)

### Research Execution
- [ ] 5-10+ sources identified & accessed
- [ ] Sources diverse:
  - [ ] Government sources: _______ (count)
  - [ ] Academic sources: _______ (count)
  - [ ] Industry sources: _______ (count)
  - [ ] Case studies: _______ (count)
- [ ] Findings extracted to template (per-source)
- [ ] Statistics verified & sourced

### Synthesis
- [ ] Common themes identified (3+ themes)
- [ ] Contradictions/nuance discussed
- [ ] Original insights articulated (not just summaries)
- [ ] Gaps & limitations acknowledged
- [ ] Proposed article structure created (4-5 sections)

### Reference List
- [ ] All sources cited consistently
- [ ] Complete reference list compiled
- [ ] Format: [Author (Year) format, minimum]

### Quality Check
- [ ] All key research questions answered? ☐ YES ☐ NO
- [ ] Sources diverse & credible? ☐ YES ☐ NO
- [ ] Synthesis includes original analysis? ☐ YES ☐ NO
- [ ] Gaps acknowledged? ☐ YES ☐ NO
- [ ] Reference list complete? ☐ YES ☐ NO
- [ ] Research notes well-organized? ☐ YES ☐ NO

### Sign-off
- [ ] Research quality: ___/10 (1=shallow, 10=thorough)
- [ ] Ready for writing: ☐ YES ☐ NO
- [ ] Research completion date: _______

---

## PHASE 3: CLAUDE CODE INTEGRATION (Est. 1-2 hours)

### Outline & Structure
- [ ] Research file submitted to Claude Code
- [ ] Outline requested & received
- [ ] Outline reviewed
- [ ] Structure approved: ☐ YES ☐ NEEDS CHANGES
- [ ] (If changes needed) Claude Code revision requested & reviewed

### Section-by-Section Writing
- [ ] Section 1 written & reviewed
  - [ ] Accurate & well-sourced? ☐ YES ☐ NO
  - [ ] Clear & well-written? ☐ YES ☐ NO
  - [ ] Approved: ☐ YES ☐ NEEDS REVISION
- [ ] Section 2 written & reviewed
  - [ ] Accurate? ☐ YES ☐ NO
  - [ ] Clear? ☐ YES ☐ NO
  - [ ] Approved: ☐ YES ☐ NEEDS REVISION
- [ ] Section 3 written & reviewed
  - [ ] Accurate? ☐ YES ☐ NO
  - [ ] Clear? ☐ YES ☐ NO
  - [ ] Approved: ☐ YES ☐ NEEDS REVISION
- [ ] Section 4 written & reviewed (if applicable)
  - [ ] Accurate? ☐ YES ☐ NO
  - [ ] Clear? ☐ YES ☐ NO
  - [ ] Approved: ☐ YES ☐ NEEDS REVISION
- [ ] Introduction written & reviewed
  - [ ] Sets context? ☐ YES ☐ NO
  - [ ] Hooks reader? ☐ YES ☐ NO
  - [ ] Approved: ☐ YES ☐ NEEDS REVISION
- [ ] Conclusion written & reviewed
  - [ ] Summarizes key points? ☐ YES ☐ NO
  - [ ] Provides implications? ☐ YES ☐ NO
  - [ ] Approved: ☐ YES ☐ NEEDS REVISION

### Draft Compilation
- [ ] All sections compiled into single document
- [ ] Frontmatter added (title, description, date)
- [ ] Citations checked for format consistency
- [ ] Reference list formatted properly
- [ ] Draft saved as: `content/insights/[article-title]-draft.md`

### Sign-off
- [ ] Draft quality: ___/10 (1=rough, 10=near-final)
- [ ] Ready for editing: ☐ YES ☐ NO
- [ ] Draft completion date: _______

---

## PHASE 4: REFINEMENT & PUBLICATION (Est. 1-2 hours)

### Quality Verification
- [ ] Facts & statistics accurate? ☐ YES ☐ NO
- [ ] Clear for target audience? ☐ YES ☐ NO
- [ ] Logical flow between sections? ☐ YES ☐ NO
- [ ] All key questions answered? ☐ YES ☐ NO
- [ ] Citations complete & proper? ☐ YES ☐ NO
- [ ] Reference list complete? ☐ YES ☐ NO
- [ ] Word count appropriate? (Target: 2000-3500) _____ words

### Editing & Polish
- [ ] Typos fixed? ☐ YES ☐ N/A
- [ ] Grammar checked? ☐ YES ☐ N/A
- [ ] Clarity improved (dense sentences rewritten)? ☐ YES ☐ N/A
- [ ] Citations format consistent? ☐ YES ☐ N/A
- [ ] Tone consistent throughout? ☐ YES ☐ N/A

### Final File Preparation
- [ ] File path: `content/insights/[article-title].md`
- [ ] Frontmatter complete:
  - [ ] Title: [Title]
  - [ ] Description: [1-2 sentence summary]
  - [ ] Date: [YYYY-MM-DD]
- [ ] No draft artifacts left in content

### Build & Deployment
- [ ] Local build successful: `hugo --minify`
  - [ ] Build time: _____ ms
  - [ ] Pages generated: _____ (should include new article)
- [ ] Local preview tested: `hugo server`
  - [ ] Article loads? ☐ YES ☐ NO
  - [ ] Links work? ☐ YES ☐ NO
  - [ ] Formatting correct? ☐ YES ☐ NO
- [ ] Deploy to Cloudflare: `wrangler pages deploy public/ --project-name rinji-id`
  - [ ] Deployment successful? ☐ YES ☐ NO
  - [ ] Live URL: https://rinji.id/[article-path]/

### Post-Publish
- [ ] Article live & accessible? ☐ YES ☐ NO
- [ ] Links from menu working? ☐ YES ☐ NO
- [ ] Archive research notes: `research/insights/[article-title]-notes.md`
  - [ ] Saved for future updates? ☐ YES ☐ NO

### Sign-off
- [ ] Final quality: ___/10 (1=poor, 10=excellent)
- [ ] Publication date: _______
- [ ] Promotion plan (if applicable): _________________

---

## COMPLETION SUMMARY

**Article:** [Title]

**Research effort:** _____ hours | **Writing effort:** _____ hours | **Total effort:** _____ hours

**Publication date:** _______

**Feedback/Lessons learned:**
```
[Notes for next article iteration]
```

**Next article priority:** _________________

---

## TRACKING TEMPLATE (Copy for each article)

```markdown
## Article: [TITLE]
- **Scope:** [1-2 line description]
- **Status:** Planned → Research → Draft → Published
- **Effort:** Research _h | Writing _h | Total _h
- **Pub Date:** _______
```

---

## Overall Progress

### Insights Articles (Phase 1)
- [ ] Benchmark Kinerja PDAM
  - Status: ☐ Planned ☐ Research ☐ Draft ☐ Published
  - Date: _______
- [ ] Tren Industri Air Indonesia
  - Status: ☐ Planned ☐ Research ☐ Draft ☐ Published
  - Date: _______
- [ ] Landscape Regulasi Industri Air
  - Status: ☐ Planned ☐ Research ☐ Draft ☐ Published
  - Date: _______

### Resources Articles (Phase 2)
- [ ] GRC Framework (Expanded)
  - Status: ☐ Planned ☐ Research ☐ Draft ☐ Published
  - Date: _______
- [ ] NRW Reduction Checklist (Expanded)
  - Status: ☐ Planned ☐ Research ☐ Draft ☐ Published
  - Date: _______

### Pemikiran Articles (Phase 3)
- [ ] Masa Depan Air Indonesia (Expanded)
  - Status: ☐ Planned ☐ Research ☐ Draft ☐ Published
  - Date: _______
- [ ] Kepemimpinan Transformasi (Expanded)
  - Status: ☐ Planned ☐ Research ☐ Draft ☐ Published
  - Date: _______

### Summary
- **Total articles planned:** 7 (3 Insights + 2 Resources + 2 Pemikiran)
- **Articles published:** _____ / 7
- **Articles in progress:** _____ / 7
- **Articles remaining:** _____ / 7
- **Overall completion:** _____ %

---

**Notes:**
- Print this checklist for each article
- Update status weekly
- Save completed checklists for documentation
- Review lessons learned to improve next article

---

Last updated: December 20, 2025
