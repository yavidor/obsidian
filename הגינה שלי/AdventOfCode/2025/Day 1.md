---
title: Advent of Code 2025 - Day 1
tags:
  - אישי
  - מדמח
  - aoc
permalink: 7bae38fd-1bd9-40fc-b102-555ee5ea99b9
modified: 2026-11-27T18:41:41+02:00
created: 2026-11-15T12:10:53+02:00
---
Since my goals is to get better with the restrictions posed by the course #מבוא-למדעי-המחשב I will not use `strlib.h`, which is not really a big deal. Mostly writing some of the functions myself, pretty _trivial_.

# Part 1
The problem itself was pretty _trivial_, if the first character is R, add a positive number, if L, negative
If the result is negative add 100 to simulate circling back from the left, then modulo 100 to simulate circling back from the right.
# Part 2
Exactly the same as part one but rotate one click at a time.
