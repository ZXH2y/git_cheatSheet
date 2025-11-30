## CONFIGURASI AWAL:
1. git config --global user.name "nama kamu"
2. git config --global user.email kamu@email.com

## melihat history commit
- git log                => melihat log commit 
- git log --oneline      => melihat 1 baris log commit saja

## Membatalkan perubahan saat belum di add(masih di working directory)
- git restore nama_file
- git restore .             => mengembalikan semua file ke semula.

## Membatalkan perubahan setelah di git add (di dalam staging area)
- git reset .               => mengembalikan semua file

## kasus menghilangkan fitur baru( KEMBALI KE VERSI/COMMIT SEBELUMNYA )
1. git log
    ambil nomor_hasnya
2. git reset --hard nomor_hash
contoh:
git reset --hard dcd7b650d2c5074c2e679f7bc497bc24233cf7d7


## Branch dan Merge:
1. git checkout -b nama-branch       => membuat branch dan langsung masuk ke branch tersebut.
2. git status
3. git add . 
4. git commit -m "pesan fitur branch mu"
5. git checkout master
6. git merge nama_branch

## Merefisi Commit yang sudah terjadi:
## kita bisa pakai :
### 1.checkout
### 2. git reset    -> ini akan menjadikan commit yng di pilih menjadi commit paling terakhir, jadi commit setelahnya akan di hapus, tidak direkomendasikan apabila commit selanjutnya masih di butuhkan.
### 3. git revert, karena kita bisa kembali ke commit sebelumnya tanpa menghapus commit setelahnya.
1. git log --oneline
2. git revert hash_commitnya
3. perbaiki konflik file,codenya kalau ada