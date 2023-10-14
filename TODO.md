## TODO

- [ ] SSH keys

- [ ] Workflow

---

- [ ] Fetch a sub-dir only - *'sparse checkout'*?? 
- [ ] Commit with *different* (PAST!) dates...

----

## SSH Keys

- Prereqs:

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?tool=webui#prerequisites

> 1. Check for existing SSH keys ...
>
> 2. Generate a new SSH key ...

- 'Authentication' and 'Signing' keys: https://stackoverflow.com/a/73674287

> The difference between signing keys and authentication keys
> is that signing keys can be used to sign Git commits and
> authentication keys can be used to access repositories.
> If you add a key as only one type, then it can be used
> only for that purpose, but the same key may be added for both.


```sh
$ ssh-keygen -t ed25519 -C "efunmail@_MAIL_"

Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/demo/.ssh/id_ed25519): 
Created directory '/home/demo/.ssh'.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/demo/.ssh/id_ed25519
Your public key has been saved in /home/demo/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:jHftitDEMIUuyHCYdEnqE+GObWrNYTNwX0BR9+7keN0 efunmail@_MAIL_
The key's randomart image is:
+--[ED25519 256]--+
|.=.oo+oo..       |
|= =.  o.. .      |
| O o .o.   .     |
|+.* o o*  ..     |
|.+o= o. S .o.    |
| o= +  + .=.. .  |
|.. o  . .. +.. E |
|.      . ...     |
|        . .      |
+----[SHA256]-----+
```

- Public-key file `id_ed25519.pub` is: 

```
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIMrCVIXQDhsjVvz5v6+PfqaljOEBTP5we8IOegeA1wS1 efunmail@_MAIL_
```

### Commit Signature Verification

- [GitHub Docs](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification)
