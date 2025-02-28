# Git-exercises-advanced

## Part 1

### Exercise 1

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git log
commit 167712062fb3544d9ac6269c7c73b170ea07c6f9 (HEAD -> main)
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200

    chore: Create third and fourth files

commit d01f5cf02dd63c672f669629352a6b56bfe6ade6
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200

    chore: Create another file

commit c317a40fdea2d296cea3eedae386d3c2004c0171
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200

    chore: Create initial file

commit 470d6fc1c658fb4d9702a9adc7fecd16b0a7cc25 (origin/main, origin/HEAD)
Author: Varma Cephas <varmac231@gmail.com>
Date:   Tue Feb 25 19:07:45 2025 +0200

    Initial commit
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	test4.md

nothing added to commit but untracked files present (use "git add" to track)
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git add test4.md && git commit -m "chore: Add forgotten fourth file to commit history"
[main 70694dd] chore: Add forgotten fourth file to commit history
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md
```

### Exercise 2

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git rebase -i HEAD~4    
[detached HEAD 526a705] chore: Create second file
 Date: Wed Feb 26 11:22:07 2025 +0200
 Committer: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git log
commit bc0a685ba4cc11850029db1109dc12914a33e657 (HEAD -> main)
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:31:25 2025 +0200

    chore: Add forgotten fourth file to commit history

commit 66a247b3ce7eb9baf3ace4af9632c6c66ee5dfeb
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200

    chore: Create third and fourth files

commit 526a7055ab1fd66ffd8c3446063a5a5e17accd60
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200

    chore: Create second file

commit c317a40fdea2d296cea3eedae386d3c2004c0171
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200

    chore: Create initial file

commit 470d6fc1c658fb4d9702a9adc7fecd16b0a7cc25 (origin/main, origin/HEAD)
Author: Varma Cephas <varmac231@gmail.com>
Date:   Tue Feb 25 19:07:45 2025 +0200

    Initial commit
```

### Exercise 3

```bash
pop-os% git rebase -i HEAD~4  
[detached HEAD 5986273] chore: Squashed "Create second file" commit into "Create initial file" commit for a cleaner history. chore: Create initial file
 Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
 Date: Wed Feb 26 11:22:07 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.
```

### Exercise 4

```bash
pop-os% git rebase -i HEAD~
Stopped at 3f1ef2b...  chore: Create fifth and sixth file
You can amend the commit now, with

  git commit --amend 

Once you are satisfied with your changes, run

  git rebase --continue
pop-os% git status
interactive rebase in progress; onto 1cadb57
Last command done (1 command done):
   edit 3f1ef2b chore: Create fifth and sixth file
No commands remaining.
You are currently editing a commit while rebasing branch 'main' on '1cadb57'.
  (use "git commit --amend" to amend the current commit)
  (use "git rebase --continue" once you are satisfied with your changes)

nothing to commit, working tree clean
pop-os% git reset HEAD~
pop-os% git status
interactive rebase in progress; onto 1cadb57
Last command done (1 command done):
   edit 3f1ef2b chore: Create fifth and sixth file
No commands remaining.
You are currently editing a commit while rebasing branch 'main' on '1cadb57'.
  (use "git commit --amend" to amend the current commit)
  (use "git rebase --continue" once you are satisfied with your changes)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	test5.md
	test6.md

nothing added to commit but untracked files present (use "git add" to track)
pop-os% git add test5.md; git commit -m "chore: Create fifth file"
[detached HEAD 7fb3233] chore: Create fifth file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md
pop-os% git add test6.md; git commit -m "chore: Create sixth file"
[detached HEAD cdeffa3] chore: Create sixth file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test6.md
pop-os% git rebase --continue
Successfully rebased and updated refs/heads/main.
```

### Exercise 5

