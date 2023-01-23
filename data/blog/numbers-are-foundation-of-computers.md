---
title: How numbers works on a computer
date: '2023-01-18'
tags: ['foundation', 'computer science']
draft: false
summary: 'In this article I want to explain how the numbers are works on a computer'
---

# Numbers are foundation of computer

Fundamental dan basis sebuah komputer adalah hanyalah sebuah kumpulan angka.
Setiap instruksi yang dibuat oleh **_compiler_** akan menghasilkan sebuah angka.
Begitupula dengan bagaimana gambar ditampilkan di dalam layar komputer yang merupakan kumpulan angka dalam jumlah besar sebagai representatif sebuah warna.

## Angka Desimal

Angka yang kita gunakan sehari-hari berbeda dengan angka yang diproses oleh sebuah **CPU**.

Sehari-hari kita akan menghitung uang, mengukur jarak, menimbang berat badan dan mengisi literan air dengan menggunakan angka
berbasis 10 atau yang dikenal sebagai **_decimal system_**. Dalam sistem dengan basis 10, setiap digit angka akan merepresentasikan dirinya sebagai sebuah nilai.

Faktor pengali dalam sistem angka berbasis 10 adalah 10, sehingga basisnya adalah 1, 10, 100, 1000, 10000...

`Penguraian angka 2023 berdasarkan basis 10: `

| 100000 | 10000 | 100 | 10  | 1   |
| ------ | ----- | --- | --- | --- |
| 0      | 2     | 0   | 2   | 3   |

`[100000 * 0] + [10000 * 2] + [100 * 0] + [10 * 2] + [1 * 3] = 2023`

## Angka Binary

Komputer bekerja dengan sangat sederhana. Bekerja dengan basis angka 10 akan membuatnya terlalu kompleks dan besar untuk melakukan komputasi.
Hingga saat ini, komputer menggunakan sistem angka yang sangat sederhana yakni hanya terdiri dari 0 dan 1. Sistem ini dikenal sebagai **_binary numbers_**.

Faktor pengali dalam sistem angka berbasis 2 adalah 2, sehingga basisnya adalah 1, 2, 4, 8, 32...

`Penguraian angka 25 berdasarkan basis 2: `

| 32  | 16  | 8   | 4   | 2   | 1   |
| --- | --- | --- | --- | --- | --- |
| 0   | 1   | 1   | 0   | 0   | 1   |

`[32 * 0] + [16 * 1] + [8 * 1] + [4 * 0] + [2 * 0] + [1 * 1] = 25`

- Satu digit binary number disebut sebagai 1 bit (**_binary digit_**).
- 8 bits dikenal dengan 1 _**byte**_
- 4 bits dikenal dengan _**nibble**_

Penggunaan jumlah bits ini sering disebutkan dalam penggunaan jenis CPU seperti 32-bit atau 64-bit CPU. Jumlah ini menunjukan limitasi memori yang dimiliki sebuah komputer. Misalkan, 32 bit CPU menandakan bahwa maksimum angka yang dapat diproses adalah sebanyak 32 bit atau 4,294,967,295 dalam angka.

## Angka Hexadecimal

Terdapat basis angka lainnya yang digunakan dalam dunia komputer. Salah satu nya adalah basis 16 atau sering kita kenal dengan `hexadecimal` atau `hex`. Dalam penggunaaan sistem basis 16, angka 10-15 akan diawakili oleh sebuah huruf sebagai berikut:

- a = 10
- b = 11
- c = 12
- d = 13
- e = 14
- f = 15

`Penguraian angka 431 berdasarkan basis 16: `

| 4096 | 256 | 16  | 1   |
| ---- | --- | --- | --- |
| 0    | 1   | a   | f   |

`[4096 * 0] + [256 * 1] + [16 * 10] + [1 * 15] = 431`

Penggunaan hexadecimal juga sering kita pakai untuk sistem warna seperti `#ffffff` merepresentasikan warna putih, `#000000` merepresentasikan warna hitam
