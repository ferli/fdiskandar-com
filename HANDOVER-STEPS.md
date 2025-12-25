# Langkah-Langkah Handover: Claude Code CLI → Gemini CLI

**Tujuan:** Memindahkan konteks pekerjaan dari Claude Code CLI ke Gemini CLI secara smooth

---

## Persiapan (Sudah Selesai ✓)

- ✅ Semua perubahan terbaru sudah di-commit
- ✅ HANDOVER.md sudah dibuat dengan konteks lengkap
- ✅ HANDOVER-STEPS.md (file ini) sudah tersedia
- ✅ Repository dalam kondisi clean (no uncommitted changes kecuali public/ dan .claude/)

---

## Step 1: Verifikasi Status Repository

```bash
cd C:\Repo\fdiskandar-com
git status
git log --oneline -5
```

**Yang harus kamu lihat:**
- Branch: main
- Status: "Your branch is up to date with 'origin/main'"
- Latest commits mencakup:
  - Expertise page reframe
  - About page reframe
  - Theme toggle fix
  - Handover documentation

**Jika ada uncommitted changes di `public/` atau `.claude/` → ABAIKAN (normal, tidak perlu commit)**

---

## Step 2: Buka Gemini CLI di Directory yang Sama

```bash
# Pastikan kamu di directory yang benar
cd C:\Repo\fdiskandar-com

# Jalankan Gemini CLI (sesuaikan dengan command Gemini CLI yang kamu gunakan)
# Contoh (sesuaikan):
gemini
# atau
gemini-cli
# atau cara lain sesuai instalasi Gemini CLI kamu
```

---

## Step 3: Berikan Konteks Awal ke Gemini

**Copy-paste teks ini ke Gemini CLI:**

```
Halo Gemini, saya handover pekerjaan dari Claude Code CLI.

Tolong baca file-file berikut secara berurutan untuk memahami konteks project:

1. HANDOVER.md - Dokumen handover lengkap dari Claude
2. CLAUDE.md - Dokumentasi project overview
3. README.md - Informasi general

Setelah membaca, confirm bahwa kamu sudah memahami:
- Project ini adalah website Hugo untuk personal brand FD Iskandar di sektor air
- Recent work focus pada perubahan tone dari "expert" ke "humble collaborator"
- Dark mode only (jangan aktifkan theme toggle)
- Bahasa Indonesia
- Auto-deploy via Cloudflare Pages

Jika sudah, tolong summarize kondisi current state dalam 3-5 bullet points.
```

---

## Step 4: Test Pemahaman Gemini dengan Task Sederhana

**Berikan task kecil untuk test:**

```
Tolong jalankan command berikut dan beritahu hasil:

1. hugo --quiet
2. git log --oneline -3

Ini untuk memastikan kamu bisa run commands dan akses git history.
```

---

## Step 5: Tanyakan ke Gemini tentang Content Voice

**Test apakah Gemini paham voice guidelines:**

```
Pertanyaan:

Jika saya minta kamu update halaman expertise/digital-transformation.md,
apa prinsip-prinsip tone/voice yang harus kamu ikuti?

Beri contoh:
- ✅ Frasa yang BAIK digunakan
- ❌ Frasa yang HARUS DIHINDARI
```

**Jawaban yang BENAR dari Gemini harus mencakup:**
- ✅ Gunakan "dari diskusi dengan...", "pengamatan menunjukkan..."
- ✅ Gunakan "utilitas air" bukan "PDAM"
- ✅ Hindari klaim expertise atau angka tahun
- ✅ Tutup dengan nada humble ("bukan sebagai pakar...")
- ❌ Hindari "saya telah memimpin...", "30+ tahun", "yang membuat saya berbeda..."

**Jika Gemini menjawab benar → Lanjut ke Step 6**
**Jika salah → Ulangi Step 3, minta Gemini baca HANDOVER.md lebih detail**

---

## Step 6: Berikan Task Nyata Pertama

**Pilih salah satu task untuk test Gemini:**

### Opsi A: Update Content (Paling Recommended)
```
Task: Update file content/expertise/digital-transformation.md dengan tone yang sama seperti expertise/_index.md (yang baru saja diupdate).

Sebelum mulai:
1. Baca current content di digital-transformation.md
2. Baca expertise/_index.md sebagai reference untuk tone yang diinginkan
3. Propose changes dalam format bullet points
4. Tunggu approval dari saya sebelum implement

Jangan langsung edit, propose dulu!
```

