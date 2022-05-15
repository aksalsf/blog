---
layout: post
title: "Solusi Koneksi OpenVPN di Fedora 36"
author: aksal
categories: [ Linux ]
tags: [ Fedora, OpenVPN ]
image: -
description: "Cara mengatasi OpenSSL: error:0308010C:digital envelope routines::unsupported"
featured: true
---

> OpenSSL: error:0308010C:digital envelope routines::unsupported

### Latar Belakang
Jadi kemarin saya baru saja menginstal Fedora 36 setelah beberapa bulan menggunakan Pop!_OS. Tentu saja agenda ketika proses instalasi selesai yaitu _setup environment_ untuk bekerja.

Salah satunya, yaitu memasang VPN!

Namun, begitu saya mengimpor file VPN melalui panel *Network* di jendela *Settings* Fedora, ternyata proses koneksi gagal :(

Kemudian saya mencoba untuk melihat log galatnya melalui *Gnome Console* dengan menjalankan perintah `openvpn [nama_file].ovpn` dan saya pun mendapatkan pesan eror `OpenSSL: error:0308010C:digital envelope routines::unsupported`

### Solusi
Setelah berputar-putar tanpa arah, akhirnya saya menemukan solusinya pada [artikel](https://ask.fedoraproject.org/t/openssl-error-when-connecting-to-vpn-via-networkmanager-fedora-36/21123/8) di forum [Ask Fedora](https://ask.fedoraproject.org). Solusi yang saya temukan dan kemudian saya terapkan yaitu dengan menghapus karakter tagar untuk menonaktifkan komentar di file `/etc/ssl/openssl.cnf` pada bagian berikut:
```
[openssl_init]
   providers = provider_sect
   
   [provider_sect]
   default = default_sect
   legacy = legacy_sect
   
   [default_sect]
   activate = 1
   
   [legacy_sect]
   activate = 1
```
