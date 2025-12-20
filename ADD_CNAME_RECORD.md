# Add CNAME Record untuk fdiskandar.com

**Lokasi:** Kamu sudah di fdiskandar.com settings
**Langkah berikutnya:** Go to DNS dan add CNAME record

---

## Step 1: Click DNS

Left sidebar → Click **DNS**

---

## Step 2: Add Record

1. Click **+ Add record** button
2. Isi dengan:
   ```
   Type: CNAME
   Name: @ (atau kosong, berarti root domain)
   Content: cc3e5e05.fdiskandar.pages.dev
   Proxy status: Proxied
   TTL: Auto
   ```

3. Click **Save**

---

## Expected Result

Record akan ditambahkan:
```
Type    Name              Content                           Proxy status    TTL
CNAME   fdiskandar.com    cc3e5e05.fdiskandar.pages.dev    Proxied         Auto
```

---

## Verify It Works

1. Open baru tab: `https://fdiskandar.com/`
2. Tunggu 30 detik
3. Should see homepage
4. Click around verify pages load

---

## If There's Error

**"This record conflicts with an existing record"**
→ There might be existing A record
→ Delete it first, then add CNAME

**"fdiskandar.com shows 522 error"**
→ DNS propagating, wait 5-10 minutes, refresh

**"Page shows rinji.id content"**
→ DNS cache, clear browser cache or wait

---

## After CNAME is Added

Tell me:
```
CNAME record added!
- Type: CNAME
- Name: fdiskandar.com
- Content: cc3e5e05.fdiskandar.pages.dev
- Status: Proxied ✓
- Test: https://fdiskandar.com/ works ✓
```

Then I akan setup 301 redirects dari rinji.id!

---

**Go add CNAME record now!** 🚀

