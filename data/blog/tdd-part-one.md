---
title: Introduction to Test Driven Development Part 1
date: '2023-02-17'
tags: ['Unit Tests', 'swift']
draft: false
summary: 'In this article I want to share about the introduction to TDD and its fundamental'
---

# What is Test Driven Development?

Test Driven Development merupakan suatu cara iteratif untuk membangun sebuah software dengan pengembangan nya mulai dari fitur kecil yang ditopang oleh test di setiap unit nya.

Implementasi TDD akan sangat mudah apabila kita mengikuti step-step yang biasa dilakukan di dalam industri, yaitu dengan mengikuti TDD-Cycle atau siklus TDD. Siklus ini terdiri atas 4 tahapan, yaitu membuat failing test, passed test, refactor & repeat.

Tahapan ini akan membantu developer untuk membuat production code yang aman dan memenuhi kriteria yang diberikan, sehingga saat membuat test diharapkan kita juga mempertimbangan pembuatan failing test terlebih dahulu, agar dapat mengetahui edge cases yang dapat terjadi dan membuat bug dalam production code.

## Bagaimana membuat sebuah test yang baik?

Saat kita berbicara mengenai test, beberapa orang membicarakan mengenai prinsip dalam testing atau yang paling terkenal adalah F.I.R.S.T principles of testing. FIRST merupakan akronim dari Fast, Isolated, Repeatable, Self-validating & Thorough.

- **Fast**: Sebaiknya pada saat kita menulis sebuah test, developer harus bisa memastikan bahwa sebuah test dapat dijalankan dengan cepat.
- **Isolated/Independent**: Setiap pembuatan satu test harus spesifik untuk case atau action tertentu yang didukung dengan enviroment atau dependency yang terisolasi hanya untuk test tersebut. Hal ini bertujuan agar hasil dari sebuah test tidak dipengaruhi faktor lain.
- **Repeatable**: Setiap kali kita menjalankan sebuah test, diharapkan kita dapat menjalankan test tersebut berulang dengan menghasilkan hasil test yang sama. Hal ini bertujuan untuk meyakini bahwa di production code, action tersebut akan selalu menghasilkan output yang sesuai dengan ekspektasi developer
- **Self-validating**: Test yang dijalankan harus bisa menghasilkan yang menunjukan bahwa test berhasil atau gagal.
- **Thorough**: Test yang dibuat harus dapat mengcover semua case, happy/positive path, error & negative path.

Selain dari ke lima step diatas, ada beberapa hal yang perlu diperhatikan saat membuat sebuah test, yaitu adalah pastikan test yang dibuat adalah maintainable. Pada saat mendevelop sebuah fitur, apabila ada perubahan pada production code, pastikan dilakukan penyesuaian terhadap test terlebih dahulu untuk menghindari adanya perbedaan antara production code dan test code.

## Apa yang perlu kita test?

Tidak semua hal yang ditulis perlu dilakukan test, khususnya untuk code seperti framework atau API bawaan dari bahasa pemrograman (swift) dan third-party framework. Hal ini karena yang wajib melakukan test adalah pembuat dari framework tersebut. Kita tidak akan pernah tau edge cases seperti apa yang perlu di test dari framework tersebut dan akan menimbulkan asumsi yang membuat test tersebut menjadi tidak valid. Maka dari itu saat kita menulis sebuah test, hanya fokus saja pada code yang kita tulis.

## Mengimplementasikan TDD akan memakan waktu lebih lama dalam pengembangan project?

"Test-Driven Development adalah proses yang cukup memakan waktu saat development". Statement ini sering kali dirasakan apabila kita baru mencoba untuk mengimplementasikan TDD pada project kita. Nyatanya, pada saat kita mengembangkan sebuah program, pengembangan tidak hanya dilakukan saat kita pertama kali membuat production code, tetapi juga saat kita melakukan improvement, maintenance atau fixing bug.

Sehingga waktu untuk mengembangkan sebuah program akan memakan waktu dan biaya yang besar. Hal ini berbanding terbalik dengan tujuan utama dari TDD. Justru, saat kita mengimplementasikan TDD, seharusnya production code bisa dipastikan minim bug atau error dan juga mudah dilakukan improvement ataupun maintenance, karena sudah dilakukan saat kita membuat test untuk production code.

## Apakah setiap project perlu mengimplementasikan TDD?

Pertanyaan ini juga sering kali menjadi pembahasan saat memulai sebuah project. TDD dapat dilakukan saat memulai project ataupun meneruskan legacy code. Namun, semua bergantung pada kebutuhan team dan waktu yang dimiliki. Memang TDD akan lebih banyak memakan waktu saat initial development, karena kita perlu membuat test code dan production code saat development, tapi akan dapat mengurasi cost development di kemudian hari dengan memastikan code ini maintenance-able dan minim bug.

Bagi saya, implementasi TDD akan bisa diimplementasi apabila waktu pengerjaan panjang dan lifetime dari projectnya juga di proyeksikan panjang. Karena apabila lifetime project nya pendek, yang menjadi concern adalah apakah waktu development akan bisa mencapai tujuannya? Seperti hal nya saat kita mengembangkan prototype atau project untuk hackaton atau untuk kebutuhan pitching, yang menjadi tujuan nya adalah bagaimana product tersebut bisa ditunjukan dan digunakan bukan memastikan product nya mudah di maintain atau minim bug.
