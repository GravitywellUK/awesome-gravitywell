---
layout: article
title: Getting started MacOS X
heading: Getting started MacOS X
permalink: /developers/getting-started-macos/
---

WOW, you have a Mac...

![Niccce](https://media.giphy.com/media/pCO5tKdP22RC8/giphy.gif)

Below are some useful directives to help you get up and running quickly.

## 1. CSR Utils

The following is required for MacOS Mojave - MacOS (current). This will disable the System Integrity Protection, which will stop issues arising when using or installing development specific software.

1. Turn off Mac, turn it back on and when you see the Apple logo press and hold `CMD + R` to enter into Recovery Mode.
2. Go to Terminal and enter `csrutil disable`.
3. Restart the Mac.

## 2. Development tools

Out of the box, MacOS X does not have certain development tools installed. You can install them using the following command,

```shell
xcode-select --install
```

## 3. Homebrew

Homebrew is a CLI package manager that enables you to install various software and applications onto your machine with ease. It can also help keep software and application up-to-date.

Before you begin to install Homebrew, you will need to set certain permissions on the `/usr/local` directory as a prerequisite.

```shell
sudo chown -R $(whoami):admin /usr/local
```

Now you can install Homebrew. Go to [https://brew.sh/](https://brew.sh/) and run the given command in Terminal. Once installed, you can then install the following formulas and casks,

### Homebrew formulas

```shell
brew install node awscli aws-cdk mysql@5.7
```

### Homebrew casks

```shell
brew install --casks docker ngrok postman
```

