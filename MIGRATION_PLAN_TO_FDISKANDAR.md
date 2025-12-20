# Migration Plan: rinji-id → fdiskandar.com

Strategic migration dari rinji.id ke fdiskandar.com sebagai primary hub.

---

## Executive Summary

**Objective:** Migrate semua konten dari rinji.id ke fdiskandar.com
**Timeline:** 1-2 hari untuk complete setup
**Approach:** Copy content exactly as-is, new domain infrastructure
**Strategy:** fdiskandar.com = primary personal brand hub

**Future:** rinji.id untuk konsep berbeda (tbd)

---

## Phase 1: DNS & Domain Setup (30 minutes)

### 1.1 DNS Configuration for fdiskandar.com

**What We Need to Know:**
- Dimana kamu register fdiskandar.com? (Namecheap, GoDaddy, Cloudflare, etc.)
- Apakah sudah punya Cloudflare account?
- Apakah mau pakai Cloudflare untuk DNS management?

**Recommended Setup (Same as rinji.id):**
1. Use Cloudflare for DNS management
2. Point fdiskandar.com ke Cloudflare Pages (free tier)
3. Same deployment infrastructure as rinji.id

**Steps to Setup:**
```
1. Add fdiskandar.com ke Cloudflare
   - Login cloudflare.com
   - Add domain button
   - Select free plan
   - Cloudflare give name servers

2. Update DNS at registrar
   - Go to domain registrar
   - Change name servers to Cloudflare's
   - Wait 24-48 hours untuk DNS propagate

3. Create Cloudflare Pages project
   - New Pages project
   - Connect to GitHub (rinji-id repo)
   - Configure build settings (same as rinji.id)
   - Point to custom domain: fdiskandar.com

4. Update git config
   - Change deployment config untuk fdiskandar.com
   - Keep rinji.id config as backup
```

### 1.2 GitHub Repository Decision

**Option A: Single Repo (Recommended)**
- Keep rinji-id repository as-is
- Configure Cloudflare Pages untuk:
  - **Deploy preview** to rinji.id (for testing)
  - **Production** to fdiskandar.com (live)
- Same git history, dual deployment

**Option B: New Repo**
- Create new repo: ferli/fdiskandar.com
- Copy all content dari rinji-id repo
- Independent git history
- More clean but lose git history

**Recommendation:** Go with Option A (single repo, dual deployment)

---

## Phase 2: Content Migration (1 hour)

### 2.1 Audit Current Content

Current struktur rinji-id:
```
content/
├── _index.md (homepage)
├── about.md
├── contact.md
├── expertise/
│   ├── _index.md
│   ├── digital-transformation.md
│   ├── grc.md
│   ├── nrw.md
│   └── cybersecurity.md
├── insights/
│   ├── _index.md
│   ├── benchmark-pdam.md
│   ├── tren-industri.md
│   └── regulasi-landscape.md
├── resources/
│   ├── _index.md
│   ├── grc-framework.md
│   └── checklist-nrw.md
└── pemikiran/
    ├── _index.md
    ├── masa-depan-air.md
    └── kepemimpinan-transformasi.md

public/ (build output)
static/ (images, assets)
themes/PaperMod/
```

### 2.2 Copy Content As-Is

**Action:** All content copied exactly. No changes.

```
rinji-id/content/ → fdiskandar.com/content/
(Same structure, same files, same content)
```

**Why As-Is?**
- Content adalah substantive & good
- No time wasted on rewrites
- Immediate launch on new domain
- Can refine later

### 2.3 Required Metadata Changes

Files yang perlu update (frontmatter/config only):

#### hugo.toml
```toml
# CHANGE:
baseURL = "https://rinji.id/"
# TO:
baseURL = "https://fdiskandar.com/"

# Everything else stays the same
```

#### content/_index.md (if mentions rinji-id)
```markdown
# BEFORE:
"Saya adalah FD Iskandar, founder of rinji.id..."

# AFTER:
"Saya adalah FD Iskandar"
(Remove rinji.id reference, or mention as:)
"Founder of Rinji.id (sister platform)"

# Keep everything else same
```

#### content/contact.md (if mentions rinji.id)
```markdown
# Update email if needed
# OR keep as-is if email is personal
```

---

## Phase 3: Hugo Build & Deployment Setup (1 hour)

