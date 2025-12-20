# Fix Error 522: Connection Timed Out

**Error:** 522 Connection timed out
**Cause:** Cloudflare can't reach origin server
**Solution:** Fix CNAME record configuration

---

## Root Cause

Cloudflare Pages URL (`cc3e5e05.fdiskandar.pages.dev`) adalah **Pages deployment**, bukan traditional origin server.

Pointing CNAME directly ke Pages sometimes causes 522 error.

---

## Solution: Use Cloudflare Pages Custom Domain Feature

Instead of manual CNAME, gunakan **Pages built-in custom domain feature** yang handle DNS configuration otomatis.

---

## Step 1: Check Current DNS

Go to: **DNS** section di fdiskandar.com
Look for CNAME record kamu buat tadi.

---

## Step 2: Delete Problematic CNAME (if exists)

If kamu lihat:
```
Type: CNAME
Name: fdiskandar.com
Content: cc3e5e05.fdiskandar.pages.dev
```

Click **Delete** (trash icon)

---

## Step 3: Let Pages Handle DNS Configuration

**Better approach:** Use Pages project settings untuk add custom domain (Pages handle DNS otomatis).

**How to do it:**

1. Go to: **Workers & Pages** atau **Pages** section di Cloudflare
2. Find project: **fdiskandar**
3. Click on project name
4. Look for: **Domains** or **Custom domains** tab
5. Click: **Add custom domain**
6. Enter: `fdiskandar.com`
7. Click: **Continue**
8. Cloudflare automatically creates correct DNS records
9. Click: **Activate** or **Confirm**

---

## Step 4: Verify DNS Was Created Correctly

Go back to **DNS** section.

You should see:
```
Type: CNAME
Name: fdiskandar.com (or _pages or _cf_pages or similar)
Content: [Pages infrastructure URL]
Proxy: Proxied
```

**OR**

```
Type: A
Name: fdiskandar.com
Content: 192.x.x.x (Cloudflare Pages IP)
Proxy: Proxied
```

---

## Step 5: Test Again

1. Wait 5-10 minutes untuk DNS propagate
2. Open: `https://fdiskandar.com/`
3. Should now work (no 522 error)
4. If still error, wait more (DNS can take up to 1 hour)

---

## If Still Getting 522

**Check DNS propagation:**
1. Go to: https://dnschecker.org/
2. Enter: `fdiskandar.com`
3. Check if CNAME pointing to correct Pages URL

**OR check Pages project:**
1. Go to Pages project settings
2. Verify custom domain is actually activated
3. Check deployment status (is latest deployment successful?)

---

## Quick Troubleshooting Checklist

- [ ] Delete manual CNAME record from DNS
- [ ] Use Pages project to add custom domain (Pages handle DNS)
- [ ] Wait 5-10 minutes for DNS propagation
- [ ] Clear browser cache (Ctrl+Shift+Del)
- [ ] Try incognito/private window
- [ ] Test on different device/network
- [ ] Check Pages deployment is successful (not failed)

---

## Expected Result After Fix

```
DNS Record (auto-created by Pages):
Type: CNAME
Name: fdiskandar.com
Content: [Pages infrastructure]
Proxy: Proxied ✓

Website Access:
https://fdiskandar.com/ → Loads homepage ✓
All pages work correctly ✓
```

---

## Report Back

After fixing:
```
Error 522 fixed!
- DNS records corrected
- https://fdiskandar.com/ is now loading ✓
- Website working correctly ✓
```

Then I akan setup 301 redirects dari rinji.id & migration complete!

---

**Try this fix now!** 🚀

