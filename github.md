# GitHub MFA and tricks

<!-- TOC -->

- [GitHub MFA and tricks](#github-mfa-and-tricks)
    - [Using git with ssh](#using-git-with-ssh)
        - [GitHub sshkeys](#github-sshkeys)
        - [Generate a sshkey pair](#generate-a-sshkey-pair)
    - [Using git with https](#using-git-with-https)
    - [HTTPS vs ssh](#https-vs-ssh)

<!-- /TOC -->
***

To enable GitHub MFA visit:

https://github.com/settings/security

Don't forget to save securely your [recovery codes](https://github.com/settings/auth/recovery-codes)


## Using git with ssh

`$ git clone git@GitHub.com:FernandoMiguel/MFAguide.git`

asks for sshkey password, unless key is unlocked 

Which can be achieved with:
> $ ssh-add  ~/.ssh/ed25519

> Enter passphrase for /Users/fernando/.ssh/ed25519:

### GitHub sshkeys
You should keep your **public** sshkeys updated on GitHub

https://GitHub.com/settings/keys

You can see your keys at https://GitHub.com/YOUR-USERNAME.keys

Example: https://GitHub.com/fernandomiguel.keys

### Generate a sshkey pair
` $ ssh-keygen -t ed25519`

**Always** set a password

***

## Using git with https

`$ git clone https://GitHub.com/FernandoMiguel/MFAguide.git`

asks for your GitHub username and a '_password_'. 

But since you now have MFA enabled, your web password no longer works.

Instead you must use a [Personal access tokens](https://GitHub.com/settings/tokens)

You can securely store that token in your keychain.


## HTTPS vs ssh

Personally I opt to use https methods, since I don't like having my sshkey unlocked.

By using https methods, code editors can more easilly interact with git repos.