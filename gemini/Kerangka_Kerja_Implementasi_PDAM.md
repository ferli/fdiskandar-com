# KERANGKA KERJA IMPLEMENTASI PDAM
## Knowledge Base AI - Transformasi Digital Utilitas Air Indonesia

**Versi:** 1.0  
**Tanggal:** 22 Desember 2025  
**Penulis:** FD Iskandar  
**Status:** Final  
**Tujuan:** Framework praktis & template implementasi untuk panduan step-by-step eksekusi

---

## **1. Pendahuluan: Urgensi Transformasi Utilitas Air di Era Digital**

Perusahaan Daerah Air Minum (PDAM), atau yang kini secara regulasi bertransformasi menjadi Perusahaan Umum Daerah (Perumda) Air Minum, berdiri di persimpangan jalan yang krusial. Di satu sisi, mandat konstitusional menuntut penyediaan air bersih sebagai hak dasar warga negara yang harus dipenuhi dengan prinsip Kualitas, Kuantitas, Kontinuitas, dan Keterjangkauan (4K). Di sisi lain, realitas operasional di lapangan seringkali dipenuhi dengan tantangan inefisiensi teknis berupa tingginya tingkat kehilangan air (*Non-Revenue Water* atau NRW), keterbatasan cakupan layanan, serta kendala solvabilitas keuangan yang menghambat investasi infrastruktur baru.1 Dalam konteks ini, transformasi digital bukan lagi sekadar adopsi teknologi untuk gaya hidup perusahaan, melainkan sebuah strategi bertahan hidup dan berkembang (*survival and growth strategy*) yang fundamental.

Dokumen ini, yang diberi judul teknis FRAMEWORKS.md, dirancang sebagai repositori pengetahuan strategis dan taktis bagi jajaran manajemen puncak PDAM—mulai dari Direktur Utama hingga Manajer Teknologi Informasi (TI)—untuk menavigasi kompleksitas modernisasi utilitas. Laporan ini tidak hanya menyajikan teori, melainkan kerangka kerja implementatif yang mengintegrasikan standar global seperti *International Water Association* (IWA) dan ISO 31000 dengan realitas regulasi nasional, termasuk indikator kinerja Badan Peningkatan Penyelenggaraan Sistem Penyediaan Air Minum (BPPSPAM) dan arsitektur Sistem Pemerintahan Berbasis Elektronik (SPBE) sesuai Peraturan Presiden Nomor 95 Tahun 2018\.3

Tujuan utama dari laporan ini adalah memberikan panduan langkah demi langkah dalam lima domain kritis: pengukuran kematangan digital yang selaras dengan kinerja korporasi, penyusunan justifikasi bisnis (*business case*) yang tahan uji, audit kehilangan air yang presisi, manajemen risiko siber pada konvergensi IT/OT, dan peta jalan eksekusi 100 hari bagi kepemimpinan teknologi baru. Melalui pendekatan yang terstruktur ini, diharapkan PDAM dapat bergeser dari paradigma pengelolaan manual-reaktif menuju utilitas cerdas yang prediktif dan efisien.

## ---

**2\. Asesmen Kematangan Digital Terintegrasi (Integrated Digital Maturity Assessment)**

Mengukur kematangan digital sebuah utilitas air tidak dapat dilakukan dalam ruang hampa. Penilaian ini harus dikaitkan secara intrinsik dengan indikator kesehatan perusahaan yang telah ditetapkan oleh Kementerian Pekerjaan Umum dan Perumahan Rakyat (PUPR) dan Kementerian Dalam Negeri. Sebuah PDAM mungkin memiliki sensor IoT (*Internet of Things*) tercanggih, namun jika indikator kinerjanya masih berstatus "Sakit" atau "Kurang Sehat" akibat inefisiensi biaya atau rendahnya cakupan layanan, maka maturitas digitalnya belum memberikan dampak substansial.2 Oleh karena itu, kerangka kerja asesmen ini memetakan teknologi sebagai *enabler* bagi 18 indikator kinerja utama BPPSPAM.

### **2.1 Filosofi Asesmen: Digital sebagai Penggerak Kinerja "Sehat"**

Model kematangan ini mengadopsi pendekatan *Intelligent Water Systems* (IWS) yang dimodifikasi dengan bobot penilaian kinerja BUMD Air Minum nasional.5 Dalam regulasi nasional, penilaian kinerja dibagi menjadi empat aspek utama dengan bobot spesifik: Aspek Keuangan (25%), Aspek Pelayanan (25%), Aspek Operasional (35%), dan Aspek Sumber Daya Manusia (15%).2 Asesmen kematangan digital ini mengevaluasi sejauh mana teknologi informasi dan operasional telah berpenetrasi ke dalam keempat aspek tersebut untuk mendongkrak nilai kinerja.

Premis dasarnya adalah bahwa setiap tingkatan kematangan digital harus berkolerasi positif dengan peningkatan skor kinerja. Misalnya, implementasi sistem baca meter digital berbasis Android dengan fitur GPS (*Global Positioning System*) harus secara langsung meningkatkan indikator "Efektivitas Penagihan" dalam aspek Keuangan dan "Cakupan Pelayanan Teknis" dalam aspek Pelayanan melalui data yang lebih akurat dan penanganan komplain yang lebih cepat.6

### **2.2 Dimensi Kematangan Digital dan Indikator Kinerja Terkait**

Evaluasi dilakukan pada lima dimensi strategis yang menopang operasional PDAM. Setiap dimensi dinilai berdasarkan kapabilitas teknologi untuk mendukung pencapaian target indikator BPPSPAM.

#### **2.2.1 Dimensi Tata Kelola Digital dan Strategi (Governance & Strategy)**

Dimensi ini menyoroti bagaimana kepemimpinan PDAM mengarahkan investasi teknologi. Kematangan diukur dari keselarasan antara *IT Master Plan* dengan Rencana Bisnis (Renbis) 5 Tahunan perusahaan. Dalam konteks regulasi, ini berkaitan erat dengan indikator kesehatan finansial seperti *Return on Equity* (ROE) dan Rasio Operasi. Teknologi harus dipandang sebagai investasi modal (CAPEX) yang mampu menurunkan biaya operasional (OPEX) jangka panjang.

Pada tingkat kematangan rendah, inisiatif TI bersifat sporadis, seringkali didorong oleh vendor, dan tidak memiliki peta jalan yang jelas. Sebaliknya, pada tingkat kematangan tinggi, PDAM telah mengadopsi prinsip SPBE secara utuh, memiliki komite pengarah TI yang dipimpin direksi, dan menggunakan data analitik untuk keputusan strategis investasi infrastruktur.8 Indikator keberhasilannya adalah adanya integrasi perencanaan anggaran TI yang transparan dan akuntabel.

#### **2.2.2 Dimensi Pelayanan Pelanggan Cerdas (Smart Customer Experience)**

Aspek Pelayanan memiliki bobot 25% dalam penilaian kinerja, mencakup indikator cakupan pelayanan, pertumbuhan pelanggan, tingkat penyelesaian pengaduan, dan kualitas air pelanggan.7 Dimensi ini mengevaluasi transformasi interaksi pelanggan dari loket fisik menuju kanal digital *omnichannel*.

Penggunaan aplikasi seluler seperti mWater atau aplikasi mandiri PDAM untuk survei kepuasan pelanggan dan pelaporan meter mandiri merupakan tanda kematangan digital tingkat lanjut.6 Sistem *Customer Relationship Management* (CRM) yang terintegrasi dengan sistem *Work Order* (Perintah Kerja) lapangan memungkinkan setiap pengaduan pelanggan (misalnya, air mati atau bocor) terlacak secara *real-time* durasi penyelesaiannya. Hal ini berdampak langsung pada skor indikator "Tingkat Penyelesaian Pengaduan" yang mensyaratkan penyelesaian di atas 80% untuk nilai maksimal.7

