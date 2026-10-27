# Dataset Kegiatan Kelompok Riset Tahun 2025

Dataset ini berisi rekapitulasi jumlah kelompok riset dan jumlah kegiatan riset pada tiga pusat riset untuk tahun 2025: **PRSDI**, **PRGI**, dan **PRMC**.

> **Status data:** PRSDI dan PRGI sudah lengkap. Data jumlah kegiatan **PRMC belum tersedia** (belum diberikan) dan akan dilengkapi kemudian.

---

## Daftar Isi

1. [Gambaran Umum](#gambaran-umum)
2. [Ringkasan Data](#ringkasan-data)
3. [Detail per Pusat Riset](#detail-per-pusat-riset)
4. [Struktur Dataset](#struktur-dataset)
5. [Catatan dan Keterbatasan Data](#catatan-dan-keterbatasan-data)
6. [Cara Penggunaan](#cara-penggunaan)
7. [Rencana Pengembangan](#rencana-pengembangan)

---

## Gambaran Umum

| Keterangan | Isi |
|---|---|
| Tahun data | 2025 |
| Jumlah pusat riset | 3 (PRSDI, PRGI, PRMC) |
| Jumlah kelompok riset | 15 (5 + 4 + 6) |
| Jumlah kegiatan tercatat | 38 (PRSDI 33 + PRGI 5, PRMC belum ada data) |

### Singkatan

| Singkatan | Kepanjangan |
|---|---|
| PRSDI | Pusat Riset Sains Data dan Informasi |
| PRGI | Pusat Riset Geoinformatika |
| PRMC | Pusat Riset Mekatronika Cerdas |

---

## Ringkasan Data

| Pusat Riset | Jumlah Kelompok Riset | Total Kegiatan | Status Data |
|---|---:|---:|---|
| PRSDI | 5 | 33 | Lengkap |
| PRGI | 4 | 5 | Lengkap |
| PRMC | 6 | - | Belum ada data kegiatan |
| **Total** | **15** | **38** (belum termasuk PRMC) | |

---

## Detail per Pusat Riset

### 1. PRSDI (Pusat Riset Sains Data dan Informasi)

Terdapat **5 kelompok riset** dengan total **33 kegiatan**.

| No | Kelompok Riset | Jumlah Kegiatan |
|---:|---|---:|
| 1 | Information Retrieval | 4 |
| 2 | Knowledge and Data Engineering | 3 |
| 3 | Human Computer Interaction and Visualisation | 7 |
| 4 | Natural Language Processing | 10 |
| 5 | Digital Government | 9 |
| | **Total** | **33** |

Catatan: Natural Language Processing (10 kegiatan) dan Digital Government (9 kegiatan) adalah dua kelompok dengan kegiatan terbanyak.

### 2. PRGI (Pusat Riset Geoinformatika)

Terdapat **4 kelompok riset** dengan total **5 kegiatan**.

| No | Kelompok Riset | Jumlah Kegiatan |
|---:|---|---:|
| 1 | Kelompok Riset Geodata | 1 |
| 2 | Kelompok Riset Geoanalisis | 1 |
| 3 | Kelompok Riset Geoinformasi | 3 |
| 4 | Kelompok Riset Geovisualisasi dan Infrastruktur | 0 |
| | **Total** | **5** |

Catatan: Kelompok Riset Geovisualisasi dan Infrastruktur tercatat 0 kegiatan.

### 3. PRMC (Pusat Riset Mekatronika Cerdas)

Terdapat **6 kelompok riset**. Jumlah kegiatan **belum diberikan**.

| No | Kelompok Riset | Jumlah Kegiatan |
|---:|---|---|---|
| 1 | Sistem Instrumentasi Cerdas | _belum ada data_ |
| 2 | Biomekatronika | _belum ada data_ |
| 3 | Dinamika dan Kendali Cerdas | _belum ada data_ |
| 4 | Mesin Cerdas dan Sistem Otonomos | _belum ada data_ |
| 5 | Robotika dan Kecerdasan Sistem (RoSI) | _belum ada data_ |
| 6 | Plasma Fluida Cerdas | _belum ada data_ |

---

## Struktur Dataset

Dataset disusun dalam bentuk tabel dengan **satu baris untuk setiap kegiatan riset**. Setiap kegiatan memiliki ID unik.

| Kolom | Tipe | Deskripsi |
|---|---|---|
| `ID Riset` | string | ID unik kegiatan, format `<PUSAT>_<NOMOR URUT>` (lihat skema ID di bawah) |
| `Kelompok Riset` | string | Nama kelompok riset yang menaungi kegiatan |
| `Kegiatan Riset` | string | Nama kegiatan riset |

### Skema ID Riset

Format: `<KODE PUSAT RISET>_<NOMOR URUT 3 DIGIT>`. Nomor urut berjalan per pusat riset dan sesuai dengan jumlah kegiatannya.

| Pusat Riset | Rentang ID | Jumlah ID |
|---|---|---:|
| PRSDI | `PRSDI_001` sampai `PRSDI_033` | 33 |
| PRGI | `PRGI_001` sampai `PRGI_005` | 5 |
| PRMC | belum ditentukan (menunggu data kegiatan) | - |

## Catatan dan Keterbatasan Data

- **Data PRMC belum lengkap.** Hanya daftar kelompok riset yang tersedia, jumlah kegiatan belum diberikan. Jangan memasukkan PRMC ke dalam perbandingan atau total sebelum datanya ada.
- **Nilai 0 pada PRGI** (Geovisualisasi dan Infrastruktur) perlu dikonfirmasi: apakah memang tidak ada kegiatan pada 2025 atau datanya belum masuk.
- Dataset mencatat ID, kelompok riset, dan nama kegiatan, belum memuat waktu, anggaran, atau luaran kegiatan.
- Pada README ini baru satu kegiatan yang tercantum lengkap (`PRSDI_001`). Nama kegiatan lainnya masih perlu diisi dari tabelmu.
- Dataset hanya mencakup **tahun 2025**, sehingga belum bisa dipakai untuk melihat tren antar tahun.
- Ejaan nama kelompok mengikuti data sumber, dengan penyesuaian kecil pada salah ketik yang jelas (misalnya "Prosscesing" menjadi "Processing", "Intrumentasi" menjadi "Instrumentasi").

---

## Cara Penggunaan

1. Gunakan tabel pada bagian [Ringkasan Data](#ringkasan-data) untuk gambaran cepat.
2. Gunakan format CSV pada bagian [Struktur Dataset](#struktur-dataset) bila ingin mengolah data di Excel, Python (pandas), atau R.
3. Pusat riset dapat dikenali dari awalan `ID Riset` (misalnya `PRSDI`, `PRGI`), dan jumlah kegiatan diperoleh dengan menghitung jumlah baris.

Contoh singkat dengan Python:

```python
import pandas as pd

df = pd.read_csv("kegiatan_2025.csv")

# Ambil kode pusat riset dari ID Riset
df["Pusat Riset"] = df["ID Riset"].str.split("_").str[0]

# Jumlah kegiatan per pusat riset
print(df.groupby("Pusat Riset").size())

# Jumlah kegiatan per kelompok riset
print(df.groupby(["Pusat Riset", "Kelompok Riset"]).size())
```

Catatan: kelompok riset yang tidak punya kegiatan (misalnya Geovisualisasi dan Infrastruktur di PRGI) tidak punya baris di tabel, sehingga tidak muncul pada hasil `groupby`. Tambahkan secara manual bila ingin ditampilkan dengan nilai 0.

---

## Rencana Pengembangan

- [ ] Mengisi nama kegiatan riset untuk seluruh ID (PRSDI_001 sampai PRSDI_033, PRGI_001 sampai PRGI_005)
- [ ] Melengkapi kegiatan dan ID untuk 6 kelompok riset PRMC
- [ ] Mengonfirmasi nilai 0 pada Kelompok Riset Geovisualisasi dan Infrastruktur (PRGI)
- [ ] Menambahkan rincian kegiatan (judul, waktu, luaran)
- [ ] Menambahkan data tahun lain untuk analisis tren
- [ ] Membuat visualisasi atau dashboard perbandingan antar pusat riset

---

## Sumber Data

Data bersumber dari informasi yang diberikan oleh pembimbing di **BRIN** (Badan Riset dan Inovasi Nasional), untuk tahun 2025.

Catatan: data PRMC belum tercantum karena belum diberikan.
