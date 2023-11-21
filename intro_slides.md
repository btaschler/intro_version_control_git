---
theme: seriph
background: /OxBer_title.png
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Workshop - Version Control
  OxBer Autumn School 2023
drawings:
  persist: false
transition: 
title: Introduction to Version Control with Git and GitHub
mdc: false
level: 3
fonts:
  sans: Raleway
hideInToc: true
---

<!--
# Introduction to Version Control with Git and GitHub

### Bernd Taschler

OxBer Autumn School 2023

Oxford

2023-11-21
-->

---
layout: image
image: /OxBer_title.png
---


---
layout: image-right
image: /generic_laptop.png
level: 3
---

# Contents

<br>

<Toc maxDepth="1"></Toc>

---
layout: center
---

# Part 1 - What is Version Control?


---
layout: two-cols
level: 3
---

# Why use version control?

- a better way to “undo” changes,

- a better way to collaborate than mailing files back and forth, and
- a better way to share your code and other scientific work with the world.

<br>

---
layout: two-cols
level: 3
---

# Why use version control?

- a better way to “undo” changes,

- a better way to collaborate than mailing files back and forth, and
- a better way to share your code and other scientific work with the world.

<br>

<v-click>
  📂 my_paper

```
   - final_version.pdf
   - final_version2.pdf
   - final_version_with_comments.pdf
   - final_final_version_REVISED.pdf
   - ...
   - definitely_final_version03_updated_LASTedit.pdf
```
</v-click>

::right::

<div align="center">
<img src="/phdcomics_finaldoc.png" class="center h-120 rounded shadow"/>   
</div>

---
level: 3
layout: two-cols
---

# Main concepts

<br>

### A commit

... a recorded set of changes in your project’s files

<br>

### A repository

... the history of all your project’s commits

<br>

<v-click>

### The staging area

... where every commit is prepared - changes must be added here before they can be committed

</v-click>

::right::

<br>

<v-click>

- A **version control system** is a tool that keeps track of all changes, effectively recording snapshots of different versions of our files. 
- You decide which changes will be included in the next snapshot (each record of these changes is called a **commit**)
- The version control system keeps useful metadata about each commit. 
- The complete history of commits for a particular project and their metadata make up a **repository**. 
- Repositories can be kept in sync across different computers, facilitating collaboration among different people.

</v-click>

<br>

---
level: 3
layout: image
image: /pics_git_flow.png
---

# Git workflow

---
level: 3
---

# Configuring Git

<br>

#### Open a Terminal and type the following command

```
git config --list
```
(exit menu by typing `q`)

<br>

#### If your details are not listed:

```
git config --global user.name "My Name"

git config --global user.email "name@somewhere.ac.uk"
```

---
level: 3
layout: image-right
image: /generic_timetravel.png
---

# Let's create a new project: "Time Travel"

#### Create new project folder
```
cd ~/Desktop
mkdir time_travel
cd time_travel
```
<br>

<v-click>

#### Initialise Git

```
git init
```
</v-click>

<br>

<v-click>

#### Check folder contents

```
ls
ls -a
ls -la
```

</v-click>

<br>

<v-click>

#### Check Git status

```
git status
```
</v-click>

<!-- git keeps all files in the .git directory ! -->

---
layout: center
---

# Part 2 - Standard Git Commands

---
level: 3
---

# General command structure

```
git <verb> <options>
```

for example: `git add --all`

<br>

```
git <noun> <options>
```

for example: `git status`

<v-click>

<br>

#### Where does Git store information?

ℹ️ For each project (repository), Git stores all its files in a subdirectory called `.git`.

</v-click>

---
level: 3
---

# Tracking changes

#### Let's create a new file

```
touch time_machine.md
ls
```

<br>

<v-click>

#### Open and edit the file

- ... with any text editor (nano, Sublime text, vim, emacs, ~~MS Word~~, VS Code, RStudio, etc.)

- add a title and a short description: 

  e.g. *Project Time Travel -- How I plan to tell my younger self which netflix series are not worth watching!*

- save changes

</v-click>

<br>

<v-click>

#### Check status

- Switch back to the Terminal and use command:

```
git status
```

</v-click>

---
level: 3
layout: image-right
image: /generic_stage.png
---

# Preparing to save changes: Staging Area