```bash
pop-os% git rebase -i HEAD~3
[detached HEAD de78864] chore: Squashed Create fifth and sixth file chore: Create fifth file
 Date: Thu Feb 27 15:29:50 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md
 create mode 100644 test6.md
Successfully rebased and updated refs/heads/main.
```

### Exercise 6

```bash
pop-os% touch unwanted.txt
pop-os% git add unwanted.txt; git commit -m "chore: Unwanted commit"
[main a95b60a] chore: Unwanted commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 unwanted.txt
pop-os% git rebase -i HEAD~
error: nothing to do
pop-os% git rebase -i HEAD~
error: nothing to do
pop-os% git rebase -i HEAD~2
Successfully rebased and updated refs/heads/main.
pop-os% git log
commit 8b487ecb5d6b5a068f75621d0f7a5f8c76e42c12 (HEAD -> main, origin/main, origin/HEAD)
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:44:18 2025 +0200

    docs: Add solution for Part 1 exercise 5

commit 6dfab1be514ddefe5bfca6c129402ef537c79fee
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:33:10 2025 +0200

    chore: Add solution for Part 1 exercise 4
```

### Exercise 7

```bash
pop-os% git log
commit 9ce11c7098d89f5b9cad773b5a899b010e3e4cd3 (HEAD -> main, origin/main, origin/HEAD)
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 16:03:35 2025 +0200

    docs: Add solution for Part 1 exercise 6

commit 8b487ecb5d6b5a068f75621d0f7a5f8c76e42c12
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:44:18 2025 +0200

    docs: Add solution for Part 1 exercise 5

commit 6dfab1be514ddefe5bfca6c129402ef537c79fee
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:33:10 2025 +0200

    chore: Add solution for Part 1 exercise 4

commit de78864704877a42e80727c9a2fb1686c2a421b1
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:29:50 2025 +0200

    chore: Squashed Create fifth and sixth file
    chore: Create fifth file
    
    chore: Create sixth file

commit 1cadb571bb4133ef188e6b7d1cc8bd9a083de712
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 14:59:40 2025 +0200

    chore: Add exercise 3 completed solution to README

commit 094b580537aef68aa91235408bc1a75dda558078
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:31:25 2025 +0200

    chore: Add forgotten fourth file to commit history

commit 627e0c53c827b714a5c23bfd73db5d4805af851f
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200

    chore: Squashed "Create second file" commit into "Create initial file" commit for a cleaner history. -- patch contents already upstream

commit 6c787d26b93c5059da51ce6a6cc3c56cb4e1d42c
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200

    chore: Create initial file

commit 4dbf45d32c760ddd4c50e7dec5254ee48d31a10e
Author: Varma Cephas <varmac231@gmail.com>
Date:   Wed Feb 26 14:05:25 2025 +0200

    chore: Add exercise 2 solution

commit 7baad55310d2032b0aace622093ba0f8d595eba5
pop-os% 
pop-os% git rebase -i HEAD~4
Successfully rebased and updated refs/heads/main.
pop-os% git log
commit f3485dec9565f6962b6e0e88d4c4b97d276c6c38 (HEAD -> main)
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 16:03:35 2025 +0200

    docs: Add solution for Part 1 exercise 6

commit fb42e6ef4467f3779e41a61c1f9632065af4141d
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:29:50 2025 +0200

    chore: Squashed Create fifth and sixth file
    chore: Create fifth file
    
    chore: Create sixth file

commit ecbfbca56e0b5cfe23bb4fb0fbe86167b5c06050
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:44:18 2025 +0200

    docs: Add solution for Part 1 exercise 5

commit ed2a7fab48663f1849e429ed78de1975032f05e4
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:33:10 2025 +0200

    chore: Add solution for Part 1 exercise 4

commit 1cadb571bb4133ef188e6b7d1cc8bd9a083de712
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 14:59:40 2025 +0200

    chore: Add exercise 3 completed solution to README

commit 094b580537aef68aa91235408bc1a75dda558078
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:31:25 2025 +0200

    chore: Add forgotten fourth file to commit history

commit 627e0c53c827b714a5c23bfd73db5d4805af851f
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200

    chore: Squashed "Create second file" commit into "Create initial file" commit for a cleaner history. -- patch contents already upstream

commit 6c787d26b93c5059da51ce6a6cc3c56cb4e1d42c
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200

    chore: Create initial file

commit 4dbf45d32c760ddd4c50e7dec5254ee48d31a10e
Author: Varma Cephas <varmac231@gmail.com>
Date:   Wed Feb 26 14:05:25 2025 +0200

    chore: Add exercise 2 solution

commit 7baad55310d2032b0aace622093ba0f8d595eba5
Author: Varma Cephas <varmac231@gmail.com>
Date:   Wed Feb 26 11:48:03 2025 +0200

    chore: add log for exercise 1

commit 470d6fc1c658fb4d9702a9adc7fecd16b0a7cc25
Author: Varma Cephas <varmac231@gmail.com>
Date:   Tue Feb 25 19:07:45 2025 +0200

    Initial commit

```

