# **Dokumentasi Sistem PMA IDigital**

## **1\. PENGENALAN SISTEM**

### **1.1 Objektif dan Tujuan Aplikasi**

Aplikasi **PMA IDigital** (\#Revolusi PMA) dibangunkan khusus untuk kakitangan dan pihak pengurusan **Pondok Moden al-'Abaqirah (PMA)**. Aplikasi berpusat ini bertujuan untuk mendigitalkan dan mempermudahkan seluruh rantaian pengurusan serta penyelesaian tugas harian institusi.

Dengan menggabungkan fungsi pengurusan akademik, hal ehwal pelajar, kokurikulum, fasiliti, dan automasi kecerdasan buatan (AI), aplikasi ini memastikan kakitangan PMA dapat mengakses maklumat penting secara *real-time*, mengurangkan kebergantungan kepada proses manual, serta meningkatkan kecekapan operasi institusi secara menyeluruh.

### **1.2 Keperluan Operasi yang Diselesaikan**

Sebelum pelaksanaan PMA IDigital, pengurusan harian institusi menghadapi beberapa cabaran operasi:

> * **Pengurusan Rekod Manual & Terpisah:** Rekod hafazan pelajar, kehadiran, aduan, dan laporan kesihatan disimpan secara berasingan atau berasaskan kertas, menyukarkan pemantauan terperinci secara pantas.  
> * **Pertindihan Tempahan Fasiliti & Guru Relief:** Ketiadaan sistem tempahan berpusat bagi bilik khas (seperti Makmal Komputer, IFC, Maktabah) dan penyelarasan jadual ganti (Relief) mendedahkan operasi kepada risiko pertindihan masa (clash).  
> * **Jurang Komunikasi Notis & Pengumuman:** Pengumuman rasmi sukar dipastikan sama ada telah dibaca oleh kakitangan atau kumpulan sasaran tertentu.  
> * **Beban Pentadbiran Guru:** Penyediaan Laporan Pengajaran Harian (RPH), laporan aktiviti luar, dan pengurusan jadual peperiksaan mengambil masa yang lama tanpa bantuan automasi.

PMA IDigital menyelesaikan isu-isu ini dengan menyediakan satu platform bersepadu yang berasaskan awan (cloud-based), selamat, dan boleh dicapai pada bila-bila masa.

### 

### 

### 

### 

### **1.3 Gambaran Keseluruhan Fungsi Utama**

Sistem PMA IDigital dibahagikan kepada 5 modul teras utama:

| Modul Utama | Fungsi & Fitur Kunci | Kumpulan Sasaran |
| ----- | ----- | ----- |
| **1\. Akademik & Hafazan** | Pemantauan hafazan Al-Quran (E\_HUFFAZ), pengurusan jadual waktu (E\_JADUAL), penjanaan jadual peperiksaan PDF (E\_PEPERIKSAAN), dan pembantu penyediaan RPH berasaskan AI (AI RPH). | Guru, Penyelaras Akademik, Mudir |
| **2\. Hal Ehwal pelajar (HEP) & Kebajikan** | Rekod kehadiran pelajar (E\_KEHADIRAN), profil kesihatan & MC (E\_KESIHATAN), pangkalan data kebajikan & pendapatan keluarga (E\_KEBAJIKAN), serta kawalan bilik darjah (E\_CLASS). | Guru Kelas, Guru Bertugas, Unit HEP |
| **3\. Kokurikulum** | Pengurusan pendaftaran unit/rumah sukan (E\_KOKO DATA GURU/PELAJAR), perekodan kehadiran aktiviti (E\_KOKO KEHADIRAN), dan pelaporan aktiviti dalam/luar sekolah (E\_KOKO LAPORAN). | Penyelaras Koko, Guru Penasihat |
| **4\. Operasi, Logistik & Fasiliti** | Tempahan bilik khas/peralatan (E\_TEMPAH), semakan jadual guru ganti (E\_RELIEF), permohonan kenderaan institusi (E\_TRANSPORT), serta pengurusan jadual guru bertugas & warden. | Pentadbir, Pemandu, Semua Staf |
| **5\. Komunikasi & Alatan Pintar AI** | Penyampaian pengumuman berserta jejak pembaca (E\_PENGUMUMAN), modul Abqari AI, alatan transkripsi audio/imej kepada teks (AI AUDIO TO TEXT, AI IMAGE TO TEXT), dan Kamus Istilah (DIGIGlosari). | Semua Kakitangan PMA |

💡 **Tip:** Aplikasi PMA IDigital direka bentuk fleksibel untuk diakses melalui peranti mudah alih (iOS/Android) mahupun pelayar web desktop bagi memudahkan tugas di dalam atau di luar bilik darjah.

⚠️ **Nota:** Akses kepada Borang dan View dikawal secara dinamik berdasarkan peranan pengguna (Role-Based Access Control) seperti Admin, Mudir, Penyelaras, atau Guru Biasa bagi menjaga kerahsiaan data peribadi pelajar dan staf.

## 

## **2\. SENIBINA DATA**

Aplikasi PMA IDigital dibina di atas pangkalan data berasaskan awan (cloud) yang sangat ekstensif, merangkumi sejumlah **61 jadual (tables)** dan **4582 lajur (columns)** secara keseluruhan.

### **2.1 Senarai Jadual Utama (Tables)**

Oleh kerana terdapat ratusan jadual (termasuk jadual janaan automatik untuk automasi proses/bot), jadual-jadual ini boleh diklasifikasikan kepada 6 kumpulan modul utama:

| Kategori Modul | Contoh Jadual Utama | Tujuan & Fungsi |
| ----- | ----- | ----- |
| **1\. Pengguna & Teras** | DATA GURU, DATA PELAJAR, DATA ALUMNI | Menyimpan profil dan rekod peribadi kakitangan, pelajar, dan alumni. Bertindak sebagai pangkalan data rujukan utama. |
| **2\. Akademik & Hafazan** | E\_HUFFAZ DATA, E\_HUFFAZ REKOD, JADUAL AKADEMIK, E\_PEPERIKSAAN | Mengurus rekod hafazan secara individu, pendaftaran subjek kelas, susunan jadual waktu pengajaran, dan pemantauan peperiksaan. |
| **3\. Hal Ehwal pelajar** | E\_KEHADIRAN, E\_KESIHATAN, E\_KEBAJIKAN, E\_CLASS\_REKOD KAWALAN KELAS | Merekodkan status kehadiran harian setiap kelas, data kesihatan (termasuk rekod MC), latar belakang pendapatan keluarga, dan kawalan disiplin bilik darjah. |
| **4\. Kokurikulum** | E\_KOKO DATA GURU, E\_KOKO LAPORAN, E\_KOKO KEHADIRAN | Pangkalan data bagi setiap unit uniform/kelab berserta perekodan kehadiran pelajar dan pengesahan laporan aktiviti mingguan. |
| **5\. Operasi & Fasiliti** | E\_TEMPAH DATA, E\_TEMPAH REKOD, E\_RELIEF, E\_TRANSPORT REKOD | Mengurus inventori dan slot tempahan bilik khas (seperti IFC, Maktabah), pengurusan jadual guru ganti, dan permohonan penggunaan kenderaan institusi. |
| **6\. Sistem & Automasi** | MENU APP, NOTIFICATION, MAINTENANCE, Process for... (Pelbagai jadual) | Jadual kawalan menu navigasi, jejak status penyelenggaraan, notifikasi push, dan puluhan jadual log proses (Process Tables) untuk janaan PDF dan Webhook AI. |

### **2.2 Hubungan Antara Jadual (Ref & Virtual Columns)**

Aplikasi ini memanfaatkan sistem pangkalan data hubungan (relational database) di dalam AppSheet menggunakan fungsi Ref dan Virtual Columns bagi mengelakkan pertindihan data.

> * **Rujukan Sambungan (Ref):** Digunakan apabila satu rekod perlu mengambil data secara langsung daripada jadual lain.  
  * *Contoh:* Di dalam jadual E\_TEMPAH REKOD, lajur BILIK TEMPAHAN disetkan sebagai jenis data Ref yang merujuk terus kepada jadual E\_TEMPAH DATA. Ini memastikan senarai bilik yang ditempah sentiasa padan dengan bilik rasmi yang wujud dalam pangkalan data fasiliti.  
> * **Lajur Maya (Virtual Columns):** AppSheet akan menjana lajur maya secara automatik menggunakan formula REF\_ROWS() bagi menyenaraikan rekod berkaitan (Related Records).  
  * *Contoh 1:* Dalam jadual DATA GURU, terdapat lajur maya seperti Related E\_STAF HADIRs dan Related DATA JADUALs. Ini membolehkan admin melihat semua rekod kehadiran staf dan jadual akademik hanya dari paparan profil guru tersebut.  
  * *Contoh 2:* Dalam jadual E\_TEMPAH DATA, wujud lajur maya Data E\_TEMPAH REKOD yang akan memaparkan senarai siapa yang telah menempah bilik tertentu pada bila-bila masa.

### **2.3 Kunci Primer (Primary Keys)**

Setiap jadual memerlukan Kunci Primer (Primary Key) yang unik untuk mengenal pasti setiap baris rekod secara spesifik:

> 1. **Penggunaan Formula UNIQUEID():** Secara amnya, jadual transaksi harian (seperti E\_HUFFAZ REKOD dan E\_RELIEF) menggunakan lajur UID yang dijana oleh formula UNIQUEID() bagi memastikan nilai tersebut 100% unik setiap kali rekod ditambah.  
> 2. **Kunci Primer Kod Tersuai (Custom ID):** Terdapat jadual menggunakan formula ID pintar. Sebagai contoh, jadual E\_TEMPAH REKOD menghasilkan kunci di lajur ID TEMPAH dengan format: \=CONCATENATE("TEMP-", TEXT(TODAY(), "YYMMDD"), "-", UPPER(LEFT(UNIQUEID(), 4))). (Contoh *output*: TEMP-240518-A1B2).  
> 3. **Kunci Primer Tetap (Fixed Keys):**  
   * Jadual DATA PELAJAR: Menggunakan NO MATRIK sebagai Key.  
   * Jadual DATA GURU: Menggunakan UID (dengan nilai awalan seperti "PMA01") sebagai Key.  
   * Jadual tetapan/susunan seperti MENU APP dan MAINTENANCE: Menggunakan nilai turutan iaitu lajur BIL (dengan formula awalan \=\[\_RowNumber\]-1) sebagai Key.

### **2.4 Jenis Data Utama (Data Types)**

Sistem menggunakan jenis data khusus untuk mengoptimumkan Antara Muka Pengguna (UX) dan memudahkan kemasukan rekod.

> * **Teks & Nombor Asas (Text, Number, LongText):**  
  * LongText: Digunakan untuk nota panjang yang menyokong format perenggan seperti lajur PENGUMUMAN atau lajur ulasan LAPORAN.  
  * Number: Rekod helaian hafazan MUKA SURAT atau bilangan hari cuti sakit (BIL HARI MC).  
> * **Format Kewangan (Price):**  
  * Digunakan di dalam jadual E\_KEBAJIKAN (seperti lajur PENDAPATAN BAPA dan JUMLAH PENDAPATAN), memaparkan simbol "RM" bersama pemisah ribuan secara automatik.  
> * **Pilihan Pra-ditetapkan (Enum & EnumList):**  
  * Enum: Pengguna hanya boleh memilih SATU pilihan. Contohnya lajur STATUS TEMPAHAN (pilihan: *BERJAYA, PENDING, KONFLIK*).  
  * EnumList: Pengguna boleh menanda (tick) LEBIH DARI SATU pilihan. Contohnya lajur PELAJAR KELAS 1 TIDAK HADIR dalam modul E\_KEHADIRAN atau pelbagai blok MASA TEMPAH serentak.  
> * **Data Berkaitan Kalendar (Date, Time, DateTime):**  
  * Setiap borang laporan yang dihantar secara automatik menangkap data TIMESTAMP (menggunakan fungsi \=NOW()). Masa tempahan bilik atau pergerakan relief merujuk kepada jenis data Time (MASA MULA, MASA TAMAT).  
> * **Logik / Peranan (Yes/No):**  
  * Mewakili *Boolean* (True/False). Di dalam DATA GURU, terdapat pelbagai kawalan sistem seperti lajur ADMIN, MUDIR, NM HEP, dan WARDEN. Tetapan ini membolehkan pangkalan data menyaring akses berdasarkan status *Yes*.  
> * **Media Akses (Image, File, Url):**  
  * Image: Mengambil dan memaparkan fail imej (seperti GAMBAR PROFIL atau bukti gambar laporan aktiviti kokurikulum di lajur GAMBAR 1 hingga GAMBAR 4).  
  * File: Menyimpan janaan automatik Jadual Peperiksaan atau PDF permohonan ke dalam sistem.  
  * Url: Menyimpan hiperpautan (Hyperlink) kepada navigasi halaman luaran dalam modul Menu.

💡 **Tip Senibina AppSheet:** Untuk mengekalkan kelajuan aplikasi bagi pangkalan data yang mencecah ribuan rekod (terutama rekod kehadiran harian), penggunaan fungsi Security Filters (seperti memaparkan data bulan semasa sahaja) di peringkat senibina data adalah penting sebelum data dipindahkan ke peranti pengguna.

⚠️ **Nota:** Lajur yang mengandungi Maklumat Sensitif (seperti NO KP, NO TEL BAPA/IBU dan EMAIL ID) diletakkan di bawah pengkategorian privasi *Sensitive Data* bagi mematuhi piawaian perlindungan maklumat di dalam AppSheet.

## 

## 

## 

## 

## 

## **3\. Logik Operasi & FORMULA**

Sistem **PMA IDigital** bergantung secara meluas kepada enjin formula AppSheet untuk mengawal Logik Operasi, mengesahkan integriti data, mengira data secara automatik melalui Virtual Columns, dan mengehadkan kebenaran menyunting mengikut peranan pengguna.

### **3.1 Formula Utama dalam Lajur Maya (Virtual Columns)**

Lajur Maya (Virtual Columns) digunakan untuk membuat pengiraan secara *real-time* tanpa mengubah struktur fizikal pangkalan data asal.

| Modul / Jadual | Nama Lajur Maya | Formula AppSheet | Penjelasan Logik Mudah |
| ----- | ----- | ----- | ----- |
| **E\_HUFFAZ REKOD** | JUZUK | \=IF(\[MUKA SURAT\] \= 0, 0, IF(CEILING((\[MUKA SURAT\] \- 1\) / 20.0) \<= 30, CEILING((\[MUKA SURAT\] \- 1\) / 20.0), 30)) | 🔍 Mengira juzuk Al-Quran secara automatik berdasarkan nombor muka surat yang dimasukkan oleh pelajar (pembahagian 20 muka surat per juzuk). |
| **E\_HUFFAZ REKOD** | MUKA SURAT TERKINI | \=LOOKUP(MAXROW("E\_HUFFAZ REKOD", "MUKA SURAT", \[NAMA PELAJAR\] \= \[\_THISROW\].\[NAMA PELAJAR\]), "E\_HUFFAZ REKOD", "UID", "MUKA SURAT") | 🔍 Mengambil nombor muka surat hafazan paling tinggi yang pernah direkodkan bagi pelajar berkenaan sebagai rujukan awal. |
| **E\_JADUAL DATA** | BIL MASA | \=FLOOR((TOTALMINUTES(\[MASA AKHIR\] \- \[MASA MULA\]) / 30)) & " MASA" | 🔍 Mengira jumlah blok masa (30 minit setiap blok) berdasarkan julat waktu mula dan waktu tamat mengajar. |
| **E\_JADUAL DATA** | StopNotiCutiExam | \=ISNOTBLANK(SELECT(E\_TAQWIM\[KATEGORI\], AND(OR(\[KATEGORI\] \= "PEPERIKSAAN", \[KATEGORI\] \= "CUTI", \[KATEGORI\] \= "CUTI UMUM"), TODAY() \>= \[TARIKH MULA\], TODAY() \<= \[TARIKH TAMAT\]))) | 🔍 Menyemak samada hari ini jatuh pada tarikh Peperiksaan atau Cuti dalam E\_TAQWIM bagi menghentikan penghantaran notifikasi jadual biasa secara automatik. |
| **E\_PENGUMUMAN** | COUNT DIBACA | \=CONCATENATE("👀 Jumlah Pembaca: ", COUNT(\[DIBACA OLEH\])) | 🔍 Mengira bilangan unik e-mel pengguna yang telah membuka dan membaca sesuatu pengumuman rasmi. |
| **E\_PENGUMUMAN** | TARIKH TAMAT TEMPOH | \=DATE(\[TIMESTAMP\]) \+ NUMBER(LEFT(\[TEMPOH PENGUMUMAN\], FIND(" ", \[TEMPOH PENGUMUMAN\]) \- 1)) | 🔍 Mengira tarikh luput pengumuman secara dinamik berdasarkan pilihan tempah paparan (contoh: "3 HARI"). |

### 

### **3.2 Logik Valid\_If, Show\_If, Required\_If & Editable\_If**

Aplikasi ini menggunakan ekspresi syarat untuk mengawal aliran borang (Dynamic Forms) serta memastikan integriti data.

#### **1\. Pengesahan Data & Sekatan Konflik (Valid\_If)**

> * **Kawalan Had Tempahan Bilik (E\_TEMPAH REKOD \-\> ID TEMPAH):**

> AND(  
>   COUNT(SELECT(E\_TEMPAH REKOD\[ID TEMPAH\], AND(\[NAMA PEMOHON\] \= \[\_THISROW\].\[NAMA PEMOHON\], \[TARIKH\] \= \[\_THISROW\].\[TARIKH\], \[BILIK TEMPAHAN\] \= \[\_THISROW\].\[BILIK TEMPAHAN\]))) \< 1,  
>   COUNT(SELECT(E\_TEMPAH REKOD\[ID TEMPAH\], AND(\[NAMA PEMOHON\] \= \[\_THISROW\].\[NAMA PEMOHON\], WEEKNUM(\[TARIKH\]) \= WEEKNUM(\[\_THISROW\].\[TARIKH\]), \[BILIK TEMPAHAN\] \= \[\_THISROW\].\[BILIK TEMPAHAN\]))) \< 3  
> )

> *📖 Penjelasan:* Menghalang pengguna membuat tempahan bilik yang sama melebihi **1 kali sehari** atau **3 kali seminggu**. Sekiranya dilanggar, mesej amaran amaran tersuai akan dipaparkan: *"⚠️ Anda telah melepasi had tempahan HARIAN dan MINGGUAN"*.

> * **Penapisan Guru Lenggang / Relief (E\_RELIEF \-\> NAMA GURU):**

> SELECT(E\_JADUAL DATA\[GURU\], NOT(IN(\[GURU\], SELECT(E\_JADUAL DATA\[GURU\], AND(\[HARI\] \= \[\_THISROW\].\[HARI\], OR(AND(\[MASA MULA\] \<= \[\_THISROW\].\[MASA\_MULA\], \[MASA AKHIR\] \> \[\_THISROW\].\[MASA\_MULA\]), ...))))))

> *📖 Penjelasan:* Menapis senarai drop-down guru secara dinamik untuk hanya memaparkan guru yang **TIDAK mengajar** pada slot waktu dan hari tersebut bagi jawatan guru ganti.

> * **Pilihan Slot Masa Bebas Pertindihan (E\_TEMPAH REKOD \-\> MASA TEMPAH):** Suggested\_Values menggunakan penolakan senarai senarai SPLIT(...) \- SPLIT(...) untuk menolak slot masa yang sudah ditempah oleh pengguna lain pada tarikh dan bilik yang sama.

> 

#### **2\. Borang Dinamik (Show\_If & Required\_If)**

> * **Aduan & Kebajikan (E\_KESIHATAN \-\> BIL HARI MC):**  
  * Show\_If & Required\_If: \=\[TINDAKAN\] \= "PULANG (MC)"  
  * *📖 Penjelasan:* Medan bilangan hari MC hanya dipaparkan dan diwajibkan diisi jika tindakan yang dipilih adalah "PULANG (MC)".  
> * **Tujuan Tempahan (E\_TEMPAH REKOD \-\> TUJUAN LAIN):**  
  * Show\_If & Required\_If: \=\[TUJUAN\] \= "LAIN-LAIN"  
  * *📖 Penjelasan:* Mengaktifkan ruangan teks catatan hanya jika pengguna memilih kategori tujuan "LAIN-LAIN".

#### **3\. Hak Akses Menyunting (Editable\_If)**

> * **Pengurusan Peranan Kakitangan (DATA GURU \-\> ADMIN / MUDIR / NM HEP):**  
  * Editable\_If: \=IN(USEREMAIL(), SELECT(DATA GURU\[EMAIL ID\], \[ADMIN\]=TRUE))  
  * *📖 Penjelasan:* Lajur penetration peranan pentadbir dikunci daripada disunting oleh pengguna biasa dan hanya boleh diubah oleh pengeluar sistem bertaraf Admin.

### **3.3 Security Filters (Penapisan Capaian Data)**

Untuk memastikan prestasi aplikasi kekal pantas di peranti mudah alih dan menjaga privasi, *Security Filters* digunakan di peringkat pelayan (server-side).

⚠️ **Nota Keselamatan:** Data pelajar dan maklumat peribadi ibu bapa (seperti NO KP, PENDAPATAN BAPA, NO TEL BAPA/IBU) disetkan dengan kategori *Sensitive Data* supaya tidak mudah terdedah tanpa kebenaran peranan yang sah.

### **3.4 Slices & Tujuan Penapisan Data**

Sistem PMA IDigital mengandungi **67 Slices** yang bertindak sebagai pandangan data tersaring (filtered view) daripada jadual induk.

| Nama Slice Utama | Jadual Induk | Syarat Penapisan (Filter Expression) | Tujuan / Peranan |
| ----- | ----- | ----- | ----- |
| HOME | E\_TEMPAH REKOD | \=\[TARIKH\] \>= TODAY() | Memaparkan senarai tempahan bilik yang aktif dan akan datang sahaja di halaman utama. |
| Filter Relief Today\_Form | E\_RELIEF | \=\[TARIKH\] \= TODAY() | Menyaring jadual guru ganti bagi hari semasa sahaja untuk elak kekeliruan staf bertugas.  |
| Status Akses Exam | STATUS AKSES EXAM | \=\[STATUS AKSES\] \= TRUE | Membenarkan guru mengakses soalan peperiksaan hanya apabila mod kawalan peperiksaan dibuka oleh Penyelaras Peperiksaan. |
| Useremail Filtered\_Form | Abqari\_Ai | \=\[EMAIL\] \= USEREMAIL() | Memastikan perbualan AI pembantu peribadi (Abqari\_Ai) diasingkan mengikut akaun pengguna secara individu. |

💡 **Tip Prestasi:** Penggunaan Slices berasaskan tarikh TODAY() mengurangkan saiz memori peranti pengguna semasa membuat segerakan (*synchronization*) harian.

## **4\. ANTARA MUKA PENGGUNA (UX)**

Antara muka pengguna (UX) aplikasi **PMA IDigital** direka menggunakan tema berasaskan warna **White \- \#00acc1** dan fon jenis **Rubik** untuk memberikan visual yang bersih, moden, serta mudah dibaca pada pelbagai saiz skrin peranti. Papan pemuka sistem memuatkan **370 Views**, **429 Actions**, dan **105 Format Rules** bagi memastikan pengalaman pengguna yang lancar dan dinamik.

### **4.1 Senarai Views & Jenis Paparan Utama**

Secara keseluruhan, aplikasi ini memanfaatkan pelbagai jenis paparan (View Types) di dalam AppSheet bagi memenuhi keperluan tugas harian kakitangan:

| Kategori View | Nama View Utama | Jenis Paparan | Sumber Data / Slice | Fungsi & Pengguna Sasaran |
| ----- | ----- | ----- | ----- | ----- |
| **Papan Utama** | Kemaskini Terkini *Default Start View* | Deck / Detail | E\_PENGUMUMAN / HOME | Halaman permulaan apabila aplikasi dibuka. Memaparkan notis, pengumuman terkini, dan tempahan aktif. |
| **Navigasi Menu** | Menu Utama | Gallery / Table | MENU APP | Hub navigasi utama berasaskan ikon kad untuk mengakses ke semua modul perkhidmatan. |
| **Akademik** | E\_JADUAL | Table / Calendar | E\_JADUAL DATA | Memaparkan susunan jadual pengajaran harian dan mingguan guru. |
| **Akademik** | Jadual Peperiksaan | Table / Deck | E\_PEPERIKSAAN / Status Akses Exam | Semakan soalan dan jadual peperiksaan mengikut status kawalan akses. |
| **Hafazan** | E\_HUFFAZ | Deck / Form | E\_HUFFAZ REKOD | Perekodan pencapaian harian muka surat dan pengiraan juzuk hafazan pelajar. |
| **HEP & Disiplin** | Kawalan Kelas | Form / Deck | E\_CLASS\_REKOD KAWALAN KELAS | Borang kawalan disiplin dan suasana bilik darjah oleh guru waktu semasa. |
| **Fasiliti** | E\_TEMPAH | Form / Calendar | E\_TEMPAH REKOD / HOME | Borang tempahan slot bilik khas (IFC, Maktabah, Makmal Komputer). |
| **Operasi** | Guru Relief | Form / Table | E\_RELIEF / Filter Relief Today\_Form | Pilihan dan penetapan guru ganti yang lenggang bagi slot pengajaran terjejas. |
| **AI Smart Tools** | Abqari AI | Form / Detail | Abqari\_Ai / Useremail Filtered\_Form | Antara muka perbualan AI interaktif bagi pembantu tugas pentadbiran. |

### 

### 

### 

### 

### **4.2 Struktur Navigasi (Navigation Hierarchy)**

Navigasi aplikasi disusun dalam dua tahap utama untuk memudahkan navigasi pantas (one-tap access):

\[ APLIKASI PMA IDigital \]  
   │  
   ├── 1\. Primary Navigation Bar (Bar Navigasi Bawah)  
   │     ├── Kemaskini Terkini (Start View \- Notis & Status Ringkas)  
   │     ├── Jadual Saya (Jadual Pengajaran & Relief)  
   │     ├── Menu Utama (Hub Modul Berasaskan Kad Ikon)  
   │     ├── Abqari AI (Sembang Pembantu AI)  
   │     └── Profil (Profil Kakitangan & Tetapan)  
   │  
   └── 2\. Menu Navigation (Akses Modul Terperinci dari MENU APP)  
         ├── Modul Akademik & Peperiksaan  
         ├── Modul Hal Ehwal pelajar & Kebajikan  
         ├── Modul Kokurikulum  
         └── Modul Operasi, Transport & Fasiliti

💡 **Tip UX Navigasi:** Pengguna boleh menatal (*swipe*) ke kiri atau ke kanan di halaman utama untuk berpindah antara paparan jadual, pengumuman, dan profil tanpa perlu menekan butang menu berulang kali.

### **4.3 Tindakan Butang & Actions**

Sistem dilengkapi dengan **429 Actions** yang disesuaikan mengikut konteks borang dan status data. Sistem juga menggunakan pemetaan teks tindakan dalam Bahasa Melayu:

#### **1\. Pemetaan Tindakan Asas Sistem (System Action Mappings)**

> * **Save (Simpan):** Diubah secara dinamik mengikut View. Pada borang AI (Abqari\_Ai\_Form & Useremail Filtered\_Form), label bertukar kepada **"Tanya"**, manakala pada borang standard memaparkan **"Simpan"**.  
> * **Edit:** Dipaparkan sebagai **"Sunting"**.  
> * **Delete:** Dipaparkan sebagai **"Padam"**.  
> * **Submit:** Dipaparkan sebagai **"Hantar"**.  
> * **Cancel / Discard:** Dipaparkan sebagai **"Batal"** / **"Buang"**.  
> * **Next / Prev:** Dipaparkan sebagai **"Seterusnya"** / **"Sebelumnya"**.

#### **2\. Actions Tersuai Utama (Custom Actions)**

> * **Janaan PDF Otomatik:** Action jenis App: open a file yang membuka dokumen laporan rasmi yang telah dijana oleh bot (contoh: Laporan Kokurikulum PDF atau Jadual Peperiksaan).  
> * **Tindakan Semakan (Approval Action):** Butang khusus pada paparan E\_KOKO LAPORAN dan E\_LAPORAN RELIEF untuk Penyelaras mengubah status daripada *"BELUM DISEMAK"* kepada *"TELAH DISEMAK"* dengan satu sentuhan.  
> * **Kawalan Suis Akses Peperiksaan:** Action khas dalam jadual STATUS AKSES EXAM untuk menukar fungsi Boolean (TRUE/FALSE) secara serta-merta bagi membuka atau mengunci akses bahan peperiksaan kepada guru.

### **4.4 Peraturan Format Visual (Format Rules)**

Sebanyak **105 Format Rules** dikonfigurasi bagi memberikan penandaan visual (color coding & icons) berdasarkan syarat logik data secara dinamik:

\[Syarat Logik\]                            \[Penyampaian Visual UX\]  
\----------------------------------------------------------------------------------  
\[STATUS\] \= "DIBUKA"                  \---\> 🟢 Teks Hijau \+ Ikon Check Circle  
\[STATUS\] \= "TUTUP"                   \---\> 🔴 Teks Merah \+ Ikon Times Circle  
\[STATUS\] \= "PENDING / BELUM DISEMAK" \---\> 🟡 Teks Kuning \+ Ikon Exclamation Circle  
\[TARIKH TAMAT\] \< TODAY()             \---\> Teks Bergaris Potong (Strikethrough)  
\[STATUS AKSES EXAM\] \= TRUE           \---\> 🔓 Teks Hijau Tebal \+ Ikon Lock Open  
\[STATUS AKSES EXAM\] \= FALSE          \---\> 🔒 Teks Merah Tebal \+ Ikon Lock Alt

⚠️ **Nota Keselamatan UX:** Elemen butang sensitif seperti *Padam* atau *Tukar Peranan Admin* dilindungi dengan pengesahan pop-up **"Adakah anda pasti?"** bagi mengelakkan terpadam data secara tidak sengaja semasa pengendalian di peranti mudah alih.

## **5\. AUTOMASI & PROSES**

Automasi dalam **PMA IDigital** dikuasai oleh enjin **AppSheet Automation (Bots, Events, Processes, & Tasks)**. Enjin automasi ini bertindak secara latar belakang (background process) untuk menguruskan notifikasi *real-time*, janaan dokumen PDF rasmi, semakan konflik permohonan, pembersihan data lama, serta integrasi dengan perkhidmatan AI dan skrip luaran.

### **5.1 Gambaran Keseluruhan Enjin Automasi**

Setiap proses automasi di dalam PMA IDigital terdiri daripada tiga komponen teras:

> 1. **Event (Trigger):** Syarat pencetus seperti perubahan data (Data Change: *ADDS*, *UPDATES*, *DELETES*) atau masa berjadual (Scheduled/Timer).  
> 2. **Process:** Aliran kerja yang mengandungi satu atau beberapa langkah logik (Steps, Branching/Condition).  
> 3. **Task:** Tindakan akhir yang dilaksanakan (seperti *Send Noti*, *Create PDF File*, *Call Webhook*, atau *Call Apps Script*).

### 

### 

### 

### **5.2 Kategori Bots Utama & Triggers**

Aplikasi ini mempunyai puluhan bot berasaskan jadual proses (Process State Tables). Berikut adalah pengkategorian bot-bot utama mengikut fungsi operasi:

| Kategori Bot | Contoh Nama Bot / Process Table | Pencetus (Trigger Event) | Tugas & Tindakan (Tasks Executed) |
| :---- | :---- | :---- | :---- |
| **Notifikasi Noti Bilik Khas** | Process for Noti MAKMAL KOMP, Process for Noti IFC, Process for Noti MAKTABAH, Process for Noti B Turath, Process for Noti PANTRY, Process for Noti JIL, Process for Noti JLC | **Data Change** (*ADDS* pada E\_TEMPAH REKOD) | Menghantar *Push Notification* dan merekod log ke Noti Record Output untuk pemakluman tempahan bilik khas. |
| **Kawalan & Semakan Konflik** | Process for Konflik | **Data Change** (*ADDS / UPDATES* pada tempahan) | Melaksanakan periksa syarat PROCESS SEMAKAN Output, penangguhan 5 MINIT WAITING Output, kemaskini STATUS BERJAYA Output jika tiada pertindihan, atau STATUS KONFLIK Output dan pemadaman DELETE KONFLIK Output jika wujud pertindihan. |
| **Janaan Dokumen PDF** | Process for pdf, Process for pdf 2 hingga Process for pdf 7 | **Data Change** (Perubahan status laporan kepada *"TELAH DISEMAK"*) | Menjana fail PDF berdasarkan templat Google Docs dan menyimpan pautan fail ke dalam lajur PDF / Link PDF Output. |
| **Integrasi Pembantu AI** | Process for New Bot 55-6, Process for New Bot 55-8, Process for New Bot 55-9, Process for New Bot 84-1, Process for New Bot 85-1 | **Data Change** (*ADDS* borang soalan AI / RPH) | Memanggil API AI, memproses maklum balas (Get Response Output), menjana tajuk perbualan (Record Thread Title Output), dan merekodkan jawapan (Record Response Output). |
| **Auto-Tempah Khas** | Process for Pembersihan IFC | **Scheduled / Trigger** | Menjana rekod tempahan pembersihan IFC secara automatik di lajur auto tempah IFC 1 Output dan auto tempah IFC 2 Output. |
| **Pembersihan Data Berjadual** | Process for clear data, Process for Clear Data 2, Process for clear data 3, Process for clear data 4, Process for clear data 6 | **Scheduled** (Contoh: Setiap minggu/bulan) | Mengesan baris tamat tempoh (Delete Expired Rows Process Output / Delete Output) dan memadam rekod usang untuk mengekalkan saiz pangkalan data yang optimum. |

💡 **Tip Automasi:** Penggunaan langkah *Wait / Delay* (seperti 5 MINIT WAITING Output pada Process for Konflik) memastikan semua transaksi berasaskan peranti berbeza sempat diselaraskan di pelayan sebelum pengesahan kelulusan tempahan dimuktamadkan.

### **5.3 Integrasi Luaran (Webhooks, Apps Script & Make.com)**

Aplikasi PMA IDigital dihubungkan dengan ekosistem automasi luaran untuk melaksanakan pemprosesan kompleks yang tidak boleh dilakukan secara asli di dalam AppSheet.

\[ Form Input AppSheet \]   
       │  
       ├─► (Webhook) ────────► Ollama Server AI ──► (Jana Teks/RPH) ──┐  
       │                                                              ├─► Log & Papar dalam App  
       ├─► (Apps Script) ────► Google Drive / Sheet ──► (Manipulasi Data) ┤  
       │                                                              │  
       └─► (Make Webhook) ───► Make.com Integration ──► (Sync Luaran) ┘

#### **1\. Integrasi Webhook Ollama Server AI (Process for via ollama server)**

> * **Fungsi:** Menghantar petikan teks/prompt daripada modul AI RPH atau Abqari\_Ai ke pelayan pemprosesan AI tempatan/awan (Ollama Server).  
> * **Aliran Tugas:**  
  1. Action mencetuskan call a webhook to ollama Output.  
  2. JSON Payload dihantar mengandungi prompt pengguna.  
  3. Setelah pemprosesan selesai, jawapan diterima dan disimpan melalui record response Output 5\.

#### **2\. Integrasi Google Apps Script (Process for New Bot 84-1 & Process for via appscript 2\)**

> * **Fungsi:** Menjalankan skrip Google Apps Script untuk pengurusan fail Google Drive yang berstruktur dan pengendalian formula pemprosesan pukal.  
> * **Aliran Tugas:**  
  1. Pencetus melaksanakan langkah call a appscript Output / appscript Output.  
  2. Google Apps Script menjalankan pemprosesan luaran (seperti penyusunan folder PDF mengikut tahun/bulan).  
  3. Status transaksi direkodkan semula di Record Log Output.

#### **3\. Integrasi Make.com (Process for via make)**

> * **Fungsi:** Platform integrasi iPaaS (Make.com) dipanggil menggunakan via make Output bagi menyambungkan data PMA IDigital ke sistem notifikasi luaran atau pangkalan data pihak ketiga.

### **5.4 Templat Dokumen & Janaan PDF**

Aplikasi ini menyokong janaan dokumen rasmi dalam format PDF secara automatik untuk urusan pentadbiran dan rekod sekolah.

#### **Fail Templat & Janaan Utama:**

> 1. **Jadual Peperiksaan PDF (JADUAL PEPERIKSAAN PDF):**  
   * *Pencetus:* Penyelaras Peperiksaan mengemas kini atau melengkapkan susunan jadual.  
   * *Hasil Output:* Dokumen PDF jadual peperiksaan dijana daripada templat Google Docs (DocId=1najKYXZsgTZ8dOVezaPo4xE2MIHtFLfLUOK8UBuyNvo) dan disimpan di Google Drive.  
> 2. **Jadual Pengawas Peperiksaan PDF (JADUAL PENGAWAS PEPERIKSAAN PDF):**  
   * *Pencetus:* Kemaskini tugasan pengawasan peperiksaan.  
   * *Hasil Output:* Dokumen senarai pengawas mengikut bilik dan slot peperiksaan.  
> 3. **Laporan Aktiviti Kokurikulum (E\_KOKO LAPORAN & E\_KOKO LAPORAN AKTIVITI LUAR):**  
   * *Pencetus:* Status laporan dikemaskini kepada *"TELAH DISEMAK"*.  
   * *Hasil Output:* Dokumen PDF rasmi laporan aktiviti berserta gambaran gambar aktiviti (GAMBAR 1 hingga GAMBAR 4), senarai kehadiran, dan ruangan tandatangan penyemak.  
> 4. **Laporan Guru Ganti (E\_LAPORAN RELIEF):**  
   * *Pencetus:* Pengesahan penyeliaan relief oleh Penyelaras Akademik.

⚠️ **Nota Templat PDF:** Pautan PDF yang dijana akan disimpan dalam lajur PDF atau Link PDF Output. Pengguna boleh menekan butang Action bernikon fail/PDF pada paparan borang untuk terus membuka fail dokumen rasmi berkenaan.

### **5.5 Action Terkategori untuk Automasi**

Daripada **429 Actions** yang dibina di dalam sistem, terdapat beberapa kumpulan Action khusus yang direka khas untuk menyokong alur kerja automasi:

> * **Grouped Actions (Tindakan Berkelompok):** Menjalankan siri tindakan berturutan dengan satu sentuhan. Contohnya: *Menukar status laporan \-\> Mengisi e-mel penyemak \-\> Menjana Timestamp semakan*.  
> * **Execute an Action on a Set of Rows:** Membolehkan satu borang induk mengubah status banyak baris anak secara serentak (contohnya menukar status semua slot tempahan atau pendaftaran peperiksaan).  
> * **App: Open a File / Open a View:** Membuka paparan dokumen PDF yang baru dijana oleh bot secara *real-time*.

## **6\. KESELAMATAN & PERANAN**

Keselamatan data dan kawalan hak akses di dalam aplikasi **PMA IDigital** direka bentuk berasaskan prinsip **Role-Based Access Control (RBAC)**. Ini memastikan setiap kakitangan hanya mempunyai akses kepada maklumat, borang, dan tindakan yang berkaitan secara langsung dengan skop tugas serta jawatan mereka di Pondok Moden al-'Abaqirah (PMA).

### **6.1 Kaedah Autentikasi (Authentication Method)**

Aplikasi PMA IDigital memanfaatkan kaedah autentikasi selamat berasaskan Single Sign-On (SSO):

> * **Google OAuth 2.0 / SSO:** Pengguna log masuk menggunakan akaun e-mel rasmi (Google Workspace atau e-mel berdaftar).  
> * **Pengecaman Identiti Dinamik (USEREMAIL()):** Setiap kali pengguna membuka aplikasi, enjin AppSheet menangkap identiti e-mel pengguna menerusi formula \=USEREMAIL() secara automatik.  
> * **Penyemakan Pangkalan Data Teras (DATA GURU):** Nilai \=USEREMAIL() disemak secara *real-time* menembusi pangkalan data DATA GURU di lajur EMAIL ID. Jika e-mel pengguna tidak ditemui dalam senarai guru/staf berdaftar, akses aplikasi akan disekat serta-merta mengikut syarat kelayakan penggunaan.

⚠️ **Nota Keselamatan:** Keselamatan akaun adalah tanggungjawab individu. Pengguna dilarang berkongsi maklumat akaun atau membiarkan sesi peranti dibuka tanpa kawalan bagi mengelakkan kebocoran maklumat rahsia sekolah.

### **6.2 Peranan Pengguna (User Roles) & Logik Kawalan Akses**

Peranan dan kebenaran pengguna diselaraskan menerusi lajur logik Boolean (Yes/No) di dalam jadual DATA GURU.

\[ Input USEREMAIL() \] ──► \[ Semak DATA GURU \] ──► \[ Pengesahan Lajur Boolean (TRUE/FALSE) \]  
                                                        │  
                                                        ├─► ADMIN / SUPER ADMIN  
                                                        ├─► MUDIR / NAIB MUDIR  
                                                        ├─► PENYELARAS MODUL  
                                                        └─► GURU / STAF BIASA

#### 

#### **Pengkategorian Peranan Utama:**

> 1. **Super Admin & Admin:**  
   * Mempunyai kawalan penuh ke atas pangkalan data, tetapan peranan pengguna lain, suis penyelenggaraan (MAINTENANCE), dan konfigurasi menu.  
   * *Formula Syarat (Editable\_If / Show\_If):*

   \=IN(USEREMAIL(), SELECT(DATA GURU\[EMAIL ID\], \[ADMIN\] \= TRUE))

> 2. **Pengurusan Tertinggi (Mudir & Naib Mudir \- NM Akademik, NM HEP, NM KOKO):**  
   * Mengawasi laporan keseluruhan, meluluskan permohonan kenderaan, dan menyemak laporan kokurikulum serta aduan disiplin/kesihatan.  
   * *Formula Syarat:*

   \=IN(USEREMAIL(), SELECT(DATA GURU\[EMAIL ID\], \[MUDIR\] \= TRUE))

> 3. **Penyelaras / Unit Khas (Penyelaras Peperiksaan, Penyelaras Koko, Warden, Pemandu):**  
   * Menguruskan modul spesifik masing-masing. Sebagai contoh, Penyelaras Peperiksaan mengawal suis STATUS AKSES EXAM, manakala Penyelaras Koko menyemak dan mengubah status E\_KOKO LAPORAN kepada *"TELAH DISEMAK"*.  
   * *Formula Syarat (Contoh Penyelaras Koko):*

   \=IN(USEREMAIL(), SELECT(DATA GURU\[EMAIL ID\], \[E\_KOKO\] \= TRUE))

> 4. **Guru Biasa / Staf Operasi:**  
   * Akses untuk mengisi borang harian (kehadiran, hafazan E\_HUFFAZ, tempahan bilik E\_TEMPAH, aduan, laporan pengajaran/relief) serta melihat jadual peribadi dan pengumuman sekolah.

### **6.3 Matriks Capaian Data (Access Control Matrix)**

Jadual di bawah memperincikan tahap kebenaran capaian mengikut modul dan peranan pengguna:

| Modul / Jadual | Guru / Staf Biasa | Penyelaras / Ketua Unit | Mudir & Naib Mudir | Admin / Super Admin |
| ----- | ----- | ----- | ----- | ----- |
| **DATA GURU (Profil Staf)** | Read / Edit (Peribadi) | Read | Read | Read / Add / Edit / Delete |
| **DATA PELAJAR & KEBAJIKAN** | Read | Read / Edit (Ikut Kelas) | Read / Edit | Read / Add / Edit / Delete |
| **E\_HUFFAZ (Rekod Hafazan)** | Read / Add / Edit | Read / Add / Edit / Delete | Read | Read / Add / Edit / Delete |
| **E\_KEHADIRAN & E\_KESIHATAN** | Read / Add | Read / Add / Edit | Read / Edit | Read / Add / Edit / Delete |
| **E\_KOKO LAPORAN** | Read / Add / Edit (Borang Asal) | Read / Edit / Approve (Semakan) | Read | Read / Add / Edit / Delete |
| **E\_TEMPAH REKOD (Fasiliti)** | Read / Add / Edit (Milik Sendiri) | Read / Edit | Read | Read / Add / Edit / Delete |
| **E\_PEPERIKSAAN & SOALAN** | Read (Tergantung Suis Akses) | Read / Add / Edit / Toggle Access | Read | Read / Add / Edit / Delete |
| **Abqari AI & CHAT HISTORY** | Read / Add (Data Sendiri sahaja) | Read / Add (Data Sendiri) | Read / Add (Data Sendiri) | Read / Add / Delete |
| **MENU APP & MAINTENANCE** | Read | Read | Read | Read / Add / Edit / Delete |

### **6.4 Perlindungan Data Sensitif & Polisi Privasi**

Bagi mematuhi dasar privasi dan perlindungan data peribadi institusi:

> 1. **Tag Data Sensitif (Sensitive Data Marking):**  
   * Lajur yang mengandungi maklumat peribadi seperti NO KP (Kad Pengenalan pelajar), NO TEL BAPA/IBU, PENDAPATAN BAPA/IBU, dan EMAIL ID disetkan dengan tetapan Sensitive data \= Yes di dalam AppSheet. Data ini dienkripsi semasa penghantaran dan ditapis daripada paparan awam.  
> 2. **Pengasingan Sembang AI & Transkripsi:**  
   * Rekod perbualan dalam modul Abqari\_Ai dan transkripsi audio/imej menggunakan *Security Filter* atau *Slice Filter* \= \[EMAIL\] \= USEREMAIL(). Ini memastikan perbualan dan dokumen yang dimuat naik oleh seorang guru tidak dapat dilihat oleh guru yang lain.  
> 3. **Integriti Penyuntingan (Editable\_If Constraints):**  
   * Pengguna tidak boleh mengubah data penting seperti status pengesahan, e-mel pendaftaran, atau penetapan peranan admin. Ruangan ini akan dikunci secara automatik (Read-Only) pada borang pengguna biasa.

💡 **Tip Pentadbiran:** Apabila terdapat guru baharu yang mendaftar atau bertukar peranan (contohnya dilantik menjadi Warden atau Guru Kelas), Admin hanya perlu mengemaskini penanda TRUE pada lajur berkaitan di dalam paparan DATA GURU tanpa perlu mengubah suai kod aplikasi.

## 

## **7\. MANUAL PENGGUNA**

Manual ini menyediakan panduan langkah demi langkah untuk membantu kakitangan dan guru **Pondok Moden al-'Abaqirah (PMA)** mengendalikan aplikasi **PMA IDigital** bagi tugasan harian.

### **7.1 Langkah-Langkah Operasi Harian & Navigasi Asas**

#### **1\. Cara Log Masuk Aplikasi**

> 1. **Peranti Mudah Alih (Smartphone / Tablet):**  
   * Muat turun aplikasi **AppSheet** daripada *Google Play Store* (Android) atau *Apple App Store* (iOS).  
   * Buka aplikasi AppSheet dan tekan **"Sign in with Google"**.  
   * Log masuk menggunakan e-mel rasmi institusi yang telah mendaftar dalam sistem (DATA GURU).  
> 2. **Pelayar Web Desktop (PC / Laptop):**  
   * Buka pautan web (URL) rasmi PMA IDigital pada pelayar seperti Google Chrome, Microsoft Edge, atau Safari.  
   * Log masuk menggunakan akaun Google yang didaftarkan.

⚠️ **Nota:** Sekiranya anda menerima mesej *"Access Denied"* atau paparan kosong, sila pastikan anda log masuk menggunakan e-mel rasmi berdaftar dan hubungi Pentadbir Sistem untuk menyemak status aktif anda di dalam DATA GURU.

#### **2\. Antara Muka & Navigasi Utama**

Selepas log masuk, paparan utama akan memaparkan 5 pilihan navigasi pada Bar Navigasi Bawah (Bottom Navigation Bar):

┌─────────────────────────────────────────────────────────────────—────────┐  
│                          PMA IDigital Navigation                         │  
├─────────────┬────────────────┬─────────────┬─────────────┬───────────────┤  
│ 📰 Terkini  │ 🔔 Notifikasi │ 🔲 Menu     │ 🤖 Abqari   │ 👤 Profil     │  
│  (Start)    │                │    Utama    │    AI       │    Saya       │  
└─────────────┴────────────────┴─────────────┴─────────────┴───────────────┘

> * **📰 Kemaskini Terkini:** Paparan utama yang mengandungi pengumuman sekolah, notis penting, dan status tempahan bilik/fasiliti semasa.  
> * **🔔 Notifikasi:** Pusat makluman untuk semakan pengumuman rasmi, status tempahan, dan tugasan harian terkini.  
> * **🔲 Menu Utama:** Hub berpusat yang mengandungi ikon untuk mengakses semua modul (Akademik, HEP, Kokurikulum, Operasi, dan Tools).  
> * **🤖 Abqari AI:** Pembantu kecerdasan buatan untuk tugasan pentadbiran dan pengajaran.  
> * **👤 Profil Saya:** Melihat dan mengemaskini maklumat profil peribadi, nombor telefon, dan tetapan akaun.

> 

#### **3\. Carian (Search) dan Penapisan Data (Filter)**

> * **Membuat Carian Fast Search:** Tekan ikon **Kanta Pembesar (🔍)** di sudut atas sebelah kanan skrin. Taip kata kunci (contoh: nama pelajar, nama bilik, atau tarikh).  
> * **Menapis Data (Grouping/Sorting):** Pada paparan senarai, gunakan butang penapis di bahagian atas untuk menyusun data mengikut tarikh, status pengesahan, atau abjad.

### **7.2 Cara Menambah Rekod Baharu (Standard Form Flow)**

Secara umum, proses menambah sebarang rekod baharu (seperti tempahan bilik, rekod hafazan, atau aduan kesihatan) menggunakan aliran standard berikut:

> 1. **Pilih Modul Sasaran:** Navigasi ke modul berkaitan (contoh: *Menu Utama* ➔ *E\_TEMPAH*).  
> 2. **Buka Borang Input:** Tekan butang ikon Tambah **\+** (Action Add) yang terletak di sudut bawah sebelah kanan skrin.  
> 3. **Isi Maklumat Borang:**  
   * Medan yang bertanda **asterisk merah (\*)** atau berbingkai merah adalah **wajib diisi (Required)**.  
   * Bagi medan jenis **Enum / EnumList**, pilih daripada senarai pilihan yang disediakan.  
   * Bagi borang yang memerlukan lampiran imej/dokumen, tekan ikon **Kamera / Fail** untuk memuat naik fail dari peranti.  
> 4. **Hantar / Simpan Data:** Tekan butang **"Simpan"** (atau **"Hantar"**) di sudut bawah skrin.  
> 5. **Proses Segerakan (Synchronization):** Pastikan roda gilasan di sudut atas skrin berputar sehingga selesai untuk memastikan data berjaya disegerakan (*synced*) ke pelayan awan.

💡 **Tip Segerakan (Syncing):** Aplikasi disetkan dengan fungsi *Offline Mode*. Sekiranya peranti terputus sambungan internet, rekod akan disimpan dalam memori peranti dan akan dipindahkan secara automatik apabila internet disambung semula.

### **7.3 Cara Menyunting (Edit) dan Memadam (Delete) Rekod**

#### **1\. Menyunting Rekod Sedia Ada**

> 1. Cari dan tekan pada rekod yang ingin dikemaskini dari paparan senarai/jadual.  
> 2. Paparan butiran (*Detail View*) akan dibuka.  
> 3. Tekan butang **"Sunting"** atau ikon **Pensel (✏️)**.  
> 4. Ubah maklumat yang perlu dikemaskini pada borang yang dipaparkan.  
> 5. Tekan **"Simpan"** untuk mendokumenkan perubahan.

#### **2\. Memadam Rekod**

> 1. Buka paparan butiran (*Detail View*) rekod yang hendak dipadam.  
> 2. Tekan ikon **Tong Sampah (🗑️)** atau butang **"Padam"**.  
> 3. Mesej pengesahan akan dipaparkan: *"Adakah anda pasti mahu memadam rekod ini?"*.  
> 4. Tekan **"OK / Confirm"** untuk memadamkan data secara kekal.

> 

⚠️ **Nota Sekatan Edit & Delete:** Rekod yang telah disahkan oleh pihak Pentadbir/Mudir (seperti Laporan Kokurikulum bernilai *"TELAH DISEMAK"*) tidak lagi boleh disunting atau dipadam oleh guru biasa.

### **7.4 Panduan Penggunaan Modul-Modul Utama**

#### **Modul 1: Perekodan Hafazan Al-Quran (E\_HUFFAZ)**

Modul ini digunakan oleh guru hafazan bagi merekodkan pencapaian hafazan harian.

\[ Buka Modul E\_HUFFAZ \] ──► \[ Tekan Butang '+' \] ──► \[ Pilih Nama pelajar \] ──► \[ Masukkan Muka Surat \] ──► \[ Sistem Kira Juzuk \] ──► \[ Simpan \]

> 1. **Langkah-Langkah Perekodan:**  
   * Navigasi ke **Menu Utama** ➔ pilih ikon **E\_HUFFAZ**.  
   * Tekan butang **\+** untuk muka surat baharu.  
   * Pilih **Nama Pelajar** daripada senarai *drop-down*.  
   * Masukkan nombor **Muka Surat** Al-Quran yang dibaca/dihafal (Nombor 1 hingga 604).  
   * **Sistem Automatik:** Lajur JUZUK akan dikira secara automatik oleh sistem berdasarkan formula CEILING((\[MUKA SURAT\]-1)/20).  
   * Tekan **"Simpan"**.

#### **Modul 2: Perekodan Kehadiran & Kesihatan pelajar (E\_KEHADIRAN & E\_KESIHATAN)**

Modul ini membolehkan guru kelas dan guru bertugas merekod kehadiran harian serta aduan kesihatan pelajar.

> 1. **Merekod Kehadiran Harian Kelas:**  
   * Navigasi ke **Menu Utama** ➔ pilih **E\_KEHADIRAN**.  
   * Pilih **Kelas / Tingkatan** anda.  
   * Borang akan memaparkan senarai nama pelajar dalam kelas tersebut.  
   * Secara lalai, semua pelajar dianggap *Hadir*. Tanda (*tick*) pada nama pelajar yang **Tidak Hadir**.  
   * Pilih **Sebab Tidak Hadir** (contoh: *Sakit, Bersebab, Tanpa Sebab*).  
   * Tekan **"Simpan"**.  
> 2. **Merekod Aduan Kesihatan & Kebenaran MC:**  
   * Navigasi ke **E\_KESIHATAN** ➔ Tekan **\+**.  
   * Pilih nama pelajar dan masukkan simptom/sakit yang dialami.  
   * Di ruangan **Tindakan**, jika memilih *"PULANG (MC)"*, borang dinamik akan memaparkan medan tambahan **Bilangan Hari MC** dan butang memuat naik gambar sijil cuti sakit.  
   * Muat naik foto sijil MC dan tekan **"Simpan"**.

#### **Modul 3: Tempahan Bilik Khas & Fasiliti (E\_TEMPAH)**

Digunakan oleh staf untuk menempah bilik khas seperti Makmal Komputer, IFC, JLC, JIL, Bilik Turath, Maktabah, atau Pantry.

\[ Pilih Bilik Khas \] ──► \[ Pilih Tarikh & Slot Masa \] ──► \[ Cek Semakan Had (1/hari, 3/minggu) \] ──► \[ Pengesahan Status \]

> 1. **Prosedur Tempahan:**  
   * Navigasi ke **Menu Utama** ➔ pilih **E\_TEMPAH**.  
   * Tekan butang **\+** untuk membuat tempahan baharu.  
   * Pilih **Bilik Tempahan** (contoh: *IFC* atau *Makmal Komputer*).  
   * Pilih **Tarikh Tempahan**.  
   * Pilih **Slot Masa Tempah** daripada senarai pilihan (*EnumList*). Masa yang telah ditempah oleh pengguna lain pada tarikh yang sama akan ditapis keluar secara automatik.  
   * Nyatakan **Tujuan Tempahan** (jika memilih *"LAIN-LAIN"*, isi ruangan catatan tambahan).  
   * Tekan **"Simpan"**.

⚠️ **Amaran Had Tempahan:** Sistem menyemak syarat tempahan secara *real-time*. Anda akan disekat daripada menyimpan borang jika:

> * Telah membuat tempahan pada bilik yang sama **lebih 1 kali pada hari tersebut**.  
> * Telah membuat tempahan pada bilik yang sama **melebihi 3 kali dalam seminggu**.

#### **Modul 4: Pengurusan Guru Ganti (E\_RELIEF)**

Digunakan untuk menyemak dan menetapkan jadual pengajaran ganti bagi guru yang bercuti.

> 1. **Semakan Jadual Relief Personal:**  
   * Buka modul **E\_RELIEF** ➔ Info Relief.  
   * Sistem akan memaparkan senarai kelas ganti yang ditugaskan kepada anda pada hari ini.  
> 2. **Penetapan Guru Relief (Untuk Penyelaras Akademik):**  
   * Buka modul **E\_RELIEF** ➔ Tekan **\+**.  
   * Pilih **Hari**, **Tarikh**, dan **Kelas** yang terjejas.  
   * Di ruangan **Nama Guru Relief**, senarai *drop-down* hanya akan memaparkan nama guru yang **TIDAK mengajar** (lenggang) pada slot waktu tersebut.  
   * Simpan rekod. Notifikasi *push notification* akan dihantar secara automatik ke peranti guru yang dilantik.

#### 

#### 

#### 

#### **Modul 5: Penggunaan Alat Pintar AI (Abqari AI & AI Tools)**

Modul ini merupakan pembantu maya berasaskan kecerdasan buatan untuk memudahkan tugas harian guru.

> 1. **Penggunaan Abqari AI (Sembang Pentadbiran & RPH):**  
   * Tekan ikon **🤖 Abqari AI** pada bar navigasi bawah.  
   * Tekan butang **\+** untuk memulakan perbualan baharu (Sesi sembang diasingkan mengikut akaun anda secara peribadi).  
   * Taip soalan atau arahan di ruangan **Prompt** (contoh: *"Bantu saya sediakan draf Laporan Pengajaran Harian untuk Subjek Bahasa Arab Tingkatan 2"*).  
   * Tekan **"Tanya"**. Jawapan akan dijana dan dipaparkan dalam beberapa saat.

## **7\. MANUAL PENGGUNA (PERLUASAN MODUL LENGKAP)**

Berikut adalah panduan lengkap pengendalian untuk **kesemua 14 modul fungsi utama** yang terkandung di dalam aplikasi PMA IDigital berdasarkan pangkalan data teras sistem:

### **7.1 Modul Akademik & Penjadualan Waktu**

> * **Jadual Waktu Pengajaran (E\_JADUAL DATA / JADUAL AKADEMIK / DATA JADUAL):**  
  1. Buka **Menu Utama** ➔ pilih **E\_JADUAL**.  
  2. Guru boleh melihat susunan waktu mengajar mengikut hari dan kelas.  
  3. Sistem mengira bilangan masa mengajar secara automatik di lajur BIL MASA menggunakan formula \=FLOOR((TOTALMINUTES(\[MASA AKHIR\] \- \[MASA MULA\]) / 30)) & " MASA".  
> * **Tukar Slot Mengajar (SWAP\_KELAS):**  
  1. Navigasi ke **Menu Utama** ➔ pilih **SWAP KELAS**.  
  2. Tekan **\+** untuk memohon pertukaran waktu mengajar dengan guru lain.  
  3. Pilih tarikh, slot asal, dan nama guru pengganti. Paparan borang menapis guru yang lenggang mengikut logik Editable\_If / Valid\_If.  
> * **Import Jadual ASC XML (E\_JADUAL ASC XML):**  
  1. Khas untuk Pentadbir Kurikulum bagi memuat naik fail jadual induk format XML.

### **7.2 Modul Peperiksaan & Kawalan Soalan**

> * **Jadual Peperiksaan & Draf Soalan (E\_PEPERIKSAAN / STATUS AKSES EXAM):**  
  1. Navigasi ke **Menu Utama** ➔ pilih **E\_PEPERIKSAAN**.  
  2. Akses kepada dokumen soalan dikawal oleh Penyelaras Peperiksaan melalui suis STATUS AKSES EXAM.  
  3. Apabila status bertukar kepada TRUE (🟢 BUKA AKSES), guru boleh memuat turun atau menyemak kertas soalan.  
> * **Pengawasan Peperiksaan (E\_JADUAL PENGAWAS / JADUAL PEPERIKSAAN PDF):**  
  1. Guru menyemak jadual pengawasan peperiksaan mengikut bilik dan masa.  
  2. Format Rule menandakan status peperiksaan secara automatik: 🔴 *MENYUSUL*, 🔵 *BERLANGSUNG*, atau 🟢 *SELESAI*.  
  3. Penyelaras boleh mencetak slip rasmi menerusi paparan JADUAL PEPERIKSAAN PDF.

### **7.3 Modul Hafazan Al-Quran**

> * **Perekodan Muka Surat & Juzuk (E\_HUFFAZ DATA / E\_HUFFAZ REKOD):**  
  1. Buka modul **E\_HUFFAZ** ➔ Tekan **\+**.  
  2. Pilih **Nama Pelajar**. Sistem memapar MUKA SURAT TERKINI secara automatik melalui formula LOOKUP(MAXROW(...)).  
  3. Masukkan nombor muka surat baharu. Sistem mengira JUZUK Al-Quran (1–30) secara dinamik.  
  4. Penanda prestasi (KPI) menandakan warna merah secara automatik pada pelajar Tingkatan 2 yang belum mencapai Juzuk 3 atau Tingkatan 3 yang belum mencapai Juzuk 5\.

### **7.4 Modul Daurah & Takwim Program Khas**

> * **Jadual & Kehadiran Daurah (E\_DAURAH JADUAL / E\_DAURAH KEHADIRAN):**  
  1. Navigasi ke **Menu Utama** ➔ pilih **E\_DAURAH**.  
  2. Menyemak susunan pengajian kitab/daurah dan merekod kehadiran peserta secara harian.  
> * **Takwim & Program Sekolah (E\_TAQWIM / E\_PROGRAM):**  
  1. Memaparkan kalendar aktiviti tahunan institusi mengikut kategori: *PENTADBIRAN, KURIKULUM, KOKURIKULUM, HEP, PEPERIKSAAN, ASRAMA, CUTI*.  
  2. Program yang telah tamat tarikh akan ditanda dengan garisan potong (*strikethrough*) secara automatik melalui Format Rule.

### **7.5 Modul Kehadiran, Disiplin & Kesihatan pelajar**

> * **Kehadiran Kelas Harian (E\_KEHADIRAN / GROUP KELAS):**  
  1. Guru kelas membuka **E\_KEHADIRAN** ➔ Pilih kelas.  
  2. Tandakan nama pelajar yang **Tidak Hadir** dan nyatakan sebab.  
> * **Rekod Kesihatan & Cuti Sakit (E\_KESIHATAN):**  
  1. Merekod aduan sakit pelajar.  
  2. Jika tindakan *"PULANG (MC)"* dipilih, isi ruangan wajib BIL HARI MC dan muat naik foto Sijil Cuti Sakit.  
> * **Kawalan Disiplin Bilik Darjah (E\_CLASS\_REKOD KAWALAN KELAS):**  
  1. Guru subjek waktu semasa merekodkan suasana kelas dan salah laku pelajar.  
  2. Rekod yang memerlukan tindakan lanjut akan berada di bawah status 🔴 *BELUM DISEMAK* sehingga disahkan oleh Unit HEP/Mudir.

### **7.6 Modul Kebajikan, Profil & Alumni**

> * **Data Kebajikan & Pendapatan Keluarga (E\_KEBAJIKAN):**  
  1. Menyimpan data sosioekonomi, bilangan ahli keluarga, serta penyakit kronik pelajar.  
  2. Sistem mengira JUMLAH PENDAPATAN (\[PENDAPATAN BAPA\] \+ \[PENDAPATAN IBU\]) secara automatik.  
  3. Pendapatan keluarga di bawah RM3,500 ditanda secara visual bagi keutamaan agihan bantuan.  
> * **Pangkalan Data Profil & Alumni (DATA PELAJAR / DATA ALUMNI / UJIAN VAK):**  
  1. Menyimpan profil pelajar, nombor kad pengenalan, e-mel, dan nombor telefon ibu bapa.  
  2. GAYA PEMBELAJARAN DOMINAN ditarik automatik dari jadual UJIAN VAK menggunakan formula LOOKUP.  
  3. Profil pelajar yang telah tamat pengajian dipindahkan ke jadual DATA ALUMNI.

### **7.7 Modul Kokurikulum & Aktiviti Luar**

> * **Kehadiran Kokurikulum (E\_KOKO DATA GURU/PELAJAR / E\_KOKO KEHADIRAN):**  
  1. Buka modul **E\_KOKO KEHADIRAN** ➔ Pilih Unit Uniform / Kelab / Sukan.  
  2. Tanda kehadiran pelajar bertugas.  
> * **Laporan Aktiviti Mingguan & Luar (E\_KOKO LAPORAN / E\_KOKO LAPORAN AKTIVITI LUAR):**  
  1. Guru Penasihat mengisi borang laporan, ringkasan aktiviti, dan memuat naik sehingga 4 keping gambar (GAMBAR 1 \- GAMBAR 4).  
  2. Amaran automatik dipaparkan jika kehadiran belum direkodkan di E\_KOKO KEHADIRAN.  
  3. Laporan yang disahkan oleh Penyelaras Koko akan menjana dokumen PDF rasmi.

### **7.8 Modul Tempahan Fasiliti & Peralatan**

> * **Tempahan Bilik Khas (E\_TEMPAH DATA / E\_TEMPAH REKOD):**  
  1. Buka **E\_TEMPAH** ➔ Pilih bilik (*Makmal Komputer, IFC, Maktabah, Bilik Turath, Pantry, JIL, JLC*).  
  2. Pilih tarikh dan slot masa. Pilihan slot bertindih ditapis secara automatik.  
  3. Had sekatan: Menghalang tempahan bilik yang sama melebihi **1 kali sehari** atau **3 kali seminggu**.

### **7.9 Modul Pengurusan Guru Ganti (Relief)**

> * **Jadual & Laporan Relief (E\_RELIEF / E\_LAPORAN RELIEF):**  
  1. Penyelaras memilih waktu dan kelas yang terjejas.  
  2. Senarai nama guru ditapis secara automatik untuk memaparkan guru yang **TIDAK mengajar** pada slot tersebut.  
  3. Guru ganti mengisi laporan pelaksanaan tugas di E\_LAPORAN RELIEF.

### **7.10 Modul Pengangkutan Institusi**

> * **Permohonan Kenderaan (E\_TRANSPORT REKOD):**  
  1. Pemohon memasukkan tarikh, destinasi, jumlah penumpang, dan tujuan penggunaan kenderaan institusi.  
  2. Status borang diproses mengikut peringkat: 🟡 *BELUM DIPROSES* ➔ 🔵 *SEDANG DIPROSES* ➔ 🟢 *LULUS* / 🔴 *DITOLAK*.  
  3. Pengesahan permohonan dikawal oleh pegawai pelulus (PENGESAHAN KENDERAAN) dan tugasan diserah kepada PEMANDU.

### **7.11 Modul Kehadiran Staf, Guru Bertugas & Warden**

> * **Perekodan Kehadiran Staf (E\_STAF HADIR / LAPORAN E\_STAF HADIR):**  
  1. Staf mengimbas/merekodkan status kehadiran harian. Status dipaparkan sebagai 🟢 *HADIR* atau 🔴 *TIDAK*.  
> * **Guru Bertugas Mingguan & Warden Asrama (JADUAL GURU BERTUGAS / LAPORAN GURU BERTUGAS / JADUAL WARDEN):**  
  1. Menyemak senarai giliran guru bertugas dan warden.  
  2. Guru bertugas mingguan mengisi laporan harian keadaan sekolah di LAPORAN GURU BERTUGAS untuk pengesahan pihak pengurusan.

### **7.12 Modul Pengumuman, Aduan & Notifikasi**

> * **Pengumuman Rasmi (E\_PENGUMUMAN):**  
  1. Menyampaikan notis rasmi mengikut kumpulan sasaran (*Staf, Semua Pelajar, Kelas Spesifik*).  
  2. Mempunyai fitur **PIN PENGUMUMAN** (PINNED) untuk menyematkan notis penting di bahagian atas.  
  3. Menyediakan kaunter COUNT DIBACA dan senarai e-mel pembaca.  
> * **Aduan Awam/Staf (E\_ADUAN) & Notifikasi Push (NOTIFICATION):**  
  1. Membolehkan staf menghantar aduan kerosakan atau cadangan.  
  2. Notifikasi push dihantar secara automatik ke peranti mudah alih pengguna.

### **7.13 Modul Alatan Kecerdasan Buatan (AI Smart Tools)**

> * **Penjanaan RPH Otomatik (AI RPH):**  
  1. Masukkan tajuk subjek, tingkatan, dan standard pembelajaran.  
  2. Bot memanggil API Ollama Server/Webhook AI dan menghasilkan draf Laporan Pengajaran Harian lengkap di lajur RESPONS.  
> * **Pembantu AI & Perbualan (Abqari\_Ai / CHAT\_HISTORY):**  
  1. Sembang AI interaktif peribadi untuk soalan pentadbiran dan pendidikan.  
> * **Transkripsi Imej & Audio kepada Teks (AI IMAGE TO TEXT / AI AUDIO TO TEXT):**  
  1. Muat naik imej bahan/audio rakaman.  
  2. AI menukar media tersebut kepada teks bertulis secara automatik.  
> * **Glosari & Motivasi (DIGIGlosari / DAILY TAABIR):**  
  1. Carian istilah Arab-Melayu serta paparan kata motivasi harian automatik di halaman aplikasi.

### **7.14 Modul Tetapan Pentadbiran & Penyelenggaraan**

> * **Kawalan Pentadbir (DATA GURU / MAINTENANCE / CARD DB / APPS\_INFO):**  
  1. Menyelaraskan hak akses pengguna, menukar status mod penyelenggaraan aplikasi (MaintenanceMode: *ON/OFF*), dan menguruskan pautan kad navigasi di CARD DB.

## 

## **8\. PANDUAN PENTADBIR (ADMIN GUIDE)**

Bahagian ini menyediakan panduan teknikal komprehensif bagi **Super Admin**, **Admin**, dan **Penyelaras Sistem** untuk menguruskan konfigurasi pangkalan data, kawalan domain e-mel, pengurusan peranan pengguna, penyelenggaraan berkala, serta pemulihan sistem aplikasi **PMA IDigital**.

### **8.1 Pengurusan Pengguna & Domain E-mel Rasmi**

Sistem autentikasi PMA IDigital bergantung sepenuhnya pada domain e-mel rasmi institusi: **@alabaqirah-maiwp.edu.my**. Pengurusan peranan dan kebenaran modul dikendalikan secara dinamik menerusi jadual DATA GURU.

\[ Log Masuk Google OAuth \] ──► \[ Pengesahan Domain (@alabaqirah-maiwp.edu.my) \]  
                                            │  
                                            ▼  
\[ Semakan DATA GURU \] ───► \[ Padanan EMAIL ID \= USEREMAIL() \] ──► \[ Capaian Peranan (TRUE) \]

#### **1\. Syarat Pendaftaran E-mel Rasmi**

> * Setiap staf dan guru **WAJIB** menggunakan akaun e-mel Google Workspace rasmi bertetapan domain *@alabaqirah-maiwp.edu.my* (contoh: nama.staf@alabaqirah-maiwp.edu.my).  
> * Apabila pengguna log masuk, formula \=USEREMAIL() akan menangkap alamat e-mel tersebut dan menyemaknya dengan lajur EMAIL ID di dalam jadual DATA GURU.  
> * Jika alamat e-mel tidak menggunakan domain rasmi atau tidak didaftarkan dalam DATA GURU, sistem secara automatik menyekat akses kepada borang pentadbiran dan modul terselindung.

#### **2\. Langkah Pendaftaran Staf Baharu**

> 1. Buka modul **DATA GURU** (Akses terhad kepada akaun berstatus ADMIN \= TRUE).  
> 2. Tekan butang **\+** (Tambah) untuk menambah baris baharu.  
> 3. Masukkan data asas:  
   * **NAMA PENUH:** Nama penuh mengandungi gelaran rasmi.  
   * **NAMA:** Nama panggilan ringkas (digunakan untuk paparan antaramuka).  
   * **EMAIL ID:** Alamat e-mel rasmi berdomain *@alabaqirah-maiwp.edu.my*.  
   * **JAWATAN & NO TEL:** Maklumat perkhidmatan dan nombor telefon bimbit.  
> 4. **Janaan Kunci UID Otomatik:** Lajur UID akan dijana secara automatik oleh sistem menggunakan formula \= "PMA" & RIGHT("0" & (\[\_ROWNUMBER\] \- 1), 2\).  
> 5. Tekan **"Simpan"** dan pastikan aplikasi disegerakan (*synced*).

#### **3\. Penetapan Peranan & Kebenaran Modul (Role Assignment)**

Akses modul dikawal menerusi lajur-lajur Boolean (Yes/No) di dalam jadual DATA GURU. Tukar status kepada TRUE (🟢 BUKA) untuk memberi kebenaran khusus:

> * **Pentadbiran Induk:** Setkan ADMIN \= TRUE (kawalan struktur/data) atau SUPER ADMIN \= TRUE (termasuk akses fungsi BETA TESTER).  
> * **Pengurusan Tertinggi:** Setkan MUDIR \= TRUE, NM AKADEMIK \= TRUE, NM HEP \= TRUE, atau NM KOKO \= TRUE.  
> * **Penyelaras Modul Operasi:** Setkan TRUE pada lajur peranan spesifik seperti E\_KOKO, HAFAZAN, RELIEF, KEBAJIKAN, KESIHATAN, E\_TEMPAH, E\_TRANSPORT, PENGESAHAN KENDERAAN, PEMANDU, WARDEN, PENYELARAS DAURAH, PENYELARAS SPM, atau PENYELARAS STAM.  
> * **Guru Kelas:** Setkan TRUE pada lajur kelas berkenaan (contoh: GURU KELAS SYARAWI, GURU KELAS ZUHAILI, GURU KELAS NADWI, GURU KELAS QARDHAWI, GURU KELAS SYALTUT, GURU KELAS MARAGHI, GURU KELAS BUTHI).

#### **4\. Pembatalan / Nyahaktif Akses Pengguna**

Jika staf bertukar sekolah atau berhenti perkhidmatan:

> * Padamkan alamat e-mel *@alabaqirah-maiwp.edu.my* dari lajur EMAIL ID atau tukar semua peranan Boolean kepada FALSE (🔴 TUTUP). Sistem akan menyekat sebarang akses aplikasi serta-merta.

### **8.2 Penyelenggaraan Berkala System (System Maintenance)**

#### **1\. Mengaktifkan Mod Penyelenggaraan (Maintenance Mode)**

Gunakan fungsi ini apabila berlaku penyelenggaraan pangkalan data atau kemaskini sistem secara besar-besaran bagi mengelakkan pertindihan input data oleh pengguna.

| Nama Jadual | Lajur Terbitan | Nilai Input | Kesan / Impak Operasi |
| ----- | ----- | ----- | ----- |
| MAINTENANCE | MaintenanceMode | TRUE (*MAINTENANCE ON*) | Borang input dikunci dan paparan amaran penyelenggaraan diaktifkan untuk pengguna biasa. |
| MAINTENANCE | MESEJ\_ON | *Teks Pengumuman* (Contoh: *"Sistem sedang diselenggara dari 11.00 PM \- 12.00 AM"*) | Memaparkan teks kenyataan rasmi Admin di halaman utama aplikasi. |
| MAINTENANCE | MaintenanceMode | FALSE (*MAINTENENCE OFF*) | Membuka semula keseluruhan fungsi aplikasi seperti biasa. |

#### **2\. Kawalan Suis Akses Peperiksaan (STATUS AKSES EXAM)**

> * Buka jadual STATUS AKSES EXAM.  
> * Tukar lajur STATUS AKSES kepada FALSE (🔒 *TUTUP AKSES*) untuk mengunci kertas soalan peperiksaan di modul E\_PEPERIKSAAN selepas sesi ujian tamat.  
> * Tukar kepada TRUE (🔓 *BUKA AKSES*) apabila waktu peperiksaan bermula.

#### **3\. Pengekalan Memori Pangkalan Data (Automated Cleanup Bots)**

Sistem disokong oleh **5 Bot Pembersihan Otomatik** yang beroperasi secara latar belakang bagi mengelakkan saiz pangkalan data Google Sheets menjadi terlalu berat:

> * **Process for clear data & Process for Clear Data 2 hingga 6:** Berfungsi mengesan dan memadam rekod tempahan, jadual ganti, serta log notifikasi yang telah tamat tempoh menerusi tugasan Delete Expired Rows Process Output / Delete Output.

### **8.3 Troubleshooting & Penyelesaian Isu Lazim**

Jadual di bawah menyediakan langkah penyelesaian teknikal pantas bagi ralat yang sering dilaporkan:

| Ralat / Gejala Isu | Punca Utama Teknikal | Langkah Penyelesaian Pentadbir |
| ----- | ----- | ----- |
| **"Access Denied" / Paparan Modul Kosong** | E-mel pengguna tidak mengandungi domain @alabaqirah-maiwp.edu.my atau belum didaftarkan di DATA GURU. | 1\. Semak alamat e-mel di DATA GURU. 2\. Pastikan e-mel bertetapan domain @alabaqirah-maiwp.edu.my (contoh: nama@alabaqirah-maiwp.edu.my). 3\. Semak lajur Boolean peranan yang berkaitan diset kepada TRUE. |
| **Ralat Pertindihan Tempahan Bilik** | Pengguna menempah bilik melebihi had harian (1x) atau mingguan (3x). | 1\. Ini adalah sekatan sah dari formula Valid\_If pada E\_TEMPAH REKOD. 2\. Bot Process for Konflik akan menghentikan proses selama 5 minit (5 MINIT WAITING Output) sebelum memadam rekod bertindih (DELETE KONFLIK Output). |
| **Ollama AI Webhook Timeout / Unresponsive** | Pelayan Ollama AI tidak aktif atau URL Webhook terputus. | 1\. Buka log proses Process for via ollama server ➔ semak status call a webhook to ollama Output. 2\. Pastikan pelayan AI luaran aktif. 3\. Semak jawapan ralat di record response Output 5\. |
| **Lajur Pangkalan Data Tidak Selari (Schema Mismatch)** | Lajur baharu ditambah pada Google Sheets tetapi belum disegerakan di AppSheet. | 1\. Buka AppSheet Editor. 2\. Navigasi ke **Data ➔ Tables** ➔ pilih jadual berkaitan. **Regenerate Structure** untuk menyelaraskan skema data. |

### **8.4 Backup, Restore & Pengurusan Storan Awan**

#### **1\. Lokasi Storan & Struktur Folder Awan**

> * **Folder Induk Data:** /appsheet/data/PMAIDigital-601999319.  
> * **Pangkalan Data Google Sheets:** Fail induk Google Sheets bernama PMA IDigital (memuatkan 236 jadual/worksheets).  
> * **Penyimpanan Fail & Gambar:** Folder Google Drive yang dipautkan menerusi jadual GD\_PATH untuk menyimpan imej aktiviti (GAMBAR 1-4), imej pengumuman, dan fail PDF janaan rasmi.

#### **2\. Prosedur Sandaran Data (Data Backup)**

> 1. **Sandaran Versi Otomatik (Google Sheets Version History):**  
   * Buka fail induk Google Sheets PMA IDigital.  
   * Klik **File ➔ Version history ➔ See version history**.  
   * Klik **Name current version** dan masukkan label tarikh (contoh: *"Backup PMA IDigital \- Ogos 2026"*).  
> 2. **Eksport Salinan Fizikal Bulanan:**  
   * Buat salinan fail Google Sheets induk (File ➔ Make a copy) dan simpan di dalam folder arkib pentadbir Google Drive secara berkala.

#### **3\. Prosedur Pemulihan Data (Data Restore)**

> 1. **Pemulihan Rekod Pangkalan Data:**  
   * Sekiranya berlaku kehilangan data, buka **Version History** pada Google Sheets induk dan pilih **Restore this version**.  
   * Buka konsol AppSheet Editor dan jalankan **Regenerate Structure** pada jadual terjejas untuk menyelaraskan semula kunci primer (Key) dan Virtual Columns.  
> 2. **Pemulihan Versi Aplikasi (App Version Rollback):**  
   * Buka AppSheet Editor ➔ **Manage ➔ Version History**.  
   * Pilih versi aplikasi stabil terdahulu (contoh: *Version 1.005039*) dan tekan **Restore Version** untuk memulihkan konfigurasi UX atau Bot yang rosak.

💡 **Tip Pentadbiran:** Sentiasa pastikan pendaftaran e-mel staf baharu disahkan menggunakan domain rasmi @alabaqirah-maiwp.edu.my sebelum memberikan peranan ADMIN atau MUDIR bagi menjamin keselamatan data institusi.

⚠️ **Nota Keselamatan:** Jangan memadamkan jadual sistem berawalan Process Table (seperti Process for notification Process Table atau StepOutput) kerana jadual-jadual ini menyimpan log status pemprosesan enjin Automasi AppSheet.