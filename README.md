# GIT
<b>git init</b>
Initilize git repository

<b>git status</b>
Untuk lihat status dari file yang terdapat di repository (file baru, file yang blm di commit, buang perubahan)

<b>git add {filename} / .</b>
Untuk menambahkan file baru ke dalam repository (status new -> uncommitted)

<b> git commit {filename} -m "{message}"</b>
Untuk menambah perubahan file baru ke dalam repository (status uncommited -> committed)

<b> git commit --amend -m "{message}"</b>
Untuk mengubah commit message yang salah tulis

<b>git branch</b>
Menampilkan seluruh branch yang ada pada repository dan branch yang lagi kita gunakan, otomatis untuk pertama kali branch yang kita gunakan adalah 'master'

Apabila file yang sudah ter-commit berubah maka kita harus jalankan git add dan git commit lagi

<b>git log</b>
Melihat perubahan atau tahapan tahapan commit, dimana masing masing commit memiliki id perubahan
(HEAD -> master) perubahan terakhir kita (pointer)

<b>git checkout {commitID}</b>
Mengarahakan file ke pada perubahan terakhir dari commitID

<b>git reset --hard {commitID}</b>
Mengarahakan file ke pada perubahan terakhir dari commitID, WARNING !! dan menghapus commit di atasnya

<b>git checkout -- {filename}</b>
Akan meng-revert perubahan yang terjadi pada file tersebut (undo)

<b>git checkout -b {branchname}</b>
Akan membuat branch baru dengan nama sesuai branchname yang di isi, pada saat pembuatan branch baru, history dari original branch akan terbawa

<b>git checkout {branchname}</b>
Pointer git akan pindah ke branch yang di input (lihat git branch)

<b>git merge {branchname}</b>
Melakukan merging perubahan coding, kondisinya kita harus berada di sisi yang menarik
contoh : ada 2 branch master dan newfeature. di branch newfeature ada perubahan dan sudah di commit, maka kita pindah ke sini master kalo lakukan git merge newfeature untuk merging ke master. Note, dengan cara ini semua commit yang ada di newfeature akan ke bawa ke master SEMUANYA.

<b>git merge --squash {branchname}</b>
Sama halnya dengan di atas, perbedaanya adalah semua perubahan dari branch commitnya tidak di bawah ke master, jadi perubahan tersebut di jadikan 1 paket. Kasarnya, saya tidak mau tau perubahan kamu apa apa saja pokoknya kirim semua jadi 1 perubahan total. Hal ini dapat di lihat dari git log yang tidak memunculkan perubhan dari newfeature

<b>git branch -D {branchname}</b>
Akan menghapus branch yang di input di branchname. Note penghapusan branch tidak bisa dilakukan apabila kita sedang berada di branch tersebut

<b>git remote add origin {remote repository}.git</b>
Membuat koneksi dari repository local ke repository remote

<b>git push -u origin master</b>
Push / sychron ke remote url dgn branch remote master

<b>git rebase {branchname} atau master</b>
Warning jgn pernah rebase dgn remote repository, hanya untuk local repository saja ya.</br>
git rebase itu misal dari m1, m2 terus kita bikin cabang feature jadi f1 (yg berasal dari m2) lalu kita ubah code jadi f2. </br>
Intinya kita mau perubahan kita compatable dgn perubahan terakhir dari m2.</br>

misal master telah berubah menjadi m3.</br>
in branch fiture>git rebase master = akan mengubah root yg sebelumnya m2 menjadi m3.</br>
sama halnya dengan master bisa juga untuk menarik perubahan.</br>
in branch master>git rebase fiture.</br>

<b>Kondisi Conflict</b>
Bila terjadi konflik pada saat push, maka kita harus fixing secara manual, yang kemudian lakukan seperti biasa yaitu git add dan git commit

<b>Kasus</b>
Mencoba menghubungi antara local dan remote, Mencoba untuk pull tetapi muncul 'unrelated histories'</b>
Paksa dgn git pull --allow-unrelated-histories origin master
