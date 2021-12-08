---
layout: article
title: Getting started Linux
permalink: /developers/getting-started-linux/
---

Below are some useful directives to help you get up and running quickly.

## 1. Homebrew

Homebrew is a CLI package manager that enables you to install various software and applications onto your machine with ease. It can also help keep software and application up-to-date.

Before you begin to install Homebrew, you will need to set certain permissions on the `/usr/local` directory as a prerequisite.

```shell
$ sudo chown -R $(whoami):admin /usr/local
```

Now you can install Homebrew. Go to [https://brew.sh/](https://brew.sh/) and run the given command in Terminal. Once installed, you can then install the following formulas and casks,

### Homebrew formulas

```shell
$ brew install node awscli aws-cdk mysql@5.7
```

### Homebrew casks

```shell
$ brew install --casks docker ngrok postman
```

## React Native

Depending on your role, you may need to develop with React Native. We recommend that you install Xcode and Android Studio.

### Android Studio

Visit the [Android Studio](https://developer.android.com/studio) website to download and install the Android dev tools and SDK.
