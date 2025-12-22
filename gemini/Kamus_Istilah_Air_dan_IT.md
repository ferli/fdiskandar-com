# **Laporan Komprehensif Standardisasi Terminologi Industri Air dan Teknologi Informasi: Tinjauan Teknis, Operasional, dan Strategi Bisnis**

## **1\. Pendahuluan: Konvergensi Infrastruktur Fisik dan Digital dalam SPAM**

Transformasi industri air minum di Indonesia, yang diwakili oleh Perusahaan Daerah Air Minum (PDAM) dan operator swasta, sedang mengalami pergeseran fundamental. Pergeseran ini bergerak dari manajemen infrastruktur sipil murni menuju pengelolaan berbasis data yang terintegrasi. Dalam konteks Sistem Penyediaan Air Minum (SPAM), tantangan terbesar bukan lagi sekadar membangun bendungan atau menanam pipa, melainkan mengelola aset tersebut secara efisien untuk memenuhi standar Kualitas, Kuantitas, dan Kontinuitas (3K) di tengah tekanan efisiensi biaya.

Untuk memfasilitasi transisi ini, diperlukan pemahaman mendalam yang melintasi batas-batas disiplin ilmu tradisional. Insinyur teknik sipil dan lingkungan yang menguasai hidrolika kini harus berkolaborasi dengan pengembang perangkat lunak yang merancang sistem *Enterprise Resource Planning* (ERP) dan spesialis *Internet of Things* (IoT). Seringkali, kegagalan dalam digitalisasi PDAM disebabkan oleh kesenjangan semantik—ketidakselarasan dalam definisi istilah teknis antara tim operasional lapangan (*Operational Technology* \- OT) dan tim teknologi informasi (IT).

Laporan ini disusun sebagai dokumen referensi otoritatif untuk menjembatani kesenjangan tersebut. Dokumen ini tidak hanya menyajikan definisi, tetapi juga menguraikan konteks fisika, kimia, akuntansi, dan regulasi yang melingkupi setiap istilah. Analisis ini didasarkan pada tinjauan mendalam terhadap literatur teknis, peraturan pemerintah (PP No. 122 Tahun 2015), standar akuntansi keuangan, dan praktik terbaik manajemen aset global.1

Tujuan utamanya adalah menghasilkan landasan pengetahuan bagi penyusunan dokumen TERMINOLOGY.md, sebuah kamus teknis yang menstandardisasi komunikasi di seluruh lapisan organisasi utilitas air. Laporan ini dibagi menjadi lima domain utama: Rekayasa Hidrolika dan Infrastruktur, Proses Pengolahan Air, Manajemen Kehilangan Air (NRW), Transformasi Digital (IT/SCADA), serta Manajemen Keuangan dan Regulasi.

## ---

**2\. Rekayasa Hidrolika, Mekanika Fluida, dan Infrastruktur Sipil**

Pemahaman terhadap terminologi infrastruktur air harus dimulai dari prinsip dasar fisika yang mengatur pergerakan air. Dalam operasional sehari-hari, operator sering mempertukarkan istilah "tekanan" (*pressure*) dan "head" secara keliru, yang berakibat fatal pada pemilihan spesifikasi pompa dan kalibrasi sensor SCADA.

### **2.1 Fisika Aliran: Distingsi Fundamental Antara *Head* dan *Pressure***

Salah satu konsep yang paling sering disalahpahami oleh personel non-teknik (seperti tim IT atau keuangan) adalah konsep *Head*. Dalam fisika pompa, kinerja alat tidak diukur dengan tekanan (bar/psi) melainkan dengan *Head* (meter).

Definisi Head:  
Head merepresentasikan energi total per satuan berat fluida. Secara praktis, Head adalah ketinggian vertikal maksimum di mana pompa mampu mengangkat kolom cairan. Hukum fisika menyatakan bahwa Head bersifat independen terhadap densitas fluida. Sebuah pompa dengan spesifikasi Head 50 meter akan mengangkat air setinggi 50 meter, dan juga akan mengangkat bensin atau merkuri setinggi 50 meter (asalkan daya motor mencukupi).  
Definisi Pressure (Tekanan):  
Tekanan adalah gaya yang diberikan fluida per satuan luas. Berbeda dengan Head, tekanan sangat bergantung pada Specific Gravity (SG) atau berat jenis relatif fluida. Hubungan matematis antara keduanya diturunkan dari Prinsip Bernoulli:

$$\\text{Tekanan (Bar)} \= \\frac{\\text{Head (m)} \\times \\text{SG}}{10.197}$$  
Atau simplifikasi praktis untuk air (SG ≈ 1):

$$1 \\text{ Bar} \\approx 10 \\text{ meter kolom air (m.c.a)}$$  
Implikasi Operasional:  
Dalam sistem SCADA, sensor di lapangan biasanya adalah pressure transmitter yang mengirimkan data dalam satuan Bar atau PSI. Namun, insinyur hidrolika yang menganalisis kurva pompa bekerja dengan satuan meter. Jika tim IT tidak memprogram konversi unit ini dengan memperhitungkan SG (terutama jika air mengandung lumpur pekat atau bahan kimia dengan SG \> 1), maka algoritma kontrol otomatis bisa gagal. Misalnya, sensor tekanan di dasar tangki setinggi 10 meter yang berisi bahan kimia (SG 1.2) akan membaca tekanan 1.17 Bar. Jika sistem dikalibrasi untuk air (SG 1.0), sistem akan "mengira" tangki sudah meluap (karena 1.17 Bar setara 11.7 meter air), padahal level aktual baru 10 meter.4

### **2.2 Dinamika Pompa dan Kurva Sistem**

Jantung dari sistem distribusi adalah pompa. Pemilihan pompa didasarkan pada titik temu antara **Kurva Pompa** (kapasitas alat) dan **Kurva Sistem** (tahanan pipa).

#### **2.2.1 Komponen *Total Dynamic Head* (TDH)**