### Exercise 8

```bash
pop-os% git checkout ft/branch 
Switched to branch 'ft/branch'
pop-os% git log
commit 44df4661da39e1c11f37afb2c0e444745283cc34 (HEAD -> ft/branch)
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 16:28:32 2025 +0200

    feat: Implemented test 5

commit 2e6adb319b8135aa5791a29d284eb738ef60e938 (origin/main, origin/HEAD, main)
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 16:19:19 2025 +0200

    docs: Add solution for Part 1 exercise 7

commit f3485dec9565f6962b6e0e88d4c4b97d276c6c38
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 16:03:35 2025 +0200

    docs: Add solution for Part 1 exercise 6

commit fb42e6ef4467f3779e41a61c1f9632065af4141d
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:29:50 2025 +0200

    chore: Squashed Create fifth and sixth file
    chore: Create fifth file
    
    chore: Create sixth file

commit ecbfbca56e0b5cfe23bb4fb0fbe86167b5c06050
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:44:18 2025 +0200

    docs: Add solution for Part 1 exercise 5

commit ed2a7fab48663f1849e429ed78de1975032f05e4
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:33:10 2025 +0200

    chore: Add solution for Part 1 exercise 4

commit 1cadb571bb4133ef188e6b7d1cc8bd9a083de712
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 14:59:40 2025 +0200

    chore: Add exercise 3 completed solution to README

commit 094b580537aef68aa91235408bc1a75dda558078
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:31:25 2025 +0200

    chore: Add forgotten fourth file to commit history

commit 627e0c53c827b714a5c23bfd73db5d4805af851f
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200
pop-os% git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
pop-os% git log
commit 2e6adb319b8135aa5791a29d284eb738ef60e938 (HEAD -> main, origin/main, origin/HEAD)
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 16:19:19 2025 +0200

    docs: Add solution for Part 1 exercise 7

commit f3485dec9565f6962b6e0e88d4c4b97d276c6c38
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 16:03:35 2025 +0200

    docs: Add solution for Part 1 exercise 6

commit fb42e6ef4467f3779e41a61c1f9632065af4141d
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:29:50 2025 +0200

    chore: Squashed Create fifth and sixth file
    chore: Create fifth file
    
    chore: Create sixth file

commit ecbfbca56e0b5cfe23bb4fb0fbe86167b5c06050
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:44:18 2025 +0200

    docs: Add solution for Part 1 exercise 5

commit ed2a7fab48663f1849e429ed78de1975032f05e4
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:33:10 2025 +0200

    chore: Add solution for Part 1 exercise 4

commit 1cadb571bb4133ef188e6b7d1cc8bd9a083de712
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 14:59:40 2025 +0200

    chore: Add exercise 3 completed solution to README

commit 094b580537aef68aa91235408bc1a75dda558078
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:31:25 2025 +0200

    chore: Add forgotten fourth file to commit history

commit 627e0c53c827b714a5c23bfd73db5d4805af851f
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200

    chore: Squashed "Create second file" commit into "Create initial file" commit for a cleaner history. -- patch contents already upstream

commit 6c787d26b93c5059da51ce6a6cc3c56cb4e1d42c
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200
pop-os% git cherry-pick 44df4661da39e1c11f37afb2c0e444745283cc34
[main af2c733] feat: Implemented test 5
 Date: Thu Feb 27 16:28:32 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test7.md
pop-os% git log
commit af2c7338606d275569efa29bbd52a227d2cb59cf (HEAD -> main)
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 16:28:32 2025 +0200

    feat: Implemented test 5

commit 2e6adb319b8135aa5791a29d284eb738ef60e938 (origin/main, origin/HEAD)
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 16:19:19 2025 +0200

    docs: Add solution for Part 1 exercise 7

commit f3485dec9565f6962b6e0e88d4c4b97d276c6c38
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 16:03:35 2025 +0200

    docs: Add solution for Part 1 exercise 6

commit fb42e6ef4467f3779e41a61c1f9632065af4141d
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:29:50 2025 +0200

    chore: Squashed Create fifth and sixth file
    chore: Create fifth file
    
    chore: Create sixth file

commit ecbfbca56e0b5cfe23bb4fb0fbe86167b5c06050
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:44:18 2025 +0200

    docs: Add solution for Part 1 exercise 5

commit ed2a7fab48663f1849e429ed78de1975032f05e4
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 15:33:10 2025 +0200

    chore: Add solution for Part 1 exercise 4

commit 1cadb571bb4133ef188e6b7d1cc8bd9a083de712
Author: Varma Cephas <varmac231@gmail.com>
Date:   Thu Feb 27 14:59:40 2025 +0200

    chore: Add exercise 3 completed solution to README

commit 094b580537aef68aa91235408bc1a75dda558078
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:31:25 2025 +0200

    chore: Add forgotten fourth file to commit history

commit 627e0c53c827b714a5c23bfd73db5d4805af851f
Author: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Date:   Wed Feb 26 11:22:07 2025 +0200
```

