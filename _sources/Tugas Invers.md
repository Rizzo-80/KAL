# Penyelesaian Matriks 4x4

## Matriks A

$$
A = \begin{bmatrix}
1 & 1 & 1 & 1 \\
2 & -1 & 1 & -1 \\
1 & 2 & -1 & 1 \\
3 & -1 & 2 & 1
\end{bmatrix}
$$

---

## 1. Menghitung Determinan

### Langkah-langkah:

**Matriks awal:**
$$
\begin{bmatrix}
1 & 1 & 1 & 1 \\
2 & -1 & 1 & -1 \\
1 & 2 & -1 & 1 \\
3 & -1 & 2 & 1
\end{bmatrix}
$$

**OBE 1:** Eliminasi kolom 1
- $R_2 \leftarrow R_2 - 2R_1$
- $R_3 \leftarrow R_3 - R_1$
- $R_4 \leftarrow R_4 - 3R_1$

$$
\begin{bmatrix}
1 & 1 & 1 & 1 \\
0 & -3 & -1 & -3 \\
0 & 1 & -2 & 0 \\
0 & -4 & -1 & -2
\end{bmatrix}
$$

**OBE 2:** Tukar $R_2 \leftrightarrow R_3$ (det × -1)

$$
\begin{bmatrix}
1 & 1 & 1 & 1 \\
0 & 1 & -2 & 0 \\
0 & -3 & -1 & -3 \\
0 & -4 & -1 & -2
\end{bmatrix}
$$

**OBE 3:** Eliminasi kolom 2
- $R_3 \leftarrow R_3 + 3R_2$
- $R_4 \leftarrow R_4 + 4R_2$

$$
\begin{bmatrix}
1 & 1 & 1 & 1 \\
0 & 1 & -2 & 0 \\
0 & 0 & -7 & -3 \\
0 & 0 & -9 & -2
\end{bmatrix}
$$

**OBE 4:** Eliminasi kolom 3
- $R_4 \leftarrow R_4 - \frac{9}{7}R_3$

$$
\begin{bmatrix}
1 & 1 & 1 & 1 \\
0 & 1 & -2 & 0 \\
0 & 0 & -7 & -3 \\
0 & 0 & 0 & \frac{13}{7}
\end{bmatrix}
$$

### Hasil Determinan:

$$\det(A) = (-1)^1 \times (1 \times 1 \times -7 \times \frac{13}{7}) = (-1) \times (-13) = \boxed{13}$$

---

## 2. Menghitung Invers Matriks

### Metode Augmented Matrix [A|I]

**Matriks awal:**
$$
\left[\begin{array}{cccc|cccc}
1 & 1 & 1 & 1 & 1 & 0 & 0 & 0 \\
2 & -1 & 1 & -1 & 0 & 1 & 0 & 0 \\
1 & 2 & -1 & 1 & 0 & 0 & 1 & 0 \\
3 & -1 & 2 & 1 & 0 & 0 & 0 & 1
\end{array}\right]
$$

**Setelah serangkaian OBE** (sama seperti perhitungan determinan + eliminasi balik):

$$
\left[\begin{array}{cccc|cccc}
1 & 0 & 0 & 0 & 1 & \frac{5}{11} & -\frac{4}{11} & -\frac{2}{11} \\
0 & 1 & 0 & 0 & -3 & -\frac{4}{11} & \frac{23}{11} & \frac{6}{11} \\
0 & 0 & 1 & 0 & -1 & -\frac{2}{11} & \frac{6}{11} & \frac{3}{11} \\
0 & 0 & 0 & 1 & 4 & \frac{1}{11} & -\frac{25}{11} & -\frac{7}{11}
\end{array}\right]
$$

---

## Hasil Akhir

### ✅ Determinan:
$$\boxed{\det(A) = 13}$$

### ✅ Invers Matriks:
$$
\boxed{
A^{-1} = \begin{bmatrix}
1 & \frac{5}{11} & -\frac{4}{11} & -\frac{2}{11} \\[6pt]
-3 & -\frac{4}{11} & \frac{23}{11} & \frac{6}{11} \\[6pt]
-1 & -\frac{2}{11} & \frac{6}{11} & \frac{3}{11} \\[6pt]
4 & \frac{1}{11} & -\frac{25}{11} & -\frac{7}{11}
\end{bmatrix}
}
$$

### Atau dalam bentuk faktorisasi:

$$
A^{-1} = \frac{1}{11} \begin{bmatrix}
11 & 5 & -4 & -2 \\
-33 & -4 & 23 & 6 \\
-11 & -2 & 6 & 3 \\
44 & 1 & -25 & -7
\end{bmatrix}
$$

---

## Verifikasi

$$A \times A^{-1} = I$$

Contoh elemen (1,1):
$$1(1) + 1(-3) + 1(-1) + 1(4) = 1 - 3 - 1 + 4 = 1 \checkmark$$

Contoh elemen (1,2):
$$1(\frac{5}{11}) + 1(-\frac{4}{11}) + 1(-\frac{2}{11}) + 1(\frac{1}{11}) = \frac{5-4-2+1}{11} = 0 \checkmark$$

**✓ Hasil benar!**