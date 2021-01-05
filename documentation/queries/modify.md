---
has_children: false
layout: default
title: Modifying Data
parent: Querying Data
grand_parent: Documentation
nav_order: 4
---

# Modify
Should the client wish to update the values of a table:
```
MODIFY my_database.A
FILTERS: 1:"name"=="John Doe"
AND 1:"pass"=="abc123"
OR 2:"pass"==NUll
VALUES: "abc122", "abc133", "abc321"
```