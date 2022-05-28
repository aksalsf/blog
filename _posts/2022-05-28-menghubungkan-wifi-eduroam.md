---
layout: post
title: "Cara Menghubungkan Koneksi Wi-Fi eduroam dengan nmcli"
author: aksal
categories: [ Linux ]
tags: [ nmcli ]
image: assets/images/2022-05-28-menghubungkan-wifi-eduroam.jpg
description: "Memang agak aneh caranya bikin koneksi kalau tipe jaringannya wpa-peap"
featured: true
comments: false
---

> Memang agak aneh caranya bikin koneksi kalau tipe jaringannya wpa-peap

### Langkah-langkah
- Buka terminal (apapun nama aplikasinya)
- Jalankan perintah berikut

```
nmcli con add type wifi ifname wlan0 con-name CONNECTION_NAME ssid SSID
nmcli con edit id CONNECTION_NAME
```

- Lanjutkan menyunting connection tersebut pada terminal nmcli

```
set ipv4.method auto
set 802-1x.eap peap
set 802-1x.phase2-auth mschapv2
set 802-1x.identity USERNAME
set 802-1x.password PASSWORD
set 802-1x.anonymous-identity ANONYMOUS-IDENTITY
set wifi-sec.key-mgmt wpa-eap
save
activate
```
