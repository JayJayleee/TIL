<aside>
๐ก **Repository**
- ํน์  ๋๋ ํ ๋ฆฌ๋ฅผ ๋ฒ์  ๊ด๋ฆฌํ๋ ์ ์ฅ์๋ก init ๋ช๋ น์ด๋ก ๋ก์ปฌ ์ ์ฅ์๋ฅผ ์์ฑํจ.

</aside>

- git init โ initialized์ ์ค์๋ง. git์ด ์์ ๋ค์ด๊ฐ๋ฉด  git ๋ช๋ น์ด์
.git ๋๋ ํ ๋ฆฌ์ ๋ฒ์ ๊ด๋ฆฌ์ ํ์ํ ๋ชจ๋  ๊ฒ์ด ๋ค์ด๊ฐ ์์!
(์จ๊น ํ์ผ)
- ํน์  ๋ฒ์ ์ผ๋ก ํ์ผ์ ๋จ๊ธฐ๋ ๊ฒ โ Commit ์ด๋ผ๊ณ  ์ผ์ปฌ์
**3๊ฐ์ง ์์ญ์ ๋ฐํ์ผ๋ก ๋์!**

![working directory : ์์ ์์ญ
staging area : 1์ฐจ๋ก ์๋ฃ ์ฌ๋ฆผ
repository : commit ์๋ฃ](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7d2793c8-228c-4eb5-9ff4-6fe71060f2c6/2023-01-12-13-25-48-521.jpg)

working directory : ์์ ์์ญ
staging area : 1์ฐจ๋ก ์๋ฃ ์ฌ๋ฆผ
repository : commit ์๋ฃ

- ํ์ GIT๋ช๋ น์ด

git add : working directory โ staging 

git commit : stagingโ repository

git status : ํ์ฌ ์ํ ํ์ธ

```jsx
SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/Python_pr
$ cd ..

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop
$ mkdir git_test  **# ๊ฒฝ๋ก ์์ฑ**
SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop
$ ls
 1ํ๊ธฐ/  '2๋ฐ ์ ์ง์.md'   desktop.ini  'Eclipse IDE for Java Developers - 2022-09.lnk'*   git_test/   python_pr/   SPIKE-PRIME_Win10_2.0.9_Global.msi   Webex.lnk*                git_test/   python_pr/   SPIKE-PRIME_Win10_2.0.9_Global.msi   Webex.lnk*

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop
$ cd git_test **๊ฒฝ๋ก ๋ณ๊ฒฝ**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test
$ git init **# git initialize**
Initialized empty Git repository in C:/Users/SSAFY/Desktop/git_test/.git/

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ ls -a **# ๋๋ ํ ๋ฆฌ ๋ด ์ ์ฒด ํ์ผ ๋ณด๊ธฐ**
./  ../  .git/

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ touch README.md **#README ํ์ผ ์์ฑ**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status  
# ์ํ ๋ณด๊ธฐ : ํ์ฌ์ ๊ฒฝ์ฐ commit ํ  ํ์ผ์ ์์ฌ๋ผ์์ผ๋ ์ถ๊ฐ ๊ฐ๋ฅํ ํ์ผ์ด ์์์ ์๋ ค์ค
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git add README.md **#staging area๋ก ํ์ผ ์ฌ๋ฆผ**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status **#์ํ ๋ณด๋, ์ปค๋ฐ ๊ฐ๋ฅํ ํ์ผ ์๋ ค์ค**
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git commit -m "Add README.md"
Author identity unknown  **#git ์ ์ฅํ ์ฌ๋์ ์ด๋ฆ๊ณผ ์ด๋ฉ์ผ ์์ฑ**

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'SSAFY@DESKTOP-DOGVPUB.(none)')

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git config --global user.email "acd0825@naver.com"

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git config --global user.name "Jay"

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git commit -m "Add README.md"  **#git ์ปค๋ฐํ๊ณ  ์ค๋ช๊ธ ์์ฑ**
[main (root-commit) 3ae580b] Add README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status
On branch main
nothing to commit, working tree clean
```

git์ ์ฌ๋ฆฌ๊ธฐ

```jsx
SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git remote add origin https://github.com/JayJayleee/git_test.git
**-> ์๊ฒฉ์ผ๋ก ๋์ ์ฃผ์์ git์ ์๋ฐ์ดํธ** 

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git remote -v
origin  https://github.com/JayJayleee/git_test.git (fetch)
origin  https://github.com/JayJayleee/git_test.git (push)
**-> ํ์ฌ git ์ ์ ์ฅ๋ ์ ์ฅ์๋ฅผ ๋ํ๋**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git push -u origin main
info: please complete authentication in your browser...
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 213 bytes | 213.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/JayJayleee/git_test.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
**-> git์ ์๋ก๋ ํจ**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git add README.md
**-> ์คํ์ด์ง์ git ์ถ๊ฐ**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
**$ git restore --staged  README.md  #์คํ์ด์ง ๋ ๊ฒ์ ๋ค์ ์ํน ๋๋ ํ ๋ฆฌ๋ก ๋ด๋ฆผ**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git diff README.md
diff --git a/README.md b/README.md
index e69de29..a098547 100644
--- a/README.md
+++ b/README.md
@@ -0,0 +1,2 @@
+### ๋ฐฐ๋๋ฏผํด ๋์๋ฆฌ ๋ง๋ค์ด์ ์ด๋ํด์ผ์ง....
+## ์ง์ ๊ฐ๊ณ  ์ถ๋ค......
\ No newline at end of file

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
**$ git add README.md**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git push origin main
Everything up-to-date

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
**$ git commit -m "Edit README.md"  # ๋ก์ปฌ ์ ์ฅ์์ ๊ธฐ๋ก ๋จ๊น**
[main 2bedd6d] Edit README.md
 1 file changed, 2 insertions(+)

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
**$ git push origin main   # ํ๋ธ์ ์๋ก๋**
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 328 bytes | 109.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/JayJayleee/git_test.git
   3ae580b..2bedd6d  main -> main

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop/git_test (main)
**$ git log**
commit 2bedd6d6a9763588a4b4e60e7413b5ffa630918d (HEAD -> main, origin/main)
Author: Jay <acd0825@naver.com>
Date:   Thu Jan 12 14:29:37 2023 +0900

    Edit README.md

commit 3ae580b1697dd1340a26dc118af385f4f9b62392
Author: Jay <acd0825@naver.com>
Date:   Thu Jan 12 13:41:14 2023 +0900

    Add README.md
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/399c58b5-61b3-465e-8223-a2cd03646ecb/Untitled.png)

**์๋ก๋ ๊ณผ์ **

```java
SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop
**$ rm -rf git_test  #ํ์ผ ์ ๊ฑฐํจ**

SSAFY@DESKTOP-DOGVPUB MINGW64 ~/Desktop
**$ git clone https://github.com/JayJayleee/git_test.gitใ
-> GIT ๋ค์ ๋ณต์ ** 
Cloning into 'git_test'...
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 9 (delta 0), reused 9 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), done.

```

- ์ด๋ ฅ์ด ํ์ ์์ ๊ฒฝ์ฐ์๋ ํด๋ก  ๋์  ๋ค์ด๋ก๋ํ์ฌ ์ต์  ํ์ผ๋ง ๊ฐ์ ธ์ด!