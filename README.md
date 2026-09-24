# Pertemuan 04 Seleksi Multi-Kondisi dan Validasi Input

Nama: Iqhsan Saleh

NIM: 2225250021

Kelas: 3A

## Tujuan
Membangun program validasi dan klasifikasi dengan rantai if-elif-else.

## Cara Menjalankan
python3 praktik/validasi_klasifikasi_nilai.py

## Tabel Keputusan
| Kategori / Cabang | Syarat / Logika | Contoh Masukan |
| :--- | :--- | :--- |
| Validasi Tipe Data | Masukan harus berupa angka (lolos konversi `float`) | `abc` |
| Validasi Rentang | Nilai ujian, tugas, dan kehadiran berada di rentang 0 - 100 | `105`, `-5` |
| Syarat Kehadiran | Kehadiran minimal 80 persen | Kehadiran `75` |
| Predikat A - E | Ditentukan berdasarkan besaran Nilai Akhir ($0.6 \times \text{ujian} + 0.4 \times \text{tugas}$) | Ujian `90`, Tugas `80` |

## Hasil Pengujian
| Ujian | Tugas | Kehadiran | Nilai Akhir | Keluaran yang Diharapkan | Status |
| :---: | :---: | :---: | :---: | :--- | :---: |
| 90 | 80 | 95 | 86.00 | Predikat A, Lulus | Sesuai |
| 75 | 70 | 85 | 73.00 | Predikat B, Lulus | Sesuai |
| 60 | 60 | 80 | 60.00 | Predikat C, Lulus | Sesuai |
| 55 | 50 | 90 | 53.00 | Predikat D, Belum lulus | Sesuai |
| 40 | 30 | 100 | 36.00 | Predikat E, Belum lulus | Sesuai |
| 90 | 90 | 75 | 90.00 | Nilai akhir tetap tampil, status Tidak memenuhi syarat kehadiran | Sesuai |
| 105 | 80 | 90 | - | Pesan penolakan rentang nilai ujian | Sesuai |
| 80 | -5 | 90 | - | Pesan penolakan rentang nilai tugas | Sesuai |
| 80 | 80 | abc | - | Pesan penolakan tipe | Sesuai |

## Refleksi
Masukan tidak valid yang semula sempat terlewat adalah adanya potensi spasi berlebih pada input teks dari pengguna yang dapat mengganggu proses konversi tipe data. Hal ini diatasi dengan menambahkan fungsi `.strip()` pada setiap pengambilan masukan di awal program agar string bersih dari spasi ekstra sebelum divalidasi.
