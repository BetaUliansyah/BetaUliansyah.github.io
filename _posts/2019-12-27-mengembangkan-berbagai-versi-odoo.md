---
layout: post
title: "Menyiapkan Lingkungan Pengembangan Odoo berbagai versi dengan Docker"
date: 2019-12-27
tags: [odoo, techie]
---

Bagi para developer Odoo, mengembangkan berbagai versi bisa membuat pening kepala. Tiap versi major Odoo mensyaratkan dukungan pustaka dan lingkungan yang berbeda-beda. Untuk mengatasi hal itu, cara berikut ini dapat digunakan. Kita akan menggunakan docker untuk menjalankan dan mengembangkan modul/add-ons untuk berbagai versi Odoo.

Dalam tulisan ini, saya akan menggunakan 4 versi Odoo, yaitu:
1. Odoo CE versi 10.0 pada port 10000
2. Odoo CE versi 11.0 pada port 11000
3. Odoo CE versi 12.0 pada port 12000
4. Odoo CE versi 13.0 pada port 13000

## Langkah 1: git clone docker-compose
```
git clone https://github.com/minhng92/odoo-10-docker-compose.git
git clone https://github.com/minhng92/odoo-11-docker-compose.git
git clone https://github.com/minhng92/odoo-12-docker-compose.git
git clone https://github.com/minhng92/odoo-13-docker-compose.git
```


## Langkah 2: sesuaikan port sesuai rencana di atas
`vi odoo-10-docker-compose\docker-compose.yml`
ubah bagian ports menjadi seperti ini: 
`      - "10000:8069"`

`vi odoo-11-docker-compose\docker-compose.yml`
ubah bagian ports menjadi seperti ini: 
`      - "11000:8069"`

`vi odoo-12-docker-compose\docker-compose.yml`
ubah bagian ports menjadi seperti ini: 
`      - "12000:8069"`

`vi odoo-13-docker-compose\docker-compose.yml`
ubah bagian ports menjadi seperti ini: 
`      - "13000:8069"`


## Langkah 3: jalankan masing-masing docker-compose

```
cd odoo-10-docker-compose
docker-compose up -d
cd ..\odoo-11-docker-compose
docker-compose up -d
cd ..\odoo-12-docker-compose
docker-compose up -d
cd ..\odoo-13-docker-compose
docker-compose up -d
```

## Langkah 4: Akses dari browser

http://localhost:10000
http://localhost:11000
http://localhost:12000
http://localhost:13000


## Langkah 5: upload add-ons

Misal untuk Odoo versi 13
```
cd odoo-10-docker-compose\addons
cp Downloads\om_account_accountant-13.0.1.0.0.zip 
unzip om_account_accountant-13.0.1.0.0.zip
```

Nah, karena tiap docker-compose sudah menambahkan parameter `--dev` untuk development, maka setiap ada addons baru akan langsung terdeteksi.


## Langkah 6: mulai mengembangkan addons dengan Visual Studio Code

Semoga bermanfaat!
