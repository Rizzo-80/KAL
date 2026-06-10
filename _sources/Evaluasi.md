# 📘 Menghitung Determinan Matriks (Ekspansi Baris)

## Rumus

$$
\det(A) = \sum_{k=1}^{n} (-1)^{i+k} \, a_{ik} \, M_{ik}
$$

---

##  Soal 1

$$
A = \begin{pmatrix}
-7 & -5 \\
1 & 4
\end{pmatrix}
$$

### Proses:

Gunakan rumus determinan matriks 2x2:

$$
\det(A) = ad - bc
$$

$$
= (-7)(4) - (-5)(1)
$$

$$
= -28 + 5
$$

$$
= -23
$$

---

##  Soal 2

$$
A = \begin{pmatrix}
0 & 2 & -3 \\
1 & -2 & -1 \\
0 & 0 & 1
\end{pmatrix}
$$

### Proses (ekspansi baris pertama):

$$
\det(A) = a_{11}C_{11} + a_{12}C_{12} + a_{13}C_{13}
$$

#### 1. Elemen $a_{11} = 0$

$$
0 \times \begin{vmatrix}
-2 & -1 \\
0 & 1
\end{vmatrix} = 0
$$


#### 2. Elemen $a_{12} = 2$

Minor:

$$
\begin{vmatrix}
1 & -1 \\
0 & 1
\end{vmatrix}
= (1)(1) - (-1)(0) = 1
$$

Kofaktor:

$$
(-1)^{1+2} = -1
$$

Kontribusi:

$$
2 \times (-1) \times 1 = -2
$$


#### 3. Elemen $a_{13} = -3$

Minor:

$$
\begin{vmatrix}
1 & -2 \\
0 & 0
\end{vmatrix}
= (1)(0) - (-2)(0) = 0
$$

Kontribusi:

$$
(-3) \times (+1) \times 0 = 0
$$


### Hasil:

$$
\det(A) = 0 - 2 + 0 = -2
$$

---

## Soal 3

$$
A = \begin{pmatrix}
1 & -3 & 1 & 1 \\
-3 & 1 & 1 & 1 \\
1 & 1 & -3 & 1 \\
1 & 1 & 1 & -3
\end{pmatrix}
$$

### Proses:

Saya menggunakan operasi baris (biar lebih cepat):

Jumlahkan semua baris ke baris pertama:

$$
R_1 = R_1 + R_2 + R_3 + R_4
$$

Hasil:

$$
R_1 = (1-3+1+1,\,-3+1+1+1,\,1+1-3+1,\,1+1+1-3)
$$

$$
R_1 = (0,0,0,0)
$$

Karena satu baris menjadi nol:

$$
\det(A) = 0
$$
tidak valid langsung karena operasi ini mengubah determinan

---
##  Menghitung Invers Matriks (Metode Adjoin)

### Rumus Utama

Berdasarkan aturan matriks adjoin:

1. **Mencari elemen Adjoin:**
   $$(\text{adj } A)_{ij} = (-1)^{i+j} M_{ji}$$
   *(Ingat: Adjoin adalah transpose dari matriks kofaktor)*

2. **Mencari Invers:**
   $$A^{-1} = \frac{1}{\det A} \text{adj } A$$

---

##  Soal 4 (Matriks 2x2)

$$
A = \begin{pmatrix}
-7 & -5 \\
1 & 4
\end{pmatrix}
$$

### Langkah 1: Hitung Determinan
$$\det(A) = (-7)(4) - (-5)(1) = -28 + 5 = -23$$

### Langkah 2: Cari Adjoin (Tukar diagonal utama, ganti tanda diagonal samping)
$$\text{adj } A = \begin{pmatrix}
4 & 5 \\
-1 & -7
\end{pmatrix}$$

### Langkah 3: Hasil Invers
$$
A^{-1} = \frac{1}{-23} \begin{pmatrix}
4 & 5 \\
-1 & -7
\end{pmatrix} = \begin{pmatrix}
-\frac{4}{23} & -\frac{5}{23} \\
\frac{1}{23} & \frac{7}{23}
\end{pmatrix}
$$

---

## Soal 5 (Matriks 3x3)

$$
A = \begin{pmatrix}
0 & 2 & -3 \\
1 & -2 & -1 \\
0 & 0 & 1
\end{pmatrix}
$$

### Langkah 1: Hitung Determinan (Ekspansi Baris 3 lebih cepat)
$$\det(A) = 0(C_{31}) + 0(C_{32}) + 1 \begin{vmatrix} 0 & 2 \\ 1 & -2 \end{vmatrix}$$
$$\det(A) = 1(0 - 2) = -2$$

### Langkah 2: Cari Matriks Kofaktor lalu Transpose (Adjoin)
Setelah menghitung kofaktor tiap elemen, didapatkan:
$$\text{adj } A = \begin{pmatrix}
-2 & -2 & -8 \\
-1 & 0 & -3 \\
0 & 0 & -2
\end{pmatrix}$$

### Langkah 3: Hasil Invers
$$
A^{-1} = \frac{1}{-2} \begin{pmatrix}
-2 & -2 & -8 \\
-1 & 0 & -3 \\
0 & 0 & -2
\end{pmatrix} = \begin{pmatrix}
1 & 1 & 4 \\
0.5 & 0 & 1.5 \\
0 & 0 & 1
\end{pmatrix}
$$

---

## Soal 6 (Matriks 4x4)

$$
A = \begin{pmatrix}
1 & -3 & 1 & 1 \\
-3 & 1 & 1 & 1 \\
1 & 1 & -3 & 1 \\
1 & 1 & 1 & -3
\end{pmatrix}
$$

### Analisis:
Berdasarkan perhitungan sebelumnya, didapatkan bahwa jumlah setiap baris adalah 0 ($1-3+1+1 = 0$).
Jika jumlah baris adalah nol, maka:
$$\det(A) = 0$$

### Kesimpulan:
Karena $\det(A) = 0$, maka matriks $A$ adalah **Matriks Singular**.
**Matriks ini tidak memiliki invers ($A^{-1}$ tidak terdefinisi).**

---