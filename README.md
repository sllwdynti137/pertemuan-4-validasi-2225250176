# Pertemuan 04 Seleksi Multi-Kondisi dan Validasi Input

**Nama:** Sela Widiyanti
**NIM:** 2225250176
**Kelas:** 3F

## Tujuan

Membangun program validasi dan klasifikasi dengan menggunakan rantai `if-elif-else`.

Program yang dibuat meliputi:

1. Predikat nilai A-E.
2. Kategori bilangan.
3. Validasi rentang sudut.
4. Validasi tipe dan rentang nilai.
5. Klasifikasi segitiga berdasarkan sudut.
6. Validasi dan klasifikasi nilai mahasiswa.

## Cara Menjalankan

Pastikan Python sudah terinstall dan folder project sudah dibuka di Visual Studio Code.

Untuk menjalankan setiap latihan, gunakan perintah:

```bash
python3 latihan/01_predikat_nilai.py
python3 latihan/02_kategori_bilangan.py
python3 latihan/03_validasi_rentang.py
python3 latihan/04_validasi_tipe.py
python3 latihan/05_klasifikasi_segitiga_sudut.py
```

Untuk menjalankan Praktik 1:

```bash
python3 praktik/validasi_klasifikasi_nilai.py
```

Jika menggunakan Windows dan perintah `python3` tidak berjalan, dapat menggunakan:

```bash
python latihan/01_predikat_nilai.py
```

## Tabel Keputusan

### 1. Predikat Nilai

| Predikat | Syarat               | Contoh Masukan |
| -------- | -------------------- | -------------: |
| A        | nilai >= 85          |             92 |
| B        | nilai >= 70 dan < 85 |             76 |
| C        | nilai >= 60 dan < 70 |             65 |
| D        | nilai >= 50 dan < 60 |             55 |
| E        | nilai < 50           |             30 |

### 2. Kategori Bilangan

| Kategori       | Syarat                                | Contoh Masukan |
| -------------- | ------------------------------------- | -------------: |
| Negatif        | bilangan < 0                          |             -7 |
| Nol            | bilangan == 0                         |              0 |
| Positif genap  | bilangan > 0 dan habis dibagi 2       |              8 |
| Positif ganjil | bilangan > 0 dan tidak habis dibagi 2 |             13 |

### 3. Validasi Rentang Sudut

| Kondisi     | Syarat                       | Contoh Masukan |
| ----------- | ---------------------------- | -------------: |
| Tidak valid | sudut <= 0 atau sudut >= 180 |              0 |
| Lancip      | 0 < sudut < 90               |             45 |
| Siku-siku   | sudut == 90                  |             90 |
| Tumpul      | 90 < sudut < 180             |            135 |

### 4. Validasi Tipe dan Rentang Nilai

| Kondisi             | Syarat                    | Contoh Masukan |
| ------------------- | ------------------------- | -------------: |
| Tipe tidak valid    | input bukan angka         |    "dua belas" |
| Rentang tidak valid | nilai < 0 atau nilai > 20 |             21 |
| Belum tuntas        | persentase < 75%          |             14 |
| Tuntas              | persentase >= 75%         |             15 |

### 5. Klasifikasi Segitiga Berdasarkan Sudut

| Kondisi     | Syarat                              | Contoh Masukan |
| ----------- | ----------------------------------- | -------------- |
| Tidak valid | ada sudut <= 0                      | 0, 90, 90      |
| Tidak valid | jumlah sudut tidak sama dengan 180° | 100, 50, 40    |
| Lancip      | sudut terbesar < 90°                | 60, 60, 60     |
| Siku-siku   | sudut terbesar = 90°                | 90, 45, 45     |
| Tumpul      | sudut terbesar > 90°                | 120, 30, 30    |

### 6. Praktik 1: Validasi dan Klasifikasi Nilai

| Kondisi                  | Syarat                                     |
| ------------------------ | ------------------------------------------ |
| Input tidak valid        | salah satu input bukan angka               |
| Nilai di luar rentang    | nilai ujian/tugas/kehadiran < 0 atau > 100 |
| Tidak memenuhi kehadiran | kehadiran < 80%                            |
| Predikat A               | nilai akhir >= 85                          |
| Predikat B               | nilai akhir >= 70                          |
| Predikat C               | nilai akhir >= 60                          |
| Predikat D               | nilai akhir >= 50                          |
| Predikat E               | nilai akhir < 50                           |
| Lulus                    | predikat A, B, atau C                      |
| Belum lulus              | predikat D atau E                          |

