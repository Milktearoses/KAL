---
title: Untitled

---

### Penyelesaian Sistem Persamaan Linear dengan Metode Eliminasi Gauss dan Visualisasi dengan GeoGebra

#### 1. Pendahuluan
Sistem persamaan linear adalah kumpulan persamaan yang memiliki beberapa variabel, di mana setiap persamaan berbentuk linear. Salah satu metode untuk menyelesaikan sistem persamaan linear adalah Metode Eliminasi Gauss.

Metode Eliminasi Gauss bertujuan untuk menyederhanakan sistem persamaan ke dalam bentuk segitiga atas (eselon baris), sehingga penyelesaiannya lebih mudah ditemukan dengan substitusi balik.

#### 2. Langkah-langkah Metode Eliminasi Gauss
Menyusun Matriks Augmented

Tuliskan sistem persamaan dalam bentuk matriks yang mencakup koefisien variabel dan nilai konstanta. Mengubah Matriks ke Bentuk Eselon Baris

Gunakan operasi baris elementer untuk membuat nol di bawah elemen diagonal utama. Menyelesaikan dengan Substitusi Balik

Setelah matriks berbentuk segitiga atas, nilai variabel dapat ditemukan dengan substitusi balik.

#### 3. Contoh Soal
Misalkan kita memiliki sistem persamaan berikut:

2x+y=5 x−y=1

Kita akan menyelesaikan sistem ini menggunakan Metode Eliminasi Gauss.

#### 4. Menyusun Matriks Augmented
Sistem persamaan di atas dapat dituliskan dalam bentuk matriks augmented:

$\begin{bmatrix}
2 & 1 & | & 5 \\
1 & -1 & | & 1
\end{bmatrix}$

Di sini, kolom pertama dan kedua mewakili koefisien dari variabel x dan y, sedangkan kolom terakhir adalah nilai konstanta.

#### 5. Mengubah Matriks ke Bentuk Eselon Baris Langkah 1: Tukar Baris 1 dan Baris 2 (Opsional, agar elemen pertama menjadi 1)

$\begin{bmatrix}
1 & -1 & | & 1 \\
2 & 1 & | & 5
\end{bmatrix}$

Ini dilakukan agar perhitungan lebih sederhana.

Langkah 2: Eliminasi Elemen di Bawah Elemen Utama Pertama Kita buat elemen di bawah elemen pertama (2) menjadi nol dengan operasi:

$R_2 = R_2 -2R_1$

Perhitungannya:

- Baris 2 : (2,1,5) - 2 x (1, -1, 1)
- hasil : (0, 3, 3)

matriks menjadi:

$\begin{bmatrix}
1 & -1 & | & 1 \\
0 & 3 & | & 3
\end{bmatrix}$

Langkah 3: Ubah Elemen Diagonal Menjadi 1 Bagi Baris 2 dengan 3:

$R_2 = 1/3 R_2$

Hasilnya: $\begin{bmatrix}
1 & -1 & | & 1 \\
0 & 1 & | & 1
\end{bmatrix}$

Langkah 4: Eliminasi Elemen di Atas Elemen Utama Kita nol-kan elemen di atas 1 pada kolom kedua:

$R_1 = R_1 + R_2$

Perhitungannya:

- Baris 1 : (1, -1, 1) + (0, 1, 1)
- Hasil : (1, 0, 2)
- Matriks menjadi : $\begin{bmatrix}
1 & 0 & | & 2 \\
0 & 1 & | & 1
\end{bmatrix}$

6. Menentukan Solusi
Dari matriks akhir, kita dapat menuliskan hasil :
$x = 2, y = 1$
jadi solusi sistem persamaan adalah $(x,y) = (2,1)$

7. Visualisasi dengan GeoGebra
<iframe src="https://www.geogebra.org/calculator/yc4qjmnt?embed" width="800" height="600" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

geobra

eq1: x-y=1

eq2: 2 x+y=5

8. Kesimpulan
Metode Eliminasi Gauss adalah cara sistematis untuk menyelesaikan sistem persamaan linear dengan mengubahnya menjadi bentuk segitiga atas. Setelah itu, kita bisa menemukan nilai variabel dengan substitusi balik.

Visualisasi menggunakan GeoGebra membantu memahami solusi secara grafis dengan melihat titik perpotongan garis.

previous

Pengertian Persamaan Linear

next

Materi: Invers Matriks dan Sistem Persamaan Linear Tiga Variabel

