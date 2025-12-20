# Migration Execution: fdiskandar.com Setup

**Timeline:** Complete dalam 2-3 hari (mostly DNS propagation)
**Your Action Items:** Clear & specific steps below

---

## STEP 1: Add fdiskandar.com to Cloudflare (5 minutes)

### What to do:
1. Go to: https://dash.cloudflare.com/
2. Click "Add site" (top right)
3. Enter: `fdiskandar.com`
4. Select: **Free plan** (same as rinji.id)
5. Click "Continue"

### What Cloudflare will show:
- A list of **Cloudflare nameservers** (usually 2-4 nameservers)
- They look like: `ns1.cloudflare.com`, `ns2.cloudflare.com`, etc.
- **COPY these nameservers** (you'll need them next)

### Example of what you'll see:
```
Cloudflare Nameservers:
├─ ns1.cloudflare.com
├─ ns2.cloudflare.com
├─ ns3.cloudflare.com
└─ ns4.cloudflare.com
```

**After this step:** Come back & tell me the nameservers Cloudflare gave you.

---

## STEP 2: Update Nameservers at Cloudflare Domain Registrar (5 minutes)

### Why:
Domain kamu terdaftar di Cloudflare. Sekarang kita need update nameservers dari "Cloudflare Domain Registrar" ke "Cloudflare DNS Management".

### What to do:
1. Still at https://dash.cloudflare.com/
2. Go to: **Websites** → **fdiskandar.com**
3. Left sidebar → **Domain Settings** → **Nameservers**
4. You'll see: "Use Cloudflare nameservers" button
5. Click it

### What happens:
- Cloudflare automatically switches your domain to use Cloudflare nameservers
- **This is instant** (no waiting)
- Your domain now managed by Cloudflare DNS

**Status check:** Once done, you should see:
```
✓ Domain registered
✓ Using Cloudflare nameservers
✓ DNS management: Cloudflare
```

---

## STEP 3: Setup Cloudflare Pages for fdiskandar.com (10 minutes)

### What to do:
1. In Cloudflare dashboard, go to: **Pages** (left sidebar)
2. Click **Create project**
3. Select: **GitHub** (or **Upload custom domain** if you prefer manual)
4. If GitHub:
   - Connect to `ferli/rinji-id` repository
   - Select `main` branch
   - Click **Next**

5. Configure build:
   - **Framework:** Hugo
   - **Build command:** `hugo --minify`
   - **Build output directory:** `public`
   - **Environment variables:**
     ```
     HUGO_VERSION = 0.152.2
     ```
   - Click **Save and deploy**

6. After build completes (1-2 min):
   - Cloudflare give you URL like: `https://[random-hash].pages.dev`
   - **This is temporary test URL**

7. Add custom domain:
   - Click **Custom domain**
   - Enter: `fdiskandar.com`
   - Cloudflare automatically add DNS records
   - Click **Activate domain**

**Status check:** You should see:
```
✓ Pages project created
✓ GitHub connected
✓ Build successful
✓ Custom domain: fdiskandar.com
```

---

## STEP 4: Update Hugo Config (Claude Code will do this)

**I (Claude Code) will:**
1. Update `hugo.toml`:
   ```toml
   baseURL = "https://fdiskandar.com/"  # Changed from rinji.id
   # Everything else stays same
   ```

2. Check if any content mentions rinji-id specifically
3. Commit changes to git
4. Trigger automatic Cloudflare Pages rebuild

**You don't need to do anything** — just approve when I ask.

---

## STEP 5: Verify fdiskandar.com is Live (30 seconds)

### Wait for:
- DNS propagation (usually 15 minutes, max 48 hours)
- Typical: propagated within 5-30 minutes

### Check it works:
1. Open: `https://fdiskandar.com/`
2. Should see: Your homepage
3. Click around: Check all pages load

### If it doesn't work yet:
- Wait a bit longer (DNS propagation)
- Or check: Did Cloudflare Pages build succeed? (check build logs)

---

## STEP 6: Setup 301 Redirect from rinji.id (Claude Code will do)

**I (Claude Code) will:**
1. Create `_redirects` file in `static/` folder
2. Add rules: All rinji.id traffic → fdiskandar.com
3. Deploy to rinji.id project

**Result:** Anyone visiting rinji.id automatically redirected to fdiskandar.com (with 301 permanent redirect for SEO)

---

## STEP 7: Final Verification (5 minutes)

### Test fdiskandar.com:
- [ ] Homepage loads: https://fdiskandar.com/
- [ ] About page: https://fdiskandar.com/about/
- [ ] Expertise: https://fdiskandar.com/expertise/
- [ ] Contact: https://fdiskandar.com/contact/
- [ ] Insights: https://fdiskandar.com/insights/
- [ ] Resources: https://fdiskandar.com/resources/
- [ ] All internal links work

### Test rinji.id redirect:
- [ ] Visit https://rinji.id/
- [ ] Redirects to: https://fdiskandar.com/
- [ ] URL bar shows: fdiskandar.com

### Test social/meta:
- [ ] LinkedIn works: https://linkedin.com/in/ferli
- [ ] Email link works: ferli.deni.iskandar@gmail.com

---

## Timeline

```
RIGHT NOW:
├─ STEP 1: Add fdiskandar.com to Cloudflare (5 min)
├─ STEP 2: Update nameservers (5 min)
└─ STEP 3: Setup Cloudflare Pages (10 min)
└─ TOTAL YOUR WORK: ~20 minutes

THEN I DO:
├─ STEP 4: Update Hugo config & deploy (~5 min)
├─ STEP 6: Setup redirects (~5 min)
└─ AUTOMATIC: Cloudflare build & deploy (~2 min)

THEN WAIT:
└─ DNS propagation (~5-30 min, max 48 hours)

THEN TEST:
└─ STEP 5 & 7: Verify everything works (~5 min)

TOTAL TIME: 30-40 minutes active work
TOTAL CALENDAR: 2-3 hours (mostly waiting for DNS)
```

---

## Checklist: Before You Start

- [ ] You can login to Cloudflare account
- [ ] fdiskandar.com registered & accessible in Cloudflare
- [ ] You have a browser open (to do the steps)
- [ ] Ready to copy-paste URLs
- [ ] Ready to take screenshot of nameservers (for reference)

---

## What to Tell Me After Each Step

**After STEP 1 (Nameservers):**
```
Cloudflare gave me these nameservers:
- ns1.cloudflare.com
- ns2.cloudflare.com
- ns3.cloudflare.com
- ns4.cloudflare.com

[Or whatever they gave you]
```

**After STEP 2 (Update nameservers):**
```
Done. Cloudflare says domain is now using Cloudflare nameservers.
```

**After STEP 3 (Pages setup):**
```
Pages project created. Build succeeded.
Custom domain: fdiskandar.com activated.
```

**After STEP 5 (DNS propagates):**
```
DNS propagated. fdiskandar.com is live!
All pages load correctly.
```

---

## If Something Goes Wrong

**"Build failed in Cloudflare Pages"**
→ Check build logs in Cloudflare dashboard
→ Usually: Hugo version mismatch or config syntax error
→ I'll fix it

**"fdiskandar.com shows Cloudflare error page"**
→ DNS not yet propagated
→ Wait 5-30 more minutes
→ Or check: Is Pages project pointing to domain correctly?

**"rinji.id doesn't redirect to fdiskandar.com"**
→ Pages project for rinji.id not updated yet
→ I need to deploy _redirects file
→ I'll handle this

**"Some pages on fdiskandar.com don't load"**
→ Likely: DNS issue or Pages build issue
→ Check: What's the error message?
→ I'll debug

---

## Questions?

Before you start the 3 steps, any questions?

If unclear on any step above, ask now!

Otherwise, start with STEP 1 and tell me when done.

---

**Ready to proceed? Start STEP 1!** 🚀

Last updated: December 20, 2025
