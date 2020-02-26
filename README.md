# Dokumentasi Git
## Pembuatan repository dari awal
### 1. Membuat project/inisialisasi
Untuk membuat atau menginisialisasi sebuah project baru di komputer kita bisa menggunakan perintah `git init`.
### 2. Menambahkan file ke staging area
Staging area adalah kondisi dimana sebuah perubahan ditandai, namun belum disimpan ke dalam git. Untuk menambahkan file kedalam staging area kita dapat menggunakan perintah `git add [nama file]` atau untuk menambahkan keseluruhan, kita dapat menggunakan perintah `git .` 
### 3. Melakukkan Commit
Commit adalah sebuah kondisi dimana file baru/file revisi kita disimpan kedalam git. Perintah untuk melakukkan commit adalah `git commit -m [pesan perubahan]`
### 4. Melakukkan remote kedalam repository
Untuk melakukkan remote, pastikan kita mempunyai repository di github. untuk membuat repository di github, login ke akun github lalu pilih ikon + di pojok kanan atas, lalu pilih new repository, isi nama repository nya. Apabila ingin menambahkan readme.md, centang pada pilihan initialize this repository with a README
Selanjutnya untuk menambahkan remote ke dalam repository lokal, kita bisa menggunakan perintah `git remote add [nama remote] [alamat https remote]`. Contoh perintahnya `git remote add https://github.com/sandypracoyo/sandypracoyo.github.io.git`
### 5.Mengirimkan file kedalam repository
perintah untuk mengirimkan file kedalam repository yakni `git push [nama remote] [nama branch]` misalnya `git push origin master`, karena default nama remote dari github adalah origin dan branch nya adalah master.

## Bekerja dengan repository milik orang lain
### 1. Clone repository ke komputer lokal
kita dapat melakukan clone repository milik orang lain kedalam komputer lokal kita, dengan menggunakan perintah `git clone [alamat repository]` . contohnya disini menggunakan repository yang sudah ada, maka perintahnya `git clone https://github.com/sandypracoyo/sandypracoyo.github.io.git`
### 2. Membuat branch
Agar lebih aman ketika kita bekerja dengan source code kita, pastikan tidak mengubah isi dari branch master. kita dapat membuat branch kita sendiri menggunakan perintah `git brach [nama branch]` lalu pindah kedalam branch kita dengan perintah `git checkout [nama branch]` atau agar lebih cepat bisa menggunakan perintah `git checkout -b [nama branch]`.
### 3. Mengambil perubahan terbaru dari repository ke komputer lokal
Ada 2 perintah untuk mengambil perubahan dari repository remote, yang pertama adalah menggunakan perintah pull, yakni `git pull [nama remote] [nama branch]` yang kedua adalah menggunakan perintah fetch yakni `git fetch [nama remote] [nama branch]`, perbedaan kedua perintah ini yakni pull untuk menarik/mengambil perubahan dan melakukan merge terhadap repo lokal kita. sedangkan untuk fetch adalah kebalikannya.
### 4. Melakukkan perubahan di repository komputer lokal
untuk melakukkan perubahan di komputer lokal, ada baiknya kita membuat branch baru, agar branch master lokal kita tidak terjadi conflict apabila branch master di repository remote terjadi perubahan. setelah melakukan perubahan, pastikkan sudah melakukkan `git add [nama file]` atau dengan `git add .` untuk semua file. lalu lakukkan commit dengan perintah `git commit -m "[pesan perubahan]"`.
### 5. Mengirimkan perubahan ke repository remote
Pastikkan kita sudah mempunyai hak akses kedalam repository yang ingin kita kirim perubahannya. misalnya kita adalah pemilik repository nya, klik icon setting di repository, lalu pilih menu manage access lalu cari user yang ingin kita tambahkan hak aksesnya. sebagai kontributor, cek email lalu akan ada invitation. pastikkan juga, kita sudah menambahkan remote repository yang akan kita kirim perubahannya, dengan menggunakan perintah `git remote -v`. 

Apabila sudah sama, selanjutnya lakukkan rebase dengan perintah `git rebase [nama remote] [nama branch]` lalu lakukkan push dengan menggunakan perintah `git push [nama remote] [nama branch]`.

setelah kita melakukkan push, masuk kedalam repository remote, lalu akan ada menu compare & pull request,pilih menu tersebut lalu kita akan melakukkan pull request ke repository remote untuk membandingkan perubahan yang kita lakukkan apabila sudah yakin, lakukkan pull request dengan memilih create pull request. pemilik repository akan menerima pesan bahwa kita melakukkan pull request, selanjutnya pemilik akan me review hasil perubahan kita, ketika pemilik sudah menyetujui maka pemilik akan memilih menu merge pull request untuk menggabungkan branch yang kita push dengan branch di master repository.


`
