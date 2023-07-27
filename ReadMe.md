// This file will help me to work on git bundles

# Git Exercises

## Bundle1

### exercise1

```bash

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git init
Reinitialized existing Git repository in E:/Git exercise/.git/

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   ReadMe.md


EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git commit -m "project init "
[main (root-commit) 827c55f] project init
 1 file changed, 1 insertion(+)
 create mode 100644 ReadMe.md

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git remote add origin git@github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 259 bytes | 86.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0      
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 * [new branch]      main -> main

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git status
On branch main
nothing to commit, working tree clean

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git checkout -b dev
Switched to a new branch 'dev'

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/AdelineA/Gym-Bundle-Exercises-Solutions/pull/new/dev
remote:
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git 
 * [new branch]      dev -> dev

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git checkout -b test
Switched to a new branch 'test'

EDELINE@Mugunga MINGW64 /e/Git exercise (test)
$ git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/AdelineA/Gym-Bundle-Exercises-Solutions/pull/new/test
remote:
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 * [new branch]      test -> test

EDELINE@Mugunga MINGW64 /e/Git exercise (test)
$ git checkout dev
Switched to branch 'dev'

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git branch -D test
Deleted branch test (was 827c55f).

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git push origin --delete test
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 - [deleted]         test

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$
```
# Bundle 1
## Exercise 2

```bash
EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash list

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git status
On branch dev
nothing to commit, working tree clean

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash list
stash@{0}: WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git status
On branch dev
nothing to commit, working tree clean

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash list
stash@{0}: WIP on dev: 827c55f project init
stash@{1}: WIP on dev: 827c55f project init
stash@{2}: WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (755be2104d9d29aea21b7f988e10ca3aef0716a5)

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash list
stash@{0}: WIP on dev: 827c55f project init
stash@{1}: WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (588a3464b4d28e53805b3829a63b7aa59f08e1b8)

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git commit -m "adding home and about page"
[dev bbd9fe9] adding home and about page
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 557 bytes | 92.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
   827c55f..bbd9fe9  dev -> dev

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash list
stash@{0}: WIP on dev: 827c55f project init

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (488e3d7648c1f398e350c3ba920b067c6ca48f61)

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git reset --hard
HEAD is now at bbd9fe9 adding home and about page

EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$
```
# Bundle2
## Exercise1

```bash
EDELINE@Mugunga MINGW64 /e/Git exercise (dev)
$ git checkout -b ft/bundle-2 
Switched to a new branch 'ft/bundle-2'

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/bundle-2)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/bundle-2)
$ git status
On branch ft/bundle-2
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   services.html


EDELINE@Mugunga MINGW64 /e/Git exercise (ft/bundle-2)
$ git commit -m"adding services page"
[ft/bundle-2 0b1dee5] adding services page
 1 file changed, 11 insertions(+)
 create mode 100644 services.html

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/bundle-2)
$ git push origin ft/bundle-2 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 432 bytes | 216.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/AdelineA/Gym-Bundle-Exercises-Solutions/pull/new/ft/bundle-2
remote:
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/bundle-2)
$ 
```



# bundle 2
## exercise 2
```bash
EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git pull origin main
From github.com:AdelineA/Gym-Bundle-Exercises-Solutions
 * branch            main       -> FETCH_HEAD
Updating 827c55f..77148eb
Fast-forward
 about.html    | 11 +++++++++++
 home.html     | 11 +++++++++++
 services.html | 11 +++++++++++
 3 files changed, 33 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git checkout -b ft/service-redesign
fatal: A branch named 'ft/service-redesign' already exists.

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git branch -D ft/service-redesign
Deleted branch ft/service-redesign (was dd34a67).

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/service-redesign)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/service-redesign)
$ git commit -m "adding changes on service page"
[ft/service-redesign 28deec6] adding changes on service page
 1 file changed, 4 insertions(+)

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 349 bytes | 349.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/AdelineA/Gym-Bundle-Exercises-Solutions/pull/new/ft/service-redesign       
remote:
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/service-redesign)
$ git checkout main
Switched to branch 'main'

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git commit -m"adding list on service page"
[main 8eb37ac] adding list on service page
 1 file changed, 5 insertions(+), 1 deletion(-)

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git push origin main
ssh: Could not resolve hostname github.com: Name or service not known
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git status
On branch main
nothing to commit, working tree clean

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git push origin main
ssh: Could not resolve hostname github.com: Name or service not known
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git push origin main
ssh: Could not resolve hostname github.com: Name or service not known
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 365 bytes | 182.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
   77148eb..8eb37ac  main -> main

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/service-redesign|MERGING)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/service-redesign|MERGING)
$ git commit -m"merging changes"
[ft/service-redesign 665cab1] merging changes

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/service-redesign)
$ git push
```

# bundle3
## exercise1

