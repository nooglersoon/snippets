---
title: How to write a good variable in python
date: '2023-02-14'
tags: ['foundation', 'python', 'python roadmap']
draft: false
summary: 'In this article I want to share how to write a good variable in python programming languages'
---

# Apa itu variabel?

Variabel adalah sebuah kontainer yang berfungsi untuk menyimpan sebuah data atau nilai. Variabel juga dapat diartikan sebagai sebuah cara untuk membuat label pada sebuah objek data dengan tujuan mendeksiprsikan objek tersebut.

Variabel memungkinkan kita menyimpan sebuah data di memori komputer yang nantinya dapat kita pakai berulang.

Cara membuat variable menggunakan bahasa pemrograman `python`:

```
# Syntax
variable_name = value

# Example
name = 'Fauzi'
age = 20
```

# Why do we need to write a good variable?

Pada saat menulis sebuah program, penamaan variabel akan menjadi sangat penting, karena:

- Variabel akan memungkinkan digunakan berulang oleh beberapa fungsi atau operasi di dalam sebuah script
- Program yang kita buat harus dapat dipahami oleh orang lain agar program dapat dieksekusi, dimodifikasi dan diperbaharui tanpa perlu konfirmasi ke kita sebagai penulis program
- Variabel merupakan representatif sebuah data atau objek, sehingga penamaan yang tidak sesuai dapat berakibat kesalahan penulisan lojik sebuah program

## Examples

### 1. Penamaan variabel harus dapat mendeskripsikan objek atau nilai dari variabel tersebut, jelas dan memiliki makna

#### Good Variables ✅

```
name = 'Fauzi'
capital_city = 'London'
total_time_in_seconds = 45
```

#### Bad Variables ❌

```
biodata = 'Fauzi'
x = 'London'
time = 45
```

### 2. Penamaan variabel dapat mengkombinasikan huruf, angka dan underscore(\_). Namun, harus diawali dengan huruf atau underscore(\_).

Apabila nama variabel terlalu panjang, hindari penggunaan spasi dan gunakan underscore untuk pemisahnya. Simbol selain underscore dapat merepresentasikan operasi matematika atau reserved words di dalam bahasa pemrograman sehingga tidak dapat dituliskan di dalam variabel.

#### Good Variables ✅

```
nama_pelanggan_1 = 'Fauzi'
nama_pelanggan_2 = 'Achmad'
_last_name = 'Bangsa Diria'
```

#### Bad Variables ❌

```
1_nama_pelanggan = 'Fauzi'
e*& = 'Simbol'
```

### 3. Tidak menggunakan python keywords atau reserved words

Selain tidak merepresentasikan sebuah objek, reserved keywords biasanya sudah digunakan untuk penulisan sebuah program di dalam bahasa pemrograman untuk menulis lojik boolean, pengulangan dan kebutuhan lainnya seperti `for`, `True`, `else`, `not`, `and`, atau `if`.

#### Good Variables ✅

```
is_data_fetched = False
is_main_character_graduated = True
print_name = 'Fauzi'
```

#### Bad Variables ❌

```
True = not False
if = 'Aji'
print = 'Fauzi'
```

### 4. Gunakan naming rules yang dianjurkan oleh bahasa pemrogramman python

#### Good Variables ✅

```
# snake_case
full_name = 'Fauzi Achmad'
# MACRO_CASE
CAPITAL_CITY = 'Amsterdam'
# camelCase
databaseName = 'English Football Clubs'
# PascalCase
PortNumber = 5432
```
