---
layout: default
title: Harvard CS50
---
<h1 class="page-title">Harvard CS50 - Intro to CS</h1>
<!-- ### Table of Content: -->
<!-- 1. [Writing Cls](#writing-cls) -->
<!-- 2. [Writing CL descriptions](#writing-cl-descriptions) -->
<!-- 3. [Handling reviewers comments](#handling-reviewers-comments) -->

# Lecture 0
## Representations
### Numbers
* Bit is a binary digit
* You can't describe to much information with a single bit, except True or False, so we need a more useful measure - a byte
* 1 byte is 8 bits
* Transistor is a tiny little switch in our computer that represents a information and stored value - a bit
### Characters
* Represent characters as numbers, as long as the context is knwon (like a word processor)
* Long time ago people agreed that a capital latter "A" will be prepresented as 65
* Then 65 can be represented with 2 bits in a byte 01000001
* ASCII - American Standard Code for Information Interchange - is a well defined map of characters, panctuation marks etc. in numbers
* However there are more characters and symbols in different languages - this lead to creation of Unicode, which is a superset of ASCII
* ASCII uses only a byte to represent all characters, UNICODE is not bounded to a byte and uses sometimes 8, 16, 24, 32 bits
* With unicode you can represent emojis
* Given that new emojis gets added all the time, the numbers gets very big
### Other forms of information
* RGB - composes any color of the rainbow combining 3 colors
* Each pixels is a combination of 3 numbers
* In context of colors  72 72 33 - is a shade of yellow, but in context of charcters it's "HI!"
* Gif's are multiple images looped in a single file
* Video is a sequence of images
* Music notes can be also represented as numbers

## Algorithms
* Alogorithm is a step by step recipe of instructions for solving problems
* Many algorithms, we carry out in real world, sometimes we just need to translate them to form that machines can understand
* We can compare alogrithms by finding their relation of time to solve with size of a problem - Big O
* When you half the problem set at each iteration, the time to solve will be log(n), as if there were 1024 pages to search, when you halve it each time you get 512, 256, 128, 64, 32, 16, 8, 4, 2, 1. So in only 10 iteration you can find something rather than 1024 iterations. log2(1024) is 10.
* Functions are verbs or actions
* Conditions are questions
* Variables hold information


