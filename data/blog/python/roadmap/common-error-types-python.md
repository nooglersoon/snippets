---
title: Get to know with common error types in python
date: '2023-02-14'
tags: ['foundation', 'python', 'python roadmap']
draft: false
summary: 'In this article I want to share about common error types in python'
---

# Apa itu error dalam programming?

_*Programming Error*_ adalah sebuah error atau kesalahan yang terjadi dalam pengembangan program atau saat suatu program dijalankan karena terjadinya kesalahan penulisan, lojik atau kesalahan lain baik dari sisi developer maupun sistem. Error dalam programming sangat lumrah terjadi, dikarenakan banyak faktor. Beberapa diantaranya termasuk kedalam error yang dihasilkan karena kesalahan developer.

Apabila menemukan sebuah error, jangan panik dan coba pahami maksud dari error tersebut sebelum akhirnya mencari tau cara memperbaiki error nya melalui situs pencaharian. Setiap bahasa pemrogragaman memiliki keunikan dan ciri khas masing-masing menyesuaikan dengan kebutuhan dan tujuan bahasa tersebut. Sehingga, error yang dihasilkan atau terjadi juga bisa berbeda-beda penyebabnya dan dalam pembahasan ini akan difokuskan pada error yang sering terjadi saat menulis program menggunakan bahasa python.

## Syntax Errors, Logic Errors & Exceptions

Pada dasarnya error dalam bahasa pemrograman python dapat dibagi kedalam tiga kelompok, yaitu syntax errors, logic errors dan exceptions. Syntax errors terjadi saat kita melakukan kesalahan penulisan kode yang tidak dipahami atau keluar dari aturan bahasa pemrograman python. Logic errors terjadi saat sebuah program tidak dapat dijalankan atau mengalami crash saat operasi karena lojik yang dibuat tidak mungkin dilakukan dan exceptions merupakan bentuk error saat python parser mengetahui apa yang akan dilakukan namun tidak dapat menjalankan operasi tersebut. Agar penamaan error menjadi lebih detail dan semantik, maka jenis error dapat dispesifikan lagi menyesuaikan dengan error yang terjadi seperti beberapa contoh dibawah.

## `SyntaxError`

Syntax error adalah salah satu jenis error yang sering terjadi di apabila kita menulis program. Setiap bahasa pemrogragaman memiliki cara penulisan yang berbeda, sehingga antar bahasa akan memiliki perbedaan sintaks penulisan. Pada dasarnya, kesalahan penulisan pada program yang tidak dimengerti oleh compiler/interpreter/parser atau yang menjalankan program sering dikenal sebagai syntax error atau kesalahan sintaks.

```
age = 20

if age > 25
  print("You are old!")
```

Kode diatas akan menghasilkan syntax error:

```
File "test.py", line 3
    if age > 25
                  ^
SyntaxError: invalid syntax
```

Karena parser/compiler tidak memahami bahasa tersebut, seharusnya pada bahasa python, apabila kita menuliskan if conditional, perlu diakhiri dengan ":"

```
age = 20

if age > 25:
  print("You are old!")
```

## `IdentiationError`

Kita tahu bahwa bahasa pemrograman python berbeda dengan bahasa lain, khususnya pada saat membuat sebuah blok kode. Apabila kalian familiar dengan bahasa pemrograman seperti java, javaScript atau C++, kalian akan sering menemukan tanda kurung kurawal `{}` sebagai penanda sebuah blok kode. Pada bahasa python, pemuatan blok sebuah kode di tandakan dengan level identasi atau spasi yang menjorok.

```
if age > 25:
  print("You are old!")
```

Kode diatas menunjukan bahwa `print("You are old!")` merupakan ekspresi yang akan dieksekusi apabila age lebih dari 25, bukan melainkan dua hal yang berbeda.

```
if age > 25:
print("You are old!")

IndentationError: expected an indented block
```

Kesalahan penulisan indentation akan memberikan IndentationError yang menunjukan bahwa pada kode tersebut, terdapat kesalahan penulisan yang membuat compiler bingung saat mengeksekusi kode tersebut.

## `NameError`

