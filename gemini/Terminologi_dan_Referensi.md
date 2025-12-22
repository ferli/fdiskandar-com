# TERMINOLOGI DAN REFERENSI
## Knowledge Base AI - Transformasi Digital Utilitas Air Indonesia

**Versi:** 1.0  
**Tanggal:** 22 Desember 2025  
**Penulis:** FD Iskandar  
**Status:** Final  
**Tujuan:** Kamus istilah bilingual dan referensi regulasi untuk standardisasi komunikasi AI

---

## DAFTAR ISI

1. [Kamus Istilah Bilingual (EN ↔ ID)](#kamus-istilah-bilingual)
2. [Akronim dan Singkatan](#akronim-dan-singkatan)
3. [Referensi Regulasi Indonesia](#referensi-regulasi-indonesia)
4. [Standar Teknis Internasional](#standar-teknis-internasional)
5. [Metrik dan Benchmark](#metrik-dan-benchmark)

---

## KAMUS ISTILAH BILINGUAL

### Domain 1: Transformasi Digital & SPBE

| Istilah EN | Istilah ID | Definisi & Konteks |
|-----------|-----------|-------------------|
| **Digital Transformation** | **Transformasi Digital** | Perubahan fundamental proses bisnis PDAM menggunakan teknologi digital untuk meningkatkan efisiensi, transparansi, dan kualitas layanan. Mencakup digitalisasi baca meter, sistem billing otomatis, SCADA, dan customer service berbasis aplikasi. |
| **Digital Twin** | **Kembar Digital** | Replika virtual dinamis dari seluruh jaringan distribusi fisik (pipa, pompa, reservoir) yang mengintegrasikan data statis (peta aset) dengan data real-time (tekanan, aliran) dari sensor IoT untuk simulasi prediktif dan deteksi kebocoran presisi. |
| **Smart Water Metering (SWM)** | **Pencatatan Meter Pintar** | Sistem pembacaan meter air otomatis menggunakan teknologi IoT (biasanya LoRaWAN di Indonesia) yang mengirimkan data pemakaian air pelanggan secara real-time ke server PDAM, mengeliminasi kesalahan pencatatan manual dan memungkinkan deteksi dini kebocoran pelanggan. |
| **LoRaWAN** | **LoRaWAN** | Long Range Wide Area Network - teknologi komunikasi nirkabel jarak jauh dengan konsumsi daya sangat rendah yang beroperasi pada frekuensi AS923 (920-923 MHz) di Indonesia. Standar de-facto untuk konektivitas smart water meter dengan jangkauan 2-15 km dan daya tahan baterai 10-16 tahun. |
| **SCADA System** | **Sistem SCADA** | Supervisory Control and Data Acquisition - sistem untuk monitoring dan kontrol infrastruktur kritis (IPA, reservoir, pompa) secara real-time dari pusat kontrol. Komponen: sensor (PLC), HMI (antarmuka operator), server, dan jaringan komunikasi (RTU/telemetri). |
| **Enterprise Resource Planning (ERP)** | **Sistem Perencanaan Sumber Daya Perusahaan** | Sistem terintegrasi yang menghubungkan seluruh fungsi bisnis PDAM (keuangan, SDM, pengadaan, aset, billing, customer service) dalam satu database terpusat untuk eliminasi silo data dan otomatisasi proses bisnis. |
| **Customer Relationship Management (CRM)** | **Manajemen Hubungan Pelanggan** | Platform digital untuk mengelola interaksi dengan pelanggan mulai dari pendaftaran, pengaduan, survei kepuasan hingga analisis pola konsumsi. Terintegrasi dengan sistem Work Order untuk tracking penyelesaian komplain. |
| **Geographic Information System (GIS)** | **Sistem Informasi Geografis** | Platform pemetaan digital aset PDAM (pipa, valve, hydrant, meter) dengan atribut teknis lengkap (jenis, diameter, umur, material) dan koordinat GPS akurat. Essential untuk perencanaan ekspansi, deteksi kebocoran, dan manajemen pemeliharaan. |
| **Internet of Things (IoT)** | **Internet untuk Segala** | Ekosistem sensor dan perangkat terhubung yang mengumpulkan data operasional (tekanan, debit, kualitas air, level tangki) dan mengirimkannya ke cloud/server untuk analisis real-time dan pengambilan keputusan otomatis. |
| **Cloud Computing** | **Komputasi Awan** | Model penyediaan infrastruktur IT (server, storage, aplikasi) sebagai layanan berbasis internet (IaaS, PaaS, SaaS). Untuk PDAM: mengurangi CAPEX infrastruktur, skalabilitas elastis, dan disaster recovery. Contoh: Microsoft Azure, AWS, Google Cloud. |
| **Big Data Analytics** | **Analitik Data Besar** | Teknik analisis dataset masif (jutaan transaksi billing, data sensor per detik) untuk mengidentifikasi pola tersembunyi (anomali pemakaian = kebocoran pelanggan, prediksi kebutuhan air masa depan) menggunakan algoritma statistik dan machine learning. |
| **Business Intelligence (BI)** | **Kecerdasan Bisnis** | Platform dashboard interaktif yang memvisualisasikan metrik kinerja perusahaan (NRW, collection rate, revenue, OPEX) secara real-time untuk mendukung pengambilan keputusan manajemen berbasis data. Contoh tools: Power BI, Tableau. |
| **Artificial Intelligence (AI)** | **Kecerdasan Buatan** | Algoritma pembelajaran mesin untuk prediksi (forecast demand air, prediksi kerusakan pompa), optimalisasi (scheduling pompa efisien energi, routing petugas lapangan), dan automasi (chatbot customer service, validasi foto meter). |
| **Machine Learning (ML)** | **Pembelajaran Mesin** | Subset AI yang menggunakan model statistik untuk "belajar" dari data historis tanpa pemrograman eksplisit. Aplikasi PDAM: prediksi kebocoran pipa berdasarkan umur/material/tekanan, segmentasi pelanggan untuk tariff optimization. |
| **Robotic Process Automation (RPA)** | **Automasi Proses Robotik** | Software bot yang mengotomatisasi tugas repetitif berbasis aturan (entry data, rekonsiliasi bank, generate laporan bulanan) untuk meningkatkan efisiensi staf back-office dan mengurangi human error. |
| **API (Application Programming Interface)** | **Antarmuka Pemrograman Aplikasi** | Protokol yang memungkinkan sistem berbeda saling berkomunikasi dan bertukar data. Contoh: Integrasi sistem billing PDAM dengan payment gateway (GoPay, OVO) atau dengan sistem BPJS untuk validasi kepesertaan pelanggan. |

### Domain 2: Tata Kelola, Risiko & Kepatuhan (GRC)

| Istilah EN | Istilah ID | Definisi & Konteks |
|-----------|-----------|-------------------|
| **Governance, Risk & Compliance (GRC)** | **Tata Kelola, Risiko & Kepatuhan** | Kerangka kerja terintegrasi untuk memastikan perusahaan dikelola sesuai prinsip GCG, risiko diidentifikasi dan dimitigasi, serta seluruh operasi mematuhi regulasi yang berlaku (UU, Permendagri, Perpres). |
| **Good Corporate Governance (GCG)** | **Tata Kelola Perusahaan yang Baik** | Prinsip pengelolaan perusahaan yang transparan, akuntabel, bertanggung jawab, independen, dan adil. Untuk BUMD: diwujudkan melalui struktur organ yang jelas (KPM, Dewan Pengawas, Direksi), SOP terstandar, dan audit rutin. |
| **COBIT (Control Objectives for Information and Related Technology)** | **COBIT** | Framework tata kelola IT global yang menyediakan best practices untuk alignment IT dengan tujuan bisnis, manajemen risiko IT, dan pengukuran kinerja IT. COBIT 2019 menggunakan pendekatan berbasis tujuan dengan 40 governance and management objectives. |
| **ISO 27001** | **ISO 27001** | Standar internasional untuk Information Security Management System (ISMS). Untuk PDAM: mengatur keamanan data pelanggan, proteksi sistem SCADA dari cyber attack, business continuity planning. Sertifikasi ISO 27001 meningkatkan kepercayaan stakeholder. |
| **ISO 31000** | **ISO 31000** | Standar internasional untuk Enterprise Risk Management. Menyediakan framework sistematis untuk identifikasi, analisis, evaluasi, treatment, dan monitoring risiko (finansial, operasional, reputasi, regulasi, cyber). |
| **Internal Control** | **Pengendalian Internal** | Prosedur dan mekanisme yang dirancang untuk memastikan integritas informasi keuangan, kepatuhan hukum, dan efektivitas operasi. Contoh: segregation of duties (pemisahan fungsi approve dan execute payment), dual authorization, audit trail. |
| **Audit Trail** | **Jejak Audit** | Log digital yang merekam siapa, kapan, dan apa yang dilakukan dalam sistem (login, ubah data, approve transaksi). Crucial untuk forensik investigasi fraud dan compliance PDP (data access tracking). |
| **Segregation of Duties (SoD)** | **Pemisahan Tugas** | Prinsip pengendalian internal yang memastikan tidak ada satu orang yang mengendalikan seluruh proses transaksi kritis (contoh: orang yang approve purchase order ≠ orang yang receive barang ≠ orang yang process payment). |
| **Fiduciary Duty** | **Kewajiban Fidusia** | Tanggung jawab hukum Direksi untuk bertindak dengan itikad baik, penuh kehati-hatian, dan untuk kepentingan perusahaan (bukan kepentingan pribadi). Diatur dalam Permendagri 23/2024: Direksi bertanggung jawab pribadi atas kerugian akibat kesalahan/kelalaian. |
| **Due Diligence** | **Uji Tuntas** | Investigasi menyeluruh terhadap vendor/partner sebelum kontrak (verifikasi legalitas, kapabilitas teknis, kesehatan finansial, track record). Untuk PDAM: wajib dilakukan saat procurement sistem IT besar atau kemitraan investasi infrastruktur. |
| **Compliance Framework** | **Kerangka Kepatuhan** | Sistem kebijakan, prosedur, dan kontrol untuk memastikan organisasi mematuhi seluruh regulasi yang berlaku. Untuk PDAM Indonesia: UU 17/2019 (SDA), UU 27/2022 (PDP), Permendagri 23/2024, Perpres 95/2018 (SPBE), dll. |
| **Data Protection Impact Assessment (DPIA)** | **Penilaian Dampak Perlindungan Data** | Analisis sistematis yang diwajibkan UU PDP untuk pemrosesan data pribadi yang berisiko tinggi (profiling pelanggan, geo-tracking). DPIA menilai risiko kebocoran data dan menentukan mitigasi yang diperlukan. |
| **Data Protection Officer (DPO)** | **Pejabat Pelindungan Data Pribadi** | Posisi yang diwajibkan UU PDP untuk organisasi yang memproses data dalam skala besar. DPO bertanggung jawab untuk monitoring kepatuhan UU PDP, edukasi internal, dan menjadi contact point untuk subjek data dan regulator. |

### Domain 3: Operasi Teknis Utilitas Air

| Istilah EN | Istilah ID | Definisi & Konteks |
|-----------|-----------|-------------------|
| **Water Supply System (SPAM)** | **Sistem Penyediaan Air Minum** | Kesatuan sarana dan prasarana penyediaan air minum. Komponen: Unit Air Baku (intake), Unit Produksi (IPA), Unit Distribusi (pipa transmisi & distribusi), Unit Pelayanan (meter & billing). |
| **Raw Water** | **Air Baku** | Air dari sumber alam (sungai, danau, mata air, air tanah) yang belum diolah. Kualitasnya menentukan kompleksitas IPA. Sumber terbaik: mata air pegunungan (minimal treatment). Terburuk: sungai perkotaan tercemar (perlu advanced treatment). |
| **Water Treatment Plant (WTP)** | **Instalasi Pengolahan Air (IPA)** | Fasilitas untuk mengubah air baku menjadi air minum yang memenuhi standar Permenkes 492/2010. Proses tipikal: koagulasi-flokulasi-sedimentasi-filtrasi-desinfeksi. Kapasitas diukur dalam liter/detik atau m³/hari. |
| **Total Dynamic Head (TDH)** | **Total Head Dinamis** | Total energi (dalam meter) yang harus disediakan pompa untuk mengatasi: (1) Static Head (beda tinggi), (2) Friction Loss (gesekan pipa), (3) Pressure Head (tekanan sisa yang dibutuhkan). TDH = titik kerja pompa pada kurva karakteristik. |
| **Cavitation** | **Kavitasi** | Fenomena pembentukan dan pecahnya gelembung uap di dalam impeller pompa akibat tekanan lokal turun di bawah tekanan uap jenuh air. Menyebabkan erosi logam, noise, dan penurunan efisiensi pompa. Dicegah dengan memastikan NPSHa > NPSHr. |
| **Net Positive Suction Head (NPSH)** | **Tinggi Tekan Hisap Positif Neto** | Parameter kritis untuk mencegah kavitasi. NPSHa (available) = tekanan tersedia di sisi hisap pompa (ditentukan desain sistem). NPSHr (required) = tekanan minimum yang dibutuhkan pompa (spesifikasi pabrikan). Syarat operasi aman: NPSHa > NPSHr + margin. |
| **Variable Speed Drive (VSD)** | **Penggerak Kecepatan Variabel** | Inverter elektronik yang mengatur kecepatan motor pompa sesuai demand secara real-time. Manfaat: hemat energi 20-50% (hukum kubik: power ∝ speed³), mengurangi water hammer, memperpanjang umur pompa. |
| **Pressure Reducing Valve (PRV)** | **Katup Penurun Tekanan** | Valve otomatis yang menurunkan tekanan air di zona tertentu untuk mengurangi tekanan berlebih yang menyebabkan kebocoran pipa (pressure management). Crucial untuk DMA (District Meter Area) dalam strategi penurunan NRW. |
| **Reservoir** | **Reservoir / Bak Penampung** | Tangki penyimpanan air (elevated tower atau ground tank) yang berfungsi sebagai buffer untuk menyeimbangkan produksi dengan konsumsi fluktuatif harian (peak morning & evening demand). Kapasitas ideal: 20-30% produksi harian. |
| **Transmission Main** | **Pipa Transmisi** | Pipa diameter besar yang mengangkut air dari sumber ke IPA atau dari IPA ke reservoir utama tanpa sambungan pelanggan langsung. Biasanya diameter > 400mm, material ductile iron atau steel. |
| **Distribution Network** | **Jaringan Distribusi** | Sistem pipa yang melayani pelanggan langsung. Tipe: Branch system (cabang/radial) atau Loop system (tertutup). Loop system lebih reliable (air mengalir dari 2 arah), tapi lebih kompleks hidrolis dan mahal. |
| **District Meter Area (DMA)** | **Zona Meteran Distrik** | Zona geografis kecil (1.000-3.000 pelanggan) dalam jaringan distribusi yang diisolasi secara hidrolis dengan 1-2 inlet saja yang dipasangi master meter akurat. DMA adalah fondasi manajemen NRW modern untuk mempersempit lokasi kebocoran. |
| **Water Balance** | **Neraca Air** | Perhitungan akuntansi air yang membandingkan System Input (air masuk jaringan) dengan Authorized Consumption (konsumsi resmi). Selisihnya adalah NRW. Komponen NRW: kehilangan fisik (kebocoran) + kehilangan komersial (pencurian, meter inakurat). |

### Domain 4: Non-Revenue Water (NRW)

| Istilah EN | Istilah ID | Definisi & Konteks |
|-----------|-----------|-------------------|
| **Non-Revenue Water (NRW)** | **Air Tak Berekening (ATB)** | Air yang diproduksi tetapi tidak menghasilkan pendapatan. Rumus: NRW = (System Input - Billed Authorized Consumption) / System Input × 100%. Target IWA: < 15%. Rata-rata nasional Indonesia: 33,7% (2023). NRW tinggi melumpuhkan kemampuan investasi PDAM. |
| **Physical Losses** | **Kehilangan Fisik** | Air yang hilang secara fisik dari sistem sebelum sampai ke pelanggan. Penyebab: (1) Leakage (kebocoran pipa transmisi/distribusi/sambungan rumah), (2) Overflow reservoir karena kontrol level buruk. Kontribusi ~60-70% dari total NRW di PDAM Indonesia. |
| **Commercial Losses** | **Kehilangan Komersial** | Air yang sampai ke pelanggan tetapi tidak tercatat atau tidak tertagih. Penyebab: (1) Meter inakurat (under-recording), (2) Pencurian (illegal connections), (3) Error billing data, (4) Piutang macet. Kontribusi ~30-40% total NRW. |
| **Real Losses** | **Kehilangan Nyata** | Sinonim Physical Losses. Komponen: Background leakage (rembesan kecil di sambungan pipa), Reported bursts (pipa pecah yang dilaporkan), Unreported bursts (kebocoran invisible underground yang terdeteksi via DMA night flow analysis). |
| **Apparent Losses** | **Kehilangan Semu** | Sinonim Commercial Losses. Air yang digunakan pelanggan tapi tidak tercatat sebagai revenue. Penyebab utama di Indonesia: meter tua yang under-register (air velocity rendah tidak tercatat), meter macet, dan illegal tapping. |
| **Leakage Detection** | **Deteksi Kebocoran** | Aktivitas mencari kebocoran yang tidak terlihat di permukaan (underground leaks). Metode: (1) Acoustic (ground microphone, leak noise correlator), (2) Step testing (isolasi zona dan analisis pressure/flow), (3) Tracer gas (inject gas di pipa, detect di permukaan). |
| **Active Leakage Control (ALC)** | **Pengendalian Kebocoran Aktif** | Program sistematis untuk mencari dan memperbaiki kebocoran secara proaktif sebelum bocor muncul ke permukaan. Dilakukan tim leak detection pada malam hari (minimum night flow = MNF analysis) di setiap DMA secara berkala (cycle 1-3 bulan). |
| **Minimum Night Flow (MNF)** | **Aliran Minimum Malam** | Volume aliran air di DMA pada jam 2-4 pagi (saat konsumsi pelanggan minimum ~0). MNF yang tinggi mengindikasikan kebocoran. Rumus sederhana: MNF > expected legitimate night use (toilet flush, dll) → leakage. |
| **Infrastructure Leakage Index (ILI)** | **Indeks Kebocoran Infrastruktur** | Rasio antara current annual real losses (CARL) dengan unavoidable annual real losses (UARL). ILI = CARL/UARL. Benchmark: ILI < 2 = excellent, 2-4 = good, 4-8 = average, > 8 = poor. ILI lebih fair daripada % NRW karena memperhitungkan panjang pipa dan jumlah sambungan. |
| **Pressure Management** | **Manajemen Tekanan** | Strategi menurunkan tekanan jaringan distribusi (khususnya malam hari) menggunakan PRV untuk: (1) mengurangi leak rate (hukum: flow α pressure^0.5), (2) mengurangi frekuensi burst pipa, (3) memperpanjang umur pipa. Target: tekanan minimum 1 bar di ujung pipa. |
| **Water Audit** | **Audit Air** | Proses verifikasi dan rekonsiliasi neraca air menggunakan metodologi IWA Water Balance. Identifikasi komponen NRW (fisik vs komersial), validasi akurasi master meter dan customer meter, dan quantify financial losses dari NRW. |

### Domain 5: Keamanan Siber & Infrastruktur Kritis

| Istilah EN | Istilah ID | Definisi & Konteks |
|-----------|-----------|-------------------|
| **Cybersecurity** | **Keamanan Siber** | Praktik melindungi sistem komputer, jaringan, dan data dari serangan digital (hacking, malware, ransomware). Untuk PDAM: meliputi keamanan sistem billing, database pelanggan, sistem SCADA, dan infrastruktur cloud. |
| **Operational Technology (OT)** | **Teknologi Operasional** | Perangkat keras dan software yang mendeteksi atau mengontrol perubahan proses fisik (PLC, RTU, HMI di SCADA). Berbeda dari IT (Information Technology) yang mengelola data. Konvergensi IT/OT di PDAM menciptakan risiko cyber-physical attack. |
| **IT/OT Convergence** | **Konvergensi IT/OT** | Integrasi antara sistem IT (ERP, billing, email) dengan sistem OT (SCADA, sensor IoT). Manfaat: efisiensi, real-time analytics. Risiko: cyber attack dari jaringan IT bisa mencapai sistem OT dan mengganggu operasi fisik (shut down pompa, manipulasi dosing kimia). |
| **Ransomware** | **Perangkat Tebusan** | Malware yang mengenkripsi file sistem/database dan meminta tebusan (ransom) untuk dekripsi. Serangan ransomware di PDAM bisa lumpuhkan billing system, hilangkan data pelanggan, atau bahkan hentikan operasi SCADA jika tidak ada network segmentation. |
| **Firewall** | **Tembok Api** | Perangkat/software yang memfilter traffic jaringan berdasarkan aturan keamanan. Untuk PDAM: Next-Generation Firewall (NGFW) yang bisa Deep Packet Inspection, IPS (Intrusion Prevention), dan Application Control diperlukan untuk proteksi SCADA. |
| **Intrusion Detection System (IDS)** | **Sistem Deteksi Intrusi** | Software yang memonitor jaringan untuk aktivitas mencurigakan (scan port, brute force login, command injection). IDS memberikan alert ke security team. Untuk sistem kritis (SCADA), gunakan Intrusion Prevention System (IPS) yang bisa auto-block. |
| **Vulnerability Assessment** | **Penilaian Kerentanan** | Proses scanning sistem untuk mengidentifikasi kelemahan keamanan (unpatched software, weak password, misconfigured firewall). Harus dilakukan rutin (quarterly) terutama setelah update sistem atau penambahan device baru. |
| **Penetration Testing** | **Uji Penetrasi** | Simulasi cyber attack oleh ethical hacker untuk menguji efektivitas pertahanan. Untuk PDAM: pen-test harus mencakup web application (portal pelanggan), network infrastructure, dan SCADA system (dalam controlled environment). |
| **Business Continuity Plan (BCP)** | **Rencana Keberlangsungan Bisnis** | Dokumentasi prosedur untuk memastikan fungsi kritis PDAM tetap berjalan saat insiden (cyber attack, bencana alam, sabotase). Komponen: backup data (3-2-1 rule), alternate site, communication plan, recovery time objective (RTO), recovery point objective (RPO). |
| **Disaster Recovery Plan (DRP)** | **Rencana Pemulihan Bencana** | Subset dari BCP yang fokus pada pemulihan sistem IT/OT setelah disaster. Untuk PDAM: backup server di lokasi terpisah (offsite/cloud), redundant communication link untuk SCADA, documented recovery procedures dengan RTO < 24 jam untuk billing system. |
| **Encryption** | **Enkripsi** | Proses mengacak data menjadi ciphertext yang tidak bisa dibaca tanpa kunci dekripsi. Untuk PDAM: (1) Data at rest encryption untuk database pelanggan (compliance UU PDP), (2) Data in transit encryption (TLS/SSL) untuk API billing-payment gateway, (3) AES-128 untuk komunikasi LoRaWAN. |
| **Access Control** | **Kontrol Akses** | Mekanisme membatasi siapa yang bisa akses sistem apa. Model: Role-Based Access Control (RBAC) - akses berdasarkan jabatan. Contoh: operator lapangan bisa lihat data SCADA tapi tidak bisa ubah setpoint, hanya supervisor yang bisa. Prinsip: Least Privilege. |
| **Multi-Factor Authentication (MFA)** | **Autentikasi Multi-Faktor** | Keamanan login yang memerlukan 2+ faktor verifikasi (password + SMS OTP, atau password + biometric). Wajib untuk akses sistem kritis (SCADA HMI, database server, admin ERP). Mencegah account takeover jika password bocor. |
| **Security Information and Event Management (SIEM)** | **Manajemen Informasi dan Kejadian Keamanan** | Platform yang mengumpulkan, menganalisis, dan mengorelasikan log dari berbagai sistem (firewall, server, aplikasi) untuk mendeteksi anomali dan insiden keamanan secara real-time. Essential untuk PDAM besar dengan infrastruktur IT/OT kompleks. |

### Domain 6: Manajemen Keuangan & Regulasi

| Istilah EN | Istilah ID | Definisi & Konteks |
|-----------|-----------|-------------------|
| **Full Cost Recovery (FCR)** | **Pemulihan Biaya Penuh** | Kondisi dimana tarif rata-rata air minum sudah menutup seluruh biaya operasional (O&M), depresiasi, dan biaya modal. FCR adalah syarat PDAM untuk dapat ekspansi tanpa subsidi. Mandatori untuk PDAM yang ingin akses kredit perbankan (Permen PUPR 29/2020). |
| **Return on Equity (ROE)** | **Pengembalian atas Ekuitas** | Rasio laba bersih terhadap modal sendiri. ROE = Laba Bersih / Ekuitas × 100%. Untuk BUMD Air Minum kategori "Sehat": ROE > 0% (profitable). Target ideal: ROE > 10% (comparable dengan BUMD lain). |
| **Operating Ratio** | **Rasio Operasi (BOPO)** | Rasio biaya operasional terhadap pendapatan operasional. Operating Ratio = OPEX / Revenue. Benchmark Permendagri 23/2024: BUMD Kecil < 0,95; Sedang < 0,90; Besar < 0,85. Semakin rendah semakin efisien. |
| **Collection Rate** | **Tingkat Penagihan** | Persentase tagihan air yang berhasil ditagih dalam periode tertentu. Collection Rate = Cash Collected / Billed Amount × 100%. Target BPPSPAM untuk status "Sehat": > 90%. Collection rate rendah mengindikasikan piutang macet atau sistem billing bermasalah. |
| **Accounts Receivable (AR)** | **Piutang Usaha** | Tagihan yang sudah dikeluarkan tetapi belum dibayar pelanggan. Aging analysis penting: < 30 days (current), 30-60 days (overdue), > 90 days (bad debt risk). PDAM harus punya kebijakan cutoff jelas untuk piutang > 90 hari (pemutusan sementara). |
| **Capital Expenditure (CAPEX)** | **Belanja Modal** | Pengeluaran untuk akuisisi atau upgrade aset tetap jangka panjang (pipa baru, pompa, IPA, sistem IT). CAPEX diamortisasi selama umur ekonomis aset. Untuk PDAM: sumber CAPEX = APBD, kredit bank, atau kemitraan swasta (KPS). |
| **Operating Expenditure (OPEX)** | **Biaya Operasional** | Pengeluaran rutin untuk operasi sehari-hari (listrik, bahan kimia, gaji, pemeliharaan rutin, lisensi software). OPEX harus di-cover penuh oleh revenue operasional untuk mencapai FCR. |
| **Tariff Structure** | **Struktur Tarif** | Skema penetapan harga air berdasarkan kategori pelanggan dan volume konsumsi. Permendagri 21/2020: (1) Tarif Rendah (subsidi untuk MBR), (2) Tarif Dasar (cost recovery), (3) Tarif Penuh (profit margin untuk pelanggan mampu/industri), (4) Tarif Kesepakatan (kontrak khusus). |
| **Cross-Subsidy** | **Subsidi Silang** | Mekanisme dimana pelanggan kategori mampu/industri (tarif tinggi) mensubsidi pelanggan tidak mampu (tarif rendah). Syarat: aggregate revenue tetap mencapai FCR. Jika tidak, Pemda wajib beri subsidi APBD untuk menutup gap (Subsidi Tarif). |
| **Depreciation** | **Penyusutan** | Alokasi sistematis nilai aset tetap selama umur ekonomisnya. Metode untuk PDAM: straight-line depreciation. Contoh: pipa HDPE umur 50 tahun, nilai Rp 1M → depresiasi Rp 20 juta/tahun. Depresiasi adalah biaya non-kas tetapi harus masuk perhitungan tarif FCR. |

---

## AKRONIM DAN SINGKATAN

### Regulasi & Kelembagaan

| Akronim | Kepanjangan Indonesia | Kepanjangan EN | Keterangan |
|---------|----------------------|----------------|------------|
| **PDAM** | Perusahaan Daerah Air Minum | Regional Water Company | Nama lama BUMD air minum sebelum transformasi regulasi 2024. Beberapa masih menggunakan nama ini. |
| **BUMD** | Badan Usaha Milik Daerah | Regional-Owned Enterprise | Badan usaha yang modalnya dimiliki pemerintah daerah. |
| **Perumda** | Perusahaan Umum Daerah | Regional Public Company | Bentuk hukum BUMD yang fokus pada public service obligation (PSO), modal 100% satu daerah. |
| **Perseroda** | Perusahaan Perseroan Daerah | Regional Limited Liability Company | Bentuk hukum BUMD profit-oriented, modal min 51% daerah, bisa multi-daerah atau mixed ownership. |
| **KPM** | Kuasa Pemilik Modal | Principal Owner Authority | Kepala Daerah selaku wakil pemerintah daerah dalam kepemilikan modal BUMD (setara RUPS di Perseroda). |
| **RUPS** | Rapat Umum Pemegang Saham | General Meeting of Shareholders | Organ tertinggi Perseroda yang terdiri dari semua pemegang saham. |
| **BPPSPAM** | Badan Peningkatan Penyelenggaraan Sistem Penyediaan Air Minum | Agency for Improvement of Drinking Water Supply Systems | Badan di bawah Kementerian PUPR yang melakukan evaluasi kinerja PDAM dan pembinaan teknis. |
| **PERPAMSI** | Persatuan Perusahaan Air Minum Seluruh Indonesia | Association of Indonesian Water Supply Companies | Asosiasi profesi PDAM se-Indonesia, menjadi forum knowledge sharing dan advokasi kebijakan. |
| **BSSN** | Badan Siber dan Sandi Negara | National Cyber and Crypto Agency | Lembaga pemerintah yang mengatur keamanan siber infrastruktur kritis termasuk utilitas air (sektor IIV). |
| **BPK** | Badan Pemeriksa Keuangan | Supreme Audit Board | Lembaga negara yang mengaudit keuangan BUMD untuk laporan ke DPR/DPRD. |
| **BPKP** | Badan Pengawasan Keuangan dan Pembangunan | Finance and Development Supervisory Agency | Lembaga pengawas internal pemerintah yang melakukan audit kinerja PDAM bersama Kementerian PUPR. |

### Teknologi & Operasional

| Akronim | Kepanjangan Indonesia | Kepanjangan EN | Keterangan |
|---------|----------------------|----------------|------------|
| **SCADA** | - | Supervisory Control and Data Acquisition | Sistem monitoring dan kontrol infrastruktur kritis (IPA, pompa, reservoir) secara real-time. |
| **PLC** | - | Programmable Logic Controller | Komputer industrial yang mengendalikan mesin/proses otomatis berdasarkan program logic. Core dari sistem SCADA. |
| **HMI** | - | Human-Machine Interface | Antarmuka grafis yang digunakan operator untuk monitoring dan kontrol sistem SCADA. |
| **RTU** | - | Remote Terminal Unit | Perangkat di lapangan yang mengumpulkan data sensor dan mengirimnya ke master station SCADA via telemetri. |
| **IoT** | - | Internet of Things | Ekosistem sensor dan device terhubung internet untuk monitoring dan kontrol real-time. |
| **LoRaWAN** | - | Long Range Wide Area Network | Teknologi komunikasi wireless jarak jauh untuk smart metering di PDAM Indonesia. |
| **GIS** | Sistem Informasi Geografis | Geographic Information System | Platform pemetaan digital aset PDAM (pipa, valve, meter) dengan koordinat GPS dan atribut teknis. |
| **ERP** | - | Enterprise Resource Planning | Sistem terintegrasi yang menghubungkan fungsi bisnis (finance, HR, procurement, billing) dalam satu database. |
| **CRM** | - | Customer Relationship Management | Platform untuk mengelola interaksi dengan pelanggan (pendaftaran, pengaduan, billing). |
| **AMR** | - | Automatic Meter Reading | Sistem pembacaan meter otomatis menggunakan teknologi wireless (LoRaWAN, RF, GSM). |
| **AMI** | - | Advanced Metering Infrastructure | Evolusi dari AMR, dua-arah komunikasi yang memungkinkan remote disconnect, demand response, dan real-time pricing. |
| **API** | Antarmuka Pemrograman Aplikasi | Application Programming Interface | Protokol untuk integrasi sistem berbeda (contoh: billing PDAM dengan payment gateway). |
| **SaaS** | - | Software as a Service | Model cloud computing dimana software diakses via internet (subscription), tanpa install di server lokal. |
| **IaaS** | - | Infrastructure as a Service | Model cloud computing yang menyediakan server virtual, storage, network as a service (contoh: AWS EC2). |
| **VPN** | - | Virtual Private Network | Koneksi terenkripsi untuk akses remote yang aman ke jaringan internal PDAM. |
| **VSD** | Penggerak Kecepatan Variabel | Variable Speed Drive | Inverter untuk mengatur kecepatan motor pompa sesuai demand, hemat energi signifikan. |

### Keuangan & Kinerja

| Akronim | Kepanjangan Indonesia | Kepanjangan EN | Keterangan |
|---------|----------------------|----------------|------------|
| **FCR** | Pemulihan Biaya Penuh | Full Cost Recovery | Tarif sudah menutup O&M + depresiasi + biaya modal. Syarat akses kredit bank. |
| **ROE** | Pengembalian atas Ekuitas | Return on Equity | Laba bersih / Ekuitas. Indikator profitabilitas untuk pemegang saham (Pemda). |
| **ROA** | Pengembalian atas Aset | Return on Assets | Laba bersih / Total Aset. Mengukur efisiensi penggunaan aset. |
| **BOPO** | Biaya Operasional terhadap Pendapatan Operasional | Operating Ratio | OPEX / Revenue. Benchmark Permendagri 23/2024: Besar < 0,85; Sedang < 0,90; Kecil < 0,95. |
| **EBITDA** | - | Earnings Before Interest, Tax, Depreciation, Amortization | Laba sebelum bunga, pajak, depresiasi, amortisasi. Ukuran cash flow operasional. |
| **NPV** | Nilai Kini Bersih | Net Present Value | Nilai sekarang dari cash flow masa depan project. NPV > 0 → project feasible. |
| **IRR** | Tingkat Pengembalian Internal | Internal Rate of Return | Tingkat diskonto yang membuat NPV = 0. IRR > cost of capital → project acceptable. |
| **DSCR** | Rasio Cakupan Layanan Utang | Debt Service Coverage Ratio | Cash available / Debt payment. DSCR > 1.25 → bankable. Syarat perbankan untuk kredit PDAM. |
| **CAPEX** | Belanja Modal | Capital Expenditure | Investasi aset tetap (pipa, pompa, IPA, sistem IT). Diamortisasi selama umur ekonomis. |
| **OPEX** | Biaya Operasional | Operating Expenditure | Biaya rutin (listrik, kimia, gaji, maintenance). Harus di-cover revenue untuk FCR. |

### NRW & Manajemen Aset

| Akronim | Kepanjangan Indonesia | Kepanjangan EN | Keterangan |
|---------|----------------------|----------------|------------|
| **NRW** | Air Tak Berekening | Non-Revenue Water | Air diproduksi tapi tidak menghasilkan revenue. Target IWA: < 15%. Indonesia avg: 33,7%. |
| **ATB** | Air Tak Berekening | Non-Revenue Water | Istilah Indonesia untuk NRW. |
| **DMA** | Zona Meteran Distrik | District Meter Area | Zona kecil (1.000-3.000 pelanggan) yang diisolasi dengan master meter untuk monitoring NRW presisi. |
| **MNF** | Aliran Minimum Malam | Minimum Night Flow | Aliran air jam 2-4 pagi saat konsumsi minimum. MNF tinggi = indikasi kebocoran. |
| **ALC** | Pengendalian Kebocoran Aktif | Active Leakage Control | Program proaktif mencari kebocoran dengan acoustic detection sebelum bocor muncul ke permukaan. |
| **PRV** | Katup Penurun Tekanan | Pressure Reducing Valve | Valve otomatis untuk pressure management, mengurangi kebocoran akibat tekanan berlebih. |
| **ILI** | Indeks Kebocoran Infrastruktur | Infrastructure Leakage Index | Rasio CARL/UARL. ILI < 2 = excellent. Lebih fair dari % NRW karena normalisasi panjang pipa dan sambungan. |
| **CARL** | - | Current Annual Real Losses | Kebocoran fisik aktual tahunan (dalam m³/tahun). |
| **UARL** | - | Unavoidable Annual Real Losses | Kebocoran fisik teoritis minimum yang tidak bisa dihindari (bahkan dengan infrastruktur terbaik). |
| **SL** | Sambungan Langganan | Service Connection | Jumlah sambungan pelanggan. Digunakan untuk klasifikasi BUMD (Kecil < 50k, Sedang 50-100k, Besar > 100k). |
| **SR** | Sambungan Rumah | House Connection | Sinonim SL. Istilah lama yang masih sering digunakan. |

### Keamanan & Compliance

| Akronim | Kepanjangan Indonesia | Kepanjangan EN | Keterangan |
|---------|----------------------|----------------|------------|
| **GRC** | Tata Kelola, Risiko & Kepatuhan | Governance, Risk & Compliance | Framework terintegrasi untuk GCG, risk management, dan regulatory compliance. |
| **GCG** | Tata Kelola Perusahaan yang Baik | Good Corporate Governance | Prinsip transparansi, akuntabilitas, responsibility, independensi, fairness dalam pengelolaan. |
| **PDP** | Pelindungan Data Pribadi | Personal Data Protection | UU 27/2022 yang mengatur hak privasi dan kewajiban pengendali data (termasuk PDAM). |
| **DPIA** | Penilaian Dampak Perlindungan Data | Data Protection Impact Assessment | Analisis risiko untuk pemrosesan data berisiko tinggi (wajib UU PDP). |
| **DPO** | Pejabat Pelindungan Data Pribadi | Data Protection Officer | Posisi wajib untuk organisasi yang proses data skala besar (UU PDP). |
| **ISMS** | Sistem Manajemen Keamanan Informasi | Information Security Management System | Framework sistematis untuk melindungi kerahasiaan, integritas, dan ketersediaan informasi (ISO 27001). |
| **IDS** | Sistem Deteksi Intrusi | Intrusion Detection System | Software monitoring jaringan untuk mendeteksi aktivitas mencurigakan. |
| **IPS** | Sistem Pencegahan Intrusi | Intrusion Prevention System | IDS + kemampuan auto-block threat. |
| **SIEM** | Manajemen Informasi dan Kejadian Keamanan | Security Information and Event Management | Platform yang mengumpulkan dan menganalisis log dari berbagai sistem untuk deteksi insiden real-time. |
| **BCP** | Rencana Keberlangsungan Bisnis | Business Continuity Plan | Dokumentasi prosedur untuk menjaga fungsi kritis saat insiden (cyber, bencana). |
| **DRP** | Rencana Pemulihan Bencana | Disaster Recovery Plan | Subset BCP fokus pada pemulihan sistem IT/OT setelah disaster. |
| **RTO** | Tujuan Waktu Pemulihan | Recovery Time Objective | Maksimum downtime yang dapat ditoleransi untuk fungsi kritis. Contoh: billing RTO < 24 jam. |
| **RPO** | Tujuan Titik Pemulihan | Recovery Point Objective | Maksimum data loss yang acceptable. Contoh: database pelanggan RPO < 1 jam (backup hourly). |

---

## REFERENSI REGULASI INDONESIA

### Undang-Undang (UU)

#### UU 17/2019 - Sumber Daya Air
**Judul:** Undang-Undang Nomor 17 Tahun 2019 tentang Sumber Daya Air  
**Diundangkan:** 22 Oktober 2019  
**Fungsi:** Mengatur penguasaan negara atas air, hierarki prioritas penggunaan air (kebutuhan pokok > pertanian rakyat > SPAM > industri), perizinan pengusahaan air, dan sanksi pidana penyalahgunaan sumber air.  
**Pasal Krusial:**
- Pasal 7: Hak rakyat atas air
- Pasal 46: Hierarki prioritas penggunaan air
- Pasal 54-56: Perizinan berusaha terkait sumber daya air
- Pasal 68-74: Sanksi pidana (penjara 1-3 tahun, denda miliaran rupiah)  
**Implikasi PDAM:** Wajib memiliki izin pengambilan air baku (SIPA/SIPPA) yang valid. Prioritas tinggi dalam alokasi air baku vs industri swasta.

#### UU 27/2022 - Pelindungan Data Pribadi
**Judul:** Undang-Undang Nomor 27 Tahun 2022 tentang Pelindungan Data Pribadi  
**Diundangkan:** 17 Oktober 2022  
**Berlaku Efektif:** 17 Oktober 2024 (grace period 2 tahun)  
**Fungsi:** Melindungi hak privasi warga negara, mengatur kewajiban Pengendali Data dan Prosesor Data, menentukan rezim sanksi administratif dan pidana untuk pelanggaran privasi.  
**Pasal Krusial:**
- Pasal 4-5: Hak subjek data (akses, koreksi, penghapusan)
- Pasal 11-19: Kewajiban pengendali data (persetujuan, transparansi, keamanan)
- Pasal 35: Penunjukan DPO wajib untuk pemrosesan skala besar
- Pasal 57-59: Sanksi administratif (denda hingga 2% revenue tahunan)
- Pasal 67-68: Sanksi pidana (penjara 5-6 tahun, denda Rp 5-6 miliar)  
**Implikasi PDAM:** Status sebagai Pengendali Data wajib implementasi Privacy by Design, enkripsi database pelanggan, mekanisme persetujuan (consent), notifikasi data breach dalam 3×24 jam, dan penunjukan DPO.

#### UU 23/2014 - Pemerintahan Daerah
**Judul:** Undang-Undang Nomor 23 Tahun 2014 tentang Pemerintahan Daerah  
**Diundangkan:** 2 Oktober 2014  
**Fungsi:** Mengatur urusan pemerintahan daerah termasuk pembentukan dan pengelolaan BUMD sebagai instrumen ekonomi daerah.  
**Pasal Krusial:**
- Pasal 331-354: Pembentukan, pengelolaan, pengawasan, dan pembubaran BUMD
- Pasal 338: Klasifikasi BUMD (Perumda vs Perseroda)  
**Implikasi PDAM:** Landasan hukum eksistensi BUMD Air Minum, kewenangan Kepala Daerah selaku KPM.

### Peraturan Pemerintah (PP)

#### PP 122/2015 - Sistem Penyediaan Air Minum
**Judul:** Peraturan Pemerintah Nomor 122 Tahun 2015 tentang Sistem Penyediaan Air Minum  
**Dikeluarkan:** 30 Desember 2015  
**Fungsi:** Mengatur penyelenggaraan SPAM (komponen fisik, standar pelayanan, pengembangan, pendanaan, pembiayaan).  
**Pasal Krusial:**
- Pasal 4-8: Komponen SPAM (unit air baku, produksi, distribusi, pelayanan)
- Pasal 30-35: Izin penyelenggaraan SPAM
- Pasal 52-56: Tarif layanan (prinsip keterjangkauan + pemulihan biaya)  
**Implikasi PDAM:** Blueprint teknis infrastruktur SPAM, kewajiban pemeliharaan aset, basis perhitungan tarif.

#### PP 54/2017 - BUMD
**Judul:** Peraturan Pemerintah Nomor 54 Tahun 2017 tentang Badan Usaha Milik Daerah  
**Dikeluarkan:** 15 Agustus 2017  
**Fungsi:** Mengatur pembentukan, pengelolaan, pengawasan kinerja, dan mekanisme privatisasi/likuidasi BUMD.  
**Pasal Krusial:**
- Pasal 11-15: Persyaratan pembentukan BUMD
- Pasal 76-80: Organ BUMD (RUPS/KPM, Dewan Komisaris/Pengawas, Direksi)
- Pasal 117-125: Penilaian kesehatan BUMD dan restrukturisasi  
**Implikasi PDAM:** Framework tata kelola organ BUMD, mekanisme evaluasi kinerja tahunan.

### Peraturan Presiden (Perpres)

#### Perpres 95/2018 - SPBE (Sistem Pemerintahan Berbasis Elektronik)
**Judul:** Peraturan Presiden Nomor 95 Tahun 2018 tentang Sistem Pemerintahan Berbasis Elektronik  
**Dikeluarkan:** 5 November 2018  
**Fungsi:** Mengatur arsitektur, tata kelola, manajemen, dan integrasi sistem elektronik pemerintah untuk mendukung pelayanan publik digital.  
**Pasal Krusial:**
- Pasal 13-15: Arsitektur SPBE (Proses Bisnis, Data Informasi, Infrastruktur, Aplikasi, Keamanan)
- Pasal 41-45: Integrasi layanan SPBE antar instansi
- Pasal 47-50: Keamanan informasi SPBE (berdasarkan Indeks KAMI BSSN)  
**Implikasi PDAM:** Sebagai bagian ekosistem Pemda, sistem IT PDAM harus selaras dengan arsitektur SPBE daerah (interoperability). Mandatory untuk pemeringkatan SPBE tahunan (target: Level 3 - Terintegrasi).

#### Perpres 132/2022 - SPBE (Perubahan)
**Judul:** Peraturan Presiden Nomor 132 Tahun 2022 tentang Perubahan atas Perpres 95/2018  
**Dikeluarkan:** 30 Desember 2022  
**Fungsi:** Menyempurnakan tata kelola SPBE, memperkuat peran Kementerian PANRB dan Kominfo, menambah kewajiban audit SPBE.  
**Implikasi PDAM:** Penguatan audit SPBE tahunan, wajib implementasi standar keamanan BSSN.

#### Perpres 16/2018 - Pengadaan Barang/Jasa Pemerintah
**Judul:** Peraturan Presiden Nomor 16 Tahun 2018 tentang Pengadaan Barang/Jasa Pemerintah  
**Dikeluarkan:** 26 Maret 2018  
**Fungsi:** Mengatur mekanisme procurement pemerintah termasuk BUMD (e-procurement, lelang, penunjukan langsung).  
**Pasal Krusial:**
- Pasal 8-12: Prinsip pengadaan (efisien, efektif, transparan, terbuka, bersaing, adil, akuntabel)
- Pasal 50-55: E-procurement wajib melalui LPSE  
**Implikasi PDAM:** Seluruh pengadaan > Rp 200 juta wajib melalui LPSE (Layanan Pengadaan Secara Elektronik), due diligence vendor, anti-korupsi.

### Peraturan Menteri Dalam Negeri (Permendagri)

#### Permendagri 23/2024 - Organ dan Kepegawaian BUMD Air Minum
**Judul:** Peraturan Menteri Dalam Negeri Nomor 23 Tahun 2024 tentang Organ dan Kepegawaian Badan Usaha Milik Daerah Air Minum  
**Dikeluarkan:** 26 April 2024  
**Berlaku:** 26 April 2024 (mencabut Permendagri 2/2007)  
**Fungsi:** Reformasi total tata kelola organ BUMD Air Minum (struktur, kewenangan, remunerasi, kepegawaian).  
**Pasal Krusial:**
- Pasal 6: Klasifikasi BUMD (Kecil < 50k SL, Sedang 50-100k, Besar > 100k)
- Pasal 9-11: Komposisi Direksi berdasarkan klasifikasi dan FCR
- Pasal 39-42: Rasio BOPO maksimal (Kecil 0,95; Sedang 0,90; Besar 0,85)
- Pasal 62-65: Tantiem dan Jasa Produksi (hanya jika laba bersih positif)
- Pasal 85: Rasio jumlah pegawai per 1.000 pelanggan  
**Implikasi PDAM:** Mandatory rightsizing struktur organisasi, efisiensi biaya, link remunerasi dengan kinerja.

#### Permendagri 21/2020 - Perubahan Tarif Air Minum
**Judul:** Peraturan Menteri Dalam Negeri Nomor 21 Tahun 2020 tentang Perubahan atas Permendagri 71/2016 tentang Perhitungan dan Penetapan Tarif Air Minum  
**Dikeluarkan:** 7 Juli 2020  
**Fungsi:** Mengatur metodologi perhitungan tarif berbasis Full Cost Recovery, mekanisme penetapan tarif (usulan BUMD → analisis Bappeda → penetapan Perda DPRD), struktur tarif progresif/blok.  
**Pasal Krusial:**
- Pasal 4: Prinsip tarif (keterjangkauan, keadilan, pemulihan biaya penuh)
- Pasal 7-9: Komponen biaya dasar (O&M + depresiasi + bunga)
- Pasal 13-15: Struktur tarif (Rendah, Dasar, Penuh, Kesepakatan)
- Pasal 18: Wewenang Gubernur menetapkan tarif batas atas dan bawah provinsi  
**Implikasi PDAM:** Blueprint penyusunan usulan penyesuaian tarif, justifikasi subsidi silang, mekanisme subsidi APBD jika tarif < biaya dasar.

### Peraturan Menteri PUPR

#### Permen PUPR 18/2024 - SPM Air Minum
**Judul:** Peraturan Menteri Pekerjaan Umum dan Perumahan Rakyat Nomor 18 Tahun 2024 tentang Standar Pelayanan Minimal Bidang Pekerjaan Umum dan Perumahan Rakyat  
**Dikeluarkan:** 12 Agustus 2024  
**Fungsi:** Menetapkan SPM wajib yang harus dipenuhi Pemda dalam penyediaan air minum (cakupan akses 100% air layak, kualitas sesuai Permenkes, kontinuitas 24/7).  
**Pasal Krusial:**
- Lampiran: Target SPM Air Minum (akses 100% KK pada 2024)  
**Implikasi PDAM:** Pemda wajib alokasikan APBD untuk mencapai SPM. PDAM sebagai operator wajib laporan pencapaian SPM tahunan.

#### Permen PUPR 29/2020 - Kelayakan Proyek Investasi SPAM
**Judul:** Peraturan Menteri PUPR Nomor 29 Tahun 2020 tentang Pemberian Rekomendasi dan Pedoman Teknis Kelayakan Proyek Investasi Sistem Penyediaan Air Minum  
**Dikeluarkan:** 30 November 2020  
**Fungsi:** Mengatur prosedur PDAM mengajukan rekomendasi kelayakan investasi ke Kementerian PUPR untuk akses pendanaan (kredit bank, kemitraan swasta).  
**Pasal Krusial:**
- Pasal 5: Syarat pemohon (status "Sehat", FCR minimal 2 tahun, Rencana Bisnis disahkan Pemda)
- Pasal 8-10: Dokumen yang diperlukan (Studi Kelayakan, Rencana Bisnis, Dukungan Prinsip Pemda, AMDAL)
- Pasal 13: Analisis finansial (NPV, IRR, DSCR)  
**Implikasi PDAM:** Roadmap akses kredit perbankan atau investor swasta untuk ekspansi infrastruktur. Tanpa rekomendasi Kementerian, sulit dapat pendanaan eksternal.

### Peraturan Menteri Kesehatan

#### Permenkes 492/2010 - Kualitas Air Minum
**Judul:** Peraturan Menteri Kesehatan Nomor 492/MENKES/PER/IV/2010 tentang Persyaratan Kualitas Air Minum  
**Dikeluarkan:** 19 April 2010  
**Fungsi:** Menetapkan parameter fisik, kimia, biologi, dan radioaktif yang harus dipenuhi air minum layak konsumsi.  
**Parameter Krusial:**
- Fisik: Tidak berbau, tidak berasa, tidak berwarna, suhu max 30°C
- Kimia: pH 6,5-8,5, Besi (Fe) max 0,3 mg/L, Mangan (Mn) max 0,1 mg/L, Fluorida max 1,5 mg/L
- Mikrobiologi: E.coli 0 per 100 ml (zero tolerance)  
**Implikasi PDAM:** Wajib uji laboratorium rutin (harian untuk klorin sisa, bulanan untuk parameter lengkap), investasi IPA sesuai kualitas air baku.

### Pedoman BSSN

#### Pedoman Keamanan Siber Sektor SDA
**Judul:** Pedoman Teknis Keamanan Siber Sektor Sumber Daya Air (Sektor Infrastruktur Informasi Vital)  
**Dikeluarkan:** BSSN, 2021  
**Fungsi:** Mengatur langkah-langkah perlindungan sistem OT/IT di sektor air minum sebagai infrastruktur kritis nasional (IIV).  
**Elemen Krusial:**
- Network segmentation (pemisahan jaringan OT dan IT)
- Implementasi IDS/IPS untuk SCADA
- Penetration testing rutin (minimal annual)
- Incident response plan yang teruji
- Koordinasi dengan BSSN saat insiden cyber  
**Implikasi PDAM:** Wajib registrasi sebagai penyelenggara IIV, audit keamanan siber tahunan, lapor insiden ke BSSN.

#### Indeks KAMI (Keamanan Informasi)
**Judul:** Pedoman Indeks Keamanan Informasi (KAMI) Versi 5.1  
**Dikeluarkan:** BSSN, 2022  
**Fungsi:** Framework penilaian mandiri tingkat kematangan keamanan informasi instansi pemerintah/BUMD. Skala: Tidak Layak, Perbaikan, Baik, Sangat Baik.  
**Kategori Penilaian:**
- Tata Kelola Keamanan Informasi
- Pengelolaan Risiko
- Kerangka Kerja Keamanan Informasi
- Pengelolaan Aset Informasi
- Teknologi dan Keamanan Informasi  
**Implikasi PDAM:** Self-assessment wajib tahunan, target minimal kategori "Baik" untuk BUMD besar, dokumentasi kontrol keamanan.

---

## STANDAR TEKNIS INTERNASIONAL

### ISO (International Organization for Standardization)

#### ISO 27001:2013 - Information Security Management
**Judul:** ISO/IEC 27001:2013 Information Security Management System  
**Fungsi:** Standar global untuk membangun, mengimplementasikan, memelihara, dan meningkatkan ISMS secara berkelanjutan.  
**Struktur:** 14 domain kontrol (114 kontrol spesifik dalam Annex A)  
**Domain Utama:**
- A.5: Information Security Policies
- A.9: Access Control
- A.12: Operations Security
- A.17: Information Security Aspects of Business Continuity Management
- A.18: Compliance  
**Manfaat PDAM:** Sertifikasi ISO 27001 meningkatkan kepercayaan stakeholder, mengurangi risiko data breach (compliance UU PDP), dan memperkuat posisi saat tender kemitraan.

#### ISO 31000:2018 - Risk Management
**Judul:** ISO 31000:2018 Risk Management – Guidelines  
**Fungsi:** Framework universal untuk enterprise risk management (ERM) yang dapat diterapkan di semua jenis organisasi.  
**Prinsip Utama:**
- Risk management creates and protects value
- Risk management is integral part of all organizational processes
- Risk management is part of decision making
- Risk management explicitly addresses uncertainty  
**Proses:** Establish context → Risk identification → Risk analysis → Risk evaluation → Risk treatment → Monitoring & review  
**Manfaat PDAM:** Sistematis dalam mengelola risiko strategis (regulasi, reputasi), operasional (NRW, gangguan layanan), finansial (default loan), dan teknologi (cyber attack).

#### ISO 24516:2017 - Service Activities Relating to Drinking Water Supply Systems
**Judul:** ISO 24516 Series - Guidelines for the management and assessment of service activities relating to drinking water supply systems, wastewater systems and storm drainage  
**Fungsi:** Standar spesifik untuk utilitas air tentang service level agreement, performance indicators, customer satisfaction.  
**Komponen:**
- Part 1: Drinking water supply systems
- Part 2: Wastewater systems
- Part 3: Storm drainage systems  
**Manfaat PDAM:** Benchmark internasional untuk KPI operasional dan pelayanan pelanggan.

### IWA (International Water Association)

#### IWA Water Balance Methodology
**Judul:** IWA Water Balance and Water Loss Performance Indicators  
**Fungsi:** Metodologi standar global untuk perhitungan NRW dan kategorisasi komponen kehilangan air.  
**Komponen Water Balance:**
```
System Input (SIV)
├─ Authorized Consumption (AC)
│  ├─ Billed Authorized Consumption (Revenue Water)
│  │  ├─ Billed Metered Consumption
│  │  └─ Billed Unmetered Consumption
│  └─ Unbilled Authorized Consumption
│     ├─ Unbilled Metered Consumption (hydrant testing, firefighting)
│     └─ Unbilled Unmetered Consumption
└─ Water Losses (NRW)
   ├─ Apparent Losses (Commercial Losses)
   │  ├─ Unauthorized Consumption (theft, illegal connections)
   │  └─ Customer Meter Inaccuracies (under-registration)
   └─ Real Losses (Physical Losses)
      ├─ Leakage on transmission and distribution mains
      ├─ Leakage on service connections (up to customer meter)
      └─ Leakage and overflows at storage tanks
```
**Performance Indicators:**
- % NRW = (System Input - Billed Auth Cons) / System Input × 100%
- Infrastructure Leakage Index (ILI) = CARL / UARL
- Unit NRW = NRW volume / (length of mains × operating hours)  
**Manfaat PDAM:** Standar reporting NRW yang dapat dibandingkan antar negara, basis perhitungan ILI untuk benchmark internasional.

### COBIT (Control Objectives for Information and Related Technologies)

#### COBIT 2019 Framework
**Developer:** ISACA (Information Systems Audit and Control Association)  
**Fungsi:** Framework tata kelola dan manajemen IT enterprise yang komprehensif.  
**Komponen Utama:**
- **Governance System Components:** Processes, Organizational Structures, Policies & Procedures, Information Flows, Culture & Behaviors, Skills & Competencies, Infrastructure & Applications
- **Design Factors:** Enterprise Strategy, Goals, Risk Profile, IT-related Issues, Threat Landscape, Compliance Requirements, Role of IT, Sourcing Model, IT Implementation Methods, Technology Adoption Strategy, Enterprise Size  
**40 Governance & Management Objectives:**
- 5 Governance Objectives (EDM: Evaluate, Direct, Monitor)
  - EDM01: Ensured Governance Framework Setting and Maintenance
  - EDM02: Ensured Benefits Delivery
  - EDM03: Ensured Risk Optimization
  - EDM04: Ensured Resource Optimization
  - EDM05: Ensured Stakeholder Engagement
- 35 Management Objectives (APO, BAI, DSS, MEA)
  - APO: Align, Plan, Organize
  - BAI: Build, Acquire, Implement
  - DSS: Deliver, Service, Support
  - MEA: Monitor, Evaluate, Assess  
**Manfaat PDAM:** Alignment IT strategy dengan business goals, KPI untuk measuring IT value, risk management framework untuk IT investments.

### ITIL (Information Technology Infrastructure Library)

#### ITIL 4 Framework
**Developer:** Axelos (UK Government)  
**Fungsi:** Best practice framework untuk IT service management (ITSM).  
**Konsep Inti:**
- Service Value System (SVS)
- Four Dimensions of Service Management (Organizations & People, Information & Technology, Partners & Suppliers, Value Streams & Processes)
- ITIL Service Value Chain (Plan, Improve, Engage, Design & Transition, Obtain/Build, Deliver & Support)  
**34 ITIL Practices:**
- General Management Practices: Strategy Management, Portfolio Management, Architecture Management, Continual Improvement, etc.
- Service Management Practices: Service Desk, Incident Management, Problem Management, Change Control, Service Level Management, etc.
- Technical Management Practices: Deployment Management, Infrastructure & Platform Management, Software Development & Management  
**Manfaat PDAM:** Standardisasi IT service delivery (help desk, incident response), meningkatkan availability sistem billing/SCADA, mengurangi downtime.

### NIST (National Institute of Standards and Technology)

#### NIST Cybersecurity Framework (CSF) v1.1
**Developer:** US Department of Commerce  
**Fungsi:** Framework voluntary untuk mengelola risiko keamanan siber di infrastruktur kritis.  
**5 Core Functions:**
1. **Identify:** Asset Management, Business Environment, Governance, Risk Assessment, Supply Chain Risk Management
2. **Protect:** Identity Management & Access Control, Awareness & Training, Data Security, Protective Technology
3. **Detect:** Anomalies & Events, Security Continuous Monitoring, Detection Processes
4. **Respond:** Response Planning, Communications, Analysis, Mitigation, Improvements
5. **Recover:** Recovery Planning, Improvements, Communications  
**Implementation Tiers:** Partial, Risk Informed, Repeatable, Adaptive  
**Manfaat PDAM:** Roadmap sistematis untuk memperkuat cyber resilience, komunikasi risiko cyber ke Direksi/Dewan dalam bahasa bisnis, compliance dengan standar internasional (untuk PDAM yang berpartner dengan donor/investor asing).

---

## METRIK DAN BENCHMARK

### Indikator Kinerja BPPSPAM (18 Indikator)

| No | Aspek | Indikator | Satuan | Target "Sehat" | Keterangan |
|----|-------|-----------|--------|----------------|------------|
| **A. OPERASIONAL (35%)** |
| 1 | Operasi | Efisiensi Produksi | % | > 80% | Persentase air produksi yang masuk jaringan distribusi |
| 2 | Operasi | Tingkat Kehilangan Air (NRW) | % | < 20% | Target IWA < 15%, Indonesia avg 33,7% |
| 3 | Operasi | Jam Operasi Layanan | Jam/hari | > 20 jam | Target ideal: 24 jam kontinyu |
| 4 | Operasi | Tekanan Air Minimum | Bar | > 0,5 | Di titik terjauh jaringan |
| 5 | Operasi | Kualitas Air Pelanggan | % | 100% | Memenuhi Permenkes 492/2010 |
| 6 | Operasi | Konsumsi Energi Listrik | kWh/m³ | < 0,6 | Benchmark efisiensi energi |
| **B. KEUANGAN (25%)** |
| 7 | Keuangan | ROE (Return on Equity) | % | > 0% | Laba bersih / Ekuitas |
| 8 | Keuangan | Rasio Operasi (BOPO) | Rasio | < 1,0 | OPEX / Revenue. Target: < 0,85 (Besar) |
| 9 | Keuangan | Rasio Kas (Cash Ratio) | Rasio | > 1,0 | Kas / Kewajiban Lancar |
| 10 | Keuangan | Efektivitas Penagihan | % | > 90% | Cash collected / Billed amount |
| 11 | Keuangan | Solvabilitas | Rasio | < 1,0 | Total Utang / Total Aset |
| **C. PELAYANAN (25%)** |
| 12 | Pelayanan | Cakupan Pelayanan Teknis | % | > 80% | SR / KK dalam area layanan |
| 13 | Pelayanan | Pertumbuhan Pelanggan | % | > 3% | (SR tahun ini - SR tahun lalu) / SR tahun lalu |
| 14 | Pelayanan | Tingkat Penyelesaian Pengaduan | % | > 80% | Komplain diselesaikan / Total komplain |
| 15 | Pelayanan | Konsumsi Air Domestik | L/org/hari | > 80 | WHO minimum: 60 L/org/hari |
| **D. SDM (15%)** |
| 16 | SDM | Rasio Pegawai per 1.000 Pelanggan | Orang/1000 SR | 4-6 | Target efisiensi. Di atas 10 = overstaffed |
| 17 | SDM | Rasio Diklat | % | > 20% | Pegawai yang ikut pelatihan / Total pegawai |
| 18 | SDM | Produktivitas Pegawai | m³/org/bulan | > 800 | Volume air terjual / Jumlah pegawai |

### Benchmark NRW Internasional

| Kategori | % NRW | ILI | Karakteristik | Contoh Negara |
|----------|-------|-----|---------------|---------------|
| **Excellent** | < 15% | < 2 | Infrastruktur modern, DMA full coverage, ALC proaktif | Singapura, Jepang, Denmark |
| **Good** | 15-25% | 2-4 | Manageable losses, pressure management aktif | Malaysia, Thailand, Chile |
| **Fair** | 25-35% | 4-8 | Typical developing countries, butuh improvement | Indonesia (avg 33,7%), Filipina |
| **Poor** | 35-50% | 8-16 | Infrastruktur tua, minim maintenance, no DMA | India, Bangladesh, Nigeria |
| **Critical** | > 50% | > 16 | Sistem near collapse, massive leakage & theft | Beberapa kota di Afrika, Timur Tengah |

### Benchmark Efisiensi Energi

| Konsumsi Energi | kWh/m³ | Kategori | Karakteristik |
|-----------------|--------|----------|---------------|
| **Sangat Efisien** | < 0,4 | Excellent | Gravitasi dominan, minimal pompa, VSD implementation |
| **Efisien** | 0,4-0,6 | Good | Balanced gravitasi-pompa, pressure management |
| **Rata-rata** | 0,6-0,8 | Fair | Pompa intensif, tanpa VSD, over-pressure |
| **Tidak Efisien** | > 0,8 | Poor | Pompa tua, no optimization, water hammer frequent |

### Benchmark Rasio Keuangan

| Rasio | Formula | Target "Sehat" | Keterangan |
|-------|---------|----------------|------------|
| **ROE** | Laba Bersih / Ekuitas × 100% | > 0% (min), > 10% (ideal) | Mengukur return untuk pemegang saham (Pemda) |
| **BOPO** | OPEX / Revenue | < 0,95 (Kecil), < 0,90 (Sedang), < 0,85 (Besar) | Operating efficiency. Semakin rendah semakin baik |
| **Current Ratio** | Aset Lancar / Kewajiban Lancar | > 1,5 | Kemampuan bayar utang jangka pendek |
| **DSCR** | (EBITDA - Tax) / (Principal + Interest) | > 1,25 | Bankability ratio. DSCR < 1,2 sulit dapat kredit |
| **Collection Rate** | Cash Collected / Billed Amount × 100% | > 90% | Efektivitas penagihan. < 80% = piutang macet tinggi |

---

## RIWAYAT REVISI

| Versi | Tanggal | Perubahan | Penulis |
|-------|---------|-----------|---------|
| 1.0 | 2025-12-22 | Konsolidasi dari 3 file sumber (Dokumen_Terminologi, Kamus_Istilah, File_Referensi). Struktur baru: 6 bagian utama. Tambahan referensi regulasi 2024. | FD Iskandar |

---

**Catatan:** Dokumen ini adalah bagian dari Knowledge Base FD Iskandar untuk konfigurasi AI.  
**Untuk informasi lebih lanjut:** https://rinji.id

---

**END OF DOCUMENT**