#### **2.2.3 Dimensi Operasional Cerdas (Intelligent Operations & SCADA)**

Dengan bobot terbesar (35%), aspek Operasional adalah jantung dari kinerja PDAM.2 Indikator kritis di sini meliputi Efisiensi Produksi, tingkat NRW, Jam Operasi Layanan, dan Tekanan Air. Dimensi ini mengukur adopsi teknologi *Operational Technology* (OT) seperti SCADA (*Supervisory Control and Data Acquisition*), telemetri, dan otomatisasi IPA (*Instalasi Pengolahan Air*).

Kematangan digital dinilai dari pergeseran pemantauan manual menuju otomatisasi. Pada level dasar, petugas mencatat debit dan tekanan air di buku log. Pada level optimal, sensor IoT mengirimkan data debit dan tekanan setiap detik ke pusat komando (*Command Center*), dan algoritma cerdas mengatur kecepatan pompa (*Variable Speed Drive*) secara otomatis untuk menjaga tekanan stabil sekaligus menghemat energi.5 Kematangan di dimensi ini berkontribusi langsung pada penurunan NRW fisik dan efisiensi energi.

#### **2.2.4 Dimensi Manajemen Aset Berbasis Data (Data-Driven Asset Management)**

Infrastruktur perpipaan dan mesin adalah aset terbesar PDAM. Manajemen aset yang buruk menyebabkan tingginya biaya perbaikan dan gangguan layanan. Dimensi ini menilai penggunaan sistem informasi geografis (GIS) dan sistem manajemen pemeliharaan terkomputerisasi (CMMS).

Indikator kinerja yang relevan adalah "Penggantian Meter Air" dan efisiensi biaya pemeliharaan. Asesmen melihat apakah PDAM memiliki peta digital aset yang akurat (*spatial accuracy*) dan lengkap (*attribute completeness*). Pada tingkat kematangan tinggi, data GIS terintegrasi dengan data hidrolik untuk simulasi *Digital Twin*, memungkinkan prediksi kegagalan pipa sebelum terjadi, sehingga strategi pemeliharaan berubah dari reaktif (*fix when broken*) menjadi prediktif.11

#### **2.2.5 Dimensi Analitik Data dan Pelaporan (Data Analytics & Reporting)**

Dimensi ini mengikat keempat dimensi lainnya. Kemampuan PDAM untuk mengumpulkan, memvalidasi, dan menganalisis data adalah kunci dari "Satu Data" perusahaan. Hal ini krusial untuk pelaporan kinerja ke BPKP dan Kementerian.

Kematangan dinilai dari otomatisasi laporan. Apakah Laporan Neraca Air bulanan dihasilkan secara otomatis dari sistem, atau masih diketik ulang di spreadsheet? Analitik tingkat lanjut melibatkan penggunaan *Business Intelligence* (BI) untuk memvisualisasikan tren pendapatan, pola konsumsi air, dan anomali operasional secara *real-time* bagi pengambil keputusan.1

### **2.3 Matriks Tingkat Kematangan (Maturity Level Matrix)**

Untuk memberikan penilaian yang objektif, kerangka kerja ini mendefinisikan lima tingkat kematangan yang berlaku universal untuk setiap dimensi di atas.

| Tingkat | Definisi Kematangan & Karakteristik | Implikasi pada Indikator Kinerja (BPPSPAM) |
| :---- | :---- | :---- |
| **Level 1: Ad-Hoc (Pemula)** | Proses manual, bergantung pada individu tertentu. Data tersimpan di kertas atau spreadsheet terisolasi. Tidak ada standar baku TI. | **Kinerja: Sakit/Kurang Sehat.** Data NRW dan Efektivitas Penagihan seringkali estimasi dan tidak dapat diaudit. Tingginya *human error* dalam pencatatan meter. |
| **Level 2: Terkelola (Oportunis)** | Aplikasi dasar mulai digunakan (Billing System, Akuntansi) namun terpisah (silo). GIS mulai dipetakan parsial. SCADA terbatas monitoring level reservoir. | **Kinerja: Kurang Sehat.** Pelaporan mulai tertib, namun analisis korelasi antar data (misal: produksi vs penjualan) sulit dilakukan. Respon komplain masih lambat. |
| **Level 3: Terdefinisi (Sistematis)** | Integrasi sistem inti mulai terbentuk (Billing \<-\> Akuntansi). SOP digital diterapkan. GIS mencakup \>80% aset. SCADA memonitor flow & pressure utama. | **Kinerja: Sehat (Batas Bawah).** NRW mulai terukur dengan neraca air bulanan. Efisiensi penagihan meningkat karena data piutang valid. |
| **Level 4: Terukur (Terintegrasi)** | Data-driven decision making. Dashboard kinerja real-time. Smart metering/DMA telemetri di zona prioritas. Integrasi ERP penuh. | **Kinerja: Sehat (Optimal).** NRW terkendali melalui deteksi dini. Biaya energi pompa efisien. Kepuasan pelanggan tinggi karena layanan responsif. |
| **Level 5: Optimal (Cerdas)** | Prediktif dan otomatisasi penuh (AI/ML). Digital Twin jaringan. Layanan pelanggan mandiri. Prediksi kebocoran dan kebutuhan air masa depan. | **Kinerja: Sehat (Berkelanjutan).** PDAM menjadi tolok ukur nasional. Efisiensi operasional maksimal, inovasi berkelanjutan dalam layanan. |

### **2.4 Templat Instrumen Penilaian Mandiri (Self-Assessment Tool)**

Manajer PDAM dapat menggunakan kuesioner berikut untuk melakukan *gap analysis*. Skor dihitung berdasarkan rata-rata bobot jawaban.

**Bagian A: Infrastruktur & Aset (Bobot 20%)**

* **Q1:** Sejauh mana jaringan pipa distribusi telah terpetakan dalam format digital?  
  * (1) Hanya peta kertas/gambar teknik lama, banyak perubahan di lapangan tidak tercatat.  
  * (3) Peta digital (CAD/GIS) tersedia untuk \>70% jaringan, namun atribut teknis (jenis, umur pipa) belum lengkap.  
  * (5) Web-GIS terintegrasi penuh, mencakup seluruh aset, diakses via mobile app oleh petugas, update data real-time dari lapangan.11

**Bagian B: Operasional & NRW (Bobot 30%)**

* **Q2:** Bagaimana metode perhitungan Neraca Air (*Water Balance*) dilakukan?  
  * (1) Estimasi tahunan kasar (*Top-down*) tanpa data pengukuran yang valid.  
  * (3) Perhitungan bulanan menggunakan spreadsheet manual, data produksi dari flowmeter induk, data konsumsi dari billing.  
  * (5) Otomatisasi neraca air harian per DMA (*District Meter Area*) menggunakan data telemetri SCADA dan billing system terintegrasi.14

**Bagian C: Pelayanan & Pelanggan (Bobot 25%)**

* **Q3:** Bagaimana mekanisme pembacaan meter dan validasi data pemakaian air?  
  * (1) Manual catat buku, input ulang di kantor (rentan manipulasi dan kesalahan).  
  * (3) Foto meter menggunakan HP Android, validasi anomali dilakukan manual oleh supervisor di kantor.  
  * (5) *Smart Meter* (IoT) atau Foto Meter dengan AI (*Artificial Intelligence*) untuk validasi angka stan dan koordinat GPS secara otomatis saat itu juga.6

**Bagian D: Manajemen Data & Keamanan (Bobot 25%)**