### Exercise 9

```bash
pop-os% git log --all --decorate --oneline --graph
* 8d4e590 (HEAD -> main, origin/main, origin/HEAD) docs: Add solution for Part 1 exercise 8
* af2c733 feat: Implemented test 5
| * 44df466 (ft/branch) feat: Implemented test 5
|/  
* 2e6adb3 docs: Add solution for Part 1 exercise 7
* f3485de docs: Add solution for Part 1 exercise 6
* fb42e6e chore: Squashed Create fifth and sixth file chore: Create fifth file
* ecbfbca docs: Add solution for Part 1 exercise 5
* ed2a7fa chore: Add solution for Part 1 exercise 4
* 1cadb57 chore: Add exercise 3 completed solution to README
* 094b580 chore: Add forgotten fourth file to commit history
* 627e0c5 chore: Squashed "Create second file" commit into "Create initial file" commit for a cleaner history. -- patch contents already upstream
* 6c787d2 chore: Create initial file
* 4dbf45d chore: Add exercise 2 solution
* 7baad55 chore: add log for exercise 1
* 470d6fc Initial commit
```

### Exercise 10

```bash
pop-os% git reflog
3445457 (HEAD -> main, origin/main, origin/HEAD) HEAD@{0}: commit: docs: Add solution for Part 1 exercise 9
8d4e590 HEAD@{1}: commit: docs: Add solution for Part 1 exercise 8
af2c733 HEAD@{2}: cherry-pick: feat: Implemented test 5
2e6adb3 HEAD@{3}: checkout: moving from ft/branch to main
44df466 (ft/branch) HEAD@{4}: checkout: moving from main to ft/branch
2e6adb3 HEAD@{5}: checkout: moving from ft/branch to main
44df466 (ft/branch) HEAD@{6}: commit: feat: Implemented test 5
2e6adb3 HEAD@{7}: checkout: moving from main to ft/branch
2e6adb3 HEAD@{8}: commit: docs: Add solution for Part 1 exercise 7
f3485de HEAD@{9}: rebase (finish): returning to refs/heads/main
f3485de HEAD@{10}: rebase (pick): docs: Add solution for Part 1 exercise 6
fb42e6e HEAD@{11}: rebase (pick): chore: Squashed Create fifth and sixth file
ecbfbca HEAD@{12}: rebase (pick): docs: Add solution for Part 1 exercise 5
ed2a7fa HEAD@{13}: rebase (pick): chore: Add solution for Part 1 exercise 4
1cadb57 HEAD@{14}: rebase (start): checkout HEAD~4
9ce11c7 HEAD@{15}: commit: docs: Add solution for Part 1 exercise 6
8b487ec HEAD@{16}: rebase (finish): returning to refs/heads/main
8b487ec HEAD@{17}: rebase (start): checkout HEAD~2
a95b60a HEAD@{18}: commit: chore: Unwanted commit
8b487ec HEAD@{19}: commit: docs: Add solution for Part 1 exercise 5
6dfab1b HEAD@{20}: rebase (finish): returning to refs/heads/main
6dfab1b HEAD@{21}: rebase (pick): chore: Add solution for Part 1 exercise 4
de78864 HEAD@{22}: rebase (squash): chore: Squashed Create fifth and sixth file
7fb3233 HEAD@{23}: rebase (start): checkout HEAD~3
4e8070b HEAD@{24}: rebase (finish): returning to refs/heads/main
4e8070b HEAD@{25}: rebase (start): checkout HEAD~6
4e8070b HEAD@{26}: commit: chore: Add solution for Part 1 exercise 4
cdeffa3 HEAD@{27}: rebase (continue) (finish): returning to refs/heads/main
cdeffa3 HEAD@{28}: commit: chore: Create sixth file
7fb3233 HEAD@{29}: commit: chore: Create fifth file
1cadb57 HEAD@{30}: reset: moving to HEAD~
3f1ef2b HEAD@{31}: rebase: fast-forward
1cadb57 HEAD@{32}: rebase (start): checkout HEAD~
3f1ef2b HEAD@{33}: rebase (finish): returning to refs/heads/main
3f1ef2b HEAD@{34}: rebase (start): checkout HEAD
3f1ef2b HEAD@{35}: commit: chore: Create fifth and sixth file
1cadb57 HEAD@{36}: rebase (finish): returning to refs/heads/main
1cadb57 HEAD@{37}: rebase (start): checkout HEAD~5
1cadb57 HEAD@{38}: rebase (finish): returning to refs/heads/main
1cadb57 HEAD@{39}: rebase (start): checkout HEAD~4
1cadb57 HEAD@{40}: rebase (finish): returning to refs/heads/main
1cadb57 HEAD@{41}: rebase (pick): chore: Add exercise 3 completed solution to README
094b580 HEAD@{42}: rebase (pick): chore: Add forgotten fourth file to commit history
627e0c5 HEAD@{43}: rebase (squash): chore: Squashed "Create second file" commit into "Create initial file" commit for a cleaner history. -- patch contents already upstream
8b8089f HEAD@{44}: rebase (start): checkout HEAD~4
7322f6b HEAD@{45}: pull origin main --rebase (finish): returning to refs/heads/main
7322f6b HEAD@{46}: pull origin main --rebase (pick): chore: Add exercise 3 completed solution to README
3e439b7 HEAD@{47}: pull origin main --rebase (start): checkout 3e439b764eecfba793a5eb3995d6317dbf49c82b
fa6ec23 HEAD@{48}: rebase (finish): returning to refs/heads/main
fa6ec23 HEAD@{49}: rebase (pick): chore: Add exercise 3 completed solution to README
e8f1048 HEAD@{50}: rebase (pick): chore: Add forgotten fourth file to commit history
03cdfe9 HEAD@{51}: rebase (squash): chore: Squashed "Create second file" commit into "Create initial file" commit for a cleaner history. -- patch contents already upstream
8b8089f HEAD@{52}: rebase (start): checkout HEAD~4
924d2ba HEAD@{53}: rebase (finish): returning to refs/heads/main
924d2ba HEAD@{54}: rebase (start): checkout HEAD~4
924d2ba HEAD@{55}: pull origin main --rebase (finish): returning to refs/heads/main
924d2ba HEAD@{56}: pull origin main --rebase (pick): chore: Add exercise 3 completed solution to README
3e439b7 HEAD@{57}: pull origin main --rebase (start): checkout 3e439b764eecfba793a5eb3995d6317dbf49c82b
a5663f3 HEAD@{58}: commit: chore: Add exercise 3 completed solution to README
69293ec HEAD@{59}: rebase (finish): returning to refs/heads/main
69293ec HEAD@{60}: rebase (pick): chore: Add forgotten fourth file to commit history
b1420ff HEAD@{61}: rebase (pick): chore: Create third and fourth files
d5e95ce HEAD@{62}: rebase (reword): chore: Squashed "Create second file" commit into "Create initial file" commit for a cleaner history.
5986273 HEAD@{63}: rebase: fast-forward
4dbf45d HEAD@{64}: rebase (start): checkout HEAD~4
c362399 HEAD@{65}: rebase (finish): returning to refs/heads/main
c362399 HEAD@{66}: rebase (pick): chore: Add forgotten fourth file to commit history
6227f1e HEAD@{67}: rebase (pick): chore: Create third and fourth files
5986273 HEAD@{68}: rebase (squash): chore: Squashed "Create second file" commit into "Create initial file" commit for a cleaner history.
6c787d2 HEAD@{69}: rebase (start): checkout HEAD~4
3e439b7 HEAD@{70}: rebase (abort): updating HEAD
4dbf45d HEAD@{71}: rebase (start): checkout HEAD~4
3e439b7 HEAD@{72}: pull origin main --rebase (finish): returning to refs/heads/main
3e439b7 HEAD@{73}: pull origin main --rebase (start): checkout 3e439b764eecfba793a5eb3995d6317dbf49c82b
9bc70ba HEAD@{74}: commit: chore: Create third and fourth files
fe51158 HEAD@{75}: commit: chore: Create another file
08916a6 HEAD@{76}: commit: chore: Create initial file
470d6fc HEAD@{77}: reset: moving to 470d6fc1c658fb4d9702a9adc7fecd16b0a7cc25
d28dc2a HEAD@{78}: reset: moving to HEAD
d28dc2a HEAD@{79}: commit: chore: Create another file
1440d1a HEAD@{80}: commit: chore: Create initial file
470d6fc HEAD@{81}: clone: from github.com:varma-cephas/Git-exercises-advanced.git

with the above information on commit messages, hashes, pointers and more. with all of those information we can git cherry-pick, git merge or git checkout to retrieve lost changes and reintegrage them into our main history.
```

