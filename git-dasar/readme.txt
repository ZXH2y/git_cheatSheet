# create

    git init                <= menginisialisasi repository
    git clone               <= mendownload/cloning repository dari github

# membuat perubahan

git add nama_file                                           <= memasukkan file ke history, supaya perubahan yg dilakukan dicatat oleh history git
git add .                                                   <= sama aja cuma, langsung sekaligus
git reset nama_file                                                  <= membatalkan track perubahan dalam history ketika lu ga jadi mau commit sebuah file
git reset --hard                                            <= sama aja intinya file yg seblumnya di track jadi nggak ke track lagi
git commit -m "pesan"                                       <= tujuannya memastikan perubahan yang kita lakukan tercatat dalam history & ada penjelasan singktnya juga
git diff                                                    <= melihat perubahan dalam file
git show HEAD                                               <= melihat perubahan dalam file di commit terakhir

# Sync melakukan sinkronisasi antara lokal dengan server , kamu bisa memanfaatkan server github

    buat repository di github dulu
    git remote add origin http://Link_repo_baru_github_kamu             <= mengintegrasikan dengan server
    git remote -v                                                       <= mengecek apakah benar sudah ter integrasi ke server atau belum
    git push origin master                                                           <= upload dari lokal ke server/github kamu
    git pull origin master                                                           <= menarik perubahan dari server ke lokal
    git fetch                            <=> mengambil data dari online/server tanpa mengubah data yang ada di kodingan kita,manfaatnya  seperti mengecek upadate tanpa mengubah data yang ada di local kita


## Branch biasanya dipake kalau lu mau upgrade kode tanpa mengganngu kodingan yng udah jalan
    branch ini adalah cabang, manfaaatnya supaya kita bisa membuat cabang baru dari projek kita, tanpa mempengaruhi kode yang lain.
    contoh penggunaan : misalkan lu upgrade kode/tambah fitur baru tanpa ngeganggu kode yang udah jalan


    git branch                               <= mengecek berada di branch dimana sekarang / membuat branch baru
    git branch tangakai-fitur              <= membuat branch baru lewat terminal
    git fetch                                <=> berfungsi untuk mengambil (mengunduh) perubahan terbaru dari repository remote tanpa langsung menggabungkannya ke branch lokal.
    git checkout nama_branch                 <=> tentang lu mau pindah ke branch yang mana ?
    git branch -D Landing_page               <=> ini menghapus branch 
    git merge                                => Menyatukan Branch 

## tagging 
untuk menandari veris dari repo projekan kita

    git tag -a "nama_tag"                               => Menandai Versi 
    git tag                                             => mengecek tag
    example :
    git push origin master --tags                       => push tag kita ke repository
    git tag -a "v1.0"                                   => versi 1.0
    git tag - d "v1.0"                                  => menghapus tag
    


## Menyelesaikan konflik git
ini terjadi kalau lu mau push kodingan baru ke repository dan teman teman lu juga lagi ngebuat fitur di repositorynya jadi

git pull 
git diff => lihat perubahan
git add . => tracking perubahan
git commit -m "fixing konflik"
git push origin master 