* **Q4:** Bagaimana pengelolaan keamanan data dan keberlangsungan sistem (Business Continuity)?  
  * (1) Tidak ada backup rutin, password dibagi-bagi, tidak ada antivirus terpusat.  
  * (3) Backup rutin harian di server lokal, ada firewall dasar, akses user dibatasi password.  
  * (5) Backup otomatis 3-2-1 (termasuk offsite/cloud), implementasi ISO 27001/Indeks KAMI, *Disaster Recovery Plan* teruji berkala.3

## ---

**3\. Pengembangan Business Case Investasi Teknologi**

Salah satu hambatan terbesar transformasi digital di BUMD air minum adalah kesulitan meyakinkan pemangku kepentingan (Direksi, Dewan Pengawas, Kepala Daerah/DPRD) mengenai urgensi investasi teknologi. Seringkali, TI dianggap sebagai pusat biaya (*cost center*) semata. Kerangka kerja ini mengadopsi struktur *Outline Business Case* (OBC) standar pemerintah dan metodologi Val IT untuk menerjemahkan inisiatif teknis menjadi nilai ekonomi dan pelayanan publik yang nyata.18

### **3.1 Paradigma Investasi: Dari Belanja ke Nilai**

Dalam menyusun proposal investasi, manajer TI harus menghindari bahasa teknis yang terlalu mendalam (seperti spesifikasi server atau topologi jaringan) dan beralih ke bahasa bisnis. Setiap Rupiah yang dikeluarkan harus dikaitkan dengan:

1. **Peningkatan Pendapatan:** Melalui penurunan kehilangan air komersial (akurasi meter) dan fisik (perbaikan bocor cepat).  
2. **Efisiensi Biaya:** Pengurangan biaya lembur, kertas, perjalanan dinas, dan energi listrik.  
3. **Kepatuhan Regulasi:** Pemenuhan Standar Pelayanan Minimal (SPM) dan indikator kinerja BPPSPAM.  
4. **Mitigasi Risiko:** Mencegah kegagalan sistem yang dapat melumpuhkan pelayanan.

### **3.2 Struktur Dokumen Business Case yang Efektif**

Dokumen *Business Case* harus disusun secara naratif, logis, dan persuasif, mengikuti alur berikut:

#### **3.2.1 Ringkasan Eksekutif (Executive Summary)**

Bagian ini adalah "elevator pitch" dari proposal. Harus merangkum permasalahan kritis ("burning platform"), solusi yang ditawarkan, total kebutuhan dana, dan dampak terukur terhadap kinerja PDAM. Ringkasan ini seringkali menjadi satu-satunya bagian yang dibaca oleh pengambil keputusan level tinggi.21

#### **3.2.2 Definisi Masalah dan Keselarasan Strategis**

Jelaskan konteks mengapa investasi ini diperlukan *sekarang*. Hubungkan masalah operasional dengan target strategis perusahaan (Renstra/RKAP).

* *Narasi Contoh:* "Sistem pencatatan meter manual saat ini menyebabkan rata-rata kesalahan baca 5% per bulan, yang berkontribusi langsung pada tingginya angka kehilangan air komersial. Hal ini menghambat pencapaian target penurunan NRW sebesar 2% tahun ini sebagaimana dimandatkan dalam Kontrak Kinerja Direksi.".7

#### **3.2.3 Analisis Opsi (Options Analysis)**

Jangan hanya menyajikan satu solusi. Sajikan alternatif untuk menunjukkan bahwa manajemen telah mempertimbangkan berbagai skenario.23

* **Opsi 1: Status Quo (Do Nothing).** Jelaskan konsekuensi negatif jika tidak ada tindakan (misal: potensi kehilangan pendapatan Rp X per tahun terus berlanjut, risiko audit BPKP).  
* **Opsi 2: Solusi Minimal (Do Minimum).** Perbaikan parsial dengan biaya rendah namun dampak terbatas.  
* **Opsi 3: Solusi Rekomendasi (Preferred Option).** Solusi transformasi yang diusulkan dengan keseimbangan biaya dan manfaat terbaik.

#### **3.2.4 Analisis Manfaat dan Biaya (Cost-Benefit Analysis \- CBA)**

Bagian ini menyajikan perhitungan finansial yang detail. Gunakan tabel untuk merinci komponen biaya (TCO \- *Total Cost of Ownership*) dan aliran manfaat finansial.

**Komponen Biaya (TCO):**

* **CAPEX (Biaya Modal):** Hardware (Sensor, Server), Software License, Biaya Jasa Implementasi.  
* **OPEX (Biaya Operasional 5 Tahun):** Maintenance tahunan, Langganan Cloud/Konektivitas, Pelatihan SDM, Biaya Listrik tambahan.

**Komponen Manfaat (Benefit Stream):**

* *Tangible (Dapat Diuangkan):* Peningkatan tagihan air karena meter akurat, penurunan biaya perbaikan pipa darurat (karena deteksi dini), efisiensi biaya pegawai administrasi.  
* *Intangible (Kualitatif):* Peningkatan indeks kepuasan pelanggan, ketersediaan data real-time untuk keputusan Direksi, reputasi positif Pemda.18

**Indikator Kelayakan Finansial:**

* **Net Present Value (NPV):** Selisih nilai sekarang dari arus kas masuk dan keluar. NPV positif wajib hukumnya.  
* **Internal Rate of Return (IRR):** Tingkat pengembalian modal. Harus lebih tinggi dari tingkat bunga bank atau *Cost of Capital*.  
* **Payback Period:** Berapa tahun modal kembali. Untuk teknologi, idealnya \< 3 tahun.

#### **3.2.5 Analisis Risiko Implementasi**

Identifikasi apa yang bisa salah dalam proyek ini dan bagaimana mitigasinya. Ini menunjukkan kematangan perencanaan.

* *Risiko:* Resistensi pegawai lapangan terhadap aplikasi baru.  
* *Mitigasi:* Program manajemen perubahan (*Change Management*), insentif berbasis kinerja, pelatihan intensif.21

### **3.3 Templat Business Case Siap Pakai**

Berikut adalah kerangka naratif yang dapat langsung diisi oleh tim PDAM:

# **Business Case:**

## **1\. Latar Belakang & Urgensi**

Saat ini, PDAM menghadapi tantangan. Metode konvensional terbukti tidak efektif dan memakan biaya tinggi. Hal ini mengakibatkan.

## **2\. Penyelarasan Strategis**

Proyek ini mendukung Sasaran Strategis RKAP Tahun yaitu "" serta berkontribusi pada peningkatan indikator kinerja BPPSPAM pada aspek Operasional.

## **3\. Analisis Opsi**

* **Opsi A (Status Quo):** Tetap dengan metode manual. Risiko: NRW diprediksi naik, pendapatan stagnan.  
* **Opsi B (Solusi Parsial):** Hanya mengganti meter air tanpa sistem monitoring. Biaya rendah, namun tidak mencegah kebocoran pipa kembali terjadi.  
* **Opsi C (Solusi Terintegrasi \- Rekomendasi):** Implementasi Smart DMA dengan sensor tekanan dan *flow* real-time. Biaya investasi moderat, dampak penurunan NRW signifikan dan berkelanjutan.

## **4\. Analisis Finansial (Untuk Opsi C)**

* **Total Investasi (CAPEX):** Rp \[Nilai\]  
* **Biaya Operasional Tahunan (OPEX):** Rp \[Nilai\]  
* **Proyeksi Penghematan/Pendapatan Tambahan:** Rp \[Nilai\]/tahun (Asumsi: NRW turun X%, harga air rata-rata Rp Y/m3).  
* **Payback Period:** \[Hitungan\] tahun.  
* **ROI 5 Tahun:** \[Hitungan\] %.