## Part 2


### Exercise 1

```bash
pop-os% git checkout -b ft/new-feature
Switched to a new branch 'ft/new-feature'
```

### Exercise 2

```bash
pop-os% git checkout ft/new-feature 
Switched to branch 'ft/new-feature'
pop-os% nano feature.txt
pop-os% git add feature.txt; git commit -m "feat: Implemented core functionality for new feature" 
[ft/new-feature 0e62d47] feat: Implemented core functionality for new feature
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt
```

### Exercise 3

```bash
pop-os% git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.
pop-os% nano readme.txt
pop-os% git add readme.txt; git commit -m "Updated project readme"                
[main bc51b14] Updated project readme
 1 file changed, 1 insertion(+)
 create mode 100644 readme.txt
pop-os% git rebase -i HEAD~                                       
[detached HEAD 692a5bd] chore: Updated project readme
 Date: Thu Feb 27 22:07:05 2025 +0200
 1 file changed, 1 insertion(+)
 create mode 100644 readme.txt
Successfully rebased and updated refs/heads/main.
```

### Exercise 4

```bash
git push origin ft/new-feature 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 314 bytes | 314.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/new-feature' on GitHub by visiting:
remote:      https://github.com/varma-cephas/Git-exercises-advanced/pull/new/ft/new-feature
remote: 
To github.com:varma-cephas/Git-exercises-advanced.git
 * [new branch]      ft/new-feature -> ft/new-feature
```

