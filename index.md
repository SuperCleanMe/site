---
layout: default
title: Home
nav_order: 1
---
![CI](https://github.com/KalavarDB/core/workflows/CI/badge.svg) [![Discord](https://img.shields.io/discord/792527699771129856)](https://discord.gg/jUGS8UsgUF) [![GitHub issues](https://img.shields.io/github/issues-raw/KalavarDB/core)](https://github.com/KalavarDB/core/issues) ![GitHub](https://img.shields.io/github/license/KalavarDB/core) [![GitHub Repo stars](https://img.shields.io/github/stars/KalavarDB/core)](https://github.com/KalavarDB/core/stargazers) [![GitHub watchers](https://img.shields.io/github/watchers/KalavarDB/core)](https://github.com/KalavarDB/core/watchers) ![GitHub commits since latest release (by SemVer)](https://img.shields.io/github/commits-since/KalavarDB/core/latest?sort=semver)

Kalavar is a project attempting to bring a fast, efficient, secure, and __asynchronous__ query model to the modern database system. It is designed to be quick, and secure, from the very beginning without any of that additional configuration mess.

## Why Asynchronous?
Frankly, SQL is old, and outdated, it has been in need of a refresh for a long time, and we decided to refresh it. So, we developed KQL. An exciting refreshment of the Structured Query Language used by the biggest databases, modeled to be used in an asynchronous environment with minimal pick up time.

## What is KQL?
KQL is our in-house query language. It is designed to be __asynchronous__ and provide a powerful, yet efficient, and easy to follow query structure.

## How can i use Kalavar?
Currently, Kalavar is under heavy development, most of the information on this page is a placeholder, providing an optimistic goal of the project, but until it is publicly released, this page is a goal page.

TL;DR: You cannot, it is still being developed and is not publicly available at this time.

## Im a developer, how do i write a library for Kalavar?
Again, due to us being in early development, no 3rd party library development is being encouraged, whilst we flesh out our transmission protocol. But, should you choose to begin work anyway, the [Documentation](documentation) might be a good place to look.

## Helping Test Kalavar:

Whilst there are currently no active testing events ongoing at this time, you are welcome to clone this repository and launch the dev kit in your terminal. You can do so by running `bash test.sh`, where you will be greeted with the following menu:
```
---------------------------------
       Kalavar Dev Kit V0.1      
---------------------------------
1.   Check Dependencies
2.   Build and run
3. Δ Build and run as super user
4.   Build and run tests
5. Δ Purge target directory
6.   Install Dependency Checker
7.   Exit
---------------------------------
 Δ - requires SUDO priveleges
---------------------------------
Enter your choice [1-7] : 
```
This dev kit is intended for use on unix systems, as that is what I use to develop and test Kalavar on, and this kit is primarily meant to make my life easier.

> Note: The dev kit requires that you have Cargo in your PATH, and that you have Rust and all of it's dependencies installed correctly.

If you have any feedback about the developer kit, or you want to ask for new commands, please open an issue with the "dev kit" tag.