Error pada penulisan nama juga sering dialami saat kita menulis sebuah program menggunakan bahasa pemrograman python. Bayangkan apabila tiba-tiba anda lupa apakah pernah membuat sebuah variable `nama_lengkap` dan anda hanya membuat variabel `nama`.

```
nama = "Fauzi"
print(nama_lengkap)

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'nama_lengkap' is not defined
```

Compiler akan memberikan error karena tidak pernah ada variabel nama_lengkap selama kode dibuat. Maka, anda perlu berhati-hati dan mengingat selalu setiap variabel yang telah dibuat.

## `ImportError`

Apabila program kita membutuhkan penambahan module atau dependency dari code lain, kita perlu menuliskannya di dalam kode kita dengan cara meng import library atau module kedalam kode kita.

```
import pandas as pd
```

Namun, tidak jarang module yang kita import sudah tersedia di dalam komputer kita, sehingga saat kita melakukan import module, akan menimbulkan Import Error.

```
>>> import time
>>> import pandas
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ModuleNotFoundError: No module named 'pandas'
```

Pada kode diatas, dapat dilihat bahwa saat kita melakukan `import time`, tidak ada error yang muncul, hal ini karena di dalam komputer kita sudah terdapat module `time`. Berbeda dengan saat kita melakukan `import pandas`, muncul error yang memberitahu kita bahwa di dalam komputer kita tidak terdapat module dengan nama `pandas`.

## `IndexError`

Pada saat kita bekerja dengan menggunakan `list` atau `array` dalam bahasa pemrograman lain, kita akan mendefinisikan kelompok tersebut dan memasukan nilai-nilai yang tergabung pada kelompok tersebut.

```
>>> list = [1,2,3,"hallo"]
>>> print(list)
[1, 2, 3, 'hallo']
>>> print(list[0])
1
```

Apabila kita ingin menuliskan salah satu elemen di dalam list, kita dapat mengaksesnya dengan menuliskan `list[0]` dan compiler akan mengembalikan nilai index ke 0 di dalam `list`.

```
>>> print(list[10])
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
```

Namun, apabila kita menulis index yang diluar dari jumlah elemen pada list tersebut, kita akan mendapatkan `IndexError` yang menunjukan bahwa index yang kita pilih itu diluar dari jumlah elemen yang ada di dalam list tersebut.

## `KeyError`

Kasus yang sama terjadi saat kita membuat data struktur lain, yaitu dictionary. Dictionary merupakan struktur data yang identik dengan pengelompokan data menggunakan key-value dalam pembuatannya. Setiap key akan merepresentasikan sebuah nilai di dalam satu dictionary. Hal ini sangat serupa dengan cara kita membuka kamus, untuk mencari sebuah kata,

```
>>> dict = {"Name": "Aji", "Age": 25}
>>> dict["Name"]
'Aji'
>>> dict["Age"]
25
>>> dict["Address"]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 'Address'
>>>
```

## `TypeError`

TypeError akan terjadi saat menjalankan sebuah operasi yang tidak bisa dilakukan karena tipe objek tidak mendukung atau tidak masuk logika. Contohnya saat kita melakukan penambahan dari sebuah string dengan numerik (integer).

```
>>> num = 10
>>> str = "Aji"
>>> print(num + str)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

## `ValueError`

TypeError tidak akan terjadi apabila tipe data mendukung operasi yang akan dilakukan, namun bagaimana saat tipe datanya mendukung, namun nilai dari data tersebut tidak mungkin dilakukan untuk operasi matematika tertentu? Misalkan, menghitung akar dari -4 yang secara matematis tidak dapat dilakukan.

```
>>> import math
>>> math.sqrt(4)
2.0
>>> math.sqrt(-4)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: math domain error
```

## `ZeroDivisionError`

Salah satu error yang cukup spesifik saat menangani operasi matematika adalah `ZeroDivisionError`, karena error ini terjadi apabila terdapat operasi matematika yang menghasilkan nilai tidak terdefinisi yaitu saat membagi sebuah nilai dengan 0.

```
>>> 10/0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```

Masih banyak lagi bentuk error pada bahasa pemrograman python, bergantung kepada kesalahan syntax maupun lojik yang dibuat oleh penulis kode. Terkadang bentuk error nya dapat spesifik ataupun generik bergantung dengan error yang diterima oleh python parser.