Untuk mengalirkan air dari titik A ke titik B, pompa harus mengatasi tiga jenis hambatan energi yang secara kolektif disebut TDH:

1. **Static Head (Head Statis):** Perbedaan ketinggian geometris murni antara permukaan air di sisi hisap (*suction*) dan permukaan air di sisi buang (*discharge*). Ini adalah nilai konstan yang tidak dipengaruhi oleh kecepatan aliran.  
2. **Friction Head (Head Gesekan):** Kehilangan energi akibat gesekan air dengan dinding pipa dan turbulensi. Nilai ini meningkat secara eksponensial seiring peningkatan debit aliran (kuadrat dari kecepatan). Pipa tua dengan kerak (*tuberculation*) memiliki koefisien kekasaran yang lebih tinggi, meningkatkan *friction head*.  
3. **Pressure Head (Head Tekanan):** Tekanan sisa yang diinginkan di ujung pipa (misalnya, pelanggan harus menerima air dengan tekanan minimal 0.5 Bar).5

#### **2.2.2 Fenomena Kavitasi dan NPSH**

Istilah teknis yang krusial dalam pemeliharaan aset adalah **Kavitasi**. Ini adalah pembentukan gelembung uap di dalam *impeller* pompa akibat tekanan lokal turun di bawah tekanan uap jenuh air. Ketika gelembung ini bergerak ke area bertekanan tinggi, mereka pecah (*implode*) dengan kekuatan destruktif yang dapat menggerus logam *impeller*.

Untuk mencegah kavitasi, operator harus memahami **Net Positive Suction Head (NPSH)**:

* **NPSHa (Available):** Tekanan mutlak yang tersedia di bibir hisap pompa, ditentukan oleh desain sistem (tinggi tangki hisap).  
* NPSHr (Required): Tekanan minimum yang dibutuhkan pompa agar tidak terjadi kavitasi, ditentukan oleh pabrikan.  
  Syarat mutlak operasional adalah $NPSHa \> NPSHr$. Tim IT yang membangun dasbor pemantauan aset harus menampilkan margin NPSH ini secara real-time untuk memberikan peringatan dini.7

### **2.3 Klasifikasi Infrastruktur SPAM**

Sesuai dengan regulasi PP 122/2015, infrastruktur fisik SPAM dikategorikan ke dalam unit-unit fungsional:

1. **Unit Air Baku (*Raw Water Unit*):** Bangunan pengambilan air.  
   * *Free Intake:* Intake bebas yang mengandalkan gravitasi, digunakan jika level muka air sungai relatif stabil dan tinggi.  
   * *Pontoon Intake:* Intake terapung yang mengikuti fluktuasi level air sungai, dilengkapi pompa *submersible* atau *centrifugal*.  
   * *Broncaptering:* Bangunan penangkap mata air yang melindungi sumber dari kontaminasi permukaan.1  
2. Unit Produksi:  
   Unit ini mencakup Instalasi Pengolahan Air (IPA) atau Water Treatment Plant (WTP). Di sini terjadi proses transformasi dari air baku menjadi air minum. Komponen mekanis utama meliputi Bar Screen (penyaring sampah kasar) dan Grit Chamber (pengendap pasir) untuk melindungi pompa dari abrasi material padat.2  
3. Unit Distribusi:  
   Jaringan perpipaan yang mengantar air ke pelanggan.  
   * *Transmission Main:* Pipa transmisi yang mengalirkan air dari sumber ke WTP atau dari WTP ke reservoir utama, biasanya tanpa sambungan pelanggan langsung.  
   * *Distribution Network:* Pipa yang melayani pelanggan. Dapat berupa sistem *Branch* (cabang/terbuka) atau *Loop* (tertutup). Sistem *Loop* lebih andal karena air dapat mengalir dari dua arah, meminimalkan gangguan saat perbaikan, namun lebih kompleks secara hidrolis.1

### **Tabel Referensi Terminologi: Hidrolika dan Infrastruktur**

Tabel berikut merangkum istilah-istilah kunci yang telah dibahas untuk dimasukkan ke dalam TERMINOLOGY.md.

| Istilah Inggris | Istilah Indonesia | Definisi Praktis & Konteks Operasional |
| :---- | :---- | :---- |
| **Water Supply System** | **Sistem Penyediaan Air Minum (SPAM)** | Kesatuan sarana fisik (teknik) dan non-fisik (manajemen) untuk menyediakan air minum. Terbagi menjadi Unit Air Baku, Produksi, Distribusi, dan Pelayanan. 1 |
| **Raw Water** | **Air Baku** | Air dari sumber alam (sungai, danau, air tanah) yang belum mengalami proses pengolahan apapun. Kualitasnya menentukan kompleksitas unit produksi. 9 |
| **Total Dynamic Head (TDH)** | **Total Head Dinamis** | Total energi (meter) yang harus disuplai pompa untuk melawan beda tinggi statis, gesekan pipa (*friction loss*), dan tekanan sisa yang dibutuhkan. 5 |
| **Static Head** | **Head Statis** | Beda ketinggian vertikal antara permukaan sumber air dan titik pembuangan. Nilai ini tetap tidak peduli seberapa cepat pompa berputar. 7 |
| **Friction Loss** | **Kehilangan Tekanan Akibat Gesekan** | Energi yang hilang menjadi panas akibat gesekan air dengan dinding pipa. Bergantung pada panjang pipa, diameter, kekasaran material, dan kuadrat kecepatan aliran. 5 |
| **Cavitation** | **Kavitasi** | Fenomena "mendidihnya" air pada suhu ruang di dalam pompa akibat tekanan rendah, menyebabkan ledakan gelembung uap yang merusak impeller. 8 |
| **Net Positive Suction Head (NPSH)** | **Tinggi Tekan Hisap Positif Neto** | Parameter kritis untuk mencegah kavitasi. Terdiri dari NPSHa (tersedia di sistem) dan NPSHr (dibutuhkan pompa). NPSHa harus selalu \> NPSHr. 7 |
| **Shut-off Head** | **Head Mati / Head Tutup** | Tekanan maksimum yang dihasilkan pompa pada saat debit aliran nol (katup keluaran ditutup total). Digunakan untuk mengecek kondisi keausan impeller. 8 |
| **Intake Structure** | **Bangunan Sadap / Intake** | Struktur sipil yang dibangun di sumber air (sungai/danau) untuk menyadap air baku dengan kuantitas yang terkendali. 2 |
| **Bar Screen** | **Saringan Kasar / Kisi-kisi** | Jeruji besi di pintu masuk intake yang berfungsi menahan sampah besar (kayu, plastik) agar tidak merusak pompa. 1 |

