# Quick DNS Fix Guide - 3 Simple Steps

**Goal:** Stop Error 522 and get fdiskandar.com working

**Time needed:** 5 minutes setup + 5-10 minutes waiting for DNS propagation

---

## Step 1: Delete Old CNAME Record (1 minute)

1. Go to: https://dash.cloudflare.com/
2. Click on **fdiskandar.com** domain
3. In left sidebar, click **DNS**
4. Find the CNAME record that points to `cc3e5e05.fdiskandar.pages.dev`
5. Click the **trash/delete icon** on that row
6. Confirm deletion

---

## Step 2: Add New CNAME Record (2 minutes)

1. Still in DNS section
2. Click **+ Add record** button
3. Fill in the form:
   ```
   Type:    CNAME
   Name:    @ (root domain)
   Content: rinji-id.pages.dev
   Proxy:   Proxied
   TTL:     Auto
   ```
4. Click **Save**

**Result should look like:**
```
Type   | Name           | Content            | Proxy   | TTL
-------|----------------|--------------------|---------|-----
CNAME  | fdiskandar.com | rinji-id.pages.dev | Proxied | Auto
```

---

## Step 3: Wait & Test (10 minutes)

1. **Wait 5-10 minutes** for DNS to propagate globally
2. Open new tab: `https://fdiskandar.com/`
3. **Should see your homepage** (no error!)
4. Click around to verify pages load
5. Try `https://rinji.id/` → should redirect to fdiskandar.com

---

## ✅ Expected Result

| URL | What Happens |
|-----|--------------|
| https://fdiskandar.com/ | Homepage loads ✓ |
| https://fdiskandar.com/about | About page loads ✓ |
| https://fdiskandar.com/expertise | Expertise page loads ✓ |
| https://rinji.id/ | Redirects to fdiskandar.com ✓ |

---

## 🆘 If Still Getting Error 522

1. Clear browser cache (Ctrl+Shift+Del) and try again
2. Try in private/incognito window
3. Wait another 5 minutes (DNS can take up to 30 mins sometimes)
4. Check DNS setting one more time - make sure it says `rinji-id.pages.dev` (not fdiskandar)

---

## 📝 Report Back Format

Once it's working, tell me:

```
DNS fixed! ✓
- fdiskandar.com loads correctly
- All pages accessible
- rinji.id redirects working
```

Then I'll finish the migration with final cleanup!

---

**Go fix the DNS now!** 🚀
