---
title: Another form of number type in swift
date: '2023-01-19'
tags: ['foundation', 'swift']
draft: false
summary: 'In this article I want to share another form of number types in swift programming language'
---

## Number Types in Swift

Sebagai iOS Engineer, kita akan sering menggunakan tipe data numerik seperti **_integer_**, _**double**_, atau _**float**_. Swift menyediakan lebih banyak tipe data numerik, berdasarkan kebutuhan developer apabila memiliki kebutuhan/ketentuan tertentu seperti batasan nilai atau memori yang digunakan.

Apabila developer membutuhkan tipe data numerik dengan bilangan asli (_**whole number**_), terdapat _**signed types**_ yang dapat digunakan seperti _Int8_, _Int16_, _Int32_, _Int64_ yang masing-masing akan memakan memori 1,2,4, dan 8 btyes secara berurutan.

Jika yang dibutuhkan adalah tipe data numerik dengan bilangan cacah (_**non-negative**_), terdapat _**unsigned types**_ yang dapat digunakan seperti _UInt8_, _UInt16_, _UInt32_, _UInt64_ . Karena tipe data ini tidak dapat menerima nilai negatif, maka dari itu nilai maksimum yang dapat di terima oleh tipe data ini akan 2 kali lebih besar daripada _**signed types**_ namun tetap memakan memori dalam jumlah yang sama.

Tujuan dari penggunaan tipe data ini agar developer dapat memastikan penggunaan tipe data yang tepat atau ingin mengoptimalisasi penggunaan memori yang digunakan untuk menjalankan software.

| Type    | Minimum Value        | Maximum Value        | Storage Size |
| ------- | -------------------- | -------------------- | ------------ |
| Int8    | -128                 | 127                  | 1            |
| UInt8   | 0                    | 255                  | 1            |
| Int16   | -32768               | 32767                | 2            |
| UInt16  | 0                    | 65535                | 2            |
| Int32   | -2147483648          | 2147483647           | 4            |
| UInt32  | 0                    | 4294967295           | 4            |
| Int64   | -9223372036854775808 | 9223372036854775807  | 8            |
| UInt164 | 0                    | 18446766073709551615 | 8            |