## ---

**3\. Proses Pengolahan Air dan Parameter Kualitas**

Setelah aspek transportasi air (hidrolika) dipahami, fokus beralih ke rekayasa kimia dan lingkungan dalam Unit Produksi. Terminologi di sini berkaitan dengan perubahan sifat fisik, kimia, dan biologi air untuk memenuhi standar kesehatan (Permenkes No. 492/2010).

### **3.1 Unit Operasi Fisik-Kimia**

Proses pengolahan air konvensional terdiri dari serangkaian unit operasi yang berurutan:

1. Koagulasi (Coagulation):  
   Air baku seringkali mengandung partikel koloid bermuatan negatif yang saling tolak-menolak sehingga tidak bisa mengendap secara alami. Koagulasi adalah proses destabilisasi partikel ini dengan menambahkan bahan kimia koagulan (seperti Tawas/Alumunium Sulfat atau PAC \- Poly Aluminium Chloride) pada bak pengaduk cepat (rapid mixing). Istilah teknis yang sering digunakan operator adalah "Dosing" atau pembubuhan.2  
2. Flokulasi (Flocculation):  
   Setelah partikel stabil, air diaduk secara perlahan (slow mixing) untuk memberikan kesempatan partikel-partikel kecil bertabrakan dan bergabung membentuk gumpalan besar yang disebut Flok. Kualitas flok (ukuran dan berat) sangat menentukan efisiensi tahap selanjutnya.  
3. Sedimentasi (Sedimentation):  
   Flok yang terbentuk memiliki berat jenis lebih besar dari air, sehingga akan mengendap ke dasar bak akibat gaya gravitasi. Di sini dikenal istilah Surface Loading Rate, yaitu beban hidrolis per satuan luas permukaan bak. Desain modern sering menggunakan Plate Settler atau Tube Settler untuk memperluas area pengendapan dalam ruang yang sempit.2  
4. Filtrasi (Filtration):  
   Air yang jernih dari sedimentasi masih mengandung partikel mikro yang tidak mengendap. Air dilewatkan melalui media penyaring (pasir silika, antrasit, atau membran). Di fase ini terjadi proses fisik (penyaringan mekanis) dan biologis (lapisan biofilm memakan bakteri). Istilah penting: Backwash (pencucian balik), yaitu proses membalik arah aliran air dari bawah ke atas untuk membersihkan media filter yang tersumbat kotoran.  
5. Desinfeksi (Disinfection):  
   Langkah terakhir untuk membunuh patogen. Metode paling umum adalah klorinasi. Istilah kunci adalah Sisa Klor (Residual Chlorine), yaitu kadar klorin yang sengaja disisakan dalam air (0.2 \- 0.5 mg/L) untuk mencegah rekontaminasi bakteri saat air mengalir di pipa distribusi menuju rumah pelanggan.1

### **3.2 Parameter Kualitas Air**

Regulasi mewajibkan pemantauan ketat terhadap parameter kualitas:

* **Kekeruhan (*Turbidity*):** Diukur dalam satuan NTU (*Nephelometric Turbidity Unit*). Indikator kejernihan optik air.  
* **pH:** Derajat keasaman. Air minum harus netral (6.5 \- 8.5). pH rendah bersifat korosif (merusak pipa), pH tinggi menyebabkan kerak (*scaling*).  
* **Total Dissolved Solids (TDS):** Jumlah zat padat terlarut.  
* **Parameter Mikrobiologis:** *E. Coli* dan *Total Coliform* harus nol. Kehadirannya mengindikasikan kontaminasi tinja.1

### **Tabel Referensi Terminologi: Pengolahan & Kualitas Air**

| Istilah Inggris | Istilah Indonesia | Definisi Praktis & Konteks Operasional |
| :---- | :---- | :---- |
| **Water Treatment Plant (WTP)** | **Instalasi Pengolahan Air (IPA)** | Fasilitas industri yang memproses air baku menjadi air minum melalui tahapan koagulasi, flokulasi, sedimentasi, filtrasi, dan desinfeksi. 10 |
| **Coagulation** | **Koagulasi** | Proses kimia destabilisasi partikel koloid dalam air dengan menambahkan bahan kimia (koagulan) dan pengadukan cepat. 2 |
| **Flocculation** | **Flokulasi** | Proses pembentukan gumpalan kotoran (flok) yang besar dan berat melalui pengadukan lambat agar mudah diendapkan. 2 |
| **Sedimentation Tank / Clarifier** | **Bak Pengendap / Sedimentasi** | Wadah besar di mana kecepatan air diperlambat sehingga flok dapat turun ke dasar tangki akibat gravitasi. 10 |
| **Filtration** | **Penyaringan / Filtrasi** | Proses melewatkan air melalui media berpori (pasir silika/membran) untuk menahan partikel halus yang lolos dari sedimentasi. 2 |
| **Backwash** | **Pencucian Balik** | Prosedur pembersihan filter dengan mengalirkan air (dan udara) bertekanan dari arah berlawanan untuk membuang kotoran yang tertahan. |
| **Disinfection** | **Desinfeksi / Sucihama** | Pemusnahan mikroorganisme patogen (bakteri, virus) menggunakan bahan kimia (klorin) atau fisik (UV) untuk menjamin keamanan kesehatan. 1 |
| **Residual Chlorine** | **Sisa Klor** | Konsentrasi klorin aktif yang tersisa dalam air distribusi untuk mencegah pertumbuhan kembali bakteri selama perjalanan di pipa. 1 |
| **Turbidity** | **Kekeruhan** | Ukuran kejernihan air (satuan NTU) yang menunjukkan banyaknya partikel tersuspensi yang menghalangi cahaya. 1 |
| **Sludge** | **Lumpur / Endapan** | Limbah padat hasil sampingan dari proses sedimentasi dan backwash filter yang harus diolah lebih lanjut sebelum dibuang. 10 |

