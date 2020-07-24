---
title: Cara Mencari Peraturan Turunan Undang-Undang di SJDIH Kemenkeu
date: 2015-03-23 00:00:00 +07:00
tags:
- tips
layout: post
---

Bismillah.

Tulisan berikut ini membahas cara mencari peraturan turunan Undang-Undang dengan memanfaatkan situs SJDIH Kemenkeu (Situs Jaringan Informasi dan Hukum) yang beralamat di www.sjdih.depkeu.go.id. Ada tiga alasan kenapa saya menggunakan situs tersebut: 1) karena saya bekerja di Kemenkeu, akses ke sjdih jauh lebih cepat daripada mengakses internet, 2) struktur SJDIH Kemenkeu sudah cukup baik dan runut dalam menata produk hukum mulai dari Undang-Undang sampai PMK dan KMK, 3) karena saya tidak punya software berbayar untuk mencari produk hukum Indonesia.

# Fitur Bawaan SJDIH
SJDIH sudah menyediakan fitur status aturan hukum, yakni apakah masih berlaku atau tidak. Jika suatu peraturan sudah dicabut, maka muncul info peraturan tersebut telah dicabut oleh peraturan yang mana, bahkan lengkap dengan link ke peraturan yang mencabut tsb. Jika kita ikuti link cabut-mencabut ini, maka kita akan sampai pada peraturan terbaru yang masih berlaku. Sebaliknya, jika kita ikuti ke atas, maka akan sampai pada peraturan pertama/tertua di topik tersebut.

![cek status aturan dengan sjdih](https://raw.githubusercontent.com/BetaUliansyah/BetaUliansyah.github.io/master/img/status-aturan.png)

# Cara Mencari Peraturan Turunan Undang-Undang

Nah sekarang yang ingin saya lakukan adalah mencari peraturan turunan suatu UU. Fitur ini tidak disediakan oleh SJDIH Kemenkeu, sehingga saya harus memutar otak untuk mendapatkan informasi tersebut.

Ada beberapa hal yang saya manfaatkan untuk mempermudah pencarian saya:

Konsideran Undang-Undang selalu muncul di setiap aturan, baik Perpu, PP, Perpres, Keppres, Inpres, PMK maupun KMK.
Judul Peraturan selalu ditampilkan oleh SJDIH di title tag. Misal: <title>Peraturan Pemerintah bla bla bla Nomor sekian Tahun sekian</title>
Berkas peraturan disimpan oleh SJDIH dalam folder sesuai tahun diundangkannya. Seperti ini: http://www.sjdih.depkeu.go.id/fulltext/2005/
Dari ketiga premis tersebut maka saya mencari seluruh PP turunan dari UU 33 tahun 2004, maka saya membuat query searching di Google sbb:

> inurl:www.sjdih.depkeu.go.id/fullText/2010 intitle:”Peraturan Pemerintah” “Undang-Undang Nomor 33 Tahun 2004”

Kalau dijelaskan, maka kurang lebih sbb:

1. Bagian **inurl:www.sjdih.depkeu.go.id/fullText/2010** ini memerintahkan Google untuk mencari di folder 2010 saja. Jika tidak ingin spesifik tahun, maka buang saja tahunnya sehingga menjadi **inurl:www.sjdih.depkeu.go.id/fullText/**
2. Bagian **intitle:”Peraturan Pemerintah”** ini memerintahkan Google untuk menampilkan halaman dengan title tag Peraturan Pemerintah saja, bukan yang lain.
3. Bagian **"Undang-Undang Nomor 33 Tahun 2004"** ini diharapkan untuk memeriksa apakah PP yang dicari memiliki konsideran UU tsb.

![cara mencari peraturan dari google](https://raw.githubusercontent.com/BetaUliansyah/BetaUliansyah.github.io/master/img/google-search-query.png)
