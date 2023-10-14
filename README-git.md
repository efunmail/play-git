## Init

- `~/git_hub/` dir:

```sh
mkdir -p ~/git_hub/$NAME_USER/$NAME_REPO
cd ~/git_hub/$NAME_USER/$NAME_REPO
```

## Git INIT

```sh
git init

hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: 	git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: 	git branch -m <name>
```

```sh
rm -rf .git/
```

- Init - with (initial) *branch name* of **'main'**:

```sh
git init -b main
```

## Git STATUS

- `git status`

```
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README-git.md

nothing added to commit but untracked files present (use "git add" to track)
```
