---
has_children: false
layout: default
title: Language
parent: Configuration
grand_parent: Documentation
nav_order: 2
---

# Configuration - Language
The language config is there to define a set of naming conventions, and the logic behind enforcing those conventions. A full list of the conventions which are supported can be found below.

|      Name      |    Variation   |     Identifier     |
|:--------------:|:--------------:|:------------------:|
|   Camel Case   |    Standard    |     CamelCase      |
|   Camel Case   |    Microsoft   | microsoftCamelCase |
|   Pascal Case  | Not Applicable |     PascalCase     |
|   Snake Case   | Not Applicable |     snake_case     |
|   Kebab Case   | Not Applicable |     kebab-case     |
| Screaming Case | Not Applicable |   SCREAMING_CASE   |
|      None      | Not Applicable |        none        |]


For the sake of not repeating the same thing many times over, the format for this section of the configuration file is the following:

## Convention
#### Description
The naming convention to apply (see table above)

#### Default
`snake_case`


## Force Convention
#### Description
Whether or not the database should forcibly convert all names of items such as columns, tables, databases and procedures to match the specified naming standard

#### Default
`true`


For the rest of this section within the config, the options are the same as this, but are more targeted at a single type of item for conversion