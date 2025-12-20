# Link fdiskandar.com to Pages Project

**Current status:**
- fdiskandar.com is Active in Cloudflare
- Pages project deployed at https://cc3e5e05.fdiskandar.pages.dev
- Need to connect them

---

## Step 1: Click fdiskandar.com Domain

1. From Domains list, click: **fdiskandar.com**
2. You'll enter domain settings page

---

## Step 2: Go to Pages Settings

Once inside fdiskandar.com settings:

1. Look for: **Pages** section (left sidebar)
   - Or: **Workers & Pages**
   - Or: **Deployments**

2. If you see **Pages** section with your `fdiskandar` project
   - Click on it to open project settings

---

## Step 3: Add Custom Domain to Pages Project

**Option A: If you see Pages project listed:**

1. Click: **Pages** or **fdiskandar** project
2. Look for: **Domains** or **Custom domain** section
3. Click: **+ Add custom domain** or **Add domain**
4. It should auto-suggest: `fdiskandar.com`
5. Select it and activate

**Option B: If you don't see custom domain option:**

1. Still in fdiskandar.com domain settings
2. Go to: **DNS** section
3. Click: **+ Add record**
4. Add CNAME record manually:
   ```
   Type: CNAME
   Name: @ (root domain)
   Content: cc3e5e05.fdiskandar.pages.dev
   Proxy: Proxied
   TTL: Auto
   ```
5. Click: **Save**

---

## Expected Result

After adding custom domain or CNAME record, you should see:

```
Domain: fdiskandar.com
Status: Active ✓
Points to: cc3e5e05.fdiskandar.pages.dev
Proxy: Enabled
```

---

## Test It Works

1. Open new tab: `https://fdiskandar.com/`
2. Wait 30 seconds
3. Should see your website homepage
4. Click around to verify pages load

---

## What to Tell Me After

Once custom domain is linked:

```
Custom domain linked!
- Domain: fdiskandar.com
- Points to: cc3e5e05.fdiskandar.pages.dev
- Status: Active & working ✓
- Test: https://fdiskandar.com/ loads correctly
```

Then I will:
1. Setup 301 redirects from rinji.id
2. Verify all pages
3. Migration complete!

---

**Try adding custom domain now!** 🚀

