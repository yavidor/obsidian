---
title: Advent of Code 2025 - Day 1
tags:
  - אישי
  - מדמח
  - aoc
---
Since my goals is to get better with the restrictions posed by the course #מבוא-למדעי-המחשב I will not use `strlib.h`, which is not really a big deal. Mostly writing some of the functions myself, pretty _trivial_.

# Utils
```C
char *readLines(int day, bool isRealInput);
```
To read the lines of the input and get them a single string

```C
int getFileSize(const char *fileName);
```
Get the file size in characters

```C
int nextNewline(const char* str, int pos, int end);
```
Get the position of the next '\n', if there are not newlines left, return the end position of the string

```C
int lenstr(const char* str);
```
Get the length of a string, like strlen but mine (: