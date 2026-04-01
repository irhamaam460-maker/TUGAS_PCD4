LAPORAN PENGOLAHAN CITRA DIGITAL

Judul
Implementasi Pengolahan Citra Digital Menggunakan Python (OpenCV di Google Colab)

Tujuan
Tujuan dari praktikum ini adalah untuk memahami dan mengimplementasikan berbagai teknik dasar dalam pengolahan citra digital, meliputi:

1. Konversi RGB ke grayscale
2. Konversi grayscale ke biner
3. Konversi grayscale ke m-bit
4. Operasi brightness
5. Operasi contrast
6. Histogram grayscale
7. Histogram equalization

DASAR TEORI

1. Konversi RGB ke Grayscale
   Citra RGB terdiri dari tiga kanal warna yaitu Red (R), Green (G), dan Blue (B).
   Grayscale merupakan citra yang hanya memiliki satu kanal intensitas.

Konversi dilakukan dengan rumus:
Gray = 0.299R + 0.587G + 0.114B

Tujuan:

- Menyederhanakan citra
- Mengurangi kompleksitas data
- Mempermudah proses pengolahan lanjutan

2. Konversi Grayscale ke Biner
   Citra biner hanya memiliki dua nilai intensitas:

- 0 (hitam)
- 255 (putih)

Menggunakan metode threshold:
f(x) =
0   jika x < T
255 jika x ≥ T

Tujuan:

- Segmentasi objek dan background
- Mempermudah analisis bentuk

3. Konversi Grayscale ke M-bit (Quantization)
   Quantization adalah proses pengurangan jumlah level intensitas.

Contoh:

- 8-bit = 256 level
- 4-bit = 16 level

Tujuan:

- Mengurangi ukuran data
- Efisiensi penyimpanan
- Digunakan dalam kompresi citra

4. Operasi Brightness
   Brightness adalah tingkat kecerahan citra.

Rumus:
g(x) = f(x) + β

Tujuan:

- Mencerahkan atau menggelapkan citra
- Memperbaiki pencahayaan

5. Operasi Contrast
   Contrast adalah perbedaan antara bagian terang dan gelap.

Rumus:
g(x) = α f(x)

Tujuan:

- Memperjelas detail
- Meningkatkan kualitas visual

6. Histogram Grayscale
   Histogram adalah grafik distribusi intensitas pixel.

- Sumbu X: intensitas (0–255)
- Sumbu Y: jumlah pixel

Tujuan:

- Analisis kualitas citra
- Mengetahui tingkat kontras

7. Histogram Equalization
   Histogram Equalization adalah teknik untuk meningkatkan kontras dengan meratakan distribusi intensitas.

Tujuan:

- Memperjelas detail tersembunyi
- Memperbaiki citra dengan kontras rendah

IMPLEMENTASI

Setiap teori di atas diimplementasikan menggunakan Python dan OpenCV, seperti:

- cv2.cvtColor() → grayscale
- cv2.threshold() → biner
- np.floor() → quantization
- cv2.convertScaleAbs() → brightness & contrast
- plt.hist() → histogram
- cv2.equalizeHist() → histogram equalization

ANALISIS PERTANYAAN DOSEN

Apakah teori di kelas sama dengan kode di Colab?

Jawaban:
Secara konsep, teori yang dipelajari di kelas sama dengan implementasi pada Google Colab. Keduanya menggunakan prinsip dasar yang sama dalam pengolahan citra digital.

Namun terdapat perbedaan dalam prosesnya:

1. Dari sisi teori:

- Menggunakan rumus matematis
- Dilakukan secara manual
- Fokus pada konsep dasar

2. Dari sisi implementasi:

- Menggunakan library (OpenCV)
- Proses otomatis dan cepat
- Sudah dioptimasi oleh sistem

Kesimpulan:
Proses yang dilakukan pada teori dan implementasi adalah sama secara konsep, namun berbeda dalam cara pengerjaan. Pada Google Colab, proses menjadi lebih efisien karena menggunakan fungsi yang sudah tersedia.

KESIMPULAN

Pengolahan citra digital merupakan teknik penting dalam dunia komputer untuk meningkatkan kualitas dan analisis gambar.

Setiap metode memiliki fungsi spesifik:

- Grayscale → penyederhanaan citra
- Biner → segmentasi
- Quantization → efisiensi data
- Brightness & Contrast → perbaikan visual
- Histogram → analisis distribusi
- Equalization → peningkatan kontras

Dengan menggunakan Python dan OpenCV, seluruh proses dapat dilakukan dengan cepat dan efisien tanpa mengubah konsep dasar teori.

REFERENSI

1. Gonzalez, R. C., & Woods, R. E. – Digital Image Processing
2. OpenCV Documentation
3. IEEE Journal: Image Enhancement Using Histogram Equalization
