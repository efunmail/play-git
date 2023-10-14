## Init

- Init, and **PULL from *existing* repo**: 

```sh
git init -b main
git pull https://github.com/efunmail/play-git.git
```

## Set-up

- ADD 'MIRROR' repo

```sh
git remote add origin https://github.com/$NAME_USER/$NAME_REPO.git

git remote set-url origin git@github.com:$NAME_USER/$NAME_REPO.git

# git remote -v |less  # // Can check
```

## Workflow

```sh
git add .

git commit -S -am "Add WIP.md"
```

```sh
git push origin main
```

----

## MULTIPLE repos

- *Set-up*: ADD an 'all' *remote* - containing **both** repos:

```sh
git remote  add all git@github.com:efunmail/play-git.git;
git remote    set-url --add --push all git@github.com:efunmail/play-git-2.git;
git remote    set-url --add --push all git@github.com:efunmail/play-git.git
```

- *Workflow*: PUSH 'all'

```sh
git push all main
```


## ALT method ??

- [ ] ?? Duplicating a repository
https://docs.github.com/en/repositories/creating-and-managing-repositories/duplicating-a-repository
