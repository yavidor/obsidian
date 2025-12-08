---
title: Advent of Code 2025 - Day 2
tags:
  - אישי
  - מדמח
  - aoc
---
# Part 1
The first hard part was reading the numbers, it wasn't _hard_, but it included changing some utils functions, and I had to also consider day 1 and how changing the utils affects it, this will probably be a bigger problem with each passing day.
Another problem was data types, at first I stored everything in regular `int`, but apparently the total sum and even some of the IDs themselves are too big for an int so I changed everything to a `long long` (and created a new util function for reading a `long long`)
# Part 2
