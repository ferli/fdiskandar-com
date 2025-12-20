# Add Custom Domain to fdiskandar Pages Project

**Status:** Pages project `fdiskandar` deployed at https://cc3e5e05.fdiskandar.pages.dev
**Next:** Point fdiskandar.com to this Pages project

---

## Steps to Add Custom Domain

### Step 1: Go to Pages Project Settings

1. Cloudflare dashboard: https://dash.cloudflare.com/
2. Look for: **Pages** (might be under Workers & Pages section)
3. Find project: **fdiskandar**
4. Click on it

---

### Step 2: Add Custom Domain

1. In project dashboard, look for: **Custom domain** or **Domains** section
2. Click: **Add domain** or **+ Add custom domain**
3. Enter: `fdiskandar.com`
4. Click: **Validate**

---

### Step 3: Cloudflare Auto-Creates DNS Records

Cloudflare will show:
```
Type: CNAME
Name: fdiskandar.com
Content: cc3e5e05.fdiskandar.pages.dev
Proxy: Proxied
```

It will:
- Create this CNAME record automatically
- Point to your Pages deployment
- Click: **Activate domain** or **Confirm**

---

### Step 4: Verify DNS Records in DNS Dashboard

1. Go to: **DNS** section for fdiskandar.com
2. You should now see:
   ```
   Type: CNAME
   Name: fdiskandar.com (or @ for root)
   Content: cc3e5e05.fdiskandar.pages.dev
   Proxy status: Proxied
   ```

---

### Step 5: Test the Domain

Once custom domain is active:

1. Open new tab: `https://fdiskandar.com/`
2. **Wait 30 seconds** for DNS to update locally
3. If shows your site: ✓ Success!
4. If shows error: Wait a bit more (DNS propagation)

---

## Quick Checklist

- [ ] Pages project `fdiskandar` created
- [ ] Site deployed to: https://cc3e5e05.fdiskandar.pages.dev
- [ ] Custom domain `fdiskandar.com` added to Pages project
- [ ] DNS records created automatically (CNAME)
- [ ] Domain activated in Cloudflare
- [ ] Test: https://fdiskandar.com/ loads correctly

---

## After Custom Domain is Active

Tell me:
```
Custom domain added!
- Domain: fdiskandar.com
- Pages project: fdiskandar
- Status: Active ✓
- Test URL: https://fdiskandar.com/
```

Then I will:
1. Setup 301 redirects for rinji.id → fdiskandar.com
2. Verify all pages load correctly
3. Migration complete!

---

**Go add custom domain in Cloudflare Pages now!** 🚀