## ---

**4\. Manajemen Distribusi dan Pengendalian Kehilangan Air (NRW)**

Efisiensi operasional PDAM diukur secara universal dengan metrik **Non-Revenue Water (NRW)** atau Air Tak Berekening (ATR). NRW yang tinggi (rata-rata nasional Indonesia masih berkisar 30-40%) menandakan inefisiensi yang parah dan ketidakmampuan perusahaan mencapai *Full Cost Recovery*.

### **4.1 Anatomi Kehilangan Air**

Berdasarkan standar *International Water Association* (IWA), NRW dibagi menjadi dua komponen utama yang memerlukan penanganan berbeda:

1. Kehilangan Fisik (Real Losses):  
   Air yang secara fisik keluar dari sistem perpipaan dan tidak sampai ke pelanggan.  
   * *Kebocoran Pipa Transmisi/Distribusi:* Pecah pipa (*pipe burst*) atau bocor sambungan (*joint leak*).  
   * *Luapan Reservoir:* Air yang tumpah karena tangki penuh tetapi pompa tidak mati.  
   * *Kebocoran Dinas:* Bocor pada pipa persil (pipa kecil menuju meter pelanggan).  
   * *Solusi:* Perbaikan infrastruktur, manajemen tekanan, deteksi kebocoran aktif. Ini adalah masalah **Capex/Teknis**.3  
2. Kehilangan Komersial (Apparent Losses):  
   Air yang sampai ke pelanggan dan dikonsumsi, tetapi tidak tercatat atau tidak tertagih.  
   * *Ketidakakuratan Meter:* Meter air tua cenderung "lambat" atau macet, mencatat volume lebih rendah dari aktual.  
   * *Pencurian Air:* Sambungan ilegal (*bypass*) sebelum meteran.  
   * *Kesalahan Administrasi:* Kesalahan input data pembacaan meter atau kesalahan transfer data.  
   * *Solusi:* Penggantian meter, digitalisasi pembacaan meter, audit pelanggan. Ini adalah masalah **Opex/Manajemen**.3

### **4.2 Strategi District Meter Area (DMA)**

Metode standar emas untuk menurunkan NRW fisik adalah pembentukan **District Meter Area (DMA)**. DMA adalah teknik membagi jaringan distribusi yang luas dan kompleks menjadi zona-zona kecil yang terisolasi secara hidrolis (biasanya 1.000 \- 3.000 sambungan rumah).

**Prinsip Kerja DMA:**

* **Isolasi:** Seluruh katup batas (*boundary valve*) ditutup rapat.  
* **Pengukuran:** Air hanya boleh masuk melalui satu atau dua titik yang dipasangi **Meter Induk** (*Flow Meter*).  
* **Analisis:** Selisih antara volume air yang tercatat di Meter Induk DMA dengan total volume meter pelanggan di dalam DMA adalah tingkat kebocoran zona tersebut.

Metode Deteksi (Step Test & MNF):  
Operator melakukan analisis aliran malam minimum (Minimum Night Flow \- MNF), biasanya pukul 02:00 \- 04:00 pagi. Pada jam ini, asumsinya pemakaian pelanggan mendekati nol. Jika Flow Meter induk masih menunjukkan aliran yang besar (misal 5 liter/detik), maka dapat dipastikan ada kebocoran fisik sebesar 5 liter/detik di zona tersebut. Step Test dilakukan dengan menutup katup blok demi blok di dalam DMA untuk mempersempit lokasi kebocoran.3

### **Tabel Referensi Terminologi: NRW dan Distribusi**

| Istilah Inggris | Istilah Indonesia | Definisi Praktis & Konteks Operasional |
| :---- | :---- | :---- |
| **Non-Revenue Water (NRW)** | **Air Tak Berekening (ATR)** | Selisih volume air yang masuk ke sistem distribusi (System Input) dikurangi volume air yang terjual (Billed Authorized Consumption). 3 |
| **Physical / Real Loss** | **Kehilangan Fisik** | Kehilangan air akibat kerusakan fisik infrastruktur (pipa pecah, bocor sambungan, luapan reservoir). Air hilang ke tanah/saluran. 3 |
| **Commercial / Apparent Loss** | **Kehilangan Komersial** | Kehilangan pendapatan akibat air yang dikonsumsi tapi tidak terukur dengan benar (meter rusak, pencurian, *human error* data). 3 |
| **District Meter Area (DMA)** | **Wilayah Meter Distrik** | Subsistem jaringan distribusi yang terisolasi secara hidrolis di mana volume air masuk dan keluar diukur secara permanen untuk memantau kebocoran. 3 |
| **Minimum Night Flow (MNF)** | **Aliran Malam Minimum** | Debit aliran terendah dalam DMA yang terjadi saat pemakaian pelanggan minimal (dini hari). Indikator utama besarnya kebocoran fisik. 3 |
| **Isolation Valve** | **Katup Isolasi** | Katup yang ditutup permanen untuk membentuk batas antar zona DMA. Kebocoran pada katup ini (passing valve) akan mengacaukan data DMA. 3 |
| **Step Test** | **Uji Bertahap** | Metode pencarian kebocoran dengan menutup katup-katup di dalam DMA secara berurutan sambil memantau penurunan debit di meter induk. 3 |
| **System Input Volume** | **Volume Input Sistem** | Total air yang diproduksi dan dimasukkan ke dalam jaringan distribusi. Dasar perhitungan persentase NRW. 3 |
| **Customer Meter** | **Meter Air Pelanggan** | Alat ukur volume di titik serah (Sambungan Rumah) yang menjadi dasar penagihan rekening air. 3 |