### 3.1 Update Hugo Configuration

**File: hugo.toml**
```toml
# BEFORE:
baseURL = "https://rinji.id/"
languageCode = "id"
title = "FD Iskandar | Teknolog Strategis"
theme = "PaperMod"

# AFTER:
baseURL = "https://fdiskandar.com/"
languageCode = "id"
title = "FD Iskandar | Strategic Technologist for Water Utilities"
theme = "PaperMod"

# [params] section - mostly same, check:
description = "..." (update to mention fdiskandar.com)
author = "FD Iskandar"
keywords = [...]
```

### 3.2 Setup Cloudflare Pages for fdiskandar.com

**In Cloudflare Dashboard:**
1. Go to Pages → Create project
2. Connect to GitHub (rinji-id repository)
3. Build configuration:
   - Framework: Hugo
   - Build command: `hugo --minify`
   - Build output directory: `public`
   - Environment variable: `HUGO_VERSION = 0.152.2`
4. Custom domain: `fdiskandar.com`
5. Enable automatic deployments on push

**Result:** Every git push → automatic build + deploy to fdiskandar.com

### 3.3 Wrangler Configuration

**Option A: Update existing wrangler.toml**
```toml
name = "fdiskandar"
type = "javascript"
compatibility_date = "2024-01-01"

[env.production]
name = "fdiskandar-prod"
routes = [
  { pattern = "fdiskandar.com", zone_id = "[cloudflare_zone_id]" }
]
```

**Option B: Create separate deployment**
Keep wrangler config flexible untuk both domains during transition

---

## Phase 4: DNS Migration & Testing (30 minutes)

### 4.1 DNS Setup Timeline

```
T+0:   Register fdiskandar.com
T+0.5: Add to Cloudflare, get nameservers
T+1:   Update nameservers at registrar
T+24:  DNS propagates (fully)
T+24:  Test fdiskandar.com (should work)
T+48:  Fully propagated, ready for full traffic
```

### 4.2 Pre-Launch Testing

**Before DNS points to Cloudflare:**
1. Test locally: `hugo server`
   - Check all pages load
   - Check all links work
   - Check menus display correctly

2. Test build: `hugo --minify`
   - Check public/ folder generated
   - Check no build errors
   - Inspect key pages

3. Test deployment
   ```bash
   # Via Cloudflare Pages manual deployment (temporary)
   wrangler pages deploy public/ --project-name fdiskandar
   ```

### 4.3 Post-Launch Verification

Once DNS points to fdiskandar.com:
```
1. Visit https://fdiskandar.com/
2. Verify homepage loads
3. Check all main pages:
   - /about/
   - /expertise/
   - /contact/
   - /insights/
   - /resources/
   - /pemikiran/
4. Check mobile responsiveness
5. Verify all links work (internal + external)
6. Check social icons (LinkedIn, email)
7. Run Lighthouse audit (for SEO)
```

---

## Phase 5: rinji.id Redirect Setup (30 minutes)

### 5.1 301 Redirect (Permanent)

After fdiskandar.com is live and stable, setup permanent redirect:

**In Cloudflare Pages for rinji.id:**
1. Create `_redirects` file in static/ folder:
```
# static/_redirects
/* https://fdiskandar.com/:splat 301
```

**What This Does:**
- All traffic to rinji.id → redirected to fdiskandar.com
- Preserves page paths (rinji.id/about/ → fdiskandar.com/about/)
- 301 = permanent redirect (Google respects for SEO)
- Maintains authority/rankings from rinji.id

### 5.2 Alternative: Cloudflare Rules

If using Cloudflare Rules instead of _redirects:
```
URL Rewrite Rule:
Incoming URL: rinji.id/*
Rewrite to: https://fdiskandar.com/:splat
```

---

## Phase 6: Post-Migration Considerations (Ongoing)

### 6.1 Analytics & Tracking

**Setup for fdiskandar.com:**
- Google Search Console (register domain)
- Google Analytics 4 (track visitors)
- Cloudflare Analytics (built-in)

**Migrate from rinji.id:**
- Export existing analytics data
- Compare traffic pre/post migration
- Monitor 301 redirects working

### 6.2 Email & Communication