Nilai akhir dihitung dengan rumus:

```text
Nilai akhir = (0.6 × nilai ujian) + (0.4 × nilai tugas)
```

## Hasil Pengujian

### 1. Latihan Predikat Nilai

| Input | Output yang Diharapkan |
| ----: | ---------------------- |
|    92 | A                      |
|    85 | A                      |
|  84.9 | B                      |
|    70 | B                      |
|    60 | C                      |
|    50 | D                      |
|  49.9 | E                      |

### 2. Latihan Kategori Bilangan

| Input | Output yang Diharapkan |
| ----: | ---------------------- |
|    -7 | Negatif                |
|     0 | Nol                    |
|     8 | Positif genap          |
|    13 | Positif ganjil         |

### 3. Latihan Validasi Rentang

| Input | Output yang Diharapkan |
| ----: | ---------------------- |
|    45 | Sudut lancip           |
|    90 | Sudut siku-siku        |
|   135 | Sudut tumpul           |
|     0 | Tidak valid            |
|   180 | Tidak valid            |
|   -30 | Tidak valid            |

### 4. Latihan Validasi Tipe

|       Input | Output yang Diharapkan |
| ----------: | ---------------------- |
|          15 | 75% - Tuntas           |
|          14 | 70% - Belum tuntas     |
|          20 | 100% - Tuntas          |
|           0 | 0% - Belum tuntas      |
|          21 | Tidak valid            |
| "dua belas" | Tidak valid            |

### 5. Latihan Klasifikasi Segitiga

| Input       | Output yang Diharapkan                     |
| ----------- | ------------------------------------------ |
| 60, 60, 60  | Segitiga lancip                            |
| 90, 45, 45  | Segitiga siku-siku                         |
| 120, 30, 30 | Segitiga tumpul                            |
| 100, 50, 40 | Tidak valid karena jumlah sudut bukan 180° |
| 0, 90, 90   | Tidak valid karena setiap sudut harus > 0  |

### 6. Praktik 1

| Nilai Ujian | Nilai Tugas | Kehadiran | Output yang Diharapkan                     |
| ----------: | ----------: | --------: | ------------------------------------------ |
|          90 |          80 |        95 | 86.00, A, Lulus                            |
|          75 |          70 |        85 | 73.00, B, Lulus                            |
|          60 |          60 |        80 | 60.00, C, Lulus                            |
|          55 |          50 |        90 | 53.00, D, Belum lulus                      |
|          40 |          30 |       100 | 36.00, E, Belum lulus                      |
|          90 |          90 |        75 | 90.00, Tidak memenuhi syarat kehadiran     |
|         105 |          80 |        90 | Ditolak karena nilai ujian di luar rentang |
|          80 |          -5 |        90 | Ditolak karena nilai tugas di luar rentang |
|          80 |          80 |     "abc" | Ditolak karena input bukan angka           |

## Refleksi

Salah satu masukan tidak valid yang perlu diperhatikan adalah ketika pengguna memasukkan teks, misalnya `"abc"` pada bagian nilai.

Jika input langsung dikonversi menggunakan `float()` tanpa `try-except`, program dapat mengalami error. Oleh karena itu, konversi input dilindungi menggunakan `try-except ValueError`.

Selain itu, nilai ujian, tugas, dan kehadiran harus berada pada rentang 0 sampai 100. Jika berada di luar rentang tersebut, program menolak input dan memberikan pesan kesalahan yang sesuai.

## Kesimpulan

Pada pertemuan ini dipelajari penggunaan `if-elif-else` untuk membuat beberapa kondisi, validasi tipe data, validasi rentang, serta validasi domain.

Pengujian dilakukan pada setiap cabang kondisi, termasuk nilai batas dan input yang tidak valid, agar program dapat berjalan sesuai dengan aturan yang telah ditentukan.
## Catatan Pengujian

Pengujian dilakukan dengan mencoba setiap kondisi pada program,
termasuk nilai batas, nilai di luar rentang, dan input yang bukan angka.

Pengujian dilakukan untuk memastikan setiap percabangan
if-elif-else menghasilkan keluaran yang sesuai.