### Exercise 5

```bash
pop-os% git branch -d ft/new-feature
Deleted branch ft/new-feature (was 0e62d47).
```

### Exercise 6

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git log --oneline --graph
* bac4f8b (HEAD -> main, origin/main, origin/HEAD) docs: Add solution for Part 2 exercise 5
*   14adf7f chore: Merge pull request #1 from varma-cephas/ft/new-feature
|\  
| * 0e62d47 (origin/ft/new-feature) feat: Implemented core functionality for new feature
* | 0891909 docs: Add solution for Part 2 exercise 4
* | 0384eb8 docs: Add solution for Part 2 exercise 3
* | 692a5bd chore: Updated project readme
* | 2062c51 docs: Add solution for Part 2 exercise 2
* | 00095e4 docs: Add solution for Part 2 exercise 1
|/  
* baf31b4 docs: Add solution for Part 1 exercise 10
* 3445457 docs: Add solution for Part 1 exercise 9
* 8d4e590 docs: Add solution for Part 1 exercise 8
* af2c733 feat: Implemented test 5
* 2e6adb3 docs: Add solution for Part 1 exercise 7
* f3485de docs: Add solution for Part 1 exercise 6
* fb42e6e chore: Squashed Create fifth and sixth file chore: Create fifth file
* ecbfbca docs: Add solution for Part 1 exercise 5
* ed2a7fa chore: Add solution for Part 1 exercise 4
* 1cadb57 chore: Add exercise 3 completed solution to README
* 094b580 chore: Add forgotten fourth file to commit history
* 627e0c5 chore: Squashed "Create second file" commit into "Create initial file" commit for a cleaner history. -- patch contents already upstream
* 6c787d2 chore: Create initial file
* 4dbf45d chore: Add exercise 2 solution
* 7baad55 chore: add log for exercise 1
* 470d6fc Initial commit
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git checkout -b  ft/new-branch-from-commit 0e62d47 
Switched to a new branch 'ft/new-branch-from-commit'
```

### Exercise 7

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git merge ft/new-branch-from-commit     
Already up to date.
```

