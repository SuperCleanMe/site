---
has_children: false
layout: default
title: Privacy
parent: Configuration
grand_parent: Documentation
nav_order: 4
---

# Configuration - Privacy
The privacy section of the configuration file provides you with a way to opt into providing some information about your usage of Kalavar back to the devs automatically. Some further documentation on the information shared can be found below

|Data                       |None |Minimal|Basic|Detailed|
|:-------------------------:|:---:|:-----:|:---:|:------:|
|Kalavar version            |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)   |![✅](https://kalavar.cf/assets/images/tick.png =30x30)     |
|CPU Make + Model           |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)   |![✅](https://kalavar.cf/assets/images/tick.png =30x30)     |
|Logical CPU cores          |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)   |![✅](https://kalavar.cf/assets/images/tick.png =30x30)     |
|Physical CPU cores         |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)   |![✅](https://kalavar.cf/assets/images/tick.png =30x30)     |
|Host OS                    |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)   |![✅](https://kalavar.cf/assets/images/tick.png =30x30)     |
|OS version                 |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)   |![✅](https://kalavar.cf/assets/images/tick.png =30x30)     |
|Core Frequency             |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)   |![✅](https://kalavar.cf/assets/images/tick.png =30x30)     |
|Disk overall usage*        |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)   |![✅](https://kalavar.cf/assets/images/tick.png =30x30)     |
|Total system memory (RAM)**|![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![✅](https://kalavar.cf/assets/images/tick.png =30x30)   |![✅](https://kalavar.cf/assets/images/tick.png =30x30)     |
|Disk partitions*           |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![❌](https://kalavar.cf/assets/images/cross.png =30x30)   |![✅](https://kalavar.cf/assets/images/tick.png =30x30)     |
|Swap usage (RAM dump)**    |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![❌](https://kalavar.cf/assets/images/cross.png =30x30)    |![❌](https://kalavar.cf/assets/images/cross.png =30x30)   |![✅](https://kalavar.cf/assets/images/tick.png =30x30)     |


\* Kalavar will never share any of your files with us via these settings, we will only be able to see how many megabytes of data your system has, and the number of partitions you have on it.

** once more, Kalavar will not be able to access any data stored in memory or swap, it will just query the usage of swap and RAM periodically and share that information with us at your discretion.

## Mode
This field takes one of the following values:

`None`,
`Minimal`,
`Basic`, and
`Detailed`

The default value for this parameter is `None`, meaning you share no information with us.

For reference on what these mean, please see the table at the top of the page