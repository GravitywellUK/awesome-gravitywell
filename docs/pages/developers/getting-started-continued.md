---
layout: article
title: Getting started continued
subtitle: Getting started continued guide for developers
permalink: /developers/getting-started-continued/
previous:
  title: Developers
  url: /developers/
next:
  title: Software versions
  url: /developers/software-versions/
---

At this point, you should have already followed the Getting Started guide for your specific device. Now we are going to go through the generic guide for getting setup.

## 1. GitHub

Assuming that you have a GitHub account, follow the instructions below to authorize your device with your GitHub account.

Open Terminal and perform the following commands,

```shell
$ cd ~/.ssh
$ mkdir github
$ cd ./github
$ ssh-keygen -t ed25519 -C "joe.bloggs@example.com"
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

## 2. Nodejs (LTS) & packages

At this point, you should have the latest version of NodeJs installed, however, for projects in production we tend to use NodeJs's latest LTS (Long Term Support) version. The simplest way of doing this is leveraging a package called `n`, which manages your local NodeJs versions.

We recommend using `Yarn`, which is a dependency/package manager for NodeJs. If you are using MacOS or Linux and you have followed our operating system specific guides regarding `Homebrew`, you should already have this installed.

### `n` dependency manager

To install `n` run the following command,

```shell
$ yarn global add n
```

### Managing NodeJs versions

Using `n` above, we can manage your local NodeJs version. Check our recommended [software version](/developers/software-versions/#h-nodejs) for NodeJs to install before running continuing below,

To install a new version, run the following command,

```shell
$ n 14.17.3
```

You can also view and change NodeJs version interactively using the following command,

```shell
$ n

    node/4.8.3
    node/6.0.0
    node/8.10.0
    node/8.11.3
    node/8.12.0
    node/8.15.1
    node/9.4.0
    node/9.11.1
    node/9.11.2
    node/10.14.1
    node/10.16.3
    node/11.10.0
    node/11.10.1
    node/12.6.0
    node/12.13.1
    node/12.21.0
    node/14.15.5
  ο node/14.17.3

Use up/down arrow keys to select a version, return key to install, d to delete, q to quit
```

### Recommended global packages

Once you have the correct [software versions](/developers/software-versions/) for `NodeJs` and `Yarn`, we recommend installing the follow global packages, using the command below:

- AWS Amplify CLI
- AWS CDK
- eslint
- lerna
- React Native
- Sass
- Typescript

```shell
$ yarn global add @aws-amplify/cli aws-cdk eslint lerna react-native sass tsc
```

## IDE

For an IDE, you are welcome to use any IDE you wish, however, if you are unsure which one to pick, we recommend going with one which is broadly used across the development team. Support is at hand if your IDE becomes feral or you become stuck with it. Gravitywell tends to lean towards `VSCode`.

### VSCode

Microsoft's [VSCode](https://code.visualstudio.com/) is the a popular choice for most developers at Gravitywell. Checkout the recommended pluggins to install below:

- Auto Close Tag
- Auto Import
- Better Comments
- Code Runner
- Code Spell Checker
- DotENV
- ESLint
- Import Cost
- Markdown All in One
- MJML
- npm Intellisense
- Path Intellisense
- Sass
- TypeScript Extension Pack
- vscode-styled-components
- XML Tools
- YAML
- ZipFS - a zip file system