## **5\. Rekomendasi**

Berdasarkan analisis di atas, Manajemen TI merekomendasikan Direksi untuk menyetujui pelaksanaan Opsi C, karena menawarkan nilai pengembalian investasi terbaik dan solusi jangka panjang bagi permasalahan operasional perusahaan.

## ---

**4\. Checklist Audit NRW (Non-Revenue Water) Berbasis Standar IWA**

Kehilangan air (NRW) adalah musuh utama efisiensi utilitas air. Penanganannya membutuhkan pendekatan audit yang sistematis, bukan sekadar "tambal sulam" saat ada laporan bocor. Kerangka kerja audit ini didasarkan pada metodologi Neraca Air standar *International Water Association* (IWA) dan panduan teknis Kementerian PUPR, yang membedakan secara tegas antara Kehilangan Air Fisik (Bocoran) dan Kehilangan Air Komersial (Administratif).13

### **4.1 Persiapan Audit dan Validasi Data Dasar (Baseline)**

Langkah pertama audit bukanlah turun ke lapangan, melainkan memvalidasi data di atas meja. Kesalahan data dasar akan membuat seluruh perhitungan neraca air menjadi tidak valid.

* \[ \] **Validasi Master Meter (Produksi):** Apakah meter induk di instalasi produksi (IPA) berfungsi dan terkalibrasi? Kesalahan di sini mendistorsi angka "Input Sistem".  
* \[ \] **Validasi Peta Jaringan (GIS):** Ketersediaan *as-built drawing* digital yang memuat panjang pipa, diameter, jenis material, dan tahun pemasangan. Tanpa ini, analisis ILI (*Infrastructure Leakage Index*) tidak mungkin dilakukan akurat.  
* \[ \] **Data Pelanggan (DRD):** Pastikan jumlah sambungan aktif, pasif, dan disegel tercatat rapi. Data konsumsi air berekening adalah pengurang utama NRW.15  
* \[ \] **Pengukuran Tekanan Rata-rata:** Data tekanan sistem (AZP \- *Average Zone Pressure*) diperlukan untuk menentukan kewajaran tingkat kebocoran fisik.

### **4.2 Audit Kehilangan Air Komersial (Apparent Losses)**

Ini adalah "kehilangan kertas" yang disebabkan oleh ketidakakuratan pengukuran dan data. Penanganannya seringkali lebih murah (low cost) dengan dampak pemulihan pendapatan instan.13

#### **4.2.1 Ketidakakuratan Meter Air Pelanggan (Meter Inaccuracies)**

* \[ \] **Analisis Profil Umur Meter:** Buat histogram umur meter pelanggan. Berapa persen meter yang berusia \> 5 tahun? Meter tua cenderung lambat (*under-register*).  
* \[ \] **Uji Sampel Meter (Bench Test):** Ambil sampel acak (misal 50-100 meter) dari berbagai umur dan merek, uji di meja tera metrologi. Hitung rata-rata % *error*.  
* \[ \] **Kesesuaian Ukuran (Sizing):** Cek pelanggan niaga/industri. Apakah meter terlalu besar untuk debit pemakaian kecil? Meter *oversized* tidak akan mencatat aliran rendah (*low flow*) pada malam hari.  
* \[ \] **Instalasi Meter:** Cek posisi pasang. Meter mekanis yang dipasang miring atau terbalik akan menghasilkan angka yang salah.

#### **4.2.2 Kesalahan Penanganan Data (Data Handling Errors)**

* \[ \] **Audit Proses Baca Meter:** Lakukan *spot check* mendadak di lapangan untuk membandingkan angka stan meter riil dengan angka yang diinput petugas baca meter. Deteksi praktik "tembak meter" (mengira-ngira).  
* \[ \] **Sistem Estimasi:** Periksa sistem *billing*. Berapa persen pelanggan yang tagihannya "ditaksir" sistem karena rumah terkunci atau meter tertimbun? Taksiran yang terlalu rendah berulang-ulang adalah sumber NRW komersial.

#### **4.2.3 Konsumsi Tidak Resmi (Unauthorized Consumption)**

* \[ \] **Penyisiran Sambungan Ilegal:** Apakah ada tim khusus yang mencari sambungan liar (bypass meter, sambungan langsung pipa distribusi)?  
* \[ \] **Pencurian Air Internal:** Cek pemakaian air di kantor-kantor cabang PDAM atau rumah dinas pegawai. Apakah bermeter dan dicatat?  
* \[ \] **Pemakaian Hidran:** Apakah pengambilan air oleh Damkar atau Dinas Pertamanan dicatat volumenya (meskipun gratis, harus masuk kategori *Unbilled Authorized Consumption*, bukan NRW)?

### **4.3 Audit Kehilangan Air Fisik (Real Losses)**

Kehilangan air fisik adalah air yang benar-benar keluar dari sistem perpipaan dan tidak sampai ke pelanggan. Penanganannya memerlukan investasi teknis dan perbaikan infrastruktur.16

#### **4.3.1 Kebocoran pada Pipa Transmisi & Distribusi**

* \[ \] **Minimum Night Flow (MNF) Analysis:** Lakukan pengukuran aliran minimum malam hari (jam 02.00-04.00) di DMA. Rasio MNF yang tinggi terhadap aliran rata-rata harian mengindikasikan kebocoran fisik besar (karena konsumsi pelanggan di jam tersebut minim).  
* \[ \] **Step Test:** Penutupan katup (valve) secara bertahap di zona isolasi untuk mempersempit area pencarian titik bocor.  
* \[ \] **Survei Kebocoran Aktif (ALC):** Apakah tim teknik rutin menggunakan alat deteksi akustik (*ground microphone*, *leak noise correlator*) untuk mencari kebocoran yang tidak muncul ke permukaan (*hidden leaks*)?  
* \[ \] **Analisis Kualitas Pipa:** Review data historis pipa pecah (*burst frequency*). Identifikasi ruas jalan dengan frekuensi pecah tinggi untuk prioritas penggantian pipa (*pipe replacement*).

#### **4.3.2 Kebocoran pada Sambungan Rumah (SR)**

* \[ \] **Kualitas Asesoris:** Periksa kualitas *clamp saddle* dan *ferrule* di titik penyadapan (*tapping point*). Ini adalah titik terlemah jaringan.  
* \[ \] **Tekanan Berlebih:** Apakah tekanan di jaringan melebihi kebutuhan (misal \> 3 bar di area datar perumahan)? Tekanan berlebih memaksa air keluar lebih deras dari celah kebocoran kecil. Pertimbangkan pemasangan PRV (*Pressure Reducing Valve*).

#### **4.3.3 Kebocoran dan Luapan Reservoar**

* \[ \] **Overflow Check:** Periksa pipa peluap (*overflow pipe*) di reservoir. Apakah ada air tumpah akibat kerusakan katup pelampung (*ball valve*) atau kelalaian operator pompa mematikan mesin saat tangki penuh?  
* \[ \] **Uji Struktur:** Lakukan uji rembesan dinding reservoir (*drop test*) secara berkala.

### **4.4 Tabel Neraca Air (IWA Water Balance Table)**

Tabel berikut adalah standar wajib untuk pelaporan NRW. Manajer PDAM harus mampu mengisi setiap kotak dengan data yang valid (bukan asumsi).