## ---

**5\. Transformasi Digital: Konvergensi IT dan OT**

Modernisasi PDAM menuntut integrasi antara Teknologi Operasional (OT) yang mengendalikan fisik air, dan Teknologi Informasi (IT) yang mengelola data bisnis.

### **5.1 SCADA dan IoT: Saraf Sistem Operasi**

**SCADA (*Supervisory Control and Data Acquisition*)** adalah platform pusat kendali. Sistem ini berevolusi dari sistem tertutup berbasis radio menjadi sistem berbasis **IoT (*Internet of Things*)** yang memanfaatkan jaringan seluler dan *cloud*.

* **Arsitektur:** Sensor di lapangan (RTU/PLC) membaca parameter (Level, Flow, Pressure). Data dikirim ke server pusat (Master Station). Operator melihat data melalui HMI (*Human Machine Interface*).  
* **Peran IoT:** Penggunaan *Smart Water Meter* memungkinkan pembacaan meter pelanggan secara otomatis (*Automatic Meter Reading* \- AMR) menggunakan protokol komunikasi hemat daya seperti LoRaWAN atau NB-IoT. Ini menghilangkan *human error* pencatatan manual dan mendeteksi anomali konsumsi secara *real-time*.3

### **5.2 ERP dan Komputasi Awan (*Cloud*)**

Di sisi manajemen bisnis, PDAM beralih ke **ERP (*Enterprise Resource Planning*)** berbasis *Cloud*.

* **Cloud Computing:** Menggantikan server fisik lokal (*On-Premise*) dengan layanan sewa server virtual. Ini mengubah model biaya dari investasi besar di awal (Capex) menjadi biaya langganan bulanan (Opex), serta meningkatkan keandalan data dan kemudahan akses dari mana saja.12  
* **Modul ERP:** Mengintegrasikan Penagihan (*Billing*), Keuangan, Aset, SDM, dan Gudang. Integrasi ini memungkinkan "Pemeliharaan Prediktif". Contoh: Jika SCADA mendeteksi jam operasi pompa sudah mencapai 5.000 jam, ERP otomatis menerbitkan Surat Perintah Kerja (*Work Order*) pemeliharaan dan memesan suku cadang dari gudang.13

### **5.3 API Economy dan Sistem Pembayaran**

Regulasi Bank Indonesia mengenai **SNAP (Standar Open API Pembayaran)** memaksa PDAM membuka sistem penagihannya.

* **API (*Application Programming Interface*):** Jembatan perangkat lunak yang memungkinkan aplikasi Bank atau *E-Commerce* (seperti Tokopedia, Gojek) "berbicara" dengan server tagihan PDAM.  
* **Mekanisme:**  
  1. *Inquiry:* Bank mengirim ID Pelanggan \-\> Server PDAM merespon dengan Nama & Jumlah Tagihan.  
  2. *Payment:* Bank mengirim konfirmasi bayar \-\> Server PDAM menandai lunas (*Flagging*).  
  3. Reversal: Pembatalan transaksi jika terjadi kesalahan.  
     Penggunaan API mengurangi waktu rekonsiliasi keuangan dari hari ke detik (real-time), meningkatkan arus kas perusahaan.14

### **Tabel Referensi Terminologi: Teknologi Informasi & Otomasi**

| Istilah Inggris | Istilah Indonesia | Definisi Praktis & Konteks Operasional |
| :---- | :---- | :---- |
| **SCADA** | **Sistem SCADA** | Sistem kendali terpusat yang memonitor dan mengontrol peralatan lapangan (pompa, katup) secara jarak jauh dan real-time. 3 |
| **Internet of Things (IoT)** | **IoT** | Ekosistem perangkat fisik (sensor, meter) yang terhubung internet untuk mengirim data tanpa interaksi manusia. 3 |
| **Remote Terminal Unit (RTU)** | **Unit Terminal Jarak Jauh** | Komputer mikro di lokasi terpencil (reservoir/intake) yang mengumpulkan data sensor dan mengirimkannya ke pusat SCADA. 3 |
| **Programmable Logic Controller (PLC)** | **PLC** | Komputer industri yang diprogram untuk mengotomatisasi proses elektromekanis (logika: jika air penuh, matikan pompa). 3 |
| **Enterprise Resource Planning (ERP)** | **ERP** | Paket perangkat lunak manajemen bisnis terintegrasi (Billing, Akuntansi, SDM, Logistik) untuk mengelola sumber daya perusahaan. 13 |
| **Cloud Computing** | **Komputasi Awan** | Model penyediaan sumber daya IT (server, database) melalui internet dengan sistem sewa (pay-as-you-go), mengurangi investasi hardware. 12 |
| **API (Application Programming Interface)** | **Antarmuka Pemrograman Aplikasi** | Protokol yang memungkinkan integrasi sistem berbeda (misal: sistem Billing PDAM dengan Mobile Banking) untuk pertukaran data otomatis. 14 |
| **Smart Water Meter** | **Meter Air Pintar** | Meter air digital yang dilengkapi modul komunikasi untuk mengirimkan data volume pemakaian secara otomatis ke server pusat. 3 |
| **Human Machine Interface (HMI)** | **Antarmuka Manusia-Mesin** | Tampilan visual (dashboard) pada layar komputer/tablet yang menyajikan data proses kepada operator manusia untuk pemantauan. 3 |

## ---

**6\. Aspek Keuangan, Akuntansi, dan Regulasi**

