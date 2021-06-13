# Git & GitHub Code Along

## What is version control system (VCS)?

Version control, also known as revision control or source control, is the management of changes to documents, computer programs, large websites, and other collections of information. Each revision is associated with a timestamp and the person making the change. Revisions can be compared, restored, and with some types of files, merged.

Version control implements a systematic approach to recording and managing changes in files. At its simplest, version control involves taking **snapshots** of your file at different stages. This snapshot records information about when the snapshot was made, and also about what changes occurred between different snapshots. This allows you to **rewind** your file to an older version.

#### Version control allows you to:

- Track developments and changes in your files
- Record the changes you made to your file in a way that you will be able to understand later
- Experiment with different versions of a file while maintaining the original version
- Merge two versions of a file and manage conflicts between versions
- Revert changes, moving **backward** through your history to previous versions of your file.

Some popular version control systems:

- Git
- Helix VCS
- Microsoft Team Foundation Server
- Subversion

### Distributed Version Control System (DVCS)?

A distributed version control system (DVCS) is a type of version control where the complete codebase — including its full version history — is mirrored on every developer's computer.

![DVCS](https://i.imgur.com/ZJ2Dg4c.png)

## What’s git?

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

## What’s Github?

GitHub is a Git repository hosting service, but it adds many of its own features. While Git is a command line tool, GitHub provides a Web-based graphical interface.

#### In short,

**Git** is a Version Control System. **_(used locally)_**

**GitHub** is an online platform for hosting and sharing code, that uses Git at its core in additional for more features. **_(used remotely)_**

### Why using git and github?

- Required skill for every developer to know, for companies, jobs, freelance..
- Tools to keep track of your code.
- Store your code in a remote location.
- Collaborate with other developers using git and github (also, other remote platforms)
- Keep track with open source projects

---

The most basic `git` commands that you will encounter and use:

- Git Configuration:

```bash
git config --global user.name "Your Name"
git config --global user.email "yourname@example.com"
```

to check what your configuration is:

```bash
git config --list
```

- most basic command that you will use locally

```bash
git init     // Create an empty Git repository or reinitialize an existing one
git status   // Show the working tree status and the staging area
git add <file-name>  // Add files to the staging area
git commit -m "message"  // Record changes to the repository (snapshot)
git log  // Show commit logs
```

![drawing](https://i.stack.imgur.com/UvZ0M.png)

- Let's do an [exercise](./exercises/ex1.md)

---

### Connect to github

- Create a `repo` without selecting the `README.md` option. For an example `g9` repo, then you will see this screen below.

![g9](https://i.imgur.com/sps8BQE.png)

- Let's do an [exercise](./exercises/ex2.md)

---

### Continue with connecting your local repo with the remote repo.

- [Pull requests](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)

- Merge code into the `main` branch

most basic command that you will use locally with remote

```bash
git clone <remote-link>   // Download a remote repository into your local machine
git branch  // List branches
git checkout -b <branch-name>  // Create and go into the new branch
git pull origin main  // Fetch changes from a remote repository into the current branch `main`
```

- Let's do an [exercise](./exercises/ex3.md)

---

#### Note

Recently on OCT/2020 , the default branch name changed on GitHub to be `main` instead of `master` previously, so be attentive when you came across any old or legacy code snippets about `master` branch

---

#### Git and GitHub [Glossary](./exercises/glossary.md)
