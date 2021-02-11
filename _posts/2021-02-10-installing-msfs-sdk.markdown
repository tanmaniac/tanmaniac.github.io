---
layout: post
title: "Installing the Microsoft Flight Simulator 2020 SDK"
date: 2021-02-10 22:00:00 -800
categories: msfs windows
---

I found it surprisingly hard to find documentation on installing the Microsoft Flight Simulator 2020 SDK, which includes the `simconnect` libraries for writing third-party extensions for MSFS. This document aims to get someone set up to develop for my [FriendlyButtonbox][FriendlyButtonbox] project, which exposes some minimal REST APIs for easier communication with Simconnect.

## Prerequisites

I assume you're running Windows 10 and you own a copy of Flight Simulator 2020.

Before you get started, you'll need to install the MSVC toolchain for Windows. I'm not a Windows developer, so the easiest way for me to do this was to just install [Visual Studio Community](https://visualstudio.microsoft.com/vs/community/). Use the install wizard to select the "Desktop development with C++" package from the *Workloads* tab.

## Installing the SDK

Open Microsoft Flight Simulator:

![start page](https://media.githubusercontent.com/media/tanmaniac/tanmaniac.github.io/master/assets/msfs_sdk/0_start_page.png?raw=true)

Navigate to the Settings page and select General options:

![settings](https://media.githubusercontent.com/media/tanmaniac/tanmaniac.github.io/master/assets/msfs_sdk/1_settings.png?raw=true)

![general](https://media.githubusercontent.com/media/tanmaniac/tanmaniac.github.io/master/assets/msfs_sdk/2_general.png?raw=true)

Enable Developer tools:

![developer tools](https://media.githubusercontent.com/media/tanmaniac/tanmaniac.github.io/master/assets/msfs_sdk/3_developer.png?raw=true)

![enable developer tools](https://media.githubusercontent.com/media/tanmaniac/tanmaniac.github.io/master/assets/msfs_sdk/4_dev_options_on.png?raw=true)

This will enable a toolbar at the top of the game window. Navigate to Help > SDK Installer, which will take open a web browser and start downloading the installer `.msi` package.

![install SDK package](https://media.githubusercontent.com/media/tanmaniac/tanmaniac.github.io/master/assets/msfs_sdk/5_install_sdk.png?raw=true)

Run the installer with default settings.

## Exploring the MSFS SDK

The Flight Simulator SDK is enormous and feature-rich, but really shockingly poorly documented. 

I installed the SDK to `C:\MSFS SDK`, which is the default install location. Its directory structure looks like this (browsing from Bash in WSL)

```bash
$ tree "/mnt/c/MSFS SDK" -L 1
/mnt/c/MSFS SDK
├── Documentation
├── Samples
├── Schemas
├── SimConnect SDK
├── Tools
└── WASM
```

I recommend exploring these directories yourself to understand how SimConnect works better. I hope my [FriendlyButtonbox][FriendlyButtonbox] project also helps in making the SimConnect libraries a little easier to interface with.

[FriendlyButtonbox]: https://github.com/tanmaniac/FriendlyButtonbox