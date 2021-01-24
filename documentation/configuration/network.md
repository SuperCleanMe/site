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
1234

## Bind Address
#### Description
The address which the connection listener will attempt to bind to. `localhost` refers to 127.0.0.1, otherwise known for being the computer you just Kalavar on

#### Default
`localhost`

## Max Connections
#### Description
The maximum number of concurrent connections to allow at a time.

#### Default
25

## Accept Ranges
#### Description
A range of IP addresses from which to accept incoming connections and begin the authentication progress.

#### Default
`["*"]`