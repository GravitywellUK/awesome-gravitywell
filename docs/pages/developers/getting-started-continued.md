---
layout: article
title: Getting started continued
permalink: /developers/getting-started-continued/
---

At this point, you should have already followed the Getting Started guide for your specific device. Now we are going to go through the generic guide for getting setup.

## GitHub

Assuming that you have a GitHub account, follow the instructions bellow to authorize your device with your GitHub account.

Open Terminal and perform the following commands,

```shell
$ cd ~/.ssh
$ mkdir github
$ cd ./github
$ ssh-keygen -t ed25519 -C "luke.baker@live.com"
```

When prompted, provide the following path to place the generated file(s) `~/.ssh/github/id_ed25519` (or equivalent). You should now have two files within the directory.

```shell
$ ls
id_ed25519     id_ed25519.pub
```

Now copy the contents of the `id_ed25519.pub` public-key to the [GitHub SSH settings screen](https://github.com/settings/keys) (`Settings > SSH and GPG keys`</code>`).

GitHub now has the public-key to authenticate your device. You now need to inform your device which identity file (private-key) to use when communicating with GitHub.

```shell
Host github.com
  IdentityFile ~/.ssh/github/id_ed25519
```

You should now be able to clone all the repositories that you have access to.