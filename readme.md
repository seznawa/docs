# Luxinity wiki

Repository ini digunakan untuk kontribusi dalam pembuatan artikel pada wiki milik Luxinity.

## How to contribute ?

Anda dapat fork repository ini terlebih dahulu, kemudian submit pull request anda [melalui menu pull request](https://github.com/Luxinity-Roleplay/docs/pulls).

### Important!
Ada 3 branch yang berperan penting dalam website ini, yaitu:

- `docs`: branch ini mewakili seluruh isi dokumentasi dari wiki luxinity
- `blog`: branch ini mewakili seluruh isi blog dari wiki luxinity
- `static`: branch ini mewakili seluruh isi static file dari wiki luxinity (e.g. tempat menaruh foto dokumentasi wiki, dan lain lain..)

Jika anda menemukan typo/minor bug anda bisa submit issue melalui [menu issues](https://github.com/Luxinity-Roleplay/docs/issues).

Kepada semua contributors, terimakasih telah membantu mengembangkan wiki untuk para pemula.


## Contributor Tips & Tricks

Tips dan Trik kepada Contributor dalam menulis Dokumentasi Wiki Luxinity.

### Markdown Support

Semua file _harus_ ber-ekstensi `.md` dan sudah ber-format Markdown. Untuk info lebih lanjut mengenai Markdown, silahkan cek [guide ini](https://guides.github.com/features/mastering-markdown/).

### Melampirkan link yang sudah ada didalam wiki

Jangan menggunakan link yang absolut. lampirkanlah link nya secara relative.

- ❌

  ```md
  anda dapat lihat selengkapnya di [rules](https://luxinity-roleplay.github.io/docs/rules)
  ```

- ✔

  ```md
  anda dapat lihat selengkapnya di [rules](../rules)
  ```

`../` berarti "naik satu tingkat directory" jadi, jika anda mengedit file yang berada didalam folder `blog` dan anda ingin melampirkan link ke `rules`, anda dapat menggunakan `../` untuk naik satu tingkat ke folder root dan anda dapat langsung mengarahkan linknya ke folder `docs` dimana file `rules.md` berada (tanpa extensi `*.md`).

### Gambar

Gambar berada di branch `static`, didalam folder `img`. Jika anda ingin menyisipkan gambar kedalam sebuah halaman, gunakan `![]()` dan `/static/images/` sebagai base path.

Jika anda bingung, anda boleh membaca halaman lainnya yang mencantumkan foto.

### Metadata

Hal utama yang berada di _semua_ dokumentasi/blog disini harus ada metadata seperti berikut:

```mdx
---
title: My Documentation
description: This is a page about stuff and things and burgers, yay!
---
```

Setiap halaman harus ada judul dan deskripsi.

Untuk seluruh list yang bisa ditambahkan didalam `---`, silahkan cek [Dokumentasi Docusaurus](https://docusaurus.io/docs/markdown-features#markdown-headers).

### Headings

Jangan buat level 1 heading (`<h1>`) dengan `#` hal ini akan ditangani secara otomatis. Awalan heading _selalu_ `##`

- ❌

  ```md
  # My Title

  This is documentation for ...

  # Sub-Section
  ```

- ✔

  ```md
  This is documentation for ...

  ## Sub-Section
  ```

### Gunakan `Code` Snippets untuk Petunjuk teknis

Saat menulis paragraf yang berisi nama fungsi, angka, commands ingame, hingga apapun yang tidak ada di KBBI (Kamus Besar Bahasa Indonesia), gunakan \`kutip miring\` seperti itu. Ini dapat memudahkan untuk memisahkan kalimat yang bisa dibaca dengan kalimat/command yang digunakan didalam ingame.

- ❌

  > Command /avehicle hanya dapat digunakan admin level 6+

- ✔

  > Command `/avehicle` hanya dapat digunakan admin level 6+

Dalam contoh diatas, `/aveh` adalah nama command, bukan kata kata berbahasa Inggris/Indonesia, jadi gunakanlah `Code` Snippet agar memudahkan orang yang membacanya.

### Tabel

Jika ada tabel yang memiliki heading/judul, beri heading/judul diatasnya:

- ❌

  ```md
  |         |                                      |
  | ------- | ------------------------------------ |
  | Health  | Engine Status                        |
  | 650     | Undamaged                            |
  | 650-550 | White Smoke                          |
  | 550-390 | Grey Smoke                           |
  | 390-250 | Black Smoke                          |
  | < 250   | On fire (will explode seconds later) |
  ```

- ✔

  ```md
  | Health  | Engine Status                        |
  | ------- | ------------------------------------ |
  | 650     | Undamaged                            |
  | 650-550 | White Smoke                          |
  | 550-390 | Grey Smoke                           |
  | 390-250 | Black Smoke                          |
  | < 250   | On fire (will explode seconds later) |
  ```