---
title: Introduction to Test Driven Development Part 1
date: '2023-02-17'
tags: ['unit tests', 'swift', 'Test Driven Development using Swift']
draft: false
summary: 'In this article I want to share about the introduction to TDD and its fundamental'
---

# What is Test Driven Development?

_Test Driven Development_ merupakan suatu cara iteratif untuk membangun sebuah perangkat lunak dengan pengembangan nya mulai dari fitur kecil yang ditopang oleh _test_ di setiap unit nya.

Implementasi TDD akan sangat mudah apabila kita mengikuti step-step yang biasa dilakukan di dalam industri, yaitu dengan mengikuti _TDD-Cycle_ atau siklus TDD. Siklus ini terdiri atas 4 tahapan, yaitu membuat _failing test_, _passed test_, _refactor_ & _repeat_.

Tahapan ini akan membantu _developer_ untuk membuat _production code_ yang aman dan memenuhi kriteria yang diberikan, sehingga saat membuat test diharapkan kita juga mempertimbangan pembuatan _failing test_ terlebih dahulu, agar dapat mengetahui _edge cases_ yang dapat terjadi dan membuat _bug_ dalam _production code_.

## How to make a good test?

Saat kita berbicara mengenai test, beberapa orang membicarakan mengenai prinsip dalam testing atau yang paling terkenal adalah F.I.R.S.T _principles of testing_. FIRST merupakan akronim dari _Fast_, _Isolated_, _Repeatable_, _Self-validating_ & _Thorough_.

- **_Fast_**: Sebaiknya pada saat kita menulis sebuah test, _developer_ harus bisa memastikan bahwa sebuah test dapat dijalankan dengan cepat.
- **_Isolated/Independent_**: Setiap pembuatan satu test harus spesifik untuk _case_ atau _action_ tertentu yang didukung dengan _enviroment_ atau _dependency_ yang terisolasi hanya untuk test tersebut. Hal ini bertujuan agar hasil dari sebuah test tidak dipengaruhi faktor lain.
- **_Repeatable_**: Setiap kali kita menjalankan sebuah test, diharapkan kita dapat menjalankan test tersebut berulang dengan menghasilkan hasil test yang sama. Hal ini bertujuan untuk meyakini bahwa di _production code_, _action_ tersebut akan selalu menghasilkan keluaran yang sesuai dengan ekspektasi _developer_
- **_Self-validating_**: Test yang dijalankan harus bisa menghasilkan yang menunjukan bahwa test berhasil atau gagal.
- **_Thorough_**: Test yang dibuat harus dapat mengcover semua _case_, _happy/positive path_, _error_ & _negative path_.

Selain dari ke lima step diatas, ada beberapa hal yang perlu diperhatikan saat membuat sebuah test, yaitu adalah pastikan test yang dibuat adalah _maintainable_. Pada saat mendevelop sebuah fitur, apabila ada perubahan pada _production code_, pastikan dilakukan penyesuaian terhadap test terlebih dahulu untuk menghindari adanya perbedaan antara _production code_ dan _test code_.

## What do we need to test?

Tidak semua hal yang ditulis perlu dilakukan test, khususnya untuk code seperti _framework_ atau API bawaan dari bahasa pemrograman (swift) dan _third-party framework_. Hal ini karena yang wajib melakukan test adalah pembuat dari _framework_ tersebut. Kita tidak akan pernah tau _edge cases_ seperti apa yang perlu di test dari _framework_ tersebut dan akan menimbulkan asumsi yang membuat test tersebut menjadi tidak valid. Maka dari itu saat kita menulis sebuah test, hanya fokus saja pada code yang kita tulis.

## Does implementing TDD will take a longer development time process?

"_Test-Driven Development_ adalah proses yang cukup memakan waktu saat _development_". _Statement_ ini sering kali dirasakan apabila kita baru mencoba untuk mengimplementasikan TDD pada project kita. Nyatanya, pada saat kita mengembangkan sebuah program, pengembangan tidak hanya dilakukan saat kita pertama kali membuat _production code_, tetapi juga saat kita melakukan _improvement_, _maintenance_ atau _fixing bug_.

Sehingga waktu untuk mengembangkan sebuah program akan memakan waktu dan biaya yang besar. Hal ini berbanding terbalik dengan tujuan utama dari TDD. Justru, saat kita mengimplementasikan TDD, seharusnya _production code_ bisa dipastikan minim _bug_ atau _error_ dan juga mudah dilakukan _improvement_ ataupun _maintenance_, karena sudah dilakukan saat kita membuat test untuk _production code_.

## Does we need to implement TDD on every project?

Pertanyaan ini juga sering kali menjadi pembahasan saat memulai sebuah project. TDD dapat dilakukan saat memulai project ataupun meneruskan _legacy code_. Namun, semua bergantung pada kebutuhan team dan waktu yang dimiliki. Memang TDD akan lebih banyak memakan waktu saat _initial development_, karena kita perlu membuat _test code_ dan _production code_ saat _development_, tapi akan dapat mengurasi _cost development_ di kemudian hari dengan memastikan _code_ ini _maintainable_ dan minim _bug_.

Bagi saya, implementasi TDD akan bisa diimplementasi apabila waktu pengerjaan panjang dan _lifetime_ dari proyek juga di proyeksikan panjang. Karena apabila _lifetime project_ nya pendek, yang menjadi _concern_ adalah apakah waktu _development_ akan bisa mencapai tujuannya? Seperti hal nya saat kita mengembangkan _prototype_ atau proyek untuk _hackaton_ atau untuk kebutuhan _pitching_, yang menjadi tujuan nya adalah bagaimana produk tersebut bisa ditunjukan dan digunakan bukan memastikan produk nya mudah di maintain atau minim bug.
