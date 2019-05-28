# GIT
<b>git init</b>
Initilize git repository

<b>git status</b>
Untuk lihat status dari file yang terdapat di repository (file baru, file yang blm di commit, buang perubahan)

<b>git add {filename} / .</b>
Untuk menambahkan file baru ke dalam repository (status new -> uncommitted)

<b> git commit {filename} -m "{message}"</b>
Untuk menambah perubahan file baru ke dalam repository (status uncommited -> committed)

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
contoh : ada 2 branch master dan newfeature. di branch newfeature ada perubahan dan sudah di commit, maka kita pindah ke sini master kalo lakukan git merge newfeature untuk merging ke master

<b>git branch -D {branchname}</b>
Akan menghapus branch yang di input di branchname. Note penghapusan branch tidak bisa dilakukan apabila kita sedang berada di branch tersebut

<b>Kondisi Conflict</b>
Bila terjadi konflik pada saat push, maka kita harus fixing secara manual, yang kemudian lakukan seperti biasa yaitu git add dan git commit
