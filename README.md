### FEATURE BRANCH WORKFLOW 

#### clone a remote git repository
				
`git clone <remote-repository-url>`
- example: `git clone https://github.com/username/repository.git`
- clone a remote git repository to a local system.

----------------------------------------------------------------------------------------------------------------

#### create a branch

1. `git checkout -b branchName`
- create and switch to a branch called branchName

2. ``git push` -u origin branchName`
- links local branchName with remote corresponding branch
- push local branch to remote repository for the first time (first time only)

----------------------------------------------------------------------------------------------------------------

#### merge branchName with master branch

1. `git check out master`
- point local environment to master branch

2. ``git pull``
- ensure local copy of our master branch has all latest changes from remote repository

3. `git merge branchName`
- merge branch changes from branchName with current branch. In this case, master branch

##### now local master is up-to-date

4. ``git push``
- push local master to remote master

----------------------------------------------------------------------------------------------------------------

### git commands' logs

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git

$ `git clone https://github.com/AnanthaRajuC/Git-Feature-Branch-Workflow.git`

Cloning into 'Git-Feature-Branch-Workflow'...
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), done.

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git

$ `ls`

Git-Feature-Branch-Workflow/

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git

$ `cd Git-Feature-Branch-Workflow/`

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `ls`

LICENSE  README.md

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git branch`

* master

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git checkout -b feature1`

Switched to a new branch 'feature1'

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature1)

$ `git branch`

* feature1
  master

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature1)

$ ``git push` -u origin feature1`

Total 0 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'feature1' on GitHub by visiting:
remote:      https://github.com/AnanthaRajuC/Git-Feature-Branch-Workflow/pull/new/feature1
remote:
To https://github.com/AnanthaRajuC/Git-Feature-Branch-Workflow.git
 * [new branch]      feature1 -> feature1
Branch 'feature1' set up to track remote branch 'feature1' from 'origin'.

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature1)

$ `git status`

On branch feature1
Your branch is up to date with 'origin/feature1'.

Untracked files:
  (use "`git add .`file>..." to include in what will be committed)

        feature1.txt

nothing added to commit but untracked files present (use "git add" to track)

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature1)

$ `git add .`

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature1)

$ `git status`

On branch feature1
Your branch is up to date with 'origin/feature1'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   feature1.txt


johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature1)

$ `git commit -m "ADD feature1.txt"`

[feature1 181754f] ADD feature1.txt
 1 file changed, 1 insertion(+)
 create mode 100644 feature1.txt

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature1)

$ `git status`

On branch feature1
Your branch is ahead of 'origin/feature1' by 1 commit.
  (use "`git push`" to publish your local commits)

nothing to commit, working tree clean

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature1)

$ `git checkout master`

Switched to branch 'master'
Your branch is up to date with 'origin/master'.

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git branch`

  feature1
* master

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git pull`

Already up to date.

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git merge feature1`

Updating d1297aa..181754f
Fast-forward
 feature1.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 feature1.txt

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git push`

Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 329 bytes | 65.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/AnanthaRajuC/Git-Feature-Branch-Workflow.git
   d1297aa..181754f  master -> master
   
----------------------------------------------------------------------------------------------------------------

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git branch`

  feature1
* master

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git checkout -b feature2`

Switched to a new branch 'feature2'

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature2)

$ `git branch`

  feature1
* feature2
  master

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature2)

$ `git push` -u origin feature2

Total 0 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for 'feature2' on GitHub by visiting:
remote:      https://github.com/AnanthaRajuC/Git-Feature-Branch-Workflow/pull/new/feature2
remote:
To https://github.com/AnanthaRajuC/Git-Feature-Branch-Workflow.git
 * [new branch]      feature2 -> feature2
Branch 'feature2' set up to track remote branch 'feature2' from 'origin'.

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature2)

$ `git status`

On branch feature2
Your branch is up to date with 'origin/feature2'.

Untracked files:
  (use "`git add .`file>..." to include in what will be committed)

        feature2.txt

nothing added to commit but untracked files present (use "git add" to track)

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature2)

$ `git add .`

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature2)

$ `git status`

On branch feature2
Your branch is up to date with 'origin/feature2'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   feature2.txt


johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature2)

$ `git commit -m "ADD feature2.txt"`

[feature2 ac54f45] ADD feature2.txt
 1 file changed, 1 insertion(+)
 create mode 100644 feature2.txt

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature2)

$ `git status`

On branch feature2
Your branch is ahead of 'origin/feature2' by 1 commit.
  (use "`git push`" to publish your local commits)

nothing to commit, working tree clean

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (feature2)

$ `git checkout master`

Switched to branch 'master'
Your branch is up to date with 'origin/master'.

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git branch`

  feature1
  feature2
* master

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git pull`

Already up to date.

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git merge feature2`

Updating 181754f..ac54f45
Fast-forward
 feature2.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 feature2.txt

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git status`

On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "`git push`" to publish your local commits)

nothing to commit, working tree clean

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git branch`

  feature1
  feature2
* master

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git push`

Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 288 bytes | 288.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/AnanthaRajuC/Git-Feature-Branch-Workflow.git
   181754f..ac54f45  master -> master

johndoe@lp28 MINGW64 /c/John-Doe/eclipse-workspace/WS_E_2020/Learning-Git/Git-Feature-Branch-Workflow (master)

$ `git status`

On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

----------------------------------------------------------------------------------------------------------------