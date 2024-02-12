---
title: Configuration example
description: Some page configuration and extensions usage examples
status: new
---

## Goals of this page

This page aims to demonstrate some examples of a page configuration and examples usage of some extensions.

## Admonition examples

!!! note

    note admonition example - not collapsible

??? info

    info admonition example - collapsible, not expanded by default

???+ tip

    tip admonition example - collapsible, expanded by default

!!! warning

    warning admonition example - not collapsible

???+ example

    example admonition example - collapsible, expanded by default

## Code blocks examples

```java title="frequencies-map-with-for.jsh"
/**
 * Run with JBang : jbang frequencies-map-with-for.jsh (1)
 * <p>
 * or open in JShell : /open frequencies-map-with-for.jsh
 */
import java.util.HashMap;
import java.util.List;
import java.util.Map;

List<String> daysOfWeek = List.of("Friday", "Thursday", "Thursday", "Saturday", "Thursday", "Thursday", "Monday", "Saturday", "Friday", "Saturday");
Map<String, Integer> frequencies = new HashMap<>();
int previousCount;
for (String day : daysOfWeek) {
    previousCount = frequencies.getOrDefault(day, 0);
    frequencies.put(day, previousCount + 1);
}

frequencies.entrySet().iterator().forEachRemaining(System.out::println);
```

1. :man_raising_hand: Code annotation example
