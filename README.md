# Git2
```
<!-- First Challenge -->

  <!-- creating four files -->
$ touch test{1..4}.md
 
 <!-- adding and commiting them -->
User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$ git add test1.md && git commit -m "chore: Create initial file"
[main a903256] chore: Create initial file       
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md

User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$ git add test2.md && git commit -m "chore: Create another file"
[main 41387e6] chore: Create another file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md

User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$ git add test3.md && git commit -m "chore: Create third and fourth files"
[main 7de0e34] chore: Create third and fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md


<!-- checking un added file -->
User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$ git status 
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$ git log
commit 7de0e3460134e03d1296e32c65f699c594c41943 (HEAD -> main)
Author: anifa <anifabazubagira@gmail.com>
Date:   Fri Jul 25 11:04:42 2025 +0200

    chore: Create third and fourth files

commit 41387e67db86a4749a9257cc48ebe201e1cb05fe
Author: anifa <anifabazubagira@gmail.com>
Date:   Fri Jul 25 11:04:39 2025 +0200

    chore: Create another file

commit a90325625a158538661d2cc0f7ce3f049708cb66
Author: anifa <anifabazubagira@gmail.com>
Date:   Fri Jul 25 11:04:37 2025 +0200

    chore: Create initial file

commit b3c45a42e209e8ad219d05057c4b09e3f9463ec5 (origin/main, origin/HEAD)
Author: Anifa <anifabazubagira@gmail.com>
Date:   Fri Jul 25 10:58:19 2025 +0200

    Initial commit


<!-- git reflog shows earlier commit -->
User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$ git reflog
7de0e34 (HEAD -> main) HEAD@{0}: commit: chore: Create third and fourth files
41387e6 HEAD@{1}: commit: chore: Create another file
a903256 HEAD@{2}: commit: chore: Create initial file
b3c45a4 (origin/main, origin/HEAD) HEAD@{3}: clone: from https://github.com/Anifa-hub/Git2.git


<!-- this delete the commit but the files still added -->
User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$  git reset -- soft HEAD@{3}

<!-- checking if it worked -->
User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test3.md
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$ git add test3.md 

User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$ git commit -m "created third file"
[main f32ca8c] created third file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md

User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$ git add test4.md

User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$ git commit -m "created fourth file"
[main ac8d952] created fourth file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md

User@Anifa-hub MINGW64 /e/Code/Git2 (main)
$
```

```
<!-- Seconf challenge -->
<<<<<<< HEAD
<!-- Using this rebase in head you put what you commit before what you want to edit
and you delet pick the word infront of what you are editing replace it with reword and save by write wq
 -->
git rebase -i  HEAD@{2} 
=======

>>>>>>> 84321585e5c16ed9c81d411ed33c9e7d03017ba0

```