---
layout: post
title: "Installing the Microsoft Flight Simulator 2020 SDK"
date: 2021-02-10 22:00:00 -800
categories: msfs windows
---

I found it surprisingly hard to find documentation on installing the Microsoft Flight Simulator 2020 SDK, which includes the `simconnect` libraries for writing third-party extensions for MSFS. This document aims to get someone set up to develop for my [FriendlyButtonbox](https://github.com/tanmaniac/FriendlyButtonbox) project, which exposes some minimal REST APIs for easier communication with Simconnect.

## Prerequisites

I assume you're running Windows 10 and you own a copy of Flight Simulator 2020.

## Installing the SDK

Open Microsoft Flight Simulator:

![start page](/assets/msfs_sdk/0_start_page.png)

Navigate to the Settings page and select General options:

![settings](/assets/msfs_sdk/1_settings.png)

![general](/assets/msfs_sdk/2_general.png)

Enable Developer tools:

![developer tools](/assets/msfs_sdk/3_developer.png)

![enable developer tools](/assets/msfs_sdk/4_dev_options_on.png)

This will enable a toolbar at the top of the game window. Navigate to Help > SDK Installer, which will take open a web browser and start downloading the installer `.msi` package.

Run the installer with default settings.