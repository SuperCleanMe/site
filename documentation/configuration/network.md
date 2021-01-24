---
has_children: false
layout: default
title: Network
parent: Configuration
grand_parent: Documentation
nav_order: 1
---

# Configuration - Network
The network configuration sectioncontrols who can or cannot connect to your database, and from where they may do it. It also controls things such as the maximum number of concurrent connections to allow.

## Bind Port
#### Description
The port which the connection listener will attempt to bind to

#### Default
`48173`

## Bind Address
#### Description
The address which the connection listener will attempt to bind to. `localhost` refers to 127.0.0.1, otherwise known for being the computer you just Kalavar on

#### Default
`localhost`

## Max Connections
#### Description
The maximum number of concurrent connections to allow at a time.

#### Default
`25`

## Accept Ranges
#### Description
A range of IP addresses from which to accept incoming connections and begin the authentication progress.

#### Default
`["*"]`

#### More Information:
The IP ranges can be specified using one of the following two notations:

|Example|Name|Description|Breakdown|
|:---:|:---:|:---:|:---:|
|`192.168.1.1 - 192.168.1.255`|Range|Accepts any IP address between the lower and upper limit|`LOWER_LIMIT - UPPER_LIMIT`|
|192.168.1.0/24|CIDR|Accepts any IP address which matches the specified bit width [see CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)|`BASE_ADDRESS/BIT_WIDTH` 