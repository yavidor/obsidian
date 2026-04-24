---
title: Advent of Code 2025 - Day 1
tags:
  - אישי
  - מדמח
  - aoc
---
Since my goals is to get better with the restrictions posed by the course #מבוא-למדעי-המחשב I will not use `strlib.h`, which is not really a big deal. Mostly writing some of the functions myself, pretty _trivial_.

# Part 1
The problem itself was pretty _trivial_, if the first character is R, add a positive number, if L, negative
If the result is negative add 100 to simulate circling back from the left, then modulo 100 to simulate circling back from the right.
# Part 2
Exactly the same as part one but rotate one click at a time.