Pengelolaan PDAM sebagai BUMD (Badan Usaha Milik Daerah) terikat pada aturan keuangan negara yang ketat. Terminologi keuangan di sektor ini memiliki nuansa spesifik yang berbeda dengan sektor swasta murni.

### **6.1 Capex vs Opex: Strategi Penganggaran**

Pemahaman perbedaan **Capital Expenditure (Capex)** dan **Operational Expenditure (Opex)** vital untuk perencanaan tarif dan investasi.

* **Capex (Belanja Modal):** Pengeluaran untuk aset jangka panjang (\>1 tahun) yang nilainya dikapitalisasi di neraca dan disusutkan (*depreciated*) tiap tahun. Contoh: Pembangunan WTP baru, penggantian pipa transmisi, pembelian server fisik, pemasangan sambungan rumah baru. Sumber dana biasanya dari Penyertaan Modal Pemerintah Daerah (PMPD) atau pinjaman bank.  
* **Opex (Biaya Operasional):** Pengeluaran rutin untuk menjaga aset tetap berfungsi. Contoh: Tagihan listrik pompa (biaya terbesar PDAM), bahan kimia tawas/kaporit, gaji pegawai, biaya langganan *cloud* (SaaS). Opex harus ditutup sepenuhnya oleh pendapatan tarif air agar mencapai *Full Cost Recovery*.17

*Tren Strategis:* Pergeseran ke teknologi *Cloud* dan *SaaS* mengubah komponen biaya IT dari Capex (beli server) menjadi Opex (sewa layanan). Ini menguntungkan karena Opex lebih fleksibel dan tidak memerlukan persetujuan DPRD yang rumit seperti Penyertaan Modal.

### **6.2 Ambiguitas Istilah "PDP"**

Terdapat konflik istilah pada akronim "PDP" yang harus diperjelas dalam kamus teknis:

1. PDP sebagai Akuntansi (Pekerjaan Dalam Pelaksanaan):  
   Dalam standar akuntansi (SAK-ETAP) yang dianut PDAM dan PLN, PDP atau Construction in Progress (CIP) adalah akun neraca yang menampung biaya proyek yang sedang berjalan.  
   * *Isu Kritis:* Biaya di akun PDP **belum disusutkan**. Aset baru mulai disusutkan setelah dipindahbukukan ke "Aset Tetap" saat proyek selesai (commissioning). Seringkali, PDAM membiarkan aset menggantung di PDP meski sudah dipakai, untuk menghindari beban penyusutan yang akan menurunkan laba. Ini adalah temuan audit BPK yang umum.20  
2. PDP sebagai Perencanaan Proyek (Project Development Plan):  
   Dalam konteks kerjasama internasional atau proyek strategis nasional, PDP adalah dokumen perencanaan komprehensif yang berisi studi kelayakan, desain teknis, dan struktur pembiayaan.23  
   * *Rekomendasi:* Dalam TERMINOLOGY.md, istilah ini harus dibedakan labelnya: "PDP (Akuntansi)" dan "PDP (Manajemen Proyek)".

### **6.3 Audit dan Kepatuhan (BPK)**

PDAM diperiksa secara berkala oleh Badan Pemeriksa Keuangan (BPK).

* **Pemeriksaan Keuangan:** Menilai kewajaran laporan keuangan. Targetnya adalah opini WTP (Wajar Tanpa Pengecualian).  
* **Pemeriksaan Kinerja:** Menilai aspek 3E (Ekonomis, Efisien, Efektif). Contoh: Apakah program penurunan NRW yang menghabiskan 10 Miliar benar-benar menurunkan kebocoran sesuai target? Jika tidak efektif, manajemen bisa dianggap merugikan negara.25

### **Tabel Referensi Terminologi: Keuangan & Regulasi**

| Istilah Inggris | Istilah Indonesia | Definisi Praktis & Konteks Operasional |
| :---- | :---- | :---- |
| **Capital Expenditure (Capex)** | **Belanja Modal** | Investasi untuk aset tetap (infrastruktur) yang manfaatnya lebih dari satu tahun. Nilainya disusutkan secara bertahap dalam laporan laba rugi. 17 |
| **Operational Expenditure (Opex)** | **Biaya Operasional** | Biaya rutin operasional dan pemeliharaan sehari-hari. Harus tertutup sepenuhnya oleh pendapatan air agar perusahaan sehat. 17 |
| **Construction in Progress (CIP)** | **Pekerjaan Dalam Pelaksanaan (PDP)** | Akun aset untuk mencatat akumulasi biaya proyek konstruksi yang belum selesai. Aset dalam status ini tidak dikenakan penyusutan. 21 |
| **Project Development Plan** | **Rencana Pengembangan Proyek** | Dokumen strategis pra-proyek yang mencakup studi kelayakan teknis, finansial, dan lingkungan. 24 |
| **Equity Participation** | **Penyertaan Modal Pemerintah (PMP)** | Suntikan dana atau aset dari Pemda kepada PDAM untuk memperkuat struktur modal, biasanya digunakan untuk Capex besar. 28 |
| **Full Cost Recovery (FCR)** | **Pemulihan Biaya Penuh** | Prinsip penetapan tarif di mana pendapatan harus menutup seluruh biaya operasional, pemeliharaan, penyusutan, dan biaya modal. 3 |
| **Performance Audit** | **Pemeriksaan Kinerja** | Audit oleh BPK yang fokus pada penilaian aspek ekonomi, efisiensi, dan efektivitas pencapaian tujuan organisasi, bukan sekadar kewajaran angka. 25 |
| **Unqualified Opinion** | **Opini Wajar Tanpa Pengecualian (WTP)** | Opini audit terbaik yang menyatakan laporan keuangan bebas dari salah saji material dan sesuai standar akuntansi. 25 |
| **Depreciation** | **Penyusutan** | Alokasi sistematis jumlah yang dapat disusutkan dari suatu aset selama umur manfaatnya (beban non-kas yang mengurangi laba). 18 |

