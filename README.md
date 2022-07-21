# Git dan Github

## 0. Alat dan Bahan

1. Download dan Install Git di https://git-scm.com
2. Buat akun Github dan buat project baru

## 1. Membuat repositori git di folder project dan melakukan commit pertama

1.  Buat repository git di folder dengan command:
    ```
    git init
    ```
    Ketika berhasil akan muncul pesan seperti ini:
    ```
    Initialized empty Git repository in C:/xxx/xxx/hell-on-world/.git
    ```
2.  Ketika pertama kali menggunakan git. Sebelum melakukan commit, disarankan untuk mengeset username dan email global (sebaiknya sesuai dengan email github) untuk menandakan commit dengan dua perintah ini:

    ```
    git config --global user.email "namamu@domain-emailmu.com"
    git config --global user.name "Nama Kamu"
    ```

    _(hilangkan_ `--global` _jika hanya ingin mengset username dan email di repository git)_

    Contoh nama saya yang digunakan di repository ini:

    ```
    git config --global user.email "109481409+toneres@users.noreply.github.com"
    git config --global user.name "Anton Rahmansyah Sumadi"
    ```

3.  Tambah perubahan file yang akan dicommit:
    ```
    git add "nama_file.ext"
    ```
    Misal nama file ini `README.md` yang mau dicommit, maka commandnya akan menjadi
    ```
    git add "README.md"
    ```
4.  Untuk melihat daftar file yang siap dicommit, bisa menggunakan command:

    ```
    git status
    ```

    Output dari perintah ini kurang lebih akan menjadi seperti ini

    ```
    On branch master

    No commits yet

    Changes to be committed:
        (use "git rm --cached <file>..." to unstage)
            new file:   README.md
    ```

5.  Jika sudah yakin dengan perubahan, lakukan commit dengan pesan seperti berikut:
    ```
    git commit -m "Masukkan pesan commit anda"
    ```
    Contoh, jika pesan file commit adalah "Tambahkan README.md bagian 1", maka commandnya:
    ```
    git commit -m "Tambahkan README.md bagian 1"
    ```
    Output dari command tersebut adalah sebagai berikut
    ```
    [master (root-commit) 13d428f] Tambahkan README.md bagian 1
    1 file changed, 67 insertions(+)
    create mode 100644 README.md
    ```
6.  Anda bisa melihat informasi commit terakhir dengan menggunakan command:

    ```
    git log
    ```

    Output yang keluar adalah seperti berikut:

    ```
    commit 13d428fbcb098b2f39c4f241c27662241e4b5a39 (HEAD -> master)
    Author: Anton Rahmansyah Sumadi <109481409+toneres@users.noreply.github.com>
    Date:   Thu Jul 21 21:00:00 2022 +0700

        Tambahkan README.md bagian 1
    ```

    Setelah commit, maka sudah siap untuk diupload ke GitHub

7.  Jika terdapat kesalahan pada commit terakhir, maka bisa membatalkan commit terakhir tanpa merubah kondisi saat ini dengan command:

    ```
    git reset HEAD~1 --soft
    ```

    _Catatan: tidak bisa membatalkan commit pertama dengan cara ini_

## 2. Melakukan push perubahan pertama di Github

1.  Di folder yang ingin anda push perubahannya di project GitHub kosong anda, tambahkan lokasi remote origin dengan menggunakan perintah sebagai berikut:

    ```
    git remote add origin https://github.com/username-githubmu/nama-projectmu.git
    ```

    Contoh, saya dengan username "toneres" ingin mengatur lokasi remote origin ke project kosong github "hell-on-world", maka commandnya akan menjadi:

    ```
    git remote add origin https://github.com/toneres/hell-on-world.git
    ```

2.  Lalu bisa diupload dengan menggunakan perintah di bawah ini:
    ```
    git push origin master
    ```