<br>

#### Add a file to the staging area

```
git add time_machine.md
```

<br>

<v-click>

#### Check status

```
git status
```

</v-click>

<br>

<v-click>

#### Try the help for `git status`

```
git status --help
```

*What does this do?*

```
git status -s
```

</v-click>

---
level: 3
layout: image-right
image: /generic_postcards.png
---

# Saving changes: Commits

<br>

#### Track changes (add to version control record)

```
git commit -m "my first commit"
```

<br>

<v-click>

#### Check status

```
git status
```

</v-click>

---
level: 3
layout: two-cols
---

# Exercise: 

0. (between each step: check current state with `git status`)

1. make new changes to the file `time_machine.md`

2. stage and commit new changes (describe changes in commit message)

3. repeat 1-2

4. create a new file `new_physics.md`

5. edit `new_physics.md` \
(e.g. *To make time travel work: need to find new laws of physics! -- Where did Newton and Einstein go wrong?*)

::right::

<br>

<br>

<br>

<br>

6. add `new_physics.md` to the git record (with a new commit)

7. make changes to both `time_machine.md` and `new_physics.md`

8. stage and commit all changes 

9. check the commit history with `git log` (exit log by hitting `q`)

10. create a new subdirectory with a new file and commit 


---
level: 3
---

# Comparing new changes to previous version

<br>

#### 1. Make a small change to `time_machine.md` 
(delete a word, add a sentence)

<br>

#### 2. Check what has changed since most recently saved version

<br>

```
git diff

git diff --staged
```

<!--
  To get out of the pager, press Q.
To move to the next page, press Spacebar.
To search for some_word in all pages, press / and type some_word. Navigate through matches pressing N.
-->

---
level: 3
---

# Quick summary

<br>

- `git status` shows the status of a repository.

- Files can be stored in a project’s working directory, the staging area (where the next commit is being built up) and the local repository (where commits are permanently recorded).

- `git add` puts files in the staging area.

- `git commit` saves the staged content as a new commit in the local repository.

- Tip: Write short, informative commit messages that accurately describe your changes.


---
level: 3
---

# Comparing to older versions

<br>

```
git diff time_machine.md

git diff HEAD time_machine.md

git diff HEAD~1 time_machine.md

git diff HEAD~2 time_machine.md

git diff <commit ID> time_machine.md
```

---
level: 3
---

# Reverting to an earlier version

<br>

#### If file is not in staging area (discard untracked changes)

```
git checkout -- time_machine.md

git checkout HEAD time_machine.md

git checkout <commit ID> time_machine.md
```

<br>

#### If file is already in staging area

```
git reset HEAD time_machine.md
```

---
layout: center
---

# Part 3 - Git Online: GitHub

---
level: 3
layout: image-right
image: /generic_connected_dots.png
---

# Why use GitHub?

<br>

- easy to set up

- free
- huge community
- dominates open software space
- record of what was changed, when and by whom

---
level: 3
---

# From *local* to *global*: Remote repositories

- services like GitHub, Gitlab, BitBucket, etc. 

- host a copy of your local repository on a server (in the cloud)

<div align="left">
<img src="/flowchart_git_github.png" class="center h-90"/>   
</div>

---
level: 3
layout: two-cols-header
---

# Create a remote repository for the time travel project

::left::

1. log into your GitHub account

2. click in top right corner to create a new repository

  ⚠️ *NOTE:* Note: Since we want this repository to be connected to our (existing) local repository, it needs to be empty. Leave “Initialize this repository with a README” unchecked, and keep “None” as options for both “Add .gitignore” and “Add a license.”

3. this essentially creates a folder on GitHub's servers and initialises Git there

<br>

::right::

<v-click>

### Connect local and remote repositories

4. click on the `SSH` tab

5. copy the URL of your remote repository

6. go back to your *local* repository in the terminal 

7. add information about the remote location to your local repository

```
git remote add origin <my_remote_url>
```

8. check that it worked

```
git remote -v
```

</v-click>

<!-- 
origin is a local name used to refer to the remote repository. It could be called anything, but origin is a convention that is often used by default in git and GitHub, so it’s helpful to stick with this unless there’s a reason not to.
-->


---
level: 3
layout: image-right
image: /generic_arrows.png
---

