---
layout: article
title: Getting started Linux
subtitle: Getting started Linux guide for developers
permalink: /developers/getting-started-linux/
previous:
  title: Developers
  url: /developers/
next:
  title: Getting started continued
  url: /developers/getting-started-continued/
---

Below are some useful directives to help you get up and running quickly.

## 1. Oh My Zsh (optional)

Optionally, you download and configure [Oh My Zsh](https://ohmyz.sh/) for managing your Zsh configuration.

It comes bundled with thousands of helpful functions, helpers, plugins, and themes to improve your terminal's look and feel as well as giving you additional information such as the current Git status of a project that your working on.

If this interests you, now is a good time to install this before the next steps, as you will need to append additional export paths (`export PATH="/usr/local/opt/mysql@5.7/bin:$PATH"` as an example) to your `~/.zshrc` file.

## 2. Homebrew

Homebrew is a CLI package manager that enables you to install various software and applications onto your machine with ease. It can also help keep software and application up-to-date.

Before you begin to install Homebrew, you will need to set certain permissions on the `/usr/local` directory as a prerequisite.

```shell
$ sudo chown -R $(whoami):admin /usr/local
```

Now you can install Homebrew. Go to [https://brew.sh/](https://brew.sh/) and run the given command in Terminal. Once installed, you can then install the following formulas and casks,

### Homebrew formulas

```shell
$ brew install node yarn awscli aws-cdk mysql@5.7 mongodb redis
```

### Homebrew casks

```shell
$ brew install --casks google-chrome firefox docker ngrok postman flipper java
```

## 3. React Native

Depending on your role, you may need to develop with React Native. We recommend that you install Xcode and Android Studio.

### Android Studio

Visit the [Android Studio](https://developer.android.com/studio) website to download and install the Android dev tools and SDK.
