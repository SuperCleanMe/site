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
|Kalavar version            |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>     |
|CPU Make + Model           |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>     |
|Logical CPU cores          |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>     |
|Physical CPU cores         |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>     |
|Host OS                    |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>     |
|OS version                 |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>    |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>     |
|Core Frequency             |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>    |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>     |
|Disk overall usage*        |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>    |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>     |
|Total system memory (RAM)**|<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>    |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>   |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>     |
|Disk partitions*           |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>    |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>   |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>  |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>     |
|Swap usage (RAM dump)**    |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>    |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>   |<img src="https://kalavar.cf/assets/images/cross.png" width="30px" height="30px" alt="❌"/>  |<img src="https://kalavar.cf/assets/images/tick.png" width="30px" height="30px" alt="✅"/>     |


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