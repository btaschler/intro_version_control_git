# Introduction to Version Control with GIT and GitHub

Version control workshop at the [Oxford-Berlin Autumn School on Open and Responsible Research 2023](https://osf.io/5a38t/).

<br>

## About this repository

All materials (including this guide) can be found in the corresponding [GitHub repository](https://github.com/btaschler/intro_version_control_git/tree/main).

Many of the materials included in this workshop have been adapted from two related workshops ([course 1](https://github.com/MalikaIhle/Introduction-RStudio-Git-GitHub), [course 2](https://github.com/MalikaIhle/Collaborative-RStudio-GitHub)) by [Malika Ihle](https://github.com/MalikaIhle) as well as various resources and online tutorials (incl. from [Software Carpentry](https://software-carpentry.org/), [datacamp](https://www.datacamp.com/) and [GitHub Docs](https://docs.github.com/en)).

<br>

## Getting started

### Accessing the Terminal

**Windows**

If you don't have a command-line tool installed (or if you are not sure), [download Git for Windows](https://gitforwindows.org/) which comes with a terminal emulator called `Git BASH`. Once installed open `Git Bash` from the Start Menu.

**MacOS**

Open the pre-installed `Terminal` app. Alternatively, you can install other terminal emulators with additional functionality (e.g. [iTerm2](https://iterm2.com/)). 

**Unix systems**

Depending on your distribution, look for an application called “terminal”, “command”, “prompt” or “shell”. 

ℹ️ If you have never used the command-line before, have a look at this [cheatsheet](https://www.codecademy.com/learn/learn-the-command-line/modules/learn-the-command-line-navigation/cheatsheet) explaining the basic commands. 

<br>

### Installing and configuring Git

Git is one of the most popular version control systems in the world. It is free and open source.

In its basic form Git is a command-line tool but many desktop applications and GUI's exist that offer a fully interactive interface. 

We will be looking at both the command-line as well as app-based uses of Git. We will focus on `GitHub Desktop` which provides a simple, easy-to-use graphical interface, but many other alternatives exist (see for example [GitKraken](https://www.gitkraken.com/), [Sourcetree](https://www.sourcetreeapp.com/), [TortoiseGit](https://tortoisegit.org/), [Bitbucket](https://bitbucket.org/product), etc.).

Installing GitHub Desktop will also install the latest version of Git if you don't already have it. [Download GitHub Desktop here](https://desktop.github.com/).

Alternatively, you can install Git directly by following the [instructions here](https://github.com/git-guides/install-git).

After installing Git, you need to tell it who you are:

1. Open a terminal / command-line interface.

| Windows     | MacOs       | Unix     |
| :---        | :----       | :---     |
| Open Git Bash. | Open the Terminal app. | Open a terminal emulator.  |


2. Check that `Git` is installed by typing the following command in your terminal app and hitting ENTER.
```
git version
```
If you receive an error message saying that `git` is an unknown command, try to (re)install Git following the description above.

3. Add your details.

Enter the following commands EXACTLY (spaces and quotation marks included) one after the other (hitting ENTER after each command). On successful completion, you should see no output from these commands.

Make sure to replace `my@email.com` and `My Name` with your actual email address and name.

```
git config --global user.email "my@email.com"
git config --global user.name "My Name"
```

<br>

### Create and configure an account on GitHub

Although Git can be used on its own, most people choose to use it in conjunction with an online repository service. Some of the most popular ones are [GitHub](https://github.com/), [GitLab](https://about.gitlab.com/) and [Bitbucket](https://bitbucket.org/product). We will focus on using GitHub but many of the other services have very similar functionality (and all are using the same Git under the hood).

1. Create a free account on [GitHub](https://github.com/join).

You do not need to select any additional products when creating an account.

2. Configure your GitHub account. 

Follow the steps in Part 1 of the [GitHub docs](https://docs.github.com/en/get-started/onboarding/getting-started-with-your-github-account).

3. Set up a secure connection to GitHub with an SSH-key.

Follow the steps in this [guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).

*Note:* When working with a GitHub repository, you'll need to identify yourself to GitHub using your username and password. Establishing a secure connection is mandatory since August 2021.

We will use **SSH Keys** to secure your identification to GitHub. This is a common way to secure connections and you can use your SSH keys for various appliactions.

SSH keys come in pairs, a public key that is shared with services like GitHub, and a private key that is stored only on your computer. (NEVER give away your private key!). 

ℹ️ The procedure described in the link above only needs to be done once per GitHub account and for each computer you will use to connect to GitHub.

<br>

### Using a text editor

Any text editor of your choice will do. 

If you are not sure and want to try out a popular one [download Sublime Text](https://www.sublimetext.com/).

<br>

## Exercises





<br>

## Further Resources






