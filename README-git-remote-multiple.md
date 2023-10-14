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
