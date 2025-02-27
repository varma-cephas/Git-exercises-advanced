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