# Uploading changes to a remote repository

<br>

```
git push origin main

git push -u origin main

git push
```

<br>

<v-click>

#### Downloading changes from the remote repository

<br>

```
git pull origin main
```

</v-click>

---
level: 3
---

# Cloning a repository

<br>

- This is the standard way to collaborate with others

```
git clone <url-to-repo>
```

- Note: the remote repository is already set up and called `origin` by default

---
level: 3
---

# Exercise: Explore GitHub

<br>

1. Poke around the GitHub interface

2. Create an issue

3. Assign yourself to the issue

4. Look at the commit history

5. Edit a file directly on GitHub

6. Pull changes to your local repository

---
level: 3
layout: two-cols-header
---

# Resolving conflicts (advanced git)

<br>

⛔️ ISSUE: the *same* section of a file in the local repositiory and the remote repository have both been changed independently 

<br>

::left::

### Example scenario: 

- person A works on the same code as person B

- person A makes a change and pushes it to the remote

- person B makes a change and wants to push to the remote

- git doesn't know which change to keep

<br>

::right::

<v-click>

### Possible solutions:

- B pulls first from the remote and resolves the conflict locally

- A and B work on different branches

- B creates a merge request (to be resolved on GitHub)

</v-click>

---
level: 
layout: two-cols
---

# Commands Summary

- `git status`

- `git add <filename>`
- `git commit -m "<my message>"`
- `git log`
- `git diff`
- `git clone`
- `git pull`
- `git push`
- `git remote`

::right::

<br>

### Getting help on any command

- `git help`

- `git <command> -h`

<br>

### More advanced commands

- `git branch`

- `git switch` 

- `git fetch`

- `git checkout`

- `git rebase`

- ...



<!--
# Different versions of the same files: Branches

- `git branch`
- `git switch`
-->

---
level: 3
layout: image-right
image: /generic_molecules.png
---

# How does version control benefit Open Science?

<br>

<v-click>

- makes code reproducible

- makes it easier to collaborate

- hosted repositories can be cited

- automatically backed-up (distributed servers)

- ...

</v-click>

---
level: 3
layout: two-cols-header
---

# Git can also be used with a graphical interface

::left::

## Git integrations in other software

- RStudio

- VSCode

- PyCharm

- Sublime Text

- *and many others ...*

<br>

<br>

::right::

## GUI apps for Git

- GitHub Desktop

- GitKraken

- SourceTree

- TortoiseGit

- ...

<br>

<br>

---
level: 1
---

# Additional Exercises and Resources

1. Create a new repo on GitHub (initialise with README and LICENCE files)

    - clone it to a local directory
    - make changes locally, commit and push to the remote
    - make changes on GitHub, commit and pull to local repo
    - familiarise yourself with GitHub's online functionalities
    - open an issue on GitHub

2. Learn about branches

    - e.g. follow this [tutorial](https://www.atlassian.com/git/tutorials/using-branches)

3. Git in Rstudio
  
    - If you want to use git from within RStudio, see e.g. this [tutorial](https://github.com/MalikaIhle/Introduction-RStudio-Git-GitHub/blob/main/version_control.md) or this [tutorial](https://sites.northwestern.edu/researchcomputing/2022/05/11/git-with-rstudio-order-matters/)

4. Try a GUI, e.g. [GitHub Desktop](https://desktop.github.com/) or [GitKraken](https://www.gitkraken.com/)


---
level: 3
---

# Additional Resources

- Continuous integration: run tests automatically every time you push changes to the remote
  - see e.g. [here](https://docs.github.com/en/actions/automating-builds-and-tests/about-continuous-integration)

- `.gitignore`: tell git which files to ignore
  see e.g. [here](https://git-scm.com/docs/gitignore)

- Merge conflicts and how to resolve them
  - see e.g. this [tutorial](https://www.freecodecamp.org/news/resolve-merge-conflicts-in-git-a-practical-guide/)

- Git GUIs: 
  - see e.g.g this [overview](https://git-scm.com/downloads/guis)

- a self-paced tutorial app to learn Git: [git-it -electron](https://github.com/jlord/git-it-electron)

- check out in-depth tutorials from [Software Carpentry](https://software-carpentry.org/lessons/) (incl. git, shell, python, R, etc.)

---
