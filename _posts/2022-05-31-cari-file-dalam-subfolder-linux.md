---
layout: post
title: "Cari file dalam direktori bersarang Linux"
author: aksal
categories: [ Linux ]
tags: [ bash ]
image: assets/images/2022-05-31-cari-file-dalam-subfolder-linux.jpg
description: "Menemukan file berekstensi tertentu kadang tidak mudah di File Manager Linux"
featured: false
comments: false
---

> Menemukan file berekstensi tertentu kadang tidak mudah di File Manager Linux

### Story
Ceritanya saya saat ini menggunakan salah satu distro Linux dari garis keluarga Arch, yaitu [Archcraft](https://archcraft.io/). Dari packages bawaannya sendiri, distro dengan UI yang keren abis ini sendiri menggunakan Thunar, salah satu file manager yang pertama kali saya temui di distro Linux dengan DE XFCE.

Si Thunar ini, sependek ilmu saya, belum saya jumpai fitur filter yang cukup kondang kalau di File Explorer-nya Windows. Jadi, saya ingin memindahkan sekumpulan gambar dalam beberapa direktori yang letaknya juga di dalam sub-direktori juga.

Cukup merepotkan tentu saja kalau harus pakai cara konservatif, bukan?

### What I've Done?
Singkatnya, menurut [utas](https://superuser.com/questions/658075/how-do-i-move-files-out-of-nested-subdirectories-into-another-folder-in-ubuntu) di situs https://superuser.com ini, saya menemukan caranya yang ternyata cukup memusingkan, namun sederhana.

```
find -type f -iname "*.ekstensi_file_yang_kamu_cari" -exec mv --backup=numbered -t /direktori/tujuan {} +
```