## ---

**7\. Penutup dan Rekomendasi Integrasi**

Laporan ini telah menguraikan kerangka kerja terminologi yang komprehensif, mencakup spektrum penuh operasional industri air dari hulu (teknik sipil) hingga hilir (keuangan dan IT). Temuan kunci yang harus diintegrasikan ke dalam implementasi sistem informasi dan dokumen TERMINOLOGY.md adalah:

1. **Akurasi Fisika dalam Kode Program:** Pengembang perangkat lunak wajib membedakan variabel *Head* dan *Pressure* serta memasukkan parameter *Specific Gravity* dalam formula konversi untuk menghindari kesalahan fatal dalam otomasi pompa.  
2. **Disiplin Akuntansi Aset:** Perbedaan tajam antara Capex dan Opex, serta penanganan akun PDP (Pekerjaan Dalam Pelaksanaan), harus tercermin dalam modul *Fixed Asset* pada sistem ERP untuk memastikan kepatuhan terhadap audit BPK.  
3. **Standarisasi Metrik NRW:** Definisi Kehilangan Fisik dan Komersial harus dibakukan sesuai standar IWA dalam sistem pelaporan untuk memandu strategi perbaikan yang tepat sasaran (apakah perlu perbaikan pipa atau penggantian meter).  
4. **Interoperabilitas Melalui API:** Adopsi standar Open API (SNAP) adalah prasyarat mutlak untuk modernisasi sistem pembayaran, menuntut pemahaman mendalam tentang protokol keamanan data.

Dokumen ini diharapkan menjadi referensi tunggal yang menyatukan bahasa antara insinyur, akuntan, dan ahli teknologi dalam ekosistem air minum Indonesia.

**Akhir Laporan**

#### **Works cited**

