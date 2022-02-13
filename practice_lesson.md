# Git practice instruction 
![gitlogo](Gitlogo.png)


## 1. Checking  installed git version

Execute command `git version` in terminal.
If git is installed, a message with current version will appear. If not, message with an error.

## 2. Git install
Download latest version of git from https://git-scm.com/downloads. Install it.

## 3. Git setting
First use: you have to introduce yourself by entering two commands:
```
git config --global user.name "Your name"
git config --global user.mail "e-mail"
```

## 4. Creating your first repository

After setting git you have to create __repository__ for your further work. To do this, use the command `git init` in terminal.
After this you receive next message:

---
Initialized empty Git repository in (Path to your  directory)

---

## 5.Work with file in repository
 
Next thing to do is creating new file in your repository (or maybe copying one). For example create file "practice_lesson.md". Always remember that the **file must have an extension**. 

Git doesn't version control your file yet, we need to tell it to do this by using command `git add (file_name)`. After this git starts to control versions of added file and you can work further. Remember to save file after making any changes by pressing __Ctrl+S__ (for Windows) or **Command+S** (for  Mac).

Now to commit any changes we need use command `git commit -m "Comment"`. After use you get this:

![](git_commit.PNG)

Repeat all steps again:
1. Create file with an extension.
2. Work with file.
3. Saving file.
4. Adding file by command `git add (file_name)`.
5. Commiting changes by command `git commit -m "Comment"`.
6. Repeat steps 2-6 as you work.

## 6. Work with repository
  
  Now you have file you are working with. You can check status of it by using command `git status`. If you change nothing next message will appear (or you don't save your changes yet):
  
  ```
  $ git status
On branch master
nothing to commit, working tree clean
```
Else  if you have not commited changes this message appear:
```
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   practice_lesson.md

no changes added to commit (use "git add" and/or "git commit -a")
```

Also you can check changes between commits by command `git diff`.
You get next lines in terminal:

![git diff](gitdiff.PNG)

The red one show lines that was deleted from previous commit/
The green one shows lines that was added.

Also you can see made commits by command `git log`.
It shows unique hash number of a commit, author of the commit, date and a comment added in the commit.

**Example:**
```
$ git log
commit 9a12825c5e955f1037c82bb8207c53c8c6c9d00f (HEAD -> master)
Author: Sergei_Pospelov <pospelka413@gmail.com>
Date:   Sun Feb 13 14:30:08 2022 +0300

    change name

commit 73a0926b51c4f981929b53f2d8a5d8e02e33cf94
Author: Sergei_Pospelov <pospelka413@gmail.com>
Date:   Sun Feb 13 14:27:14 2022 +0300

    added git diff.png

commit 7b399c6795e2efe67f8eef246fd203a5c94b52ac
Author: Sergei_Pospelov <pospelka413@gmail.com>
Date:   Sun Feb 13 13:55:44 2022 +0300

    Git commit instruction added
```
Also you can switch over commits by using command `git checkout (name)`.
Instead of a `(name)` you can insert a unique hash number (or **at least four digits** of it).
After that you get your file status at the moment commit was created.
**Example**

```
$ git checkout 7b399c6
Note: switching to '7b399c6'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 7b399c6 Git commit instruction added
```

If you want to go back you need to do this  `git checkout master`, and you switch to last state of your file (called __master__).

**Example**
```
$ git checkout master
Previous HEAD position was 7b399c6 Git commit instruction added
Switched to branch 'master'
```



