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
Else you have this message:
```