### Opsi B: Simple Build & Status Check
```
Task sederhana:

1. Check git status
2. Run hugo --quiet untuk build
3. List 5 file terakhir yang dimodifikasi di folder content/
4. Report hasilnya

Ini untuk test bahwa kamu bisa run basic commands.
```

### Opsi C: Review Recent Changes
```
Task review:

Lihat 3 commit terakhir:
1. 8ef3fc3 - docs: Add comprehensive handover documentation
2. 7bbcb52 - content: Reframe expertise page
3. ff74615 - content: Reframe about page

Untuk masing-masing commit:
- Baca file yang berubah
- Summarize apa yang diubah dan kenapa
- Confirm apakah perubahan sesuai dengan voice guidelines

Report findings kamu.
```

---

## Step 7: Verifikasi Gemini Memahami Hugo Workflow

**Tanya ke Gemini:**

```
Pertanyaan workflow:

Jika saya minta kamu update file content/about.md, apa langkah-langkah lengkap yang harus kamu lakukan dari awal sampai perubahan live di website?

List step by step dengan commands yang diperlukan.
```

**Jawaban BENAR harus mencakup:**
1. Read file saat ini
2. Edit dengan tone yang sesuai
3. Run `hugo --quiet` untuk test build
4. `git add content/about.md`
5. `git commit -m "description"`
6. `git push origin main`
7. Cloudflare Pages auto-deploy (1-2 menit)

**Jika Gemini menjawab benar → Handover SUKSES! ✅**

---

## Step 8: Bookmark & Quick Reference untuk Gemini

**Berikan quick reference ini ke Gemini:**

```
Quick Reference untuk kamu Gemini:

KEY FILES:
- HANDOVER.md = Konteks lengkap dari Claude
- CLAUDE.md = Project documentation
- hugo.toml = Config (JANGAN UBAH disableThemeToggle!)
- content/**/*.md = Semua content (Indonesian)

CRITICAL RULES:
1. ALWAYS use humble, collaborative tone
2. NEVER add year counts atau achievement claims
3. Use "utilitas air" NOT "PDAM"
4. Test dengan hugo --quiet before commit
5. Read file first before editing

COMMON COMMANDS:
- hugo server -D = local dev server
- hugo --quiet = build production
- git status = check changes
- git log --oneline -5 = recent commits

VOICE TEMPLATE:
✅ "Dari diskusi dengan berbagai utilitas..."
✅ "Pengamatan menunjukkan..."
✅ "Kita semua masih belajar"
❌ "Saya telah memimpin..."
❌ "30+ tahun pengalaman"

Jika ragu, tanya user dulu!
```

---

## Troubleshooting

### Issue: Gemini tidak bisa baca file
**Solution:** Pastikan Gemini CLI punya akses ke directory. Coba:
```bash
ls -la C:\Repo\fdiskandar-com\HANDOVER.md
```

### Issue: Gemini suggest changes yang melanggar voice guidelines
**Solution:** Remind Gemini:
```
Reminder: Tone harus humble dan collaborative.
Baca kembali section "Content Strategy & Voice Guidelines" di HANDOVER.md.
```

### Issue: Gemini ingin modify theme files
**Solution:** STOP immediately:
```
STOP! Jangan modify files di themes/PaperMod/.
Baca section "Things You Should NEVER Do" di HANDOVER.md.
```

---

## Checklist Handover Complete

- [ ] Gemini sudah baca HANDOVER.md
- [ ] Gemini bisa run hugo commands
- [ ] Gemini bisa access git history
- [ ] Gemini memahami voice guidelines (test passed)
- [ ] Gemini memahami Hugo workflow (test passed)
- [ ] Gemini berhasil complete 1 task sederhana
- [ ] Kamu confident untuk lanjutkan work dengan Gemini

**Jika semua checklist ✅ → Handover COMPLETE!**

---

## Pesan Penutup dari Claude

Project ini dalam kondisi baik:
- ✅ All recent work committed & pushed
- ✅ Dark mode working perfectly
- ✅ Content voice transformation mostly complete
- ✅ Documentation comprehensive

**Yang masih perlu di-update (future work):**
- Individual expertise detail pages (4 files)
- Individual insight articles
- Individual pemikiran articles
- Individual resource pages

**Semua file tersebut mungkin masih punya old voice/tone dan perlu diupdate satu-satu sesuai request user.**

Good luck! 🚀

*— Claude Code CLI, signing off*
