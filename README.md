# Lektur
Blog untuk berbagi cerita.  
> **Note**  
> Untuk saat ini belum ada jadwal terbit untuk artikel terbaru

### Instalasi Pengembangan Lokal
- Clone repositori ini

```
git clone git@github.com:aksalsf/blog.git
```
- Salin isi berkas `docker-compose.yml.local` ke dalam `docker-compose.local` dan `Gemfile.local` ke dalam `Gemfile`
- Hapus berkas Gemfile.lock

```
rm Gemfile.lock
```
- Jalankan container Jekyll dengan docker-compose

```
docker-compose up
```
- Have fun!

### Copyright
Blog ini dibuat dengan [Jekyll](https://jekyllrb.com/) dengan tema [Mediumish](https://github.com/wowthemesnet/mediumish-theme-jekyll). 

### Pranala
- [Panduan Instalasi Jekyll](https://jekyllrb.com/docs/installation)
- [Panduan Instalasi Mediumish](https://bootstrapstarter.com/template-mediumish-bootstrap-jekyll/)
