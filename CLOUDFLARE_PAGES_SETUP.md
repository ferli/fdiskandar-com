# Setup Cloudflare Pages untuk fdiskandar.com

**Status:** Domain di Cloudflare ✓
**Next:** Create Pages project & connect GitHub

---

## STEP 1: Go to Cloudflare Pages

1. In Cloudflare dashboard, left sidebar → **Pages**
2. Click **Create a project**
3. Choose: **Connect to Git** (if you haven't authorized yet, authorize GitHub first)

---

## STEP 2: Select Repository

1. You'll see GitHub authorization prompt
   - Click **Authorize Cloudflare**
   - Select: `ferli/rinji-id` repository
   - Click **Begin setup**

2. Select branch: **main** (or master if that's your default)

3. Click **Next configuration**

---

## STEP 3: Configure Build Settings

Enter these exact values:

```
Framework preset: Hugo

Build command: hugo --minify

Build output directory: public

Environment variables:
  HUGO_VERSION = 0.152.2
```

**Example screenshot of what to enter:**
```
┌─────────────────────────────────────┐
│ Build Configuration                 │
├─────────────────────────────────────┤
│ Framework preset: [Hugo ▼]          │
│ Build command: [hugo --minify    ] │
│ Build output dir: [public        ] │
│                                     │
│ Environment variables:              │
│ ┌─────────────────────────────────┐ │
│ │ HUGO_VERSION = 0.152.2          │ │
│ └─────────────────────────────────┘ │
└─────────────────────────────────────┘
```

Click **Save and Deploy**

---

## STEP 4: Wait for Build

Cloudflare akan:
1. Clone repository dari GitHub
2. Run `hugo --minify` command
3. Upload `public/` folder ke Pages
4. Give you URL like: `https://[random-hash].pages.dev`

**Build usually takes:** 1-2 minutes

You'll see progress: "Building... → Deploying... → Success ✓"

---

## STEP 5: After Build Succeeds

Kamu akan lihat:
- **Project name:** fdiskandar (or whatever GitHub suggests)
- **Pages URL:** `https://[hash].pages.dev`
- **Status:** ✓ Deployment successful

**Important:** This is temporary test URL. We'll add custom domain next.

---

## STEP 6: Add Custom Domain

1. Still in Pages project settings
2. Click: **Custom domain**
3. Enter: `fdiskandar.com` (root domain, no www)
4. Click **Continue**

Cloudflare akan:
- Create CNAME record automatically
- Point to Pages infrastructure
- Ask for confirmation

5. Click: **Activate domain**

---

## STEP 7: Verify DNS Records Created

Go back to: **DNS** section (left sidebar)

You should see new records:
```
Type: CNAME
Name: fdiskandar.com
Content: [hash].pages.dev
Proxy status: Proxied
```

This is what Cloudflare added automatically.

---

## STEP 8: Quick Test

In same browser:
1. Open new tab: `https://fdiskandar.com/`
2. **WAIT 1-2 minutes** for DNS to cache
3. If error: That's OK, DNS still propagating (wait more)
4. If loads: ✓ Success!

If you get error, that's normal — DNS takes a few minutes to propagate globally.

---

## What to Tell Me After

Once Pages project is created and custom domain added:

```
Pages project created!
- Pages URL: [what Cloudflare gave you, e.g., https://abc123.pages.dev]
- Custom domain: fdiskandar.com activated
- Build status: Success ✓
```

Then I'll:
1. Update hugo.toml with baseURL = https://fdiskandar.com/
2. Commit changes
3. Trigger new build
4. Setup redirects for rinji.id

---

## Troubleshooting

**"Build failed"**
- Check build logs in Cloudflare
- Usually: Hugo version issue or YAML syntax error
- I'll fix it

**"Custom domain won't activate"**
- Make sure nameservers are set correctly
- Try again in 5-10 minutes

**"fdiskandar.com shows error page"**
- DNS not fully propagated yet
- Wait 5-30 minutes and refresh
- Check: Is Pages project healthy?

**"Pages keeps rebuilding"**
- Normal if you have github integration
- Each git push triggers rebuild
- Usually fine

---

**Ready? Follow the steps above and report back!** 🚀

