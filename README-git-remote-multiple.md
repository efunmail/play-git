## Git - Pushing to TWO remotes

https://stackoverflow.com/a/14290145


```sh
# // Initial - necessary??
git remote set-url origin git@github.com:efunmail/play-git.git

# // Add `all`, plus `set-url` 
git remote  add all git@github.com:efunmail/play-git.git
git remote    set-url --add --push all git@github.com:efunmail/play-git-2.git
git remote    set-url --add --push all git@github.com:efunmail/play-git.git
```

- At each step, a can check:

```sh
git remote -v |less
git config -l |less
```


> IMPORTANT NOTE: If your remotes have distinct rules (hooks) to accept/reject a push, one remote may accept it while the other doesn't. Therefore, if you want them to have the exact same history, you'll need to fix your commits locally to make them acceptable by both remotes and push again, or you might end up in a situation where you can only fix it by rewriting history (using push -f), and that could cause problems for people that have already pulled your previous changes from the repo.


## Push ALL 


```sh
$ git push all main

Enter passphrase for key '/home/demo/.ssh/id_ed25519': 
Enter passphrase for key '/home/demo/.ssh/id_ed25519': 
Enumerating objects: 18, done.
Counting objects: 100% (18/18), done.
Delta compression using up to 8 threads
Compressing objects: 100% (17/17), done.
Writing objects: 100% (18/18), 4.74 KiB | 2.37 MiB/s, done.
Total 18 (delta 4), reused 3 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), done.
remote: fatal: did not receive expected object 5be5917d9f6a0487a530d178b9c892aba660aeac
error: remote unpack failed: index-pack failed
To github.com:efunmail/play-git-2.git
 ! [remote rejected] main -> main (failed)
error: failed to push some refs to 'github.com:efunmail/play-git-2.git'
#      ========================
```
