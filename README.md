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