```bash

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/team-page)    
$ git checkout main
Switched to branch 'main'

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/team-page)
$ git log
commit dc58334d6280b8d852cc325cbd0e845e0a214dbc (HEAD -> ft/team-page, origin/ft/team-page)
Author: Adeline <adelinemug6@gmail.com>
Date:   Sun Jul 16 01:24:50 2023 +0200

    adding team page

commit 665cab1bfeb8289eadc6d3d69ba997c4f18b9fc5 (ft/service-redesign)
Merge: 28deec6 8eb37ac
Author: Adeline <adelinemug6@gmail.com>
Date:   Sun Jul 16 01:09:34 2023 +0200

    merging changes

commit 8eb37aced41a0ccba77d966dda10d65e9f5029cf
Author: Adeline <adelinemug6@gmail.com>
Date:   Sun Jul 16 00:55:41 2023 +0200


EDELINE@Mugunga MINGW64 /e/Git exercise (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/contact-page)
$ git cherry-pick dc58334d6280b8d852cc325cbd0e845e0a214dbc
[ft/contact-page 831067f] adding team page
 Date: Sun Jul 16 01:24:50 2023 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/contact-page)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/contact-page)
$ git commit -m"adding contact page"
[ft/contact-page ea1c6c3] adding contact page
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 675 bytes | 168.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/AdelineA/Gym-Bundle-Exercises-Solutions/pull/new/ft/contact-page
remote:
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/faq-page)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/faq-page)
$ git commit -m"adding FAQ page"
[ft/faq-page c8728c9] adding FAQ page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 419 bytes | 419.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/AdelineA/Gym-Bundle-Exercises-Solutions/pull/new/ft/faq-page
remote:
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/faq-page)
$ git log
commit c8728c9c4e4ff2ef5e49bc651b6232b124bee8cd (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Adeline <adelinemug6@gmail.com>
Date:   Sun Jul 16 01:51:48 2023 +0200

Revert "adding team page"
    adding FAQ page

commit ea1c6c3fa925d9efc0461d20d1d6d2de5130d215 (origin/ft/contact-page, ft/contact-page)
Author: Adeline <adelinemug6@gmail.com>
Date:   Sun Jul 16 01:48:25 2023 +0200

    adding contact page

commit 831067f7b2792fc70a5e54df6ed9a2f62b73188a
Author: Adeline <adelinemug6@gmail.com>
Date:   Sun Jul 16 01:24:50 2023 +0200

    adding team page


EDELINE@Mugunga MINGW64 /e/Git exercise (ft/faq-page)
$ git revert 831067f7b2792fc70a5e54df6ed9a2f62b73188a
[ft/faq-page a06c459] Revert "adding team page"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 269 bytes | 269.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
   c8728c9..a06c459  ft/faq-page -> ft/faq-page

EDELIN
```
# Budle 3 
# exercise2
```bash

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git commit -m"changes on home.html file"
[main 9793fd9] changes on home.html file
 1 file changed, 3 insertions(+), 1 deletion(-)

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git push origin main
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git commit -m "changes"
[main 70f37ac] changes
 1 file changed, 4 insertions(+), 3 deletions(-)

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/home-page-redesign)
$ git add .

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/home-page-redesign)
$ git commit -m"adding menu"
[ft/home-page-redesign 2433cd7] adding menu
 1 file changed, 4 insertions(+)

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/home-page-redesign)
$ git push origin ft/home-page-redesign
Enumerating objects: 22, done.
Counting objects: 100% (22/22), done.
Delta compression using up to 4 threads
Compressing objects: 100% (20/20), done.
Writing objects: 100% (20/20), 2.00 KiB | 408.00 KiB/s, done.
Total 20 (delta 11), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (11/11), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/AdelineA/Gym-Bundle-Exercises-Solutions/pull/new/ft/home-page-redesign
remote:
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign

EDELINE@Mugunga MINGW64 /e/Git exercise (ft/home-page-redesign)
$
```

# Bundele 4
## Exercise 1
```bash
EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git add home.html

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git commit -m"adding changes on home file"
[main cb1cfb2] adding changes on home file
 1 file changed, 7 insertions(+)

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git push git-copy
Enumerating objects: 34, done.
Counting objects: 100% (34/34), done.
Delta compression using up to 4 threads
Compressing objects: 100% (32/32), done.
Writing objects: 100% (34/34), 4.80 KiB | 351.00 KiB/s, done.
Total 34 (delta 16), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (16/16), done.
To github.com:AdelineA/Git-exercises.git
 * [new branch]      main -> main

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git checkout main
Already on 'main'

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git pull
remote: Enumerating objects: 11, done.
remote: Counting objects: 100% (11/11), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (6/6), 3.08 KiB | 7.00 KiB/s, done.
From github.com:AdelineA/Gym-Bundle-Exercises-Solutions
   28deec6..9adbdfa  ft/service-redesign -> origin/ft/service-redesign
   dc58334..8b77395  ft/team-page        -> origin/ft/team-page
   f335626..19da6c2  main                -> origin/main
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=<remote>/<branch> main


EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git remote --v
git-copy        git@github.com:AdelineA/Git-exercises.git (fetch)
git-copy        git@github.com:AdelineA/Git-exercises.git (push)
origin  git@github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git (fetch)
origin  git@github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git (push) 

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git status
On branch main
nothing to commit, working tree clean

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git push origin main
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git pull origin main
From github.com:AdelineA/Gym-Bundle-Exercises-Solutions
 * branch            main       -> FETCH_HEAD
Auto-merging home.html
Merge made by the 'ort' strategy.
 contact.html  | 11 +++++++++++
 faq.html      | 11 +++++++++++
 home.html     |  4 ++++
 services.html |  1 -
 team.html     | 11 +++++++++++
 5 files changed, 37 insertions(+), 1 deletion(-)
 create mode 100644 contact.html
 create mode 100644 faq.html
 create mode 100644 team.html

EDELINE@Mugunga MINGW64 /e/Git exercise (main)
$ git push origin main
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 4 threads
Compressing objects: 100% (10/10), done.
Writing objects: 100% (10/10), 1.07 KiB | 109.00 KiB/s, done.
Total 10 (delta 6), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (6/6), completed with 3 local objects.
To github.com:AdelineA/Gym-Bundle-Exercises-Solutions.git
   19da6c2..52ed76b  main -> main

```