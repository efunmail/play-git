## WIP

- REMOVE exising 'origin'

```sh
# git remote -v |less  # // Can check

git remote remove origin

# git remote -v |less  # // Can check
```

- ADD 'MIRROR' repo

```sh
git remote add origin https://github.com/$NAME_USER/$NAME_REPO.git

git remote set-url origin git@github.com:$NAME_USER/$NAME_REPO.git

# git remote -v |less  # // Can check
```

----

```sh
git add .

git commit -S -am "Add WIP.md"
```

```sh
git push origin main

Enter passphrase for key '/home/demo/.ssh/id_ed25519': 
Enumerating objects: 18, done.
Counting objects: 100% (18/18), done.
Delta compression using up to 8 threads
Compressing objects: 100% (17/17), done.
Writing objects: 100% (18/18), 4.31 KiB | 883.00 KiB/s, done.
Total 18 (delta 5), reused 3 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (5/5), done.
remote: fatal: did not receive expected object 5be5917d9f6a0487a530d178b9c892aba660aeac
error: remote unpack failed: index-pack failed
To github.com:efunmail/play-git-2.git
 ! [remote rejected] main -> main (failed)
error: failed to push some refs to 'github.com:efunmail/play-git-2.git'
```


> remote: fatal: **did not receive expected object** `5be5917d9f6a0487a530d178b9c892aba660aeac`
> error: **remote unpack failed**: *index-pack failed*
> To github.com:efunmail/play-git-2.git
>  ! [remote rejected] main -> main (failed)
> error: **failed to push some refs** to 'github.com:efunmail/play-git-2.git'