| Input Sistem (System Input Volume) | Konsumsi Resmi (Authorized Consumption) | Konsumsi Resmi Berekening (Billed Authorized) | Pendapatan Air (Revenue Water) |
| :---- | :---- | :---- | :---- |
| **(A) Volume Produksi Sendiri** \+ **(B) Beli Air Curah** | **(C) Total Konsumsi Resmi** | (D) Billed Metered \+ (E) Billed Unmetered | **Volume Air Terjual** |
|  |  | Konsumsi Resmi Tak Berekening (Unbilled Authorized) | **NRW (Non-Revenue Water)** |
|  | **Kehilangan Air (Water Losses)** | (F) Unbilled Metered \+ (G) Unbilled Unmetered | **Komponen NRW (Non-Komersial)** |
|  | **(H) Total Kehilangan** | Kehilangan Air Komersial (Apparent Losses) | **NRW (Potensi Pendapatan Hilang)** |
|  | (A+B) \- C | (I) Konsumsi Ilegal \+ (J) Ketidakakuratan Meter | **Fokus Audit Komersial** |
|  |  | Kehilangan Air Fisik (Real Losses) | **NRW (Biaya Produksi Terbuang)** |
|  |  | (K) Kebocoran Pipa Utama \+ (L) Kebocoran Pipa Dinas \+ (M) Luapan Tangki | **Fokus Audit Fisik** |

* **Rumus NRW (%)** \= $\\frac{\\text{NRW Volume}}{\\text{Input Sistem}} \\times 100\\%$  
* **Target:** Mengetahui *breakdown* antara Kehilangan Fisik vs Komersial untuk menentukan prioritas penanganan. Jika Komersial tinggi \-\> Ganti Meter. Jika Fisik tinggi \-\> Perbaiki Pipa/Manajemen Tekanan.

## ---

**5\. Matriks Risiko TI dan OT (Integrated IT/OT Risk Management)**

Modernisasi PDAM membawa risiko baru: konvergensi antara jaringan Teknologi Informasi (TI \- data perusahaan) dan Teknologi Operasional (OT \- SCADA, pompa). Serangan siber pada PDAM bukan hanya soal pencurian data, tapi bisa berdampak pada kesehatan publik (misalnya: manipulasi dosis klorin) atau kelumpuhan suplai air. Kerangka kerja risiko ini menggunakan standar ISO 31000, NIST Cybersecurity Framework, dan diselaraskan dengan pedoman BSSN (Badan Siber dan Sandi Negara) melalui instrumen Indeks KAMI dan Manajemen Risiko SPBE.3

### **5.1 Metodologi Penilaian Risiko: Matriks 5x5**

Untuk mengukur risiko secara kuantitatif dan kualitatif, digunakan matriks 5x5 yang memetakan **Kemungkinan (Likelihood)** kejadian terhadap **Dampak (Impact)** yang ditimbulkan. Definisi level harus disepakati di awal agar penilaian konsisten.

Sumbu X: Kemungkinan (Likelihood) 29

1. **Rare (Sangat Jarang):** Kemungkinan terjadi \< 5% per tahun. Belum pernah terjadi dalam sejarah perusahaan.  
2. **Unlikely (Jarang):** Kemungkinan 5-20%. Pernah terjadi sekali dalam 5 tahun terakhir.  
3. **Possible (Mungkin):** Kemungkinan 21-50%. Terjadi sekali setahun.  
4. **Likely (Sering):** Kemungkinan 51-80%. Terjadi beberapa kali setahun (per kuartal).  
5. **Almost Certain (Hampir Pasti):** Kemungkinan \> 80%. Terjadi rutin (bulanan/mingguan) atau sedang terjadi saat ini.

Sumbu Y: Dampak (Impact/Severity) pada Konteks PDAM 9

1. **Insignificant:** Gangguan kecil pada sistem internal, tidak ada dampak layanan pelanggan, kerugian finansial \< 0.1% pendapatan.  
2. **Minor:** Gangguan layanan \< 4 jam, keluhan pelanggan \< 10, kerugian finansial kecil.  
3. **Moderate:** Gangguan layanan sebagian wilayah (zona tertentu), keluhan meningkat, sistem billing offline sementara, kerugian finansial sedang.  
4. **Major:** Gangguan layanan luas \> 24 jam, kerusakan aset SCADA/Pompa, pemberitaan media negatif, denda regulasi, data pelanggan bocor.  
5. **Catastrophic:** Lumpuhnya total suplai air \> 48 jam, kontaminasi kualitas air yang membahayakan nyawa, tuntutan hukum pidana, kebangkrutan/kerugian finansial masif.

### **5.2 Daftar Risiko Kunci dan Skenario Mitigasi (Risk Register)**

PDAM harus memiliki *Risk Register* yang hidup dan diperbarui berkala. Berikut adalah risiko-risiko prioritas tinggi yang wajib dikelola:

#### **5.2.1 Risiko Keamanan Siber (Cybersecurity Risks)**

* **Skenario 1: Ransomware pada Server Billing & Database Pelanggan.**  
  * *Analisis:* Hacker mengenkripsi data tagihan dan meminta tebusan.  
  * *Penilaian:* Likelihood (4) x Impact (4) \= **Extreme Risk**.  
  * *Mitigasi:* Implementasi strategi backup 3-2-1 (3 copy, 2 media berbeda, 1 offsite/cloud immutable). Segmentasi jaringan agar malware tidak menyebar. Edukasi anti-phishing untuk staf.32  
* **Skenario 2: Peretasan Sistem SCADA/PLC.**  
  * *Analisis:* Penyerang mengambil alih kontrol PLC (*Programmable Logic Controller*) untuk mematikan pompa atau mengubah set-point dosis kimia.  
  * *Penilaian:* Likelihood (2) x Impact (5) \= **High Risk**.  
  * *Mitigasi:* **Air Gap** (pemisahan fisik) jaringan SCADA dari internet publik. Jika butuh akses remote, gunakan VPN industri dengan MFA (*Multi-Factor Authentication*). Ganti password default pabrikan pada semua perangkat PLC.12

#### **5.2.2 Risiko Infrastruktur dan Keberlangsungan (Availability Risks)**

* **Skenario 3: Kegagalan Daya/Listrik pada Data Center.**  
  * *Analisis:* Mati listrik menyebabkan server mati mendadak, data korup, harddisk rusak.  
  * *Penilaian:* Likelihood (3) x Impact (4) \= **High Risk**.  
  * *Mitigasi:* UPS (*Uninterruptible Power Supply*) dengan kapasitas backup minimal 30 menit, Genset otomatis (ATS), dan replikasi data ke DRC (*Disaster Recovery Center*).32  
* **Skenario 4: Putusnya Koneksi Loket Pembayaran.**  
  * *Analisis:* Jaringan internet kantor cabang mati, pelanggan tidak bisa bayar, antrian menumpuk.  
  * *Penilaian:* Likelihood (4) x Impact (3) \= **High Risk**.  
  * *Mitigasi:* Redundansi koneksi (misal: Fiber Optic utama \+ Backup Modem 4G LTE/SD-WAN).

#### **5.2.3 Risiko Kepatuhan dan Tata Kelola (Compliance Risks)**

* **Skenario 5: Rendahnya Skor Indeks KAMI/SPBE.**  
  * *Analisis:* Kegagalan memenuhi standar keamanan informasi BSSN mengakibatkan teguran Pemda dan ketidakpercayaan publik.  
  * *Penilaian:* Likelihood (3) x Impact (3) \= **Medium Risk**.  
  * *Mitigasi:* Pembentukan tim CSIRT (*Computer Security Incident Response Team*), audit keamanan berkala, penyusunan dokumen kebijakan keamanan informasi.28

### **5.3 Templat Visual Matriks Risiko**

Tabel ini digunakan untuk memetakan posisi risiko setelah mitigasi (*Residual Risk*).

