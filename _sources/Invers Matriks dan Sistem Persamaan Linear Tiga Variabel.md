---
title: Invers Matriks dan Sistem Persamaan Linear Tiga Variabel

---

### Materi ini menjelaskan bagaimana cara:

- Membuat sistem persamaan linear tiga variabel dengan koefisien yang unik.

- Menentukan invers dari matriks koefisien.

- Menentukan vektor ( B ) sehingga $( A^{-1} \times B = \begin{bmatrix}1 \ 0 \ 0\end{bmatrix} )$

Menyelesaikan sistem tersebut baik secara teoretis maupun melalui implementasi di Excel.

#### 1. Menentukan Matriks Koefisien ( A )
Pilihlah sebuah matriks ( A ) berukuran 3×3 dengan koefisien yang berbeda (tidak ada persamaan yang identik) dan pastikan (\det(A) \neq 0) agar matriks tersebut dapat diinverskan.
Misalnya, kita ambil:

 
 
Penjelasan:

- Baris pertama merepresentasikan persamaan: (3x + 1y + 2z).

- Baris kedua merepresentasikan persamaan: (1x + 4y - 1z).

- Baris ketiga merepresentasikan persamaan: (2x - 2y + 5z).

Pastikan nilai determinan dari ( A ) tidak nol agar ( A ) memiliki invers.

#### 2. Menentukan Vektor ( B )
Untuk mendapatkan agar hasil perkalian invers ( A ) dengan vektor ( B ) menghasilkan:

$$A^{-1}\times B = \begin{bmatrix} 1 \\
0 \\
0
\end{bmatrix}$$
 
salah satu cara yang paling mudah adalah dengan memilih ( B ) sebagai kolom pertama dari ( A ).
Dengan demikian, kita tetapkan:

$$B = \begin{bmatrix} 3 \\
1 \\
2
\end{bmatrix}$$
 
Alasan Pemilihan ( B ):

Misalkan kita ingin mencari solusi ( X ) dari persamaan

$$A \times X = B$$

Jika kita memilih

$$X = \begin{bmatrix} 1 \\
0 \\
0
\end{bmatrix}$$
 
maka kita peroleh:

$A \times \begin{bmatrix} 1 \\0 \\0\end{bmatrix}$ = 1 . (kolom pertama A) + 0 . (kolom kedua A) + 0 . (kolom ketiga A) = kolom pertama A

 Karena kolom pertama ( A ) adalah ( B ), maka:

$$A \times \begin{bmatrix} 1\\ 0\\ 0\end{bmatrix} = B$$
 
Mengalikan kedua sisi dengan ( A^{-1} ) (dengan ( A ) invertibel) memberikan:

$$A^{-1} \times B  = \begin{bmatrix} 1\\ 0\\ 0\end{bmatrix}$$
 
#### 3. Menuliskan Sistem Persamaan Linear
Dengan matriks ( A ) dan vektor ( B ) yang telah ditentukan, sistem persamaan linear yang harus dipenuhi adalah:

$$\begin{cases}
3x + y + 2z = 3, \\
x + 4y - z = 1, \\
2x - 2y + 5z = 2
\end{cases}$$


Detail:

- Persamaan 1: Diambil dari baris pertama ( A ) dan elemen pertama ( B ): ( 3x + 1y + 2z = 3 ).

- Persamaan 2: Diambil dari baris kedua ( A ) dan elemen kedua ( B ): ( 1x + 4y - 1z = 1 ).

- Persamaan 3: Diambil dari baris ketiga ( A ) dan elemen ketiga ( B ): ( 2x - 2y + 5z = 2 ).

#### 4. Hubungan Antara Invers Matriks dan Solusi Sistem
Karena ( A ) adalah matriks invertibel, kita dapat menyelesaikan sistem:

$$A \times X = B$$

dengan cara mengalikan kedua sisi persamaan tersebut dengan $( A^{-1} )$:

$$X = A^{-1} \ times B$$

Dengan pemilihan ( B ) sebagai kolom pertama ( A ), maka solusi yang diperoleh adalah:

$$X \begin{bmatrix} 1\\ 0\\ 0 \end{bmatrix}$$
 
Artinya, jika kita menghitung $( A^{-1} \times B )$ secara manual atau dengan alat bantu (misalnya kalkulator matriks), hasilnya haruslah:

$$\begin{bmatrix}1\\0\\0\end{bmatrix}$$
 
#### 5. Implementasi di Excel (Tanpa Coding)
Anda juga dapat menyelesaikan perhitungan ini di Excel tanpa menggunakan kode pemrograman. Berikut langkah-langkahnya:

##### a. Menuliskan Matriks ( A ) dan Vektor ( B )
- Matriks ( A ):
Masukkan koefisien matriks ke dalam sel A1:C3 seperti berikut:
A1: 3  B1: 1  C1: 2
A2: 1  B2: 4  C2: -1
A3: 2  B3: -2  C3: 5

- Vektor ( B ):
Masukkan elemen vektor ke dalam sel E1:E3:
E1: 3  E2: 1  E3: 2

##### b. Menghitung Invers Matriks ( A )
1. Pilih area kosong untuk menampilkan invers, misalnya A5:C7.

2. Ketikkan formula:

3. Tekan Ctrl+Shift+Enter (jika menggunakan Excel versi lama) atau cukup Enter (di Excel 365) untuk mendapatkan hasil invers ( A^{-1} ).

##### c. Mengalikan ( A^{-1} ) dengan ( B )
1. Pilih area kosong, misalnya E5:E7, untuk menampilkan hasil perkalian.

2. Ketikkan formula:

3. Tekan Ctrl+Shift+Enter atau Enter sesuai dengan versi Excel yang Anda gunakan.

Hasil yang akan muncul di E5:E7 adalah:

E5: 1
E6: 0
E7: 0

Hal ini menunjukkan bahwa $( A^{-1} \times B = \begin{bmatrix}1 \ 0 \ 0\end{bmatrix} )$

### Ringkasan Materi
1. Matriks ( A ):

$$A = \begin{bmatrix}3 & 1 & 2\\
1 & 4 & -1\\
2 & -2 & 5\end{bmatrix}$$
 
2. Vektor ( B ) (dipilih sebagai kolom pertama ( A )):

$$B = \begin{bmatrix}3\\ 1\\ 2\end{bmatrix}$$
 
3. Sistem Persamaan Linear:

$$\begin{cases}3x + y +2z = 3,\\
x + 4y - z = 1,\\
2x - 2y +5z = 2.\end{cases}$$
 
4. Hubungan Invers:

Karena $( A \times \begin{bmatrix}1 \ 0 \ 0\end{bmatrix} = B )$, maka

$$A^{-1} \times B = \begin{bmatrix}1\\ 0\\ 0\end{bmatrix}$$
 
Implementasi di Excel:

- Gunakan fungsi MINVERSE untuk menghitung $( A^{-1} )$

- Gunakan fungsi MMULT untuk menghitung $( A^{-1} \times B )$ sehingga diperoleh $\begin{bmatrix}1 \ 0 \ 0\end{bmatrix}$