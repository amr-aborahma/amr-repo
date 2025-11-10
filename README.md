### 📄 Contents of `commands.txt`

#### Create a new project on your local machine, then push it your remote repo.

<pre>
$ git init
Initialized empty Git repository in C:/Users/Amr AboRahma/Desktop/task_2_version_control/.git/

$ git add .
warning: in the working copy of '7.0+CSS+Cascade/index.html', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of '7.0+CSS+Cascade/solution/solution.css', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of '7.0+CSS+Cascade/solution/solution.html', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of '7.0+CSS+Cascade/style.css', LF will be replaced by CRLF the next time Git touches it

$ git commit -m "1st commit"
[master (root-commit) f936262] 1st commit
 10 files changed, 407 insertions(+)
 create mode 100644 7.0+CSS+Cascade/goal.png
 create mode 100644 7.0+CSS+Cascade/index.html
 create mode 100644 7.0+CSS+Cascade/solution/solution.css
 create mode 100644 7.0+CSS+Cascade/solution/solution.html
 create mode 100644 7.0+CSS+Cascade/style.css
 create mode 100644 README.md
 create mode 100644 commands.txt
 create mode 100644 dev-file.txt
 create mode 100644 images/git_cheatsheet.jpg
 create mode 100644 test-file.txt

$ git remote add origin git@github.com:amr-aborahma/amr-repo.git
$ git branch -M main
$ git push -u origin main
    
Enumerating objects: 18, done.
Counting objects: 100% (18/18), done.
Delta compression using up to 4 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (17/17), 940.72 KiB | 9.80 MiB/s, done.
Total 17 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), done.
To https://github.com/amr-aborahma/amr-repo.git
   605ee7a..ebce5e9  main -> main
branch 'main' set up to track 'origin/main'.
</pre>

#### Create two branches (dev & test) then create one file on each branch, and push this changes to the remote repo.

<pre>
$ git switch -c dev
Switched to a new branch 'dev'

$ git add .
$ git commit -m "dev 1st commit"
On branch dev
nothing to commit, working tree clean

$ git push -u origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/amr-aborahma/amr-repo/pull/new/dev
remote:
To https://github.com/amr-aborahma/amr-repo.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.

$ git checkout -b test
    Switched to a new branch 'test'

$ git add .
$ git commit -m "test 1st commit"
On branch test
nothing to commit, working tree clean

$ git push -u origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/amr-aborahma/amr-repo/pull/new/test
remote:
To https://github.com/amr-aborahma/amr-repo.git
 * [new branch]      test -> test
branch 'test' set up to track 'origin/test'.
</pre>

#### Merge these changes on Main branch and then push it to your remote main branch.

<pre>
$ git checkout -b newBranch
    Switched to a new branch 'newBranch'

$ git add new-branch.txt
=> new-branch.txt file is created and added to stage

$ git stash         // stash saves your current stash, but u have to Saved working directory and index state WIP on newBranch: ebce5e9 Merge branch 'main' of https://github.com/amr-aborahma/amr-repo

$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
</pre>

#### Create an annotated tag with tagname (v1.7)

<pre>
$ git add .
$ git commit -m "3rd commit"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

$ git tag -a v1.7 -m "version 1.7"
</pre>

#### Push it to the remote repository

<pre>
$ git push origin v1.7
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 167 bytes | 167.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/amr-aborahma/amr-repo.git
 * [new tag]         v1.7 -> v1.7
</pre>

#### Tell me how to list tags.

<pre>
$ git tag
    v1.7
</pre>

#### Tell me how to delete tag locally and remotely.

<pre>
$ git tag -d v1.7
    Deleted tag 'v1.7' (was efd8adf)

$ git push origin --delete v1.7
To https://github.com/amr-aborahma/amr-repo.git
 - [deleted]         v1.7
</pre>

# president

![president](images/president.jpg)
