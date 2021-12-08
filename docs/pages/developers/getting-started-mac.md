---
layout: article
title: Getting started MaxOS
subheading: Getting started MacOS guide for developers
permalink: /developers/getting-started-macos/
previous:
  title: Developers
  url: /developers/
next:
  title: Getting started continued
  url: /developers/getting-started-continued/
---

WOW, you have a Mac...

![South Park "Niccce" quote](https://media.giphy.com/media/pCO5tKdP22RC8/giphy.gif)

Ideally you want to make sure that your Mac is running the latest MacOS before continuing. Below are some useful directives to help you get up and running quickly.

## 1. CSR Utils

The following is required for MacOS Mojave - MacOS (current). This will disable the System Integrity Protection, which will stop issues arising when using or installing development specific software.

1. Turn off Mac, turn it back on and when you see the Apple logo press and hold `CMD + R` to enter into Recovery Mode.
2. Go to Terminal and enter `csrutil disable`.
3. Restart the Mac.

## 2. Development tools

Out of the box, MacOS X does not have certain development tools installed. You can install them using the following command,

```shell
$ xcode-select --install
```

## 3. Oh My Zsh (optional)

Optionally, you download and configure [Oh My Zsh](https://ohmyz.sh/) for managing your Zsh configuration.

It comes bundled with thousands of helpful functions, helpers, plugins, and themes to improve your terminal's look and feel as well as giving you additional information such as the current Git status of a project that your working on.

If this interests you, now is a good time to install this before the next steps, as you will need to append additional export paths (`export PATH="/usr/local/opt/mysql@5.7/bin:$PATH"` as an example) to your `~/.zshrc` file.

## 4. Homebrew

Homebrew is a CLI package manager that enables you to install various software and applications onto your machine with ease. It can also help keep software and application up-to-date.

Before you begin to install Homebrew, you will need to set certain permissions on the `/usr/local` directory as a prerequisite.

```shell
$ sudo chown -R $(whoami):admin /usr/local
```

Now you can install Homebrew. Go to [https://brew.sh/](https://brew.sh/) and run the given command in Terminal. Once installed, you can then install the following formulas and casks,

### Homebrew formulas

```shell
$ brew install node yarn awscli aws-cdk mysql@5.7
```

### Homebrew casks

```shell
$ brew install --casks docker ngrok postman
```

## 5. React Native

Depending on your role, you may need to develop with React Native. We recommend that you install Xcode and Android Studio.

### Xcode

Go to the MacOS App Store to download and install Xcode.

### Android Studio

Visit the [Android Studio](https://developer.android.com/studio) website to download and install the Android dev tools and SDK.