**Update in new site:**
- Meta tags (og:image, etc.) point to fdiskandar.com
- Email footer links point to new domain
- Social media profiles mention fdiskandar.com
- LinkedIn update

**Email forwarding:**
- If contact@rinji.id used, setup forwarding to personal email
- Or update to contact@fdiskandar.com (if you own that)

### 6.3 Link Updates

**Places to update link references:**
- LinkedIn profile → link to fdiskandar.com
- Email signature → link to fdiskandar.com
- Business cards → fdiskandar.com
- Twitter/social profiles → fdiskandar.com
- Any external mentions/backlinks → will auto-redirect via 301

### 6.4 Git History & Comments

**Future consideration:**
- Rename repository to fdiskandar-com (optional)
- Update README in repo to mention fdiskandar.com
- Add comments explaining dual deployment

---

## Detailed Step-by-Step Execution

### Step 1: DNS Setup (Start here)

**What we need from you:**
1. Where did you buy fdiskandar.com? (Registrar name)
2. Do you have Cloudflare account already?
3. Access to domain registrar (to update nameservers)

**What I'll do:**
1. Guide you through adding domain to Cloudflare
2. Get nameservers from Cloudflare
3. Tell you exactly what to change at registrar

**Time:** 10-15 minutes

### Step 2: Hugo Configuration Update

**What I'll do:**
1. Update hugo.toml: baseURL → fdiskandar.com
2. Review content for any rinji-id specific mentions
3. Update title/description if needed
4. Commit changes

**Time:** 10-15 minutes

### Step 3: Cloudflare Pages Setup

**What I'll do:**
1. Create Cloudflare Pages project for fdiskandar.com
2. Connect GitHub repo
3. Configure build settings
4. Test deployment

**What you do:**
1. Approve Cloudflare access to GitHub (if first time)
2. Verify build completes successfully

**Time:** 15-20 minutes

### Step 4: Testing & Verification

**What I'll do:**
1. Test locally: `hugo server`
2. Build production: `hugo --minify`
3. Verify no errors in build output

**What you do:**
1. Once DNS propagates (24-48 hours), test website
2. Verify all pages load correctly
3. Check links, menus, responsiveness

**Time:** 15-20 minutes

### Step 5: 301 Redirect Setup

**What I'll do:**
1. Create _redirects file
2. Setup permanent redirect: rinji-id → fdiskandar.com
3. Deploy to rinji.id

**Time:** 5-10 minutes

---

## Timeline Summary

| Phase | Task | Time | When |
|-------|------|------|------|
| 1 | DNS setup | 15 min | Today |
| 1 | Nameserver update | 5 min | Today (at registrar) |
| 2 | Hugo config update | 15 min | Today |
| 3 | Cloudflare Pages setup | 20 min | Today |
| 4 | Testing & verification | 20 min | Today |
| - | DNS propagation | 24-48 hrs | Automatic |
| 5 | Post-DNS testing | 15 min | Day 2-3 |
| 5 | Redirect setup | 10 min | Day 2-3 |
| 6 | Analytics & final setup | 30 min | Day 3+ |

**Total active work: ~2 hours**
**Total calendar time: 2-3 days (mostly waiting for DNS propagation)**

---

## Rollback Plan

If something goes wrong:

### Option A: Quick Rollback (keep rinji.id live)
1. Revert hugo.toml changes
2. Redeploy to rinji.id
3. Debug fdiskandar.com separately

### Option B: Parallel Running
1. Keep rinji.id live while setting up fdiskandar.com
2. Test fdiskandar.com thoroughly
3. Switch traffic once confident

**We'll use Option B for safety** — no downtime risk

---

## Questions Before We Start

1. **Where is fdiskandar.com registered?** (Namecheap, GoDaddy, Cloudflare, etc.)
2. **Do you have Cloudflare account?** (Yes/No)
3. **Can you access domain registrar to change nameservers?**
4. **Timeline preference:** Quick (2-3 days) or slow (1-2 weeks of testing)?

---

## Next Steps

1. Answer the 4 questions above
2. I'll give you exact DNS nameservers to use
3. You update nameservers at registrar
4. While waiting for DNS, I'll update Hugo config & deploy
5. Once DNS propagates, we test and verify
6. Then setup redirects

**Ready to start?** Answer the 4 questions above! 🚀

---

Last updated: December 20, 2025