| Dampak \\ Kemungkinan | 1 (Rare) | 2 (Unlikely) | 3 (Possible) | 4 (Likely) | 5 (Almost Certain) |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **5 (Catastrophic)** | Medium | High | High | **Extreme** | **Extreme** |
| **4 (Major)** | Medium | Medium | High | **Extreme** | **Extreme** |
| **3 (Moderate)** | Low | Medium | Medium | High | High |
| **2 (Minor)** | Low | Low | Medium | Medium | Medium |
| **1 (Insignificant)** | Low | Low | Low | Low | Medium |

**Tindakan Manajerial:**

* **Extreme (Merah):** Tidak dapat ditoleransi. Wajib tindakan mitigasi segera (dalam 24 jam). Eskalasi ke Direksi Utama.  
* **High (Jingga):** Perlu perhatian serius. Rencana mitigasi harus ada dalam prioritas anggaran.  
* **Medium (Kuning):** Dikelola dengan prosedur rutin SOP.  
* **Low (Hijau):** Risiko diterima (*Accept*), monitor tahunan.

## ---

**6\. Rencana Kerja Strategis 100 Hari CIO Baru (The First 100 Days Roadmap)**

Posisi Kepala Bagian TI, Manajer Sistem Informasi, atau CIO (*Chief Information Officer*) di PDAM memiliki tantangan unik: menjembatani kesenjangan teknis warisan lama (*legacy systems*) dengan tuntutan modernisasi yang cepat, sambil menavigasi dinamika birokrasi BUMD. Rencana 100 hari ini dirancang dengan pendekatan "Diagnosa, Penyelarasan, dan Aksi Cepat" untuk membangun momentum dan kredibilitas.34

### **Fase 1: Diagnosa Mendalam & Membangun Relasi (Hari 1-30)**

**Tujuan:** Memahami kondisi lapangan yang sebenarnya ("The Real Truth"), bukan hanya laporan di atas meja. Jangan membuat keputusan besar atau perubahan drastis di fase ini.

* **Minggu 1: Stakeholder Listening Tour.**  
  * Bertemu Direksi: Pahami visi bisnis, keluhan utama (pain points), dan batasan anggaran.  
  * Bertemu Manajer Divisi Lain (Keuangan, Hublang, Teknik): Dengarkan keluhan mereka tentang TI. Apakah billing sering lambat? Apakah data teknik sulit diakses?  
  * Kunjungan Lapangan: Ikut petugas pembaca meter dan tim perbaikan pipa. Rasakan pengalaman pengguna (*User Experience*) aplikasi lapangan secara langsung.  
* **Minggu 2: Audit Aset dan Infrastruktur (IT Health Check).**  
  * Inventarisasi aset fisik (Server, PC, Network) dan non-fisik (Lisensi Software, Kontrak Vendor).  
  * Identifikasi "Shadow IT": Aplikasi atau database Excel yang dibuat sendiri oleh departemen lain karena ketidakpercayaan pada sistem pusat.  
  * Cek status keamanan: Kapan backup terakhir yang *berhasil* dipulihkan? Apakah antivirus terupdate?  
* **Minggu 3-4: Penilaian Kapabilitas Tim & Budaya.**  
  * Evaluasi kompetensi staf TI (Skill Matrix). Apakah tim didominasi tenaga support/teknisi hardware, atau ada kemampuan analitik/development?  
  * Identifikasi budaya kerja: Apakah proaktif atau reaktif "pemadam kebakaran"?

**Luaran (Deliverable) Hari 30:** Laporan "State of IT" yang jujur, memuat pemetaan aset, risiko kritis, dan celah kapabilitas SDM.

### **Fase 2: Identifikasi "Quick Wins" & Penyelarasan Strategi (Hari 31-60)**

**Tujuan:** Memberikan bukti nyata perbaikan untuk membangun kepercayaan (*Trust Building*) dan mulai menyusun rencana jangka panjang.

* **Minggu 5: Eksekusi "Quick Wins" (Kemenangan Cepat).**  
  * Pilih 2-3 masalah yang mengganggu tapi mudah diperbaiki (*Low Effort, High Impact*).  
  * *Contoh:* Memperbaiki koneksi Wi-Fi yang tidak stabil di area pelayanan, mengotomatisasi satu laporan harian yang memakan waktu, atau membersihkan malware di komputer front-office. Keberhasilan kecil ini penting untuk moral tim dan kepercayaan user.  
* **Minggu 6: Penyelarasan dengan Indikator Kinerja.**  
  * Analisis bagaimana TI dapat membantu pencapaian 18 indikator BPPSPAM.  
  * *Tindakan:* Prioritaskan perbaikan data untuk indikator yang "merah" atau "kuning" (misal: Efektivitas Penagihan atau NRW).  
* **Minggu 7-8: Penyusunan Business Case Prioritas.**  
  * Mulai susun proposal investasi (lihat Bagian 3\) untuk proyek strategis yang akan diajukan di RKAP tahun depan. Fokus pada proyek yang punya ROI jelas.  
  * Sosialisasi rencana ini secara informal ke bagian Keuangan untuk mendapatkan masukan awal (*Pre-alignment*).

**Luaran (Deliverable) Hari 60:** Realisasi *Quick Wins* yang dipublikasikan internal, dan Draft Awal *IT Master Plan*.

### **Fase 3: Perencanaan Jangka Panjang & Pelembagaan (Hari 61-90)**

**Tujuan:** Menetapkan arah strategis dan struktur tata kelola yang permanen.

* **Minggu 9-10: Finalisasi IT Master Plan / Peta Rencana SPBE.**  
  * Menyusun peta jalan 3-5 tahun yang mencakup modernisasi ERP, implementasi Smart Water Grid, dan integrasi GIS-SCADA.  
  * Peta jalan ini harus selaras dengan masa jabatan Direksi dan rencana pembangunan daerah.  
* **Minggu 11: Reformasi Tata Kelola (Governance).**  
  * Mengusulkan pembentukan Komite Pengarah TI (*IT Steering Committee*) yang diketuai Direktur Utama, untuk memutuskan prioritas proyek TI secara kolektif (menghindari TI jalan sendiri).  
  * Memperbarui SOP TI: Manajemen Insiden, Manajemen Akses User, dan Prosedur Backup.  
* **Minggu 12: Pengajuan Anggaran.**  
  * Finalisasi angka anggaran CAPEX dan OPEX untuk tahun depan berdasarkan Business Case yang kuat.

**Luaran (Deliverable) Hari 90:** Dokumen *IT Master Plan*, SOP TI Baru, dan Proposal Anggaran Definitif.

### **Fase 4: Peluncuran & Momentum (Hari 91-100)**

**Tujuan:** Memulai eksekusi dan mengkomunikasikan visi masa depan.

* **Hari 91-100: Townhall & Kick-off.**  
  * Presentasi visi transformasi digital kepada seluruh pegawai PDAM. Gunakan bahasa yang inspiratif namun membumi.  
  * Peluncuran resmi proyek strategis pertama.  
  * Menetapkan Key Performance Indicators (KPI) baru untuk tim TI yang berbasis layanan (*Service Level Agreement*).

Kunci Sukses CIO PDAM:  
Keberhasilan CIO di BUMD air minum tidak diukur dari seberapa canggih teknologi yang dibeli, melainkan dari seberapa besar kontribusi teknologi tersebut dalam menurunkan NRW, meningkatkan pendapatan, dan memperbaiki layanan kepada masyarakat. CIO harus bertindak sebagai Business Partner bagi Direksi, bukan sekadar "Orang IT".36

## ---

**7\. Penutup: Mengintegrasikan Framework ke dalam Aksi**

Dokumen FRAMEWORKS.md ini menyajikan serangkaian alat kerja yang saling terkait. Asesmen Kematangan Digital (Bagian 2\) memberikan peta posisi awal. Business Case (Bagian 3\) menyediakan bahan bakar investasi untuk bergerak maju. Audit NRW (Bagian 4\) memastikan operasional dasar efisien. Matriks Risiko (Bagian 5\) menjadi sabuk pengaman selama perjalanan. Dan Rencana 100 Hari CIO (Bagian 6\) adalah kemudi bagi pemimpin transformasi.

