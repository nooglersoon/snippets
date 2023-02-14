---
title: Arrays, Dictionaries and Sets in Swift
date: '2023-01-26'
tags: ['foundation', 'swift']
draft: true
summary: 'In this article I want to share about the differences between array, dictionary, and set based on its purpose, performance and memory usage'
---

# Apa itu collections di dalam bahasa pemrograman swift?

Collections dapat diartikan sebagai kontainer/wadah yang bersifat fleksibel untuk menyimpan beberapa data dengan tipe data yang sama. Untuk pembahasan di dalam micro blog ini, collections yang akan dibahas mencakup Array, Dictionary dan Set yang merupakan collections paling sederhana dan sering digunakan di bahasa pemrograman swift.

## Array

Array merupakan tipe collection yang paling umum digunakan di dalam swift. Setiap kali menginisialisasi array, perlu dijelaskan tipe data apa yang digunakan oleh elemen pada array tersebut.

```
// myCollections merupakan sebuah array dengan tipe data String
let myCollections: [String] = ["Fauzi", "Achmad", "Bangsa", "Diria"]
```

### Karakteristik

Array merupakan ordered collection yang memiliki tipe data yang sama. Setiap elemen di dalam array akan memiliki sebuah index yang menunjukan posisi data tersebut di dalam array. Seperti pada bahasa pemrograman pada umumnya, array di Swift akan dimulai dengan index berbasis 0 dan index terakhir adalah jumlah elemen array dikurangi dengan 1.

| Element | Fauzi | Achmad | Bangsa | Diria |
| ------- | ----- | ------ | ------ | ----- |
| Index   | 0     | 1      | 2      | 3     |

### Penggunaan tipe data array

Array cocok digunakan untuk menyimpan sebuah koleksi data yang urutannya diperhatikan, sehingga apabila ada kebutuhan untuk dapat mengurutkan data, array sudah memiliki method yang dapat mendukung kebutuhan tersebut.

### Menilai operasi sebuah array

#### Mengakses elemen

Untuk mengakses satu elemen pada spesifik posisi di sebuah array, running time yang dibutuhkan (dalam big-O notation) adalah linear time atau constant time.

Constant time - O(1): Dapat terjadi apabila array hanya memiliki satu elemen, sehingga tidak perlu mengecek lokasi dimana elemen tersebut disimpan

Linear time - O(n): Dapat terjadi apabila array memiliki lebih dari satu elemen, karena pointer perlu mengecek lokasi elemen pada array satu per satu sampai dengan index yang diingingkan.

#### Memambahkan elemen

Untuk menambahkan elemen di dalam sebuah array, running time yang dibutuhkan akan bergantung pada posisi elemen akan ditambahkan.

Apabila ingin menambahkan elemen pada index pertama (0), maka swift perlu melakukan pemindahan elemen dari index pertama ke index + 1, sehingga running time yang dibutuhkan adalah linear time O(n), bergantung dengan jumlah elemen yang akan dipindahkan

Apabila ingin menambahkan elemen pada di tengah sebuah array, maka running time yang dibutuhkan adalah linear time O(n), menyesuaikan dengan jumlah elemen yang dipindahkan.

Apabila ingin menbamahkan elemen di akhir sebuah array atau pada index ke (jumlah array-1), waktu yang dibutuhkan adalah O(1), meskipun swift perlu menambahkan space, tapi tidak perlu ada waktu untuk menggeser elemen lain pada array tersebut.

#### Menghapus elemen

Menghapus atau mengeluarkan elemen dari sebuah array akan membuat satu tempat kosong, sehingga elemen sisanya perlu bergerak memenuhi tempat tersebut. Menggerakan elemen ke kiri (untuk memenuhi) space kosong tersebut akan membutuhkan linear time O(n). Namun, apabila elemen yang dihapus adalah elemen yang terletak di akhir atau dengan index (jumlah array - 1), maka hanya dibutuhkan waktu O(1) karena tidak mempengaruhi posisi elemen lainnya di dalam array tersebut.

#### Mencari sebuah elemen

Mencari sebuah elemen yang spesifik di sebuah array akan membutuhkan waktu O(n), karena pointer perlu melakukan pengecekan disetiap index untuk dapat menemukan elemen yang diinginkan.
