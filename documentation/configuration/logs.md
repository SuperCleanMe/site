---
has_children: false
layout: default
title: Logs
parent: Configuration
grand_parent: Documentation
nav_order: 3
---

# Configuration - Logging
The logging configuration controls which levels of logs are displayed and/or written to file. It also controls where the log files are written, and if the log files are written.

## Path
#### Description
The path in which to write log files to

#### Default Value
`/var/lib/kalavar/logs`

## Debug
#### Description
If the logger should display (and write) `DEBUG` level log messages

#### Default Value
`true`

## Info
#### Description
If the logger should display (and write) `INFO` level log messages

#### Default Value
`true`

## Log
#### Description
If the logger should display (and write) `LOG` level log messages

#### Default Value
`true`

## Warn
#### Description
If the logger should display (and write) `WARN` level log messages

#### Default Value
`true`

## Error
#### Description
If the logger should display (and write) `ERROR` level log messages

#### Default Value
`true`

## Log To File
#### Description
Whether or not the logger should write logs to a file as well as the terminal, or just the terminal.

`true` - Write logs to terminal and file

`false` - Write logs to terminal, but not to file

> Note: It is highly recommended to leave this set to `true` due to the nature of error messages being logged once before exiting, meaning they have a natural tendency to get lost