### Exercise 8

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git rebase  ft/new-branch-from-commit
Successfully rebased and updated refs/heads/main.
```


### Exercise 9

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git branch -m ft/new-branch-from-commit ft/improved-branch-name
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git branch
  ft/improved-branch-name
* main
```

### Exercise 10
```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git log --oneline      
5771b78 (HEAD -> main, origin/main, origin/HEAD) docs: Add solution for Part 2 exercise 9
cbea6bb docs: Add solution for Part 2 exercise 8
158a648 docs: Add solution for Part 2 exercise 7
c3ce2bd docs: Add solution for Part 2 exercise 6
987a5a7 docs: Add solution for Part 2 exercise 5
4e793bd docs: Add solution for Part 2 exercise 4
c2f687e docs: Add solution for Part 2 exercise 3
621ad40 chore: Updated project readme
7c85a7e docs: Add solution for Part 2 exercise 2
fbaeba7 docs: Add solution for Part 2 exercise 1
0e62d47 (origin/ft/new-feature, ft/improved-branch-name) feat: Implemented core functionality for new feature
baf31b4 docs: Add solution for Part 1 exercise 10
3445457 docs: Add solution for Part 1 exercise 9
8d4e590 docs: Add solution for Part 1 exercise 8
af2c733 feat: Implemented test 5
2e6adb3 docs: Add solution for Part 1 exercise 7
f3485de docs: Add solution for Part 1 exercise 6
fb42e6e chore: Squashed Create fifth and sixth file chore: Create fifth file
ecbfbca docs: Add solution for Part 1 exercise 5
ed2a7fa chore: Add solution for Part 1 exercise 4
1cadb57 chore: Add exercise 3 completed solution to README
094b580 chore: Add forgotten fourth file to commit history
627e0c5 chore: Squashed "Create second file" commit into "Create initial file" commit for a cleaner history. -- patch contents already upstream
6c787d2 chore: Create initial file
4dbf45d chore: Add exercise 2 solution
7baad55 chore: add log for exercise 1
470d6fc Initial commit
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git checkout 621ad40
Note: switching to '621ad40'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 621ad40 chore: Updated project readme
```


