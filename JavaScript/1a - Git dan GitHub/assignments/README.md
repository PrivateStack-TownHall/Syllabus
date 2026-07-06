# Tujuan Pembelajaran
- Memahami konsep version control dan cara kerja Git
- Mampu menggunakan perintah dasar Git (init, add, commit, status, log)
- Memahami branching, merging, dan kolaborasi via GitHub
- Mampu menyelesaikan merge conflict sederhana

---

# Assignment 1 - Inisialisasi Repository (Easy)
Buat folder bernama `latihan-git`, lalu inisialisasi sebagai Git repository.

```bash
mkdir latihan-git
cd latihan-git
git init
```

**Hasil yang diharapkan:**
```
Initialized empty Git repository in .../latihan-git/.git/
```

---

# Assignment 2 - Staging dan Commit Pertama (Easy)
Buat file `index.html` kosong di dalam folder tersebut, lalu tambahkan ke staging area dan commit dengan pesan "initial commit".

```bash
touch index.html
git add index.html
git commit -m "initial commit"
```

**Hasil yang diharapkan:**
```
[main (root-commit) a1b2c3d] initial commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 index.html
```

---

# Assignment 3 - Cek Status dan Riwayat (Easy)
Ubah isi `index.html`, lalu cek status perubahan dan lihat riwayat commit.

```bash
git status
git log --oneline
```

**Hasil yang diharapkan:**
```
On branch main
Changes not staged for commit:
  modified:   index.html
```

---

# Assignment 4 - Clone Repository (Easy)
Clone salah satu repository publik dari GitHub ke komputer lokal.

```bash
git clone https://github.com/username/nama-repo.git
```

**Hasil yang diharapkan:**
```
Cloning into 'nama-repo'...
remote: Enumerating objects...
```

---

# Assignment 5 - Membuat .gitignore (Easy)
Buat file `.gitignore` agar folder `node_modules` tidak ikut ter-tracking oleh Git.

```bash
echo "node_modules/" > .gitignore
git add .gitignore
git commit -m "add gitignore"
```

**Hasil yang diharapkan:**
```
[main abc1234] add gitignore
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore
```

---

# Assignment 6 - Branching (Medium)
Buat branch baru bernama `feature-login`, berpindah ke branch tersebut, lakukan sebuah perubahan, lalu commit.

```bash
git checkout -b feature-login
# edit file
git add .
git commit -m "add login feature"
```

**Hasil yang diharapkan:**
```
Switched to a new branch 'feature-login'
[feature-login d4e5f6g] add login feature
```

---

# Assignment 7 - Merge Branch (Medium)
Gabungkan branch `feature-login` ke branch `main`.

```bash
git checkout main
git merge feature-login
```

**Hasil yang diharapkan:**
```
Updating a1b2c3d..d4e5f6g
Fast-forward
 index.html | 2 ++
 1 file changed, 2 insertions(+)
```

---

# Assignment 8 - Menyelesaikan Merge Conflict (Hard)
Simulasikan merge conflict dengan mengubah baris yang sama pada file yang sama di dua branch berbeda, lalu selesaikan conflict tersebut hingga berhasil di-commit.

```bash
git checkout main
git merge feature-login
# muncul conflict, edit file secara manual lalu:
git add index.html
git commit -m "resolve merge conflict"
```

**Hasil yang diharapkan:**
```
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
```