1. 6 BAB II TINJAUAN PUSTAKA 2.1 Umum Sistem Penyediaan Air ..., accessed December 21, 2025, [https://repo.itera.ac.id/assets/file\_upload/SB2106080004/25116025\_4\_230826.pdf](https://repo.itera.ac.id/assets/file_upload/SB2106080004/25116025_4_230826.pdf)  
2. Gambaran Umum \- Sistem Penyediaan Air Minum (SPAM) \- NUWSP, accessed December 21, 2025, [https://nuwsp.web.id/download/pelatihan/pelatihan/2BB\_GU\_SPAM\_Screen.pdf](https://nuwsp.web.id/download/pelatihan/pelatihan/2BB_GU_SPAM_Screen.pdf)  
3. strategi pengendalian non-revenue water (nrw ... \- Jurnal Purifikasi, accessed December 21, 2025, [https://purifikasi.id/index.php/purifikasi/article/download/450/394/](https://purifikasi.id/index.php/purifikasi/article/download/450/394/)  
4. Head vs Pressure \- North Ridge Pumps, accessed December 21, 2025, [https://www.northridgepumps.com/article-223\_head-vs-pressure](https://www.northridgepumps.com/article-223_head-vs-pressure)  
5. Head pada Sistem Pompa: Pengertian, Rumus, dan Cara Perhitungan Lengkap \- pt tensor, accessed December 21, 2025, [https://pttensor.com/2025/10/29/head-pada-sistem-pompa-pengertian-rumus-dan-cara-perhitungan-lengkap/](https://pttensor.com/2025/10/29/head-pada-sistem-pompa-pengertian-rumus-dan-cara-perhitungan-lengkap/)  
6. Head Pompa, Ketinggian Maksimum Pompa Melawan Gravitasi \- Winston Engineering, accessed December 21, 2025, [https://winstonengineering.com/id/head-pompa/](https://winstonengineering.com/id/head-pompa/)  
7. Apa Itu Head Pompa? Jenis, Komponen, dan Fungsi pada Vacuum Pump, accessed December 21, 2025, [https://vacuumpump.co.id/blog/head-pompa](https://vacuumpump.co.id/blog/head-pompa)  
8. Penjelasan tentang Kepala Pompa: Perhitungan, Rumus, Kurva Kinerja \- Kingda Pump, accessed December 21, 2025, [https://kingdapump.com/id/kepala-pompa/](https://kingdapump.com/id/kepala-pompa/)  
9. Daftar Istilah SDA BK \- dinas sumber daya air dan bina konstruksi, accessed December 21, 2025, [https://sdabk.sumbarprov.go.id/details/pages/55](https://sdabk.sumbarprov.go.id/details/pages/55)  
10. Beberapa Istilah Teknik Lingkungan | PDF \- Scribd, accessed December 21, 2025, [https://id.scribd.com/document/454779777/Beberapa-Istilah-Teknik-Lingkungan](https://id.scribd.com/document/454779777/Beberapa-Istilah-Teknik-Lingkungan)  
11. BAB II TINJAUAN PUSTAKA 2.1 Dasar Teori 2.1.1 Sistem Penyediaan Air Minum 2.1.1.1 Definisi dan Komponen Utama Sistem Penyediaan, accessed December 21, 2025, [https://eprints.upj.ac.id/id/eprint/11531/10/10.%20BAB%20II.pdf](https://eprints.upj.ac.id/id/eprint/11531/10/10.%20BAB%20II.pdf)  
12. 15 Benefits of Cloud Computing for Your Business \- XLSMART, accessed December 21, 2025, [https://www.xlsmart.co.id/bisnis/insights/article/manfaat-cloud-computing-bagi-bisnis/](https://www.xlsmart.co.id/bisnis/insights/article/manfaat-cloud-computing-bagi-bisnis/)  
13. Contoh Penerapan ERP pada Perusahaan Jasa \- HashMicro, accessed December 21, 2025, [https://www.hashmicro.com/id/blog/contoh-penerapan-erp-oleh-6-perusahaan-besar-di-indonesia/](https://www.hashmicro.com/id/blog/contoh-penerapan-erp-oleh-6-perusahaan-besar-di-indonesia/)  
14. 7 Manfaat API Bank bagi Pebisnis dan Developer \- BRIAPI, accessed December 21, 2025, [https://developers.bri.co.id/id/news/7-manfaat-api-bank-bagi-pebisnis-dan-developer](https://developers.bri.co.id/id/news/7-manfaat-api-bank-bagi-pebisnis-dan-developer)  
15. Payment API: Pengertian, Cara Kerja, Manfaat, & Tipsnya, accessed December 21, 2025, [https://pivot-payment.com/blog/payment-api-adalah/](https://pivot-payment.com/blog/payment-api-adalah/)  
16. Open API: Solusi Sistem Transaksi Digital? \- Jalin, accessed December 21, 2025, [https://www.jalin.co.id/id-id/berita/blog/open-api-solusi-sistem-transaksi-digital](https://www.jalin.co.id/id-id/berita/blog/open-api-solusi-sistem-transaksi-digital)  
17. Bedanya CaPex dan OpEx dengan Contoh yang Mudah Dipahami \- Mekari, accessed December 21, 2025, [https://mekari.com/blog/perbedaan-capex-dan-opex/](https://mekari.com/blog/perbedaan-capex-dan-opex/)  
18. Capex Adalah: Arti, Cara Hitung dan Bedanya dengan Opex \- OCBC, accessed December 21, 2025, [https://www.ocbc.id/id/article/2021/09/16/capex-adalah](https://www.ocbc.id/id/article/2021/09/16/capex-adalah)  
19. CaPex dan OpEx: Pengertian, Perbedaan, Contoh, Rumus Hitung \- Bizhare, accessed December 21, 2025, [https://www.bizhare.id/media/keuangan/capex-opex](https://www.bizhare.id/media/keuangan/capex-opex)  
20. Pengakuan pencatatan akuntansi pekerjaan dalam pelaksanaan (PDP) pada PT.PLN (persero) P3B Region Jawa Barat \- Repository UNIKOM, accessed December 21, 2025, [https://repository.unikom.ac.id/12966/](https://repository.unikom.ac.id/12966/)  
21. 1 BAB I PENDAHULUAN 1.1. Latar Belakang Perusahaan merupakan organisasi modern yang mempunyai kegiatan tertentu untuk mencapai t \- Repository UIN Suska, accessed December 21, 2025, [https://repository.uin-suska.ac.id/15889/6/6.%20BAB%201.pdf](https://repository.uin-suska.ac.id/15889/6/6.%20BAB%201.pdf)  
22. 1 BAB I PENDAHULUAN 1.1. Latar Belakang Akuntansi Pekerjaan Dalam Pelaksanaan (PDP) atau dalam istilah akuntansi secara umum dap \- Repository UIN Suska, accessed December 21, 2025, [https://repository.uin-suska.ac.id/14993/6/6.%20BAB%20I\_201875AKT.pdf](https://repository.uin-suska.ac.id/14993/6/6.%20BAB%20I_201875AKT.pdf)  
23. license application for construction of distribution facility \- karpowership sa saldanha bay (rf) proprietary limited index \- NERSA, accessed December 21, 2025, [https://www.nersa.org.za/files/files/2021/12/Licence-application-for-construction-of-distribution-facility-Karpowership-SA-Saldanha-Bay-RF-Proprietary-Limited..pdf](https://www.nersa.org.za/files/files/2021/12/Licence-application-for-construction-of-distribution-facility-Karpowership-SA-Saldanha-Bay-RF-Proprietary-Limited..pdf)  
24. The Project on Integrated Urban Development Master Plan for the City of Nairobi in the Republic of Kenya, accessed December 21, 2025, [https://openjicareport.jica.go.jp/pdf/12184040.pdf](https://openjicareport.jica.go.jp/pdf/12184040.pdf)  
25. Jenis Pemeriksaan BPK \- BPK RI, accessed December 21, 2025, [https://www.bpk.go.id/news/jenis-pemeriksaan-bpk](https://www.bpk.go.id/news/jenis-pemeriksaan-bpk)  
26. Pemeriksaan Kinerja \- BPK RI, accessed December 21, 2025, [https://www.bpk.go.id/assets/files/ihps/2014/I/ihps\_i\_2014\_1414644056.pdf](https://www.bpk.go.id/assets/files/ihps/2014/I/ihps_i_2014_1414644056.pdf)  
27. BPK Audit Kinerja Tiga PDAM \- BPK Perwakilan Provinsi BENGKULU, accessed December 21, 2025, [https://bengkulu.bpk.go.id/bpk-audit-kinerja-3-pdam/](https://bengkulu.bpk.go.id/bpk-audit-kinerja-3-pdam/)  
28. 1\. Penghentian Penyaluran dana Bergulir 2\. Kas dana Bergulir yang tersimpan di Bank Penerima wajib disetorkan ke Rekening Kas Um, accessed December 21, 2025, [https://jdih.pacitankab.go.id/upload/16385/PERDA\_NO\_002\_TAHUN\_2024\_LAMPIRAN\_3.pdf](https://jdih.pacitankab.go.id/upload/16385/PERDA_NO_002_TAHUN_2024_LAMPIRAN_3.pdf)  
29. WALIKOTA BENGKULU PROVINSI BENGKULU PERATURAN DAERAH KOTA BENGKULU NOMOR 1 TAHUN 2020 TENTANG PENAMBAHAN PENYERTAAN MODAL \- Peraturan BPK, accessed December 21, 2025, [https://peraturan.bpk.go.id/Download/157841/PERDA%20NO.%201%20TAHUN%202020%20TTG%20PENAMBAHAN%20PENYERTAAN%20MODAL%20PDAM.pdf](https://peraturan.bpk.go.id/Download/157841/PERDA%20NO.%201%20TAHUN%202020%20TTG%20PENAMBAHAN%20PENYERTAAN%20MODAL%20PDAM.pdf)