Implementasi kerangka kerja ini membutuhkan ketekunan, konsistensi, dan keberanian untuk mengubah *status quo*. Bagi manajemen PDAM, tantangannya bukan pada ketiadaan teknologi, melainkan pada kemampuan manajemen perubahan (*change management*) untuk mengadopsi cara kerja baru. Dengan berpedoman pada kerangka kerja ini, PDAM dapat melangkah pasti menuju visi perusahaan air minum yang modern, mandiri, dan berkinerja unggul.

#### **Works cited**

1. The Measuring the Efficiency and Productivity of Regional Water Utility Company (PDAM) in Indonesia from 2012 to 2016 \- ResearchGate, accessed December 21, 2025, [https://www.researchgate.net/publication/360714644\_The\_Measuring\_the\_Efficiency\_and\_Productivity\_of\_Regional\_Water\_Utility\_Company\_PDAM\_in\_Indonesia\_from\_2012\_to\_2016](https://www.researchgate.net/publication/360714644_The_Measuring_the_Efficiency_and_Productivity_of_Regional_Water_Utility_Company_PDAM_in_Indonesia_from_2012_to_2016)  
2. Buku Kinerja BUMD Air Minum 2023 \- PERPAMSI, accessed December 21, 2025, [https://www.perpamsi.or.id/storage/assets/upload/3m4pBwREtq7nSEIsaguDMgwnROX5h7pwqOuw7HD2.pdf](https://www.perpamsi.or.id/storage/assets/upload/3m4pBwREtq7nSEIsaguDMgwnROX5h7pwqOuw7HD2.pdf)  
3. ewlsCL4w\_13-35.-PEDOMAN-TEKNIS-MANAJEMEN-RISIKO-SPBE-KEMENTAN.pdf, accessed December 21, 2025, [https://itjen.pertanian.go.id/storage/master/file/ewlsCL4w\_13-35.-PEDOMAN-TEKNIS-MANAJEMEN-RISIKO-SPBE-KEMENTAN.pdf](https://itjen.pertanian.go.id/storage/master/file/ewlsCL4w_13-35.-PEDOMAN-TEKNIS-MANAJEMEN-RISIKO-SPBE-KEMENTAN.pdf)  
4. Kinerja BUMD Air Minum \- Open Data PU, accessed December 21, 2025, [https://data.pu.go.id/dataset/kinerja-bumd-air-minum](https://data.pu.go.id/dataset/kinerja-bumd-air-minum)  
5. Definition, Framework, and Maturity Assessment for Intelligent Water Systems, accessed December 21, 2025, [https://www.waterrf.org/research/projects/definition-framework-and-maturity-assessment-intelligent-water-systems](https://www.waterrf.org/research/projects/definition-framework-and-maturity-assessment-intelligent-water-systems)  
6. (PDF) Digital Survey for Customer Satisfaction of Regional Drinking Water Companies (PDAM) using the mWater Application and the Slovin Formula Method \- ResearchGate, accessed December 21, 2025, [https://www.researchgate.net/publication/386107382\_Digital\_Survey\_for\_Customer\_Satisfaction\_of\_Regional\_Drinking\_Water\_Companies\_PDAM\_using\_the\_mWater\_Application\_and\_the\_Slovin\_Formula\_Method](https://www.researchgate.net/publication/386107382_Digital_Survey_for_Customer_Satisfaction_of_Regional_Drinking_Water_Companies_PDAM_using_the_mWater_Application_and_the_Slovin_Formula_Method)  
7. Nomor 002/KPTS/K-6/IV/2010 \- PDAM Kabupaten Pacitan, accessed December 21, 2025, [https://pdampacitan.co.id/berkas/produk\_hukum/PH-210906-101348\_0.docx](https://pdampacitan.co.id/berkas/produk_hukum/PH-210906-101348_0.docx)  
8. Rencana Strategis BP BUMD Provinsi DKI Jakarta Tahun 2023-2026, accessed December 21, 2025, [https://bpbumd.jakarta.go.id/dok/RenstraBPBUMDTahun2023-2026.pdf](https://bpbumd.jakarta.go.id/dok/RenstraBPBUMDTahun2023-2026.pdf)  
9. MATERI PEMANTAUAN DAN EVALUASI SPBE, accessed December 21, 2025, [https://wiki.jogjaprov.go.id/diskominfo/sosialiasi\_spbe\_2024/bag3modulmanajemenspbe2024.pdf](https://wiki.jogjaprov.go.id/diskominfo/sosialiasi_spbe_2024/bag3modulmanajemenspbe2024.pdf)  
10. Upaya Peningkatan Kinerja Pdam Berdasarkan Jalur Hubungan Sebab-Akibat Indikator Kinerja \- FTSL, accessed December 21, 2025, [https://ftsl.itb.ac.id/wp-content/uploads/sites/8/2019/09/6.-INNA-RUBHASY.pdf](https://ftsl.itb.ac.id/wp-content/uploads/sites/8/2019/09/6.-INNA-RUBHASY.pdf)  
11. Water utilities' experiences with mWater in Indonesia, accessed December 21, 2025, [https://www.mwater.co/blog/water-utilities-experiences-with-mwater-in-indonesia](https://www.mwater.co/blog/water-utilities-experiences-with-mwater-in-indonesia)  
12. Cyber Threats to Water and Wastewater Sector | TXOne Networks, accessed December 21, 2025, [https://www.txone.com/blog/cyber-threats-to-water-and-wastewater-sector/](https://www.txone.com/blog/cyber-threats-to-water-and-wastewater-sector/)  
13. Penerapan Jaringan Distribusi Sistem District Meter Area (DMA) SPAM Semarang Barat dalam Optimalisasi Penurunan Kehilangan Air D \- undip e-journal system, accessed December 21, 2025, [https://ejournal.undip.ac.id/index.php/ilmulingkungan/article/download/45773/pdf](https://ejournal.undip.ac.id/index.php/ilmulingkungan/article/download/45773/pdf)  
14. Studi Tingkat Kehilangan Air Minum Perumda Air Minum Tirta Moedal Kota Semarang Dengan Neraca Air Wb-Easycalc dan \- Jurnal Serambi Engineering, accessed December 21, 2025, [https://jse.serambimekkah.id/index.php/jse/article/download/540/419/1023](https://jse.serambimekkah.id/index.php/jse/article/download/540/419/1023)  
15. Analisis Air Tak Berekening (Non Revenue Water) Menggunakan Metode Neraca Air di Perumda Air Minum Tirta Giri Nata Kota Cirebon, accessed December 21, 2025, [https://jse.serambimekkah.id/index.php/jse/article/download/1125/816/2535](https://jse.serambimekkah.id/index.php/jse/article/download/1125/816/2535)  
16. Studi Kehilangan Air PDAM Tirta Bukae Luwu Utara (Studi Kasus Kec. Masamba) Tahun 2017 \- Neliti, accessed December 21, 2025, [https://media.neliti.com/media/publications/315808-studi-kehilangan-air-pdam-tirta-bukae-lu-96ec7708.pdf](https://media.neliti.com/media/publications/315808-studi-kehilangan-air-pdam-tirta-bukae-lu-96ec7708.pdf)  
17. Indeks Keamanan Informasi (KAMI) Versi 5.0 \- digitama \- MySPBE, accessed December 21, 2025, [https://www.myspbe.id/training/indeks-keamanan-informasi-kami-versi-50-pykqyBOory](https://www.myspbe.id/training/indeks-keamanan-informasi-kami-versi-50-pykqyBOory)  
18. VAL IT: KERANGKA KERJA EVALUASI INVESTASI TEKNOLOGI INFORMASI \- Journal UII, accessed December 21, 2025, [https://journal.uii.ac.id/index.php/Snati/article/download/1715/1496](https://journal.uii.ac.id/index.php/Snati/article/download/1715/1496)  
19. Project Development Routemap untuk Proyek Infrastruktur: Handbook untuk Indonesia \- Perpustakaan Digital Kementerian PPN/Bappenas, accessed December 21, 2025, [https://perpustakaan.bappenas.go.id/e-library/file\_upload/koleksi/dokumenbappenas/konten/Upload%20Terbaru/Project%20Development%20Routemap%20untuk%20Proyek%20Infrastruktur%20untuk%20Indonesia%20-%20Modul%20(versi%20Bahasa)%20(2).pdf](https://perpustakaan.bappenas.go.id/e-library/file_upload/koleksi/dokumenbappenas/konten/Upload%20Terbaru/Project%20Development%20Routemap%20untuk%20Proyek%20Infrastruktur%20untuk%20Indonesia%20-%20Modul%20\(versi%20Bahasa\)%20\(2\).pdf)  
20. TEMPLATE PENYUSUNAN DOKUMEN OUTLINE BUSINESS CASE \- KPBU, accessed December 21, 2025, [https://kpbu.kemenkeu.go.id/backend/Upload/guideline/GUIDELINE22110708102554.pdf](https://kpbu.kemenkeu.go.id/backend/Upload/guideline/GUIDELINE22110708102554.pdf)  
21. Contoh Proposal Bisnis yang Benar untuk Investor \- Brother Indonesia, accessed December 21, 2025, [https://www.brother.co.id/id-id/blog/contoh-proposal-bisnis-yang-benar-untuk-investor](https://www.brother.co.id/id-id/blog/contoh-proposal-bisnis-yang-benar-untuk-investor)  
22. Panduan Menulis Kasus Bisnis Efektif Untuk Pemula \[2025\] \- Asana, accessed December 21, 2025, [https://asana.com/id/resources/business-case](https://asana.com/id/resources/business-case)  
23. Cara Membuat Kasus Bisnis (Panduan & Contoh) \- Canva, accessed December 21, 2025, [https://www.canva.com/id\_id/docs/kasus-bisnis/](https://www.canva.com/id_id/docs/kasus-bisnis/)  
24. Mitigasi Non Revenue Water (NRW) Sistem Jaringan Distribusi pada District Meter Area (DMA) Zona Kota Blahbatuh PDAM Gianyar \- undip e-journal system, accessed December 21, 2025, [https://ejournal.undip.ac.id/index.php/mkts/article/download/23619/16532](https://ejournal.undip.ac.id/index.php/mkts/article/download/23619/16532)  
25. PEDOMAN, accessed December 21, 2025, [https://pdamciamis.co.id/uploads/ebuku/Pedoman\_Kehilangan\_Air\_-\_Kementrian\_PU.pdf](https://pdamciamis.co.id/uploads/ebuku/Pedoman_Kehilangan_Air_-_Kementrian_PU.pdf)  
26. 50 Bab III Metodologi Penelitian Tahapan dalam penelitian ini dapat dilihat pada Gambar III. 1 ini. Gambar III. 1\. Alur peneliti \- Digilib ITB, accessed December 21, 2025, [https://digilib.itb.ac.id/assets/files/disk1/697/jbptitbpp-gdl-imanullahi-34839-4-2015ts-3.pdf](https://digilib.itb.ac.id/assets/files/disk1/697/jbptitbpp-gdl-imanullahi-34839-4-2015ts-3.pdf)  
27. A Risk Assessment Model for Cyber-Physical Water and Wastewater Systems: Towards Sustainable Development \- MDPI, accessed December 21, 2025, [https://www.mdpi.com/2071-1050/14/8/4480](https://www.mdpi.com/2071-1050/14/8/4480)

---

## RIWAYAT REVISI

| Versi | Tanggal | Perubahan | Penulis |
|-------|---------|-----------|---------|
| 1.0 | 2025-12-22 | Konsolidasi final dengan metadata standar. Update header & footer sesuai struktur knowledge base terpadu. | FD Iskandar |

---

**Catatan:** Dokumen ini adalah bagian dari Knowledge Base FD Iskandar untuk konfigurasi AI.  
**Untuk informasi lebih lanjut:** https://rinji.id

---

**END OF DOCUMENT**
28. BSSN Beri Kemendikburistek Predikat Baik dalam Verifikasi Indeks KAMI 2022, accessed December 21, 2025, [https://csirt.unesa.ac.id/post/bssn-beri-kemendikburistek-predikat-baik-dalam-verifikasi-indeks-kami-2022](https://csirt.unesa.ac.id/post/bssn-beri-kemendikburistek-predikat-baik-dalam-verifikasi-indeks-kami-2022)  
29. What is a 5x5 Risk Matrix & How to Use it? | SafetyCulture, accessed December 21, 2025, [https://safetyculture.com/topics/risk-assessment/5x5-risk-matrix](https://safetyculture.com/topics/risk-assessment/5x5-risk-matrix)  
30. WSP manual supplementary tool Module 4: examples of risk assessment matrices \- Water Safety Portal |, accessed December 21, 2025, [https://wsportal.org/wp-content/uploads/2023/02/Module-4-supplementary-tool-examples-of-risk-assessment-matrices-1.pdf](https://wsportal.org/wp-content/uploads/2023/02/Module-4-supplementary-tool-examples-of-risk-assessment-matrices-1.pdf)  
31. Guidance for Small Community Water Systems on Risk and Resilience Assessments under AWIA \- Crestline Village Water District, accessed December 21, 2025, [https://www.cvwater.com/files/d76e61a31/CVWD+-+AWIA+Checklist+DRAFT.pdf](https://www.cvwater.com/files/d76e61a31/CVWD+-+AWIA+Checklist+DRAFT.pdf)  
32. Advanced SCADA Cybersecurity for Water Utility Personnel \- PNWS-AWWA, accessed December 21, 2025, [https://www.pnws-awwa.org/wp-content/uploads/2022/05/Advanced-SCADA-Cybersecurity-for-Water-Utility-Personnel.pdf](https://www.pnws-awwa.org/wp-content/uploads/2022/05/Advanced-SCADA-Cybersecurity-for-Water-Utility-Personnel.pdf)  
33. Dampak Indeks KAMI 5.0 terhadap Maturitas Keamanan Informasi di Daerah, accessed December 21, 2025, [https://digitama.consulting/dampak-indeks-kami-5-0-terhadap-maturitas-keamanan-informasi-di-daerah/](https://digitama.consulting/dampak-indeks-kami-5-0-terhadap-maturitas-keamanan-informasi-di-daerah/)  
34. FIVE PRIORITIES FOR A CIO'S FIRST 100 DAYS \- Eficio, accessed December 21, 2025, [https://eficio.ca/en/blog/five-priorities-for-a-cios-first-100-days/](https://eficio.ca/en/blog/five-priorities-for-a-cios-first-100-days/)  
35. CIO 100 Day Action Plan \[2025\] \- DigitalDefynd, accessed December 21, 2025, [https://digitaldefynd.com/IQ/cio-action-plan/](https://digitaldefynd.com/IQ/cio-action-plan/)  
36. Your first 100 days: A playbook for building credibility fast \- CIO, accessed December 21, 2025, [https://www.cio.com/article/4033687/your-first-100-days-a-playbook-for-building-credibility-fast.html](https://www.cio.com/article/4033687/your-first-100-days-a-playbook-for-building-credibility-fast.html)