## Part 3


### Exercise 1

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   test1.md

no changes added to commit (use "git add" and/or "git commit -a")
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git stash
Saved working directory and index state WIP on main: c2143d3 docs: Add solution for Part 2 exercise 10
```

### Exercise 2

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   test1.md

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (80f25dc0d4ce86ce0ec84e1cd471b84b9fd5648e)
```

### Exercise 3

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git branch
  ft/improved-branch-name
* main
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git checkout ft/improved-branch-name
Switched to branch 'ft/improved-branch-name'
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % ls
README.md	feature.txt	test1.md	test2.md	test3.md	test4.md	test5.md	test6.md	test7.md
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % nano feature.txt 
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git add feature.txt; git commit -m "chore: Add description to feature.txt file"
[ft/improved-branch-name 726dc88] chore: Add description to feature.txt file
 Committer: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name "Your Name"
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 1 insertion(+), 1 deletion(-)
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % nano feature.txt 
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git add feature.txt; git commit -m "chore: Add description to feature.txt file on main branch"
[main 9fbd80e] chore: Add description to feature.txt file on main branch
 Committer: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name "Your Name"
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 1 insertion(+), 1 deletion(-)
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git merge ft/improved-branch-name
Auto-merging feature.txt
CONFLICT (content): Merge conflict in feature.txt
Automatic merge failed; fix conflicts and then commit the result.
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
	both modified:   feature.txt

no changes added to commit (use "git add" and/or "git commit -a")
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % nano feature.txt 
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
	both modified:   feature.txt

no changes added to commit (use "git add" and/or "git commit -a")
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git commit          
U	feature.txt
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
	both modified:   feature.txt

no changes added to commit (use "git add" and/or "git commit -a")
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git add feature.txt 
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git commit 
[main 0b08396] Merge branch 'ft/improved-branch-name'
 Committer: Gym Ubutwari <gymubutwari@Ubutwaris-iMac-2.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name "Your Name"
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```

### Exercise 4

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git mergetool

This message is displayed because 'merge.tool' is not configured.
See 'git mergetool --tool-help' or 'git help config' for more details.
'git mergetool' will now attempt to use one of the following tools:
opendiff tortoisemerge emerge vimdiff nvimdiff
No files need merging
```

### Exercise 5

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git checkout 9fbd80e
Note: switching to '9fbd80e'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 9fbd80e chore: Add description to feature.txt file on main branch
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % 
```

### Exercise 6

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % nano .gitignore
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.gitignore

nothing added to commit but untracked files present (use "git add" to track)
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % cat .gitignore 
/tmp
```

### Exercise 7

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git tag v1.0
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git tag        
v1.0
```

### Exercise 8

```bash
gymubutwari@Ubutwaris-iMac-2 Git-exercises-advanced % git tag -d v1.0
Deleted tag 'v1.0' (was 1b7fbff)
``
