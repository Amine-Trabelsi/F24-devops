Reset practice:

I created 3 commits as in the task.
Here is the log:
> git log

    commit 316ca8b31eeb8a7456c901c8b40ec90dd8531000 (HEAD -> git-reset-practice)
    Author: Amine <aminetr76@gmail.com>
    Date:   Tue Sep 10 11:56:32 2024 +0300

        Third commit

    commit 473f4225335b8443d647bcde6ba990e6813f56ef
    Author: Amine <aminetr76@gmail.com>
    Date:   Tue Sep 10 11:56:30 2024 +0300

        Second commit

    commit 77484373aaa7844ca33ba7d01bd9b55b7e020452
    Author: Amine <aminetr76@gmail.com>
    Date:   Tue Sep 10 11:56:30 2024 +0300

        First commit

The I ran reset commands

> git reset --soft HEAD~1
> git reset --hard HEAD~1

    HEAD is now at 7748437 First commit

The I tried git reflog (output is partial)
> git reflog

    7748437 (HEAD -> git-reset-practice) HEAD@{0}: reset: moving to HEAD~1
    473f422 HEAD@{1}: reset: moving to HEAD~1
    316ca8b HEAD@{2}: commit: Third commit
    473f422 HEAD@{3}: commit: Second commit
    7748437 (HEAD -> git-reset-practice) HEAD@{4}: commit: First commit
    2c468f9 (origin/master, origin/HEAD, master) HEAD@{5}: checkout: moving from master to git-reset-practice

After that I recovered the commits using reset command and the hash from the reflog command:
> git reset --hard 316ca8b

    HEAD is now at 316ca8b Third commit

