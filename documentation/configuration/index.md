---
has_children: true
layout: default
title: Configuration
parent: Documentation
nav_order: 5
---
# Configuration
Kalavar uses a TOML file to host its configurations, this allows us to parse the config quickly and easily, whilst providing a more friendly config to new users which makes sense to all who use it.

The configuration file is made up of four key sections, they are:

- `network`
- `language`
- `logs`
- `privacy`

A summary of each of these sections is below.

### [Network](./network.md)
The network configuration is the most vital part of the whole configuration file, with it you can define who can and cannot connect to your database and attempt to authenticate. By default the configuration will accept connections from your "localhost" (your computer), this means that only you will be able to connect, and nobody else on the network will be able to.

### [Language](./language.md)
The language configuration section defines a set of rules to enforce upon things like database names, table names, column names, and even procedure names.

### [Logs](./logs.md)
The log configuration section defines which types of logs you would like to allow by default. It also controls settings such as the location of log files, and if they get created at all

### [Privacy](./privacy.md)
This section allows you to determine if you send us any data to allow us to improve the products we are making for you. By default you do not send us any data, and it is an opt-in option, but because we like being clear about how we do things, we have written a complete breakdown of what each of the different privacy levels will provide us